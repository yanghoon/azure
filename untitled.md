---
description: '2019-07-09, AZ-300'
---

# Monitoring

## Monitoring

* Azure
  * Metric : 1분 단위 수집
  * Logging : 실시간 접근 가능
* AWS
  * Metric : 초단위, 과금, 인스턴스가격보다 비쌈...
  * Logging : 동기화까지 5분

### Application

* Agent 방식

### Infrastructure

* Service Map : Connectivity
* Network Monitoring : ICMP\(x\), trace route\(x\), TCP Ping

### Core

* Azure Monitor \(CPU\)
* Advisor \(AWS, Google, OSS?\)
  * High availability \(가용성\)
  * Security \(취약점 탐지\)
  * Performance \(성능제약, 리소스 제약\)
  * Cost \(과금 최적화\)
* Service Health
* Activity Log \(Audit, 90 days\)

### Shared

* Alerts \(모니터 &gt; 경고\)
  * Trigger 설정
  * Log 기반 \(Log 저장소 생성필요\)
* Signal \(source\) : Metrics, Audit, Application Insights, Logs
* Action Group
  * Email, Email\(Role\), SMS\(5 min\), Call

