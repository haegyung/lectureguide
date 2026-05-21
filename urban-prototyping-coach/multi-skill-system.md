# Urban Prototyping Coach: 여러 기준이 함께 쓰이는 방식

## Goal

학생에게는 `urban-prototyping-coach` 하나가 코치처럼 보이게 두고,
뒤에서는 지속가능한 Urban테크 수업에 필요한 기준을 역할별로 나눠 적용한다.

## 역할 나눔

| 도움 | 담당 기준 | 하는 일 | 언제 쓰나 |
| --- | --- | --- | --- |
| 학생 코칭 | `urban-prototyping-coach` | 아이디어를 질문, 작은 실험, 증거, 다음 결정으로 바꾼다 | 항상 먼저 |
| 문제 범위 정리 | `cogarch` | 행위자, 상황, 장소, 책임 범위를 줄인다 | 문제 범위가 크거나 여러 행위자가 섞일 때 |
| 증거와 주장 구분 | `vector-language-cognition` | 관찰, 간접 신호, 해석, 말할 수 있는 범위를 나눈다 | 증거가 약한데 주장이 커질 때 |
| 패키지 검증 | `generate-skill` | 스킬 구조, 호환성, 배포 검증을 관리한다 | 스킬 파일이나 배포 구조를 바꿀 때 |

## 학생에게 보이는 원칙

학생이나 강의 참가자에게는 항상 `urban-prototyping-coach`가
보이는 주 스킬로 동작합니다.

다른 스킬은 아래 역할만 맡습니다.

- `cogarch`: 구조 정렬
- `vector-language-cognition`: 증거 경계 정렬
- `generate-skill`: 패키징과 검증 정렬

즉, 뒤에서는 여러 기준을 쓰더라도
**학생에게는 하나의 코칭 흐름**으로 보이게 유지합니다.

## 함께 들고 가는 메모

여러 기준을 함께 쓰더라도 같은 프로젝트 메모를 보고 판단합니다.
아래 항목명은 내부 기록용입니다.

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

## 진행 순서

### 1. 문제를 한 문장으로 줄이기

- 중심 기준: `urban-prototyping-coach`
- 결과: `learning_question`이 있는 1문장 문제 정의

### 2. 사람과 장소를 좁히기

- 중심 기준: `urban-prototyping-coach`
- 보조 기준: `cogarch`
- 결과: `primary_actor`, `situation`, `place_or_touchpoint`, `current_workaround`

### 3. 오늘의 실험 방식 고르기

- 중심 기준: `urban-prototyping-coach`
- 결과: `prototype_method`, 오늘 만들 가장 작은 실험물

### 4. 증거와 주장 범위 확인하기

- 중심 기준: `urban-prototyping-coach`
- 보조 기준: `vector-language-cognition`
- 결과: `evidence_targets`, `evidence_state`, `claim_boundary`

### 5. 문서와 배포 상태 관리하기

- 중심 기준: `generate-skill`
- 보조 기준: `cogarch`
- 결과: 갱신된 `SKILL.md`, 운영 문서, `MANIFEST.md`, 검증 기록

## 적용 규칙

- 아이디어를 바로 실험 질문으로 줄일 수 있으면 `urban-prototyping-coach`만 사용합니다.
- 행위자가 2개 이상 섞이거나 도시 전체 문제처럼 커지면 `cogarch` 기준으로 사람과 상황을 먼저 줄입니다.
- 클릭이나 인터뷰 반응만 있는데 도시 효과나 정책 효과를 말하려 하면 `vector-language-cognition` 기준으로 말할 수 있는 범위를 낮춥니다.
- 스킬 구조, 함께 제공되는 문서, 검증 방식을 바꾸면 `generate-skill` 기준으로 닫습니다.

## 마무리 방식

한 번의 반복은 항상 아래 3줄로 닫습니다.

1. 결론
2. 근거
3. 다음 행동

그리고 시스템 레벨에서는 아래 3개가 함께 남아야 합니다.

- 어떤 기준이 중심이었는가
- 어떤 보조 기준이 들어왔는가
- 어떤 증거 상태와 말할 수 있는 범위로 닫았는가

## 예시

`분리배출 도우미`를 예로 들면:

1. `urban-prototyping-coach`가 자취생의 분리배출 혼란을 학습 질문으로 줄입니다.
2. `cogarch`가 `자취생 / 배출 직전 / 집 앞 배출 지점`으로 상황을 줄입니다.
3. `urban-prototyping-coach`가 `Wizard of Oz` 또는 `Tiny Functional Prototype`을 고릅니다.
4. `vector-language-cognition`이 `실제 입력`, `재질문`, `다시 사용`은 관찰 신호로 두고, `도시 전체 수요`는 아직 검증되지 않은 주장으로 남깁니다.
5. `generate-skill`은 이 흐름이 패키지 안에서 재사용 가능하게 문서와 검증 구조로 닫습니다.
