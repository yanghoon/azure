---
description: '2019-07-08, AZ-300'
---

# Networks

### Multiple NIC

* 외부 네트워크 장비 연동 \(다수의 NIC 가 필요한 장비\)
* 공용, 사설 망분리 \(트래픽 분리, 과금 등\)
* 컨테이너 간 동일포트 사용 \(IP 방식의 제약이 있음?!?!\)

> [https://youngmind.tistory.com/entry/Network-Overlay-VXLAN-%EB%B6%84%EC%84%9D-3?category=394664](https://youngmind.tistory.com/entry/Network-Overlay-VXLAN-%EB%B6%84%EC%84%9D-3?category=394664)

### Networks

#### Default Routing

Public 접근, Private 접근 \(VPN\) 기본허용.  
모든 Outbound를 기본 NAT 허용.

#### Static IP

* NLB \(1:N\)
* IP to VM \(1:1\)

#### VPN Gateway

* S2S, P2S 제약 존재 \(bandwidth 공유\)
* bandwidth 보장\(max\), ???\(up to\)
* Server Mode
  * Active-Active \(multiple charge\)
  * Active-Passive \(default\)

#### Peering

분리된 CIDR 간  
CIDR 수정가능 \(단, 리소스가 없는 경우\)

* Regional : 각 가상 네트워크마다 연결구성
* Global : 

#### Gateway Transit

