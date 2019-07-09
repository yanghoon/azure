---
description: '2019-07-08, AZ-300'
---

# VMs

## Create VM

| Step | Name | Value | Notes |
| :--- | :--- | :--- | :--- |
|  | Machine Type | B1s | Temp Storage \(VM Host\) |
|  |  |  |  |
|  | Monitoring | Boot Log, Console |  |
|  | Extensions | Provisioning Tools | Custom Script for Linux |
|  | Cloud Init |  | OSS |

{% hint style="info" %}
B-xxx : 기준/부스팅 성능 존재. 기준성능 이상에서는 Credit 차감. 소진시 기준성능으로 제한됨.  
D-xxx : Umm....
{% endhint %}

{% hint style="info" %}
Scale-Out 대신 부스팅을 통해 순간부하를 처리하는 아키텍쳐 사례가 있음.  
Scale-Out 속도/확장 시간의 중요도에 따라 전략이 달라질 수 있음.  
일반적으로 VM 수가 많은 수록 유리함.
{% endhint %}

{% hint style="info" %}
{TYPE}-{CORE}-{STORAGE}
{% endhint %}

## CLI

```bash
$ az login
# Session Type : URL+Code
$ az vm create ?
```

## ARM Templates

JSON

* Parameters
  * Style: default, select item
  * `[parameters('key')]`
* Variables : Value Generator
* Resources
  * dependsOn : validation, cascade
  * ```text
    "imageReference": {
      "publisher": "Canonical", "offer": "UbuntuServer",
      "sku": "18.04-LTS", "version": "latest"
    }
    ```

```text
az login
az account set -subscription xxxxx

group=<group-name>
az group create -g $group -l southeastasia
az group deployment create -g $group --name deploy_wordpress_on_mysql \
    --template-file azure_template.json --parameters parameters.json
```

## Monitoring

* Metrics : CPU, Network, Disk I/O \(Only Hypervisor Metrics\)
* Memory Usage : Need to Monitoring Agent

