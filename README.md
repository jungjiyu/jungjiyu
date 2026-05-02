<div align="center">

# 운영 가능한 AI 시스템을 설계하는 <br/>백엔드 엔지니어, 정지유입니다.

**정지유 | Backend Engineer**

[![Email](https://img.shields.io/badge/Email-Contact-FF7EB3?style=flat-square&logo=gmail&logoColor=white)](mailto:libraryofjiyu@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-FF7EB3?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jungjiyu)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FFD1E8,100:FF7EB3&height=2&section=footer" />

<br/>

 **"성능과 정합성이 중요한 백엔드 시스템을 설계하고,<br/>AI 기능이 실제 서비스에서 안정적으로 동작하도록 운영 흐름을 구조화하는 개발자입니다."**

</div>




<br/>

## 💗 Featured Projects

<details>
<summary><strong>🏆 OCEAN-KIT : 공간 분석, RAG, ML 파이프라인을 통합한 해양 복원 성과 분석 플랫폼</strong></summary>
<br/>

> 과학기술정보통신부 주최, 제15회 ICT 피우다프로젝트 최우수상(정보통신산업진흥원장상, 1위) 수상

`Spring Boot` `FastAPI` `RAG` `vLLM` `PostGIS` `Redis` `H3` `Airflow` `RabbitMQ` `MLflow`

- **Architecture**: 공간 분석, RAG 응답, ML 실행 흐름을 하나의 서비스/운영 구조로 통합
- **Geo Performance**: PostGIS GiST 인덱스 + H3 격자 + Redis 캐시 계층으로 **TPS 40 → 7,000+**, **응답 2.5s → 3ms(cache hit)** 개선
- **Reliable ML Workflow**: `preprocess → train → eval_gate → deploy` 파이프라인을 이벤트 기반으로 자동화하고, 평가 기준 미달 시 배포 차단
- **Operational AI**: Hybrid RAG와 vLLM 서빙을 연결해 질의응답 기능을 제공하되, 실행·검증·배포 플로우를 재현 가능한 구조로 설계
- **Deployment Engineering**: vLLM Docker 환경의 NCCL 공유 메모리 이슈를 해결하고 volume 캐싱으로 배포 시간 **20분 → 1분** 단축
- **Field Reliability**: 수중 네트워크 단절 환경을 고려한 Bulk Insert API와 재전송/중복/부분 실패 대응 로직 설계

</details>



<details>
<summary><strong>🛒 모구시장 : 공동구매 예약·결제 정합성을 설계한 커머스 플랫폼</strong></summary>
<br/>

> 선착순 예약의 재고 정합성과 결제 일관성을 동시에 보장하도록 hot path를 재설계한 공동구매 커머스 플랫폼

`Spring Boot` `JPA` `Redis` `RabbitMQ` `vLLM` `TRON`

- **Reservation Consistency**: Redis Lua 기반 원자 연산으로 선착순 예약 구간의 동시성 제어를 구현하고 **오버셀 0건** 달성
- **Hot Path Redesign**: Redis 도입 후에도 DB 병목이 남아 있던 예약 경로를 분석해, 불필요한 조회·정리 로직을 요청 경로 밖으로 분리
- **Performance Recovery**: DB-heavy 경로를 insert 중심 흐름으로 축소해 고트래픽 상황에서 처리량과 응답 지연을 안정화
- **Payment Reliability**: PortOne Webhook + 서버 재조회 기반 SSOT 검증, 상태 머신, 멱등성 키로 결제 정합성 보장
- **Operational Workflow**: 누적 주문량 기반 계단식 할인과 자동 정산(환불/포인트) 프로세스로 운영 공수 절감
- **Recommendation Serving**: 1,600만+ 공공데이터 기반 TRON 파인튜닝과 LLM Re-ranking을 결합한 추천 파이프라인 구성

</details>


<details>
<summary><strong>💬 StoryBridge : 실시간 채팅 & AI 피드백 네트워킹 플랫폼</strong></summary>
<br/>

> 실시간 메시징, AI 피드백 서빙, 관측 환경을 분리해 운영 가능한 구조로 재구성한 네트워킹 플랫폼

`Spring Boot` `STOMP` `RabbitMQ` `FastAPI` `Prometheus` `Grafana` `Elasticsearch`

- **Messaging Architecture**: SimpleBroker를 STOMP Relay + RabbitMQ 구조로 전환해 **k6 1,000 VUs 기준 채팅 서버 CPU 65% 감소**
- **AI Serving Separation**: AI 피드백 서버를 FastAPI 기반으로 분리 구축·배포해 메인 서버와 추론 부하를 분리
- **Observability**: Micrometer 커스텀 메트릭과 PromQL 조인으로 사용자/경로별 예상 과금액을 실시간 산출하는 Grafana 대시보드 구축
- **Search Quality**: Elasticsearch Nori 형태소 분석과 다국어 필드 매핑으로 한·영 혼합 텍스트 검색 품질 개선
- **Operational Stability**: 실시간 채팅, AI 기능, 운영 모니터링을 한 프로세스에 몰아넣지 않고 역할별로 분리해 장애 전파 범위를 축소

</details>

<details>
<summary><strong>🥗 오래살장 : VLM 기반 식단 분석 및 헬스케어 코칭 솔루션</strong></summary>
<br/>

> 비정형 식단 이미지를 구조화된 건강 데이터로 변환하고, 이를 개인화 RAG와 연결한 헬스케어 코칭 시스템 

`FastAPI` `Qwen2-VL` `RAG` `FAISS` `TRON`

- **Multimodal Extraction**: 식단 이미지를 영양소·노화 인자 기반 구조화 JSON으로 자동 변환
- **Personalized Response**: 사용자 건강 데이터, 식단 분석 결과, 저속노화 가이드를 결합한 개인화 RAG 응답 생성
- **Scoring Logic**: AHEI/aMED 기반 5개 핵심 지표 가중치로 저속노화 점수 산출 로직 구현
- **Real-time Retrieval**: FAISS HNSW 인덱스 실시간 증분 업데이트로 신규 아이템 콜드스타트 완화

</details>

<br/>

## 💗 Experience

<details>
<summary><strong>☁️ NAVER Cloud MLOps Intern (2026.03 - 현재)</strong></summary>
<br/>

- **Workflow Automation**: Kubernetes·Argo Workflow 기반 이벤트 중심 평가·배포 오케스트레이션 구조를 설계·구현
- **Evaluation Operations**: 분산된 멀티모달 평가 흐름을 정리하고 공통 운영 기준을 수립
- **Operational Stability**: 대규모 benchmark 실행 이슈를 분석하며 안정적인 실행 기준 정립

</details>


<details>
<summary><strong>🔬 CILAB 학부 연구생 (2024.03 - 2026.03)</strong></summary>
<br/>

- **Lab Infrastructure**: Prometheus(node_exporter, cAdvisor) + Grafana 기반 연구실 서버 통합 관측 환경 구축
- **Project Maintenance**: 연구·산학 프로젝트의 백엔드/AI 시스템 유지보수 및 성능 개선 수행
- **Research Engineering**: 이기종 문서 메타정보 추출·통합 및 자동 지식 그래프 구축 기반 RAG 연구 수행

</details>
<br/>

## 💗 Leadership & Community

<details>
<summary><strong>🦁 멋쟁이사자처럼 13기 대표 (2025.01 - 2025.12)</strong></summary>
<br/>

- **Operation**: 기획/디자인/프론트엔드/백엔드 다직군 지부 운영 총괄 (모집·온보딩·팀빌딩·일정/산출물 관리)
- **Mentoring**: 백엔드 기초·심화 투트랙 설계/운영 (JPA·영속성·Spring Security / Redis·RabbitMQ·동시성·모니터링)
- **Achievement**: 전국 연합 해커톤 Top 49/250(상위 20%) 3개 팀 진출 (단일 대학 최다·공동 1위, 전년 0팀→3팀)
- **Award**: 팀장으로 지부 멤버들과 팀 구성, 대외 공모전 최우수상(1위) 수상

</details>


<details>
<summary><strong>☁️ 구름톤 유니브 4기 백엔드 운영진 (2025.01 - 2025.12)</strong></summary>
<br/>

- **Process**: GitHub Projects·Issues 기반 협업 워크플로우 표준화 도입
- **Code Review**: DB 스키마·서버 아키텍처·코드 리뷰 및 트레이드오프 기반 피드백 제공
- **Study Lead**: Redis·RabbitMQ·동시성 제어·모니터링 등 고트래픽/아키텍처 주제 기술 스터디 주도

</details>

<br/>

## 💗 Tech Stack


![Infrastructure & Runtime](https://img.shields.io/badge/Infrastructure_%26_Runtime-white?style=flat-square)
![Kubernetes](https://img.shields.io/badge/Kubernetes-FF7EB3?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-FF9FCB?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-FFB6D6?style=flat-square&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-FF7EB3?style=flat-square&logo=githubactions&logoColor=white)
![GHCR](https://img.shields.io/badge/GHCR-FF9FCB?style=flat-square&logo=github&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FFB6D6?style=flat-square&logo=amazonwebservices&logoColor=white)


![MLOps](https://img.shields.io/badge/MLOps-white?style=flat-square)
![Airflow](https://img.shields.io/badge/Airflow-FF7EB3?style=flat-square&logo=apacheairflow&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-FF9FCB?style=flat-square&logo=mlflow&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-FFB6D6?style=flat-square)
![Argo Workflows](https://img.shields.io/badge/Argo_Workflows-FF7EB3?style=flat-square&logo=argo&logoColor=white)


![Real-time & Messaging](https://img.shields.io/badge/Real--time_%26_Messaging-white?style=flat-square)
![Kafka](https://img.shields.io/badge/Kafka-FF7EB3?style=flat-square&logo=apachekafka&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF9FCB?style=flat-square&logo=rabbitmq&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-FFB6D6?style=flat-square&logo=socketdotio&logoColor=white)
![STOMP](https://img.shields.io/badge/STOMP-FF7EB3?style=flat-square)


![Observability & Testing](https://img.shields.io/badge/Observability_%26_Testing-white?style=flat-square)
![Prometheus](https://img.shields.io/badge/Prometheus-FF7EB3?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-FF9FCB?style=flat-square&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-FF7EB3?style=flat-square&logo=k6&logoColor=white)


![Languages & Backend](https://img.shields.io/badge/Languages_%26_Backend-white?style=flat-square)
![Java](https://img.shields.io/badge/Java-FF7EB3?style=flat-square&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-FF9FCB?style=flat-square&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-FFB6D6?style=flat-square&logo=python&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-FF7EB3?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-FF9FCB?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-FFB6D6?style=flat-square&logo=hibernate&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-FF7EB3?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-FF9FCB?style=flat-square&logo=fastapi&logoColor=white)


![Data & Storage](https://img.shields.io/badge/Data_%26_Storage-white?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-FF7EB3?style=flat-square&logo=redis&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-FF9FCB?style=flat-square&logo=elasticsearch&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-FFB6D6?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-FF7EB3?style=flat-square&logo=mysql&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS_GiST-FF9FCB?style=flat-square&logo=postgresql&logoColor=white)
![H3](https://img.shields.io/badge/H3-FFB6D6?style=flat-square)
