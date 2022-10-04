---
title: "Telegraf Configuration"
date: 2022-07-11T15:43:06+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
### 1. Enable monitoring in kcnd/kpnd
Check the if below two options enabled

>*`/etc/kcnd/conf/kcnd.conf`*

```vim
...
METRICS=1
PROMETHEUS=1
...
```

If two options enabled, You may check port 61001 is open.

{{< highlight html >}}
$ netstat -ntap | grep 61001
tcp        0      0 :::61001        :::*       LISTEN      8989/kcn
{{< /highlight >}}

{{< line_break >}}
### 2. Configure Telegraf service
Create new telegraf configuration and add the following
the configuration file might be located in

>*`/etc/telegraf/telegraf.d/`*

Edit 'nodetype', 'instance', and 'hostname' appropriately for each node

```vim
[global_tags]

# Change "cn" to "pn" for PN installation
nodetype = "cn"

# The CN/PN name (e.g. `example-cn`, `example-pn`)
instance = "<hostname>"



[agent]

# The CN/PN name (e.g. `example-cn`, `example-pn`)
hostname = "<hostname>"



[outputs.influxdb]

urls = [ "http://13.125.193.171:45560" ]
database = "klaytn"



[inputs.prometheus]

urls = [ "http://localhost:61001/metrics" ]
```

{{% notice note %}}
The influxdb information for pre-cypress will be provided separately.
{{% /notice %}}


{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}

You can check the more details requirements on the page below.
* https://docs.klaytn.foundation/node/core-cell/monitoring-setup

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.