# DB접근제어란?
#### 사전에 미리 정의된 보안 정책에 따라 DBMS에 로그인하는 사용자의 접근을 제어한다.
#### 접근이 사용자가 SQL수행 등 작업을 진행할때도 권한에 따라 가능여부를 판단하여 접근을 제어한다.
#### 감사를 위해 DBMS의 사용자 접근부터 작업기록이 모두 로그로 기록되어 보관된다.

## DB접근제어 방식
### 1. Gateway 방식
#### 프록시 방식  
- DB서버에 접속하는 모든 IP를 DB 접근 제어 서버로 통하도록 설정하여 내부 사용자의 개인정보 등의 중요정보의 유출 통제에 용이한 방식  
- 인라인 방식보다 조금 더 부하가 있지만 DB접근 제어 서버의 장애 발생 시 이중화 구성으로 온라인 업무에도 지장 없이 복구 가능하며 대규모 시스템에 적합
#### 인라인 방식  
- 타깃 DB서버와 클라이언트 네트워크 사이에 DB 접근 제어 서버를 구성하여 서버나 클라이언트에 별도의 설치 또는 변경이 필요없고 DB서버와 클라이언트 간 모든 패킷에 대한 통제가 가능한 방식  
- DB 접근 제어 서버가 다운 시 해당 DBMS의 모든 업무가 중단될 우려가 있어 소규모 시스템에 적합  
### 2. Sniffing 방식
- 네트워크 상의 패킷들을 미러링 방식으로 DB사용 시의 패킷을 감시하며 로그에 기록  
- 네트워크에 큰 부하 없이 시스템을 구축 할 수 있으며, DBMS 감사의 의미를 두고 있는 방식  
- 오로지 감시만 가능하여 즉각적인 접근제어나 차단은 불가능  
### 3. Agent 방식
- 서버자체에 접근제어와 로깅하는 기능을 포함시킨 에이전트를 설치  
- DB에 직접 접근하는 전용 클라이언트를 포함하여 모든 접근 루트를 제어  
- DB서버에 트래픽을 발생시켜 DB서버의 부하 증가 및 성능 저하가 발생 가능하여 시스템 정지의 리스크가 있음  


