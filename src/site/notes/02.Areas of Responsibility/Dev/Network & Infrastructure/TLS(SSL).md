---
{"dg-publish":true,"permalink":"/02-areas-of-responsibility/dev/network-and-infrastructure/tls-ssl/","tags":["dev","cs"],"noteIcon":""}
---

## SSL 동작 흐름
---
### Handshake: 암호 방식 협의 및 인증서 전달
- client: 클라이언트 측 랜덤데이터와 클라이언트 지원 암호화 방식, 세션아이디 전송
- server: 서버측 랜덤 데이터와 서버측이 선택한 클라이언트 암호화 방식, 인증서 전송
### 인증서 검증
- 브라우저가 브라우저에 등록된 CA와 서버가 제공한 인증서의 CA가 일치하는지 확인
- CA가 제공한 공개키로 서버 인증서를 복호화
- 복호화가 성공하면 인증서가 해당 CA의 비공개키에 의해 암호화 된 것이 증명되어 신뢰가능한 서비스로 간주
### 데이터 암호화 통신
- client: 
	- 클라이언트 랜덤 데이터 + 서버 랜덤 데이터로 대칭키(pre master secret) 생성 
	- 서버의 인증서에 들어있는 공개키로 대칭키를 암호화하여 서버로 요청 전송
- server:
	- 클라이언트로 받은 암호화된 대칭키(pre master secret)를 서버측 비공개키로 복호화하여 대칭키 획득
	- pre master secret을 일련의 과정을 거쳐 master secret > session key로 생성
	- 향후 통신시 데이터를 암호화(session key를 대칭키로 사용)