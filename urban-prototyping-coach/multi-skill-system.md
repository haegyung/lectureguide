# Urban Prototyping Multi-Skill System

## Goal

`urban-prototyping-coach`를 단일 동반 스킬이 아니라,
지속가능한 Urban테크 프로젝트에서 여러 스킬이 역할을 나눠 함께 작동하는 시스템으로 정의한다.

## 역할 분담

| 역할 | 담당 | 하는 일 | 언제 들어오는가 |
| --- | --- | --- | --- |
| 학생 코칭 중심 | `urban-prototyping-coach` | 아이디어를 질문, 작은 실험, 증거, 다음 결정으로 바꾼다 | 기본 진입점 |
| 문제 줄이기 child skill | `skills/urban-scope` | 행위자, 상황, 장소, 마찰, 학습 질문으로 줄인다 | `/urban:scope` 단계 |
| 흐름 설계 child skill | `skills/urban-service-loop` | 입력, 처리, 결과, 다음 행동의 서비스 루프를 정리한다 | `/urban:service-loop` 단계 |
| 프로토타입 child skill | `skills/urban-prototype` | 가장 작은 실험물 형식을 정하고 빌드 프롬프트를 만든다 | `/urban:prototype` 단계 |
| 시연 점검 child skill | `skills/urban-demo-review` | 시연 흐름과 관찰 포인트를 점검한다 | `/urban:demo-review` 단계 |
| 발표 정리 child skill | `skills/urban-pitch` | 1페이지 설명, 발표 요약, 주장 경계를 정리한다 | `/urban:pitch` 단계 |
| 구현 정리 child skill | `skills/urban-spec`, `skills/urban-plan` | 기능 범위와 작은 구현 계획을 정리한다 | 설계로 넘어갈 때 |
| 맥락 점검 child skill | `skills/urban-context-audit` | 폴더와 메모가 AI에게 충분한 맥락을 주는지 점검한다 | 파일 구조를 정리할 때 |
| 증거 경계 child skill | `skills/urban-evidence-boundary` | 관찰, 해석, 주장 범위를 다시 잠근다 | 증거가 약한데 주장이 커질 때 |
| 행위자 구조 보조 | `cogarch` | actor-first 구조를 정리한다 | child skill이 범위를 더 줄여야 할 때 |
| 증거 경계 보조 | `vector-language-cognition` | 관찰, 간접 신호, 해석, 주장 범위를 구분한다 | evidence child skill의 기준이 더 필요할 때 |
| 패키지와 검증 관리 | `generate-skill` | 스킬 구조, 호환성, 검증 계약을 관리한다 | 스킬 파일이나 시스템 구조를 바꿀 때 |

## Single Visible Owner Rule

학생이나 강의 참가자에게는 항상 `urban-prototyping-coach`가
보이는 주 스킬로 동작합니다.

다른 스킬은 아래처럼 owner 뒤에서 역할을 나눕니다.

- `skills/urban-*`: 현재 단계별 child skill
- `cogarch`: 구조 정렬 helper
- `vector-language-cognition`: 증거 경계 helper
- `generate-skill`: 패키징과 검증 정렬 helper

즉, 시스템은 멀티 스킬이지만
**사용자 표면은 하나의 코칭 흐름**으로 유지합니다.

## 함께 넘겨받는 정보

모든 스킬은 아래 패킷을 공유합니다.

```text
project_name:
urban_domain:
primary_actor:
situation:
place_or_touchpoint:
current_workaround:
friction:
learning_question:
sustainability_hypothesis:
prototype_method:
evidence_targets:
evidence_state:
claim_boundary:
next_decision:
```

## 단계별 흐름

### 1. 문제 줄이기

- 중심 담당: `urban-prototyping-coach`
- child skill: `skills/urban-scope`
- 결과: `learning_question`이 있는 1문장 문제 정의

### 2. 행위자와 장소 줄이기

- 중심 담당: `urban-prototyping-coach`
- child skill: `skills/urban-scope`
- 보조 기준: `cogarch`
- 결과: `primary_actor`, `situation`, `place_or_touchpoint`, `current_workaround`

### 3. 프로토타이핑 방식 고르기

- 중심 담당: `urban-prototyping-coach`
- child skill: `skills/urban-service-loop`, `skills/urban-prototype`
- 결과: `prototype_method`, `today's smallest artifact`

### 4. 증거 경계 점검

- 중심 담당: `urban-prototyping-coach`
- child skill: `skills/urban-evidence-boundary`, `skills/urban-demo-review`
- 보조 기준: `vector-language-cognition`
- 결과: `evidence_targets`, `evidence_state`, `claim_boundary`

### 5. 설계 이동 판단

- 중심 담당: `urban-prototyping-coach`
- child skill: `skills/urban-spec`, `skills/urban-plan`, `skills/urban-pitch`
- 결과: 구현 범위, 빌드 순서, 현재 주장 경계가 분리된 발표 초안

### 6. 시스템과 패키지 정리

- 중심 담당: `generate-skill`
- 보조 기준: `cogarch`
- 결과: 바뀐 `SKILL.md`, 흐름 문서, manifest, 검증 기록

## 흐름 규칙

- 아이디어를 바로 실험 질문으로 줄일 수 있으면 `urban-prototyping-coach`와 `skills/urban-scope`만 사용합니다.
- 행위자가 2개 이상 섞이거나 도시 전체 문제처럼 커지면 `cogarch`를 호출해 actor-first로 줄입니다.
- 클릭이나 인터뷰 반응만 있는데 도시 효과나 정책 효과를 말하려 하면 `skills/urban-evidence-boundary`와 `vector-language-cognition` 규칙으로 claim boundary를 낮춥니다.
- 스킬 구조, companion docs, validation contract를 바꾸면 `generate-skill`이 owner가 됩니다.

## Closeout Contract

한 번의 반복은 항상 아래 3줄로 닫습니다.

1. 결론
2. 근거
3. 다음 행동

그리고 시스템 레벨에서는 아래 3개가 함께 남아야 합니다.

- 어떤 스킬이 owner였는가
- 어떤 helper가 개입했는가
- 어떤 evidence_state / claim_boundary로 닫았는가

## Example

`분리배출 도우미`를 예로 들면:

1. `urban-prototyping-coach`와 `skills/urban-scope`가 자취생의 분리배출 혼란을 학습 질문으로 줄입니다.
2. `cogarch`가 `자취생 / 배출 직전 / 집 앞 배출 지점`으로 상황을 더 줄입니다.
3. `skills/urban-service-loop`와 `skills/urban-prototype`가 `Wizard of Oz` 또는 `Tiny Functional Prototype` 경로를 고릅니다.
4. `skills/urban-evidence-boundary`와 `vector-language-cognition`이 `실제 입력`, `재질문`, `다시 사용`은 관찰 신호로 두고, `도시 전체 수요`는 미검증 claim으로 남깁니다.
5. `generate-skill`은 이 흐름이 패키지 안에서 재사용 가능하게 command, child skill, 검증 구조로 닫습니다.
