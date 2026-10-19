# 법무법인 로연 블로그 운영 시스템

내부 작성 원고를 대상으로 하는 Markdown 기반 수동·AI 보조 운영 체계다. 자동 수집기, 계정 연동, 자동 발행기, 예약 작업은 포함하지 않는다.

## 시작하기

1. [공통 운영 원칙](POLICY.md)을 읽는다.
2. [서울 설정](seoul/config.md)과 [광주 설정](gwangju/config.md)에 사용자가 확인한 URL·공식 정보만 입력한다. 과거 대화의 블로그를 어느 사무소에도 자동 배정하지 않는다.
3. 새 원고는 [발행 전 검수](prepublication-workflow.md), 기존 글은 [수집·분석](collection-workflow.md) 절차를 따른다.
4. 해당 사무소의 `inventory.md`, `priorities.md`, `metrics.md`, `observations.md`, `changes.md`, `topics.md`에 각각 기록한다.
5. [성과 비교](measurement-workflow.md) 후 [보고서 운영](reports/README.md)에 따라 주간·월간 보고서를 작성한다.

## 구현 범위와 외부 의존성

| 기능 | 현재 사용할 수 있는 부분 | 추가로 필요한 것 |
|---|---|---|
| 원고 검수 | 체크리스트, 근거 확인표, 승인 기록 | 내부에서 비식별 처리한 원고와 담당 변호사 검토 |
| 기존 글 조사 | 공개 접근·본문 평가·누락 관리 절차 | 사무소별 블로그 URL, 필요 시 공개 URL 목록 |
| 우선순위 | P0~P3 기준과 사무소별 작업 목록 | 실제 열람 결과·자료 |
| 성과 비교 | 입력표, 결측·분모·기간 비교 규칙 | 계정 보유자의 비식별 집계 통계 |
| 검색·AI 관찰 | 질의·시각·조건·출처 URL 기록표 | 실제 검색 또는 AI 검색 세션 |
| 보고 | 주간·월간 양식과 분리 집계 규칙 | 각 사무소에서 확인한 운영 데이터 |
| 수정·발행 | 승인 전후 절차 | 구체적 변경안에 대한 사용자 승인과 계정 작업자 |

계정 비밀번호·토큰을 이 저장소나 채팅에 입력하지 않는다. 공개 읽기만 가능한 경우에도 순위·유입·인용 실적을 임의 생성하지 않는다.

## 스킬 적용

[SKILL.md](../.agents/skills/fire-your-seo-agency/SKILL.md)와 한국어 [SEO](../.agents/skills/fire-your-seo-agency/references/seo.md), [AEO](../.agents/skills/fire-your-seo-agency/references/aeo.md), [GEO](../.agents/skills/fire-your-seo-agency/references/geo.md), [LLMO](../.agents/skills/fire-your-seo-agency/references/llmo.md), [NEO](../.agents/skills/fire-your-seo-agency/references/neo-naver.md), [콘텐츠](../.agents/skills/fire-your-seo-agency/references/content.md), [측정](../.agents/skills/fire-your-seo-agency/references/measure.md)을 바탕으로 한다.

사용자 지시를 우선하여 AI의 원고 생성은 금지한다. 직답·Q&A·소제목 보강은 누락을 지적하고 내부 작성자에게 요청하는 방식이다. 수치·출처·학습 효과에 관한 스킬의 일반 설명을 개별 사이트의 검증된 사실로 취급하지 않는다.

네이버가 관리하는 canonical·robots·JSON-LD·사이트맵·IndexNow·301은 블로그 운영자의 필수 실행 과제로 삼지 않는다. 변경할 수 없는 항목은 적용 제외와 이유를 기록한다. 외부 홈페이지 작업은 별도 범위·승인이 필요하다. 제목 글자 수와 Q&A 개수는 고정 합격 기준이 아니다. 네이버 에디터의 소제목·표 기능으로 옮기며 Markdown 기호가 그대로 노출되지 않는지 확인한다.
