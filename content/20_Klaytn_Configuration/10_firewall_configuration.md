---
title: "Firewall Configuration"
date: 2022-09-20T17:44:42+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---
{{< line_break >}}

### 1. *(Only for CN)* Firewall configuration

##### 1) For communication and multichannel between klaytn CN, allow TCP ```32323-32324``` with below IP addresses to your firewall ingress rule.
```vim
54.180.180.202  
54.180.18.176 
52.79.134.72  
52.78.232.39
```

##### 2) Additionally, it is required to allow UDP ``` 32323 ``` with the same IP addresses to your firewall ingress rule.
```vim
54.180.180.202   
54.180.18.176  
52.79.134.72
52.78.232.39
``` 
{{< line_break >}}

### 2. *(Only for PN)* Firewall configuration

##### 1) For communication and multichannel between Klaytn PN, allow TCP ```32323-32324``` with below IP addresses to your firewall ingress rule.
```vim
54.180.180.202  
54.180.18.176 
52.79.134.72  
52.78.232.39
```

##### 2) Additionally, it is required to allow UDP ``` 32323 ``` with the same IP addresses to your firewall ingress rule.
```vim
54.180.180.202   
54.180.18.176  
52.79.134.72
52.78.232.39
``` 


{{< line_break >}}
{{< line_break >}}

---
{{< line_break >}}
*Please note that the above four IP addresses are attached to the Klaytn CNs.*

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
