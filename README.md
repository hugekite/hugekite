# Taeyeon Kim
**Backend Engineer & System Architect**

단순한 기능 구현을 넘어, 대용량 트래픽 환경에서의 데이터 무결성 보장과 지연 시간 최소화에 집중합니다. 운영 환경의 실패를 상정하고 이를 방어하는 아키텍처 설계에 강점이 있습니다.

---

## Tech Stack

* **Backend Environment:** Node.js, NestJS, TypeScript, Express
* **Database & Cache:** MariaDB, MySQL, Redis, TypeORM
* **Infrastructure & OS:** AWS EC2, S3, PM2, Ubuntu Linux, Jenkins
* **Architecture Focus:** Transaction Management, WebSocket Streaming, TCP/IP Socket Communication

---

## Architecture Insights

| Domain | Challenge | Implementation & Result |
| :--- | :--- | :--- |
| **Data Integrity** | 다중 테이블(우편함, 소유권, 인벤토리) 갱신 중 네트워크 단절 시 데이터 오염 방지 | TypeORM QueryRunner 기반 **원자적 트랜잭션 롤백** 구조 적용. 데이터 불일치율 0% 유지 |
| **Low Latency** | 순차적 AI 오디오 처리(REST API) 시 발생하는 응답 지연 한계 극복 | WebSocket + Smart VAD 기반 **실시간 양방향 스트리밍** 전면 마이그레이션. 지연 시간 85% 단축 |
| **High Concurrency** | 당일 활성 유저 실시간 랭킹 산정 시 RDBMS Index Scan I/O 병목 발생 | **Redis Sorted Set (ZADD)** 인메모리 아키텍처 도입. 병목 해소 및 동시성 처리 속도 최적화 |
| **Fault Tolerance** | 특정 로직 결함으로 인한 메모리 누수 한계치 도달 시 서버 다운 방어 | **PM2 클러스터 기반 Auto-Healing** 파이프라인 적용. 자동 프로세스 재시작을 통한 무중단 복구 |
| **Probability Engine** | 확률형 가챠 시스템에서 클라이언트 조작 방지 및 신뢰성 확보 | 서버 사이드 유저 상태 검증 및 **안전한 난수 생성(RNG)** 기반 확률 분기 트랜잭션 처리 |
| **Closed Network** | 외부 망이 차단된 환경에서 이기종 장비 간 실시간 텔레메트리 요구 | 폐쇄망 내부 **TCP/IP 소켓 통신 규격 설계** 및 C# 통합 제어 앱 - Node.js 간 데이터 매핑 |

---

## Core Projects

### 1. 메타버스 플랫폼 백엔드 개발 및 구조 리팩토링
* 가상 경제 시스템의 재화/아이템 지급 로직 아키텍처 설계
* 기존 Node.js 레거시 코드를 중단 없이 NestJS(Controller-Service-DTO) 객체지향적 구조로 리팩토링
* Request/Response DTO 분리로 클라이언트 통신 규격 표준화 및 공통 로깅/예외 처리 체계 구축

### 2. AI 인재평가 플랫폼 (VOTMS) 데이터 파이프라인 최적화
* 단방향 오디오 처리 파이프라인의 한계 분석 및 WebSocket 기반 양방향 스트리밍 재설계
* 오디오 수신부터 AI 분석, 결과 반환까지의 지연 시간 최소화

### 3. 정부과제 기반 제조/해양 디지털트윈 인프라 구축
* 현대자동차 제조 로봇 관련 C# 제어 프로그램과 서버 간 데이터 매핑 및 통신 프로토콜 구현
* 해양물류 프로젝트 수행 시 인프라 조건, 이중화, 배포 구조 종합 분석

---

## DevSecOps & Troubleshooting Log

* **DB Connection Pool Leak:** 특정 로직 내 트랜잭션 미해제로 인한 활성 커넥션 누수 식별. Pool 반환 강제화 및 커넥션 타임아웃 튜닝.
* **Concurrent Update Collision:** 동시 다발적 보상 API 호출로 인한 동일 Row 데드락 발생. 비즈니스 로직 쿼리 순서 정렬 및 Lock 스코프 최소화 적용.
* **Pipeline Breakdown:** Ubuntu 서버 환경에서 Jenkins 배포 중 SSH 인증 실패 디버깅. 무중단 서비스 유지를 위한 PM2 배포 스크립트 멱등성 보장 코드 작성.

---

## Contact
* **Email:** ktyeon92@gmail.com
* **Interactive Portfolio:** https://hugekite.github.io/myInfo.github.io/
