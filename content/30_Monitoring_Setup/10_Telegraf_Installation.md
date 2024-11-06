---
title: "Telegraf Installation"
date: 2022-07-11T15:42:53+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

&nbsp; 

### 1. Telegraf Installation
>Telegraf Installation Guide (Amazon Linux 2 users, see below):

* https://docs.influxdata.com/telegraf/latest/introduction/installation/

&nbsp; 

{{% notice note %}}
To install Telegraph on Amazon Linux 2, you may use InfluxData's RHEL 7 yum repo as follows:
{{% /notice %}}


```vim
cat <<EOF | sudo tee /etc/yum.repos.d/influxdb.repo

[influxdb]
name = InfluxDB Repository - RHEL 7
baseurl = https://repos.influxdata.com/rhel/7/\$basearch/stable
enabled = 1
gpgcheck = 1
gpgkey = https://repos.influxdata.com/influxdata-archive_compat.key
EOF
```


&nbsp; 
&nbsp; 
&nbsp; 

If you finish this step, please click the next button ```>``` on the right side of this page.



