## Switch Jamming 공격이란?
#### 스위치는 MAC주소를 저장하는 테이블을 가지고 있으며, 이 테이블이 가득 찰 경우에 모든 네트워크(즉, 들어온 포트외 모든포트)에 브로드캐스트를 하는 특성을 가지고있다. 
#### 공격자는 이런 특성을 이용하여 위조된 MAC주소를 스위치에 지속적으로 보내고 스위치의 MAC주소를 저장하는 테이블은 위존된 MAC주소로 가득차 브로드캐스트를하게되며 브로드캐스트를 통하여 패킷정보를 공격자는 스니핑할 수 있게 된다.


### 대응 방안
#### 포트 시큐리티로 등록가능한 MAC주소의 제한을 거는 방법이 있다.(설정된 MAC주소만 해당 포트이용이 가능하며 그외 MAC주소는 사용불가)
