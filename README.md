# 면접준비 스터디 자료실

> 만화로 한 번, 도면으로 다시 한 번.

신입·주니어 백엔드 면접을 준비하며 만든 스터디 자료를 한곳에 모았습니다.
개념은 **만화**로 먼저 잡고, 구조는 **판서 도면**으로 다시 보고, 동작은 **시뮬레이터**로 한 단계씩 따라갑니다.

### 🔗 https://maoemong.github.io/interview-study/

설치할 것도, 로그인할 것도 없습니다. 링크만 열면 바로 시작합니다.

| 문서 | Q&A | 시뮬레이터 |
|:---:|:---:|:---:|
| 7종 | 270문항 | 5종 |

---

## 상시 자료

회차와 상관없이 계속 보는 자료입니다.

### [CS 면접 Q&A 정리본 — 270문항](https://maoemong.github.io/interview-study/cs-interview-qa.html)

21개 파트, Java·Spring·JPA·DB부터 React·TypeScript까지.

`Java` `JVM·GC` `Spring` `JPA` `DB·SQL` `HTTP·REST` `보안` `React` `TypeScript` `MSA` `실무 상황형`

- 카테고리 필터 + 실시간 검색
- **퀴즈 모드** — 답을 가린 채 스스로 물어볼 수 있습니다

### [요즘 공고는 어떤 기술을 원할까?](https://maoemong.github.io/interview-study/job-requirements.html)

원티드·잡코리아·사람인·점핏·인크루트의 신입·주니어 공고에서 자주 나오는 필수 기술과 우대사항을 정리했습니다. 방향 잡을 때 먼저 보면 좋습니다.

- 언어·프레임워크 / 데이터·협업·CS 기초 / 인프라·운영 / 설계·협업·AI
- 우대사항은 전부 채우는 게 아니라 내 강점이 될 한두 개를 고르는 칸이라는 관점
- 슬라이드 9장

---

## 회차별 자료

각 항목은 **만화로 개념 → 판서로 구조 → 시뮬레이터로 단계별 확인** 순서로 구성했습니다.
시뮬레이터는 `▶ 재생` / `한 단계 ▸` / `⟲ 리셋`으로 조작합니다.

### [Spring MVC — 만화 · 도면 시뮬레이터](https://maoemong.github.io/interview-study/spring-mvc/)

요청 하나가 서버 안에서 어디를 거쳐 응답이 되는지 추적합니다.

1. **요청의 여정** — DispatcherServlet → HandlerMapping → HandlerAdapter → Controller → MessageConverter
2. **두 Controller** — `@Controller`의 ViewResolver 경로 vs `@RestController`의 MessageConverter 경로
3. **데이터 받기** — `@PathVariable` / `@RequestParam` / `@RequestBody`를 언제 쓰는가
4. **상태 코드** — 서버가 의도를 코드로 표현하는 방법
5. **검증·예외** — `@Valid`로 입구에서 거르기

### [트랜잭션과 AOP — 만화 · 도면 시뮬레이터](https://maoemong.github.io/interview-study/spring-tx/)

계좌 이체를 예제로 트랜잭션의 원자성과 프록시 동작을 따라갑니다.

1. **3계층** — Controller / Service / Repository의 책임 분리
2. **트랜잭션** — 정상 이체 vs 입금 중 실패
3. **`@Transactional`**
4. **AOP** — 프록시가 언제 끼어드는가
5. **함정** — 자주 걸리는 케이스

### [데이터 모델링과 SQL — 도면 시뮬레이터](https://maoemong.github.io/interview-study/sql-db/)

1. **ERD** — 관계선은 양쪽 끝을 두 번 읽는다
2. **정규화** — 이상현상 체험 후 1NF → 2NF → 3NF 단계별 분리
3. **실행순서** — SQL이 실제로 평가되는 순서
4. **조인**
5. **NULL**
6. **윈도우 함수**
7. **트랜잭션 격리수준**

### [MSA — 서비스를 쪼갠다는 것](https://maoemong.github.io/interview-study/msa/)

> 오늘의 질문 — 서비스를 쪼개면, 트랜잭션은 누가 책임지는가

1. **모놀리식** — 출발점과 한계
2. **MSA란** — 무엇을 해결하는가
3. **DDD** — 서비스 분리의 기준
4. **동기 통신** — API 호출과 Gateway
5. **비동기 통신** — 이벤트와 Kafka
6. **분산 트랜잭션** — 쪼개진 `@Transactional`
7. **사가 패턴** — 보상으로 되돌리기
8. **운영의 산** — Docker·K8s·관측 (다음 회차 예고)

### [Docker & Kubernetes — Image에서 서비스까지](https://maoemong.github.io/interview-study/docker-kubernetes/)

Docker Image가 Container로 실행되고, Kubernetes의 Pod·Deployment·Service·Ingress를 거쳐 외부 요청을 받기까지의 흐름을 도면과 시뮬레이터로 확인합니다.

1. **Docker 흐름** — Dockerfile → `docker build` → Image → `docker run` → Container
2. **Image·Container** — Dockerfile, CMD·ENTRYPOINT, 포트·멀티 스테이지 빌드
3. **Compose** — 서비스 이름 DNS, Volume, 환경변수·ConfigMap·Secret
4. **Kubernetes** — Cluster, Control Plane, Node, YAML 기본 축
5. **Pod·Deployment** — 1 Pod = 1 Container 관행, ReplicaSet, 원하는 상태 유지
6. **Service·Ingress** — ClusterIP, NodePort, HTTP 경로 라우팅
7. **도구·운영** — Minikube·kubectl·Helm, Registry, Rolling Update, port-forward

---

## 구조

빌드 도구도 의존성도 없는 순수 정적 사이트입니다. 클론해서 `index.html`을 열면 그대로 동작합니다.

```text
.
├── index.html              # 자료실 허브
├── cs-interview-qa.html    # CS 면접 Q&A 270문항
├── job-requirements.html   # 채용 공고 기술 스택 분석
├── spring-mvc/             # Spring MVC 시뮬레이터
├── spring-tx/              # 트랜잭션·AOP 시뮬레이터
├── sql-db/                 # 데이터 모델링·SQL 시뮬레이터
├── msa/                    # MSA 시뮬레이터
└── docker-kubernetes/      # Docker·Kubernetes 시뮬레이터
```

시뮬레이터는 인라인 SVG와 바닐라 JS로 구현했습니다.

## 배포

`master` 브랜치에 푸시하면 GitHub Pages로 자동 배포됩니다.
