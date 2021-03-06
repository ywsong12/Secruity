## NAC(Network Access Control)란?
### 엔드포인트 즉, 사용자의 device가 내부 네트워크에 접근 시 내부네트워크의 피해를 막기위해 NAC에 설정된 보안정책의 준수를여부를 검사하여 내부 네트워크의 사용을 제어하는 보안장비이다.


#### NAC 동작원리
- 사용자의 단말기가 내부 네트워크에 접근 시도를 할 경우 NAC에 등록된 MAC주소를 확인하여 인증을 수행하는 등의 방법으로 사용자의 인증을 진행
- 인증 과정에서 NAC에 설정된 보안정책의 준수여부를 확인(백신관리 등 보안패치가 적절한지에 대한 여부)
- 모든 인증 과정이 완료되면 사용자의 내부 네트워크의 접근을 허용
- 만약, 보안정책에 준수되지 못한 사용자의 경우에는 내부 네트워크의 접근이 거부되고 격리되며, 이후 보안패치, 백신패치 등의 과정을 통해 보안정책에 준수될 경우 다시 인증과정을 거쳐 내부 네트워크의 접근이 가능하다. 
- 또한, 내부 네트워크에 접근한 사용자라도 보안정책에 위배된 이상행동을 수행할 경우에도 내부 네트워크에서 격리된다.


#### NAC 동작방식
##### 1. Agent 방식
각 호스트(사용자의 device)에 Agent S/W 를 설치하여 사용하는 방식으로 각 호스트의 H/W 및 프로세스 정보 수집, 백신, 보안패치 등을 지원하며 Agent에서 네트워크를 통제하는 방식
##### 2. Agentless 방식
사용자 PC에 연결된 스위치 및 포트정보, 호스트명, 도메인명 관리 등을 지원하며 네트워크 장비에서 네트워크를 통제하는 중앙 집중 통제 방식
