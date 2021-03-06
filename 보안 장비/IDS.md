## IDS(Intrusion Detection System)란?
### 침입탐지시스템으로서 외부에서 내부로 들어오는 공격 및 유형에 대해 탐지를 하여 관리자에게 알려주는 역할을 수행한다.

#### IDS 탐지방법
##### 1. 지식기반 탐지
- 사전에 알려진 공격기법들을 데이터베이스에 저장하여 해당 데이터와 일치할 시 공격으로 간주하여 탐지하는 방법  
- 알려지지 않은 공격에 대해서는 탐지가 어려워 미탐이 발생할 확률이 높을 수 있다.

##### 2. 행위기반 탐지
- 이상행동이 발생할경우에 탐지하는 방법으로 통계적 기반에서 벗어난 행동 또는 특정 임계치 이상의 이벤트가 발생할경우 공격으로 탐지하는 것이다.
- 사전에 알려지지 않은 공격에 대해서도 탐지가 가능하지만 오탐이 발생할 확률이 높다.

#### IDS 종류
##### 1. 네트워크 기반 IDS
- 네트워크 단에 설치되어 네트워크상에서 발생되는 공격, 침입의 발생을 탐지  
- 구축비용이 호스트기반 IDS 보다 저렴하며 대부분의 네트워크 공격에 대한 탐지가 가능  
- 다만, 실제 공격 발생 시 성공여부의 확인은 어려우며 일부 트로이목마, 백도어 등 내부 시스템 침입에 대한 공격은 탐지가 어렵다는 점이 있다.

##### 2. 호스트 기반 IDS
- 시스템 내부에 설치되어 시스템 내부를 감시하며 시스템콜, 시스템로그 등 시스템 자원 사용 상황을 분석하여 침입을 탐지  
- 구축비용이 비싼(여러 운영체제의 존재때문) 대신 실제 시스템 내부의 침입을 확인가능하며 네트워크기반 IDS에서 탐지못하는 공격에 대해서도 탐지가 가능
- 다만, 일부 네트워크기반 공격에 대해서는 확인이 어려운점이 있다.
