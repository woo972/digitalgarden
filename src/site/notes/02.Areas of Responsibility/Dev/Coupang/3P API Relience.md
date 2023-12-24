---
{"dg-publish":true,"permalink":"/02.Areas of Responsibility/Dev/Coupang/3P API Relience/","tags":["dev","transaction_management","fault_tolarence"],"noteIcon":""}
---

## 전략
---
1. CSP, Non CSP를 확인하여 비즈니스 임팩트를 고려한다.
2. Playbook을 작성하여 유사시 어떻게 대응할지 훈련한다.
3. 3P와 SLA를 협의하고 장애 발생시 대응 절차를 정의한다.
4. 기술적 대응
	1. 모니터링 체계 구축
	2. 다중 3P API를 orchestration할 수 있는 솔루션 구축
	3. API 장애시의 CX 워크플로우 정의
	4. 분산트랜잭션 시나리오 정의
	5. Chaos Testing 등을 통해 3P API 장애를 대비한 검증 메커니즘 확인
## 참고
---
[[02.Areas of Responsibility/Dev/Monitoring & Incident/모니터링 대상\|모니터링 대상]]
[[02.Areas of Responsibility/Dev/Monitoring & Incident/인시던트 예방 및 대응 아이디어\|인시던트 예방 및 대응 아이디어]]