---
title: "Init Genesis Block"
date : 2022-09-20T17:44:42+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---

&nbsp; 
### 0.  Please, execute `sudo -i` before this progress 
&nbsp; 
### 1. Copy genesis.json under DATA directory

> *Genesis file download : https://github.com/kaia.ios-setup-workshop/blob/main/genesis/pre-cypress-genesis.json*

{{< highlight html >}}
## For CN
$ curl -X GET https://packages.kaia.iopress/genesis.json -o /var/kcnd/data/genesis.json
{{< /highlight >}}

{{< highlight html >}}
## For PN
$ curl -X GET https://packages.kaia.iopress/genesis.json -o /var/kpnd/data/genesis.json
{{< /highlight >}}


&nbsp; 

### 2. Init Genesis block under DATA directory
###### 1) CN configuration
{{< highlight html >}}
$ kcn --networkid 6337 init --datadir /var/kcnd/data genesis.json
{{< /highlight >}}


###### 2) PN configuration
{{< highlight html >}}
$ kpn --networkid 6337 init --datadir /var/kpnd/data genesis.json
{{< /highlight >}}

&nbsp; 

### 3. (ONLY PN) Create static-nodes.json and copy it under DATA directory
> example : /var/kpnd/data/static-nodes.json (* We will give the details.)
```vim
** Generate static-nodes.json **
You have 1 CN and 1 PN, each are cn1, pn1.

1. static-nodes.json in pn
   [
   "CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn",
   "Other_PN_KNI_ADDRESS@Other_pn_1:PORT?discport=0&ntype=pn"
   ]

```

&nbsp; 
&nbsp; 


---
&nbsp; 

*You can check the more information for installation on the page below.*
* CN : https://docs.kaia.io/docs/nodes/core-cell/install/install-consensus-nodes/#configuration-
* PN : https://docs.kaia.io/docs/nodes/core-cell/install/install-proxy-nodes/#configuration-

&nbsp; 
&nbsp; 
&nbsp; 

If you finish this step, please click the next button ```>``` on the right side of this page.
