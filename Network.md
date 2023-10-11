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

