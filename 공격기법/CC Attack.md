# CC Attack(Cache-Control 공격)란?
### HTTP헤더에서 Cache-Control 필드의  no-store, must-revaildate 등 과 같은 구문을 활용하여 비정상적인 조작을통해 서버에 부하를 주는 DDoS 공격이다.
### 서버에 주는 부하를 줄이기위해서 보통이라면 사용자가 웹서버에 데이터를 요청하고 수신받은 웹의 변경사항이 없을 경우 웹서버는 사용자의 임시인터넷파일에서 수신받았던 파일을 띄우라고 한다.
### 하지만, 공격자가 Cache-Control 필드 값을 조작하여 no-store, must-revalidate 로 지정하여 보내게 되면 임시인터넷파일에 아무것도 없으니 다시 전달해달라고 요청을 하게 된다.
### 이후 웹서버는 데이터를 다시 보내주게 되는데 이 과정에서 웹서버는 갱신을 하게되고 이과정을 반복하여 서버에 부하가 발생하게 만든다. 
### 즉, Cache-Control 값을 조작하여 요청을 하여 웹서버가 직접 응답하게 유도하는 방식으로 서버에 조금씩 부하를 주는 공격이다.


## 대응방안
#### 웹서버의 웹로그를 통해 대량의 비정상적인 GET 요청을 하는 IP에 한하여 방화벽(iptable, firewalld)에서 원천 차단을 한다.
#### 웹로그를 통해 no-store, must-revalidate 문자가 포함된 패턴을 찾아 해당 패턴으로 지속적으로 탐지되는 클라이언트 IP 차단
