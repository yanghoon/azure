---
description: '2019-07-08, AZ-300'
---

# VMs

Create

| Step | Name | Value | Notes |
| :--- | :--- | :--- | :--- |
|  | Machine Type | B1s | Temp Storage \(VM Host\) |
|  |  |  |  |
|  | Monitoring | Boot Log, Console |  |
|  | Extensions | Provisioning Tools | Custom Script for Linux |
|  | Cloud Init |  | OSS |

{% hint style="info" %}
B-xxx : 기준/부스팅 성능 존재. 기준성능 이상에서는 Credit 차감. 소진시 기준성능으로 제한됨.  
D-xxx : 
{% endhint %}

{% hint style="info" %}
Scale-Out 대신 부스팅을 통해 순간부하를 처리하는 아키텍쳐 사례가 있음.
{% endhint %}

