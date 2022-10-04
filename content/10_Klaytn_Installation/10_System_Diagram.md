---
title: "Network Diagram"
date: 2022-09-20T17:44:45+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

{{< line_break >}}

### 1. CCN Diagram 
>##### CCN consists of one CN node and two PN nodes.
{{< line_break >}}
![CCN](https://raw.githubusercontent.com/klaytn/klaytn-pre-cypress-setup-workshop/main/static/images/klaytn-1.png)

{{< line_break >}}
{{< line_break >}}

### 2. Network architecture
>##### Full mesh connection should be made between CNs.
>##### So, You need to configure the firewall to allow ingress between nodes.

* For communication and multichannel between CN, allow TCP `32323-32324` and UDP `32323` to your firewall ingress rule.
* We will share CN node IPs for Pre-cypress configuration separately.
{{< line_break >}}
{{< line_break >}}
![network](https://raw.githubusercontent.com/klaytn/klaytn-pre-cypress-setup-workshop/main/static/images/klaytn-2.png)

{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}
*You can see the Klaytn Design more detailed on the page below.*
>##### https://docs.klaytn.foundation/klaytn/design/consensus-mechanism

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.