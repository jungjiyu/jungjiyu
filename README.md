<div align="center">

# 견고한 백엔드 시스템 위에<br/>AI 기술을 더하는 개발자

**정지유 | Backend Engineer**

[![Email](https://img.shields.io/badge/Email-Contact-FF7EB3?style=flat-square&logo=gmail&logoColor=white)](mailto:libraryofjiyu@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-FF7EB3?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jungjiyu)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FFD1E8,100:FF7EB3&height=2&section=footer" />

</div>

<br/>

## 💗 About Me

Spring Boot 아키텍처를 설계하며 **PostGIS 인덱싱과 H3+Redis 캐싱**을 통해 공간 API 응답을 **2.5s→3ms**(cache hit 기준)로 단축하고, 처리량을 **TPS 40→7,000+**(175배)까지 개선했습니다. 

**STOMP+RabbitMQ**로 SimpleBroker 확장성 병목을 제거해 채팅 서버 CPU를 **65% 감소**시켰으며(k6 1,000 VUs 기준), Prometheus/Grafana로 운영 관측 지표를 정의해 이상 징후를 조기 탐지하고, 멱등성·재시도·정합성을 설계해 **운영 안정성과 복원력**을 확보했습니다.

전국 연합 IT 동아리 **'멋쟁이사자처럼' 13기 대표**로서 40명 규모 지부를 운영하며 협업·개발 프로세스를 표준화했고, 전국 연합 해커톤에서 **3개 팀의 Top 49/250(상위 20%) 진출**을 이끌었습니다. (단일 대학 최다·공동 1위, 전년 0팀→3팀 개선)

**백엔드 아키텍처와 AI 활용 역량을 결합해 비즈니스 가치를 만드는 개발자**가 되겠습니다.

<br/>

## 💗 Tech Stack

### Backend & API
![Java](https://img.shields.io/badge/Java-FF7EB3?style=flat-square&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-FF9FCB?style=flat-square&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-FFB6D6?style=flat-square&logo=python&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-FF7EB3?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-FF9FCB?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-FFB6D6?style=flat-square&logo=hibernate&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-FF7EB3?style=flat-square&logo=querydsl&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-FF9FCB?style=flat-square&logo=fastapi&logoColor=white)

### Real-time & Messaging
![WebSocket](https://img.shields.io/badge/WebSocket-FF7EB3?style=flat-square&logo=socketdotio&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF9FCB?style=flat-square&logo=rabbitmq&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FFB6D6?style=flat-square&logo=redis&logoColor=white)

### AI Engineering
![RAG](https://img.shields.io/badge/RAG-FF7EB3?style=flat-square&logo=anthropic&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-FF9FCB?style=flat-square)
![FAISS](https://img.shields.io/badge/FAISS-FFB6D6?style=flat-square)

### Database, Search & Geo
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-FF7EB3?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-FF9FCB?style=flat-square&logo=mysql&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-FFB6D6?style=flat-square&logo=elasticsearch&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS-FF7EB3?style=flat-square&logo=postgresql&logoColor=white)
![H3](https://img.shields.io/badge/H3-FF9FCB?style=flat-square)

### Observability
![Prometheus](https://img.shields.io/badge/Prometheus-FF7EB3?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-FF9FCB?style=flat-square&logo=grafana&logoColor=white)

### Infra & DevOps
![Linux](https://img.shields.io/badge/Linux-FFB6D6?style=flat-square&logo=linux&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-FF7EB3?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9FCB?style=flat-square&logo=amazonwebservices&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-FFB6D6?style=flat-square&logo=githubactions&logoColor=white)

<br/>

## 💗 Featured Projects

### 🏆 [OCEAN-KIT](https://github.com/OCEAN-KIT/back-end)
**과기정통부 주최 공모전 최우수상(1위) 수상작** | RAG 기반 AI 에이전트와 공간 데이터 파이프라인을 통합한 해양 복원 성과 분석 시스템

`Spring Boot` `FastAPI` `RAG` `vLLM` `PostGIS` `Redis` `H3`

- **🎯 Agentic Workflow**: 현장 기록→승인→지표 생성→챗봇 응답의 E2E 자동화로 데이터 자산화 구현
- **🎯 Hybrid RAG Pipeline**: Intent 분류→KB 우선 응답→Context 필터링 3단계 파이프라인으로 환각 최소화 및 답변 정확도 개선
- **⚡ Performance**: PostGIS GiST 인덱스 + H3 격자 + Redis 캐시로 **TPS 40→7,000+** (175배), **응답 2.5s→3ms** (cache hit)
- **🔧 Multi-GPU Serving**: vLLM Docker 환경에서 NCCL 공유 메모리 이슈 해결 및 Volume 캐싱으로 배포 시간 **20분→1분**
- **🛡 Reliability**: 수중 네트워크 단절 환경 대응 Bulk Insert API 설계 및 재전송/중복/부분 실패 대응 트랜잭션 로직

> 제15회 ICT 피우다프로젝트 최우수상(정보통신산업진흥원장상, 1위) 수상

<br/>

### 🛒 모구시장
세션 기반 AI 추천(TRON)과 결제·재고 정합성을 보장하는 공동구매 커머스 플랫폼

`Spring Boot` `JPA` `Redis` `RabbitMQ` `vLLM` `TRON`

- **🤖 AI Rec Pipeline**: 1,600만+ 건 공공데이터로 TRON 파인튜닝 + LLM Re-ranking 2-Stage 추천 파이프라인
- **💳 Payment Reliability**: PortOne Webhook + 서버 재조회 SSOT 이중 검증으로 위·변조/누락 방지, 상태 머신과 멱등성 키로 일관성 보장
- **⚡ Concurrency Control**: JPA 비관적 락으로 동시성 해결, **JMeter 1,000 VUs에서 오버셀 0건** 달성
- **🔄 Workflow Automation**: 누적 주문량 기반 계단식 할인 및 자동 정산(환불/포인트) 프로세스로 운영 공수 절감

<br/>

### 💬 StoryBridge
실시간 채팅 인프라와 AI 피드백을 분리 서빙·관측(Observability) 기반으로 운영·통합한 네트워킹 플랫폼

`Spring Boot` `STOMP` `RabbitMQ` `FastAPI` `Prometheus` `Grafana` `Elasticsearch`

- **⚡ Real-time Infra**: SimpleBroker→STOMP Relay+RabbitMQ 전환으로 **k6 1,000 VUs에서 채팅 서버 CPU 65% 감소**
- **🤖 AI Serving**: FastAPI 기반 AI 피드백 서버 분리 구축·배포로 메인 서버 부하 분산
- **📊 Observability**: Micrometer 커스텀 메트릭 수집 + PromQL 조인으로 **사용자/경로별 예상 과금액 실시간 산출** Grafana 대시보드
- **🔍 Search**: Elasticsearch Nori 형태소 분석 + Multi-field(kor/eng) 매핑으로 한/영 혼합 텍스트 검색 품질 개선
- **🔧 Tool Chaining**: Azure Vision API 한국어 미지원 제약 해결을 위한 Azure 캡션→Groq 번역 2-step 체이닝 파이프라인

<br/>

### 🥗 오래살장
**과기정통부 주최 K-해커톤 본선 진출작** | VLM 기반 식단 분석 및 개인화 RAG 헬스케어 코칭 솔루션

`FastAPI` `Qwen2-VL` `RAG` `FAISS` `TRON`

- **📸 Multi-modal Pipeline**: Qwen2-VL로 비정형 식단 이미지→영양소/노화 인자 구조화 JSON 추출 자동화
- **🎯 Personalized RAG**: 사용자 건강 데이터(Context) + 분석 결과(Fact) + 저속노화 가이드(Retrieval) 결합 맞춤 레시피 생성
- **📊 Algorithm Engine**: AHEI/aMED 논문 기반 5개 핵심 지표 가중치로 '저속노화 점수' 산출 알고리즘 개발
- **🔄 Real-time Serving**: FAISS HNSW 인덱스 실시간 증분 업데이트(add_with_ids)로 신규 아이템 콜드스타트 해소

<br/>

## 💗 Awards & Achievements

| 수상/성과 | 주최/주관 | 날짜 |
|:---|:---|:---:|
| 🥇 **제15회 ICT 콤플렉스 SW 개발 공모전 최우수상(1위)** | 과학기술정보통신부 / NIPA | 2025.12 |
| 🎯 **제13회 K-해커톤 본선 진출** | 과학기술정보통신부 / NIPA | 2025.07 |
| 🥈 **멋쟁이사자처럼 2025 전국 운영진 연합 트렌디톤 최우수상(2위)** | 사단법인 멋쟁이사자처럼 | 2025.02 |

<br/>

## 💗 Leadership & Community

**CILAB 학부 연구생** | 2024.03 - 현재
- StoryBridge 개발: RabbitMQ 기반 채팅 및 AI 피드백·모니터링 서버 핵심 기능 전담 구현
- Prometheus(node_exporter, cAdvisor) 및 Grafana로 다수 서버 리소스 통합 관측 및 병목/과부하 탐지 환경 구축
- 2024 대학생 논문 경진대회 투고: "자동 지식 그래프 구축 기반 이기종 문서 요약 기법 제안"

**멋쟁이사자처럼 13기 대표 (회장)** | 2025.01 - 2025.12
- 40명 규모 다직군 지부 운영 총괄 (모집·온보딩·팀빌딩·일정/산출물 관리)
- 백엔드 멘토링: 기초·심화 투트랙 설계/운영 (JPA·영속성·Spring Security / Redis·RabbitMQ·동시성·모니터링)
- **전국 연합 해커톤 Top 49/250(상위 20%) 3개 팀 진출** (단일 대학 최다·공동 1위, 전년 0팀→3팀)
- 팀장으로 지부 멤버들과 팀 구성, 대외 공모전 최우수상(1위) 수상

**구름톤 유니브 4기 백엔드 운영진** | 2025.01 - 2025.12
- GitHub Projects·Issues 기반 협업 워크플로우 표준화 도입
- DB 스키마·서버 아키텍처·코드 리뷰 및 트레이드오프 기반 피드백 제공
- Redis·RabbitMQ·동시성 제어·모니터링 등 고트래픽/아키텍처 주제 기술 스터디 주도

<br/>

## 💗 Education & Certificate

**국립금오공과대학교**
- 컴퓨터공학전공 (주전공)
- AI로봇융합전공 (부전공)

**Certificate**
- TensorFlow Developer Certificate (Google)

<br/>

## 💗 Contact

- 📧 Email: libraryofjiyu@gmail.com
- 💼 LinkedIn: [https://linkedin.com/in/jungjiyu](https://linkedin.com/in/jungjiyu)

<br/>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FFD1E8,100:FF7EB3&height=2&section=header" />


</div>
