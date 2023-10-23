# Network

### 웹 통신 과정
![웹 통신 과정.png](image%2F%EC%9B%B9%20%ED%86%B5%EC%8B%A0%20%EA%B3%BC%EC%A0%95.png)

<details>
    <summary>웹 통신 흐름</summary>

    1. 웹 브라우저를 통해 사용자가 URL을 입력한다.
    2. 입력받은 URL중 도메인을 통해 DNS에 검색한다.
    3. DNS에서 일치하는 도메인의 IP를 URL 정보와 함께 HTTP 메시지로 만든다.
    4. 생성된 HTTP 메시지를 TCP로 서버와 통신한다.
    5. 서버에서 요청 URL을 통해 전달받은 응답 값을 클라이언트로 전달한다.
</details>

### DNS 라우팅 과정 
![DNS 웹:앱 라우팅 과정.png](image%2FDNS%20%EC%9B%B9%3A%EC%95%B1%20%EB%9D%BC%EC%9A%B0%ED%8C%85%20%EA%B3%BC%EC%A0%95.png)

### TCP(Transmission Control Protocol)
- 정보 전달을 하기 위한 프로토콜
- 웹 브라우저들이 www에서 서버에 연결(정보를 주고 받기 위해)할 때 사용
- 인터넷, 인트라넷, 근거리 통신에 사용되는 컴퓨터에서 안정적이고, 순서대로 오류 없이 데이터를 주고 받을 수 있게 함

### UDP(User Datagram Protocol)
- 안정성이 낮고, 순서를 보장하지 않는 대신 오버헤드가 작고, 지연시간이 짧음

### TCP 3 way handshake
데이터 전송 단계에서 연결에 사용되는 방식이다.
![3wayhandshake.png](image%2F3wayhandshake.png)
- SYN : 데이터 전송을 위해 서버로 요청
- SYN - ACK : 서버가 요청이 가능한지 확인
- ACK : 서버의 요청 사항을 수락하여 연결됨

### TCP 4 way handshake
데이터 연결이 종료된 상황에서 사용되는 방식이다.
![4wayhandshake.png](image%2F4wayhandshake.png)
- FIN : 연결이 되어 있는 상태에서 연결 종료 요청을 보내는 FLAG
- ACK : 연결 종료 요청을 받고 응답을 전달하는 FLAG