---
title: "Package Installation"
date: 2022-07-11T19:18:57+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---
&nbsp; 
### 1. Linux Archive Distribution
>The archive file consists of the executable binary and the configuration file structured as follows.

* For CN node : ```kcn``` / ```kcnd```
* For PN node : ```kpn``` / ```kpnd```


{{< highlight html >}}
- bin
  |- kcn
  |- kcnd

- conf
  |- kcnd.conf
  {{< /highlight >}}

  {{< highlight html >}}
  File Name       |     File Description
--------------------------------------------------------
bin/kcn         |     CN executable file
bin/kcnd        |     CN start/termination script file
conf/kcnd.conf  |     CN configuration file
{{< /highlight >}}

{{% notice warning %}}
Do NOT alter the file structure or file name. If you change it, the node may not function correctly.
{{% /notice %}}
&nbsp; 

#### Installation
>The installation is decompress of the downloaded package where you want to install the package.

{{< highlight html >}}
$ tar zxf kcn-vX.X.X-linux-amd64.tar.gz
or
$ tar zxf kcn-baobab-vX.X.X-linux-amd64.tar.gz
{{< /highlight >}}

{{% notice note %}}
it is recommended that decompress directory kcn-linux-amd64/bin path should be added to the environment variable $PATH to run the kcn and kcnd globally.
{{% /notice %}}
&nbsp; 
>As an example,

{{< highlight html >}}
$ export PATH=$PATH:~/downloaded/path/kcn-linux-amd64/bin
{{< /highlight >}}
The other sections assume that the path is added to the variable.

&nbsp; 
&nbsp; 
&nbsp; 


### 2. RPM Distribution (RHEL/CentOS/Fedora)

#### Install from Kaia Yum Repo
>You can install from the Kaia Yum repo, run:

###### 1) CN Installation
{{< highlight html >}}
sudo curl -o /etc/yum.repos.d/klaytn.repo https://packages.klaytn.net/config/rhel/7/prod.repo && sudo yum install kcnd
{{< /highlight >}}
###### 2) PN Installation
{{< highlight html >}}
sudo curl -o /etc/yum.repos.d/klaytn.repo https://packages.klaytn.net/config/rhel/7/prod.repo && sudo yum install kpnd
{{< /highlight >}}
&nbsp; 

#### Install downloaded RPM
>Alternatively, you can install the downloaded RPM file with the following yum command.

###### 1) CN Installation
{{< highlight html >}}
$ yum install kcnd-vX.X.X.el7.x86_64.rpm
or
$ yum install kcnd-baobab-vX.X.X.el7.x86_64.rpm
{{< /highlight >}}
###### 2) PN Installation
{{< highlight html >}}
$ yum install kpnd-vX.X.X.el7.x86_64.rpm
or
$ yum install kpnd-baobab-vX.X.X.el7.x86_64.rpm
{{< /highlight >}}
&nbsp; 

#### Installed Location
>The installed files are located as follows. (The PN node is also in the same location.)

{{< highlight html >}}
File Name    |    Location
-------------------------------------------
kcnd.conf    |    /etc/kcnd/conf/kcnd.conf
{{< /highlight >}}

&nbsp; 
&nbsp; 

---
&nbsp; 
*You can check the more details information on the page below.*
* CN : <https://docs.kaia.io/docs/nodes/core-cell/install/install-consensus-nodes/>
* PN : <https://docs.kaia.io/docs/nodes/core-cell/install/install-proxy-nodes/>

&nbsp; 
&nbsp; 
&nbsp; 

If you finish this step, please click the next button ```>``` on the right side of this page.