---
title: "Klaytn Configuration"
date : 2022-09-20T17:44:42+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---
{{< line_break >}}
>The CN configuration is to create a data directory and set up several values in the configuration file.

* Create the data/log directory.
* Install node key.
* Configure the CN(PN) with `kcnd.conf` (`kpnd.conf`).
{{< line_break >}}
{{< line_break >}}


### 1. Data,log Directory Creation
Considering the fact that the size of Klaytn blockchain data is always increased, it is recommended to use a big enough storage. You may need to create the directory on your desired path.

>##### 1) CN
{{< highlight html >}}
$ mkdir -p /var/kcnd/data
{{< /highlight >}}
{{< highlight html >}}
$ mkdir -p /var/kcnd/log
{{< /highlight >}}

>##### 2) PN
{{< highlight html >}}
$ mkdir -p /var/kpnd/data
{{< /highlight >}}
{{< highlight html >}}
$ mkdir -p /var/kpnd/log
{{< /highlight >}}

{{< line_break >}}


### 2. Install Node key

In order to operate a node, a `nodekey` is required. The KCN(KPN) binary will create a new one for you if you do not have it. {{< line_break >}}
If you have one, you need to put your `nodekey` into the  `data` directory. 

{{< highlight html >}}
$ mkdir -p /var/kcnd/data/nodekey
{{< /highlight >}}
{{< highlight html >}}
$ cp nodekey /var/kcnd/data
{{< /highlight >}}
Set the PN node in the same way.

{{< line_break >}}
{{< line_break >}}

### 3. Update the Configuration File
>Configuration File Location:

##### For the archive distribution, the config directory location defaults to `$INSTALL_PATH/kcn-linux-amd64/conf/`.
##### For the package distribution, the config directory defaults to `/etc/kcnd/conf/`.

{{< line_break >}} 

>##### 1) Add configuration for CN

```vim
NETWORK=""
NETWORK_ID=7207
DATA_DIR=/var/kcnd/data  # path where you created in #1
LOG_DIR=/var/kcnd/logs # path where you created in #1
NO_DISCOVER=0
BOOTNODES="kni://8e1881cdca97f52a76c6d2683db030f51a34ffc039476b4ed5bc5c757de1b5ce48fea1e53aa182a6ac2b076460881d50d3b57461d1cf36fae777e992893ad485@52.199.8.244:32323?discport=32323&ntype=bn"
REWARDBASE="" # ADD YOUR REWARDS ADDRESS GNNERATED BY KEYTOOL
```
>##### 2)  Add configuration for PN
```vim
NETWORK=""
NETWORK_ID=7207
DATA_DIR=/var/kpnd/data  # path where you created in #1
LOG_DIR=/var/kpnd/logs # path where you created in #1
NO_DISCOVER=1
BOOTNODES=""
```

{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}
*You can check the more information for installation on the page below.*
* CN : https://docs.klaytn.foundation/node/core-cell/installation-guide/consensus-node-setup/configuration
* PN : https://docs.klaytn.foundation/node/core-cell/installation-guide/proxy-node-setup/configuration

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
