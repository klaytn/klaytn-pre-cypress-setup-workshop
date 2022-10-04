---
title: "Check the services"
date: 2022-07-11T18:42:35+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
### 1. Watch the service log to confirm if your nodes are correctly joined.

{{% notice note %}}
If the node is not a proposer at that block, and the consensus is successful, the node have executed(==validates) the block. In other words, a block is inserted.
{{% /notice %}}

##### 1) For CN,
{{< highlight html >}}
$ tail <your_klaytn_home_path>/kcnd/log/kcnd.out
INFO Inserted a new block number=14 hash=13cbfc…f007fc txs=0 gas=0 elapsed=793.458µs processTxs=167ns finalize=157.708µs validateState=7.542µs totalWrite=443.417µs trieWrite=256.667µs
{{< /highlight >}}
##### 2) For PN,
{{< highlight html >}}
$ tail <your_klaytn_home_path>/kcnd/log/kpnd.out
INFO Inserted a new block number=14 hash=13cbfc…f007fc txs=0 gas=0 elapsed=793.458µs processTxs=167ns finalize=157.708µs validateState=7.542µs totalWrite=443.417µs trieWrite=256.667µs
{{< /highlight >}}

{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}

You can check the more details requirements on the page below.
* https://docs.klaytn.foundation/node/node-log#info-logs

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
