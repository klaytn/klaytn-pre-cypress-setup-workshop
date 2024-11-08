---
title: "Telegraf Configuration"
date: 2022-07-11T15:43:06+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}

### 1. Enable monitoring in kcnd/kpnd
Check the if below two options enabled.

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
Create new telegraf configuration file as klaytn.conf under below path and add the following
the configuration.

>*`/etc/telegraf/telegraf.d/`*

Edit 'nodetype', 'instance', and 'hostname' appropriately for each node.

```vim
[global_tags]
# Change "cn" to "pn" for PN installation
nodetype = "cn"
# The CN/PN name (e.g. `klaytn-cn`, `klaytn-pn-01`)
instance = "<hostname>"

[agent]
# The CN/PN name (e.g. `klaytn-cn`, `klaytn-pn-01`)
hostname = "<hostname>"

[outputs.influxdb]
urls = [ "http://13.125.193.171:45560" ]
database = "klaytn"

[inputs.prometheus]
urls = [ "http://localhost:61001/metrics" ]
```

{{% notice note %}}
Please find the Pre-mainnet Dashboard as below URL. The Credentials will be provided separately.
{{% /notice %}}

* http://13.125.193.171:3000/d/K2aqGNDZz/dashboardcco?orgId=1&refresh=10s

{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}

You can check the more details requirements on the page below.
* https://docs.klaytn.foundation/docs/nodes/core-cell/monitoring-setup/

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.