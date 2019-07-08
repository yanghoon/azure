---
description: '2019-07-08, AZ-300'
---

# Storage

### Azure Storage

* Blobs\(S3\)
  * WebServer\(Path\) + Metadata
* Type: blobs, tables, queues, files
  * performance: standard\(HDD\), premium\(SSD\)
  * access: hot/cool/archive \(rw\)
  * {mystorageaccount}.{type}.core.windows.net
  * 포함비용
    * access count
    * transaction
* Replication
  * Locally : Same Region, 3 Copy, Host\(o\)/Region\(x\), Premium
  * Geo : Paired Region, 3 Copy, Endpoint Fail-over
  * Read/Access Geo : Read-Only Endpoint, Master Fail-over
  * Zone : Same Region, 3 Available Zone/Set
* Azure Status
  * [https://status.azure.com/en-us/status/history/](https://status.azure.com/en-us/status/history/)
  * [https://status.azure.com/ko-kr/status](https://status.azure.com/ko-kr/status)

### Tools

* Azure Storage Explorer
* AzCopy : CLI for Automation

### CDN

* Usage
  * Origin Overhead, Location Access \(Edge Servers\)
* Config
  * Origin Type : 
  * Condition : Compression, Query String, Location Filtering
  * TTL Order
    * cache-directive
    * on Azure
* Pricing
  * Premium, Standard Verizon
  * Standard Akamai
  * Standard Microsoft



