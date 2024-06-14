# 1. 주제

- 매일 인프라 DB 일일 보고서(쿼리 튜닝 가이드) 작성 및 담당자에게 전송
    - 매일 보고서 작성
    - 롱쿼리 튜닝 가이드

# 2. 대상 서버

- 결제정보팀 카드개발 (dsl791dev)
    - 맥스게이지 서버 올라가 있음
    - 자원 여분  확인 필요 *

# 3. 필요 사항

### 1. API 종류 선택

- Open API GPT-4

### 2. 네트워크 방화벽 오픈

- AWS → 카드 개발
- AWS → 매일서버/TEAMS

### 3. AWS 환경 구축 (아키텍처)

- Terraform
- EventBridge (schedule) → Lambda → dsl791dev
- Lambda → Mail /Teams (Webhook)

### 4. DB 데이터 추출 항목 선정 🚨(추후 회의 필요)

- 테이블스페이스 사용량
1. cpu top query 추출 : cpu 사용률 시간
2. i/o 많은 쿼리
<추후 회의>

### 5. 프롬프트 작성 양식 (보고서용)  🚨(추후 회의 필요)

### 6. 튜닝 학습 (bing, rag, fine 튜닝)