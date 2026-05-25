# Urban Routing Contract

## Representative Boundary

- representative skill surface: `SKILL.md`
- child implementation surface: `skills/*/SKILL.md`
- portable command surface: `commands/urban/*.md`
- current source of truth: `student-guide.md`

## Canonical Command Rules

- canonical command names:
  - `/urban:help`
  - `/urban:scope`
  - `/urban:service-loop`
  - `/urban:prototype`
  - `/urban:demo-review`
  - `/urban:pitch`
  - `/urban:spec`
  - `/urban:plan`
  - `/urban:context-audit`
- child skill은 분석 절차를 소유하지만 command spelling을 단독으로 바꾸지 않습니다.
- `student-guide.md`, `README.md`, `commands/urban/*.md`, `skills/*/SKILL.md`는 아래 command spelling과 연결 관계를 같이 유지합니다.

## Command Matrix

| command | child skill | input focus | output focus |
| --- | --- | --- | --- |
| `/urban:help` | representative only | 현재 단계 파악 | 다음 command 1개 추천 |
| `/urban:scope` | `skills/urban-scope` | 문제, 행위자, 상황, 장소, 마찰 | 학습 질문과 첫 실험 방향 |
| `/urban:service-loop` | `skills/urban-service-loop` | 입력, 처리, 결과, 다음 행동 | 서비스 루프와 막힘 지점 |
| `/urban:prototype` | `skills/urban-prototype` | 가장 작은 실험물 | 빌드 prompt와 관찰 포인트 |
| `/urban:demo-review` | `skills/urban-demo-review` | 시연 순서와 사용자 반응 | 시연 체크리스트와 수정 우선순위 |
| `/urban:pitch` | `skills/urban-pitch` | 무엇을 왜 시험했는가 | 1페이지 설명과 claim boundary |
| `/urban:spec` | `skills/urban-spec` | 기능 범위와 제외 범위 | 작은 구현 명세 |
| `/urban:plan` | `skills/urban-plan` | 구현 순서와 검증 순서 | 하루 단위 빌드 계획 |
| `/urban:context-audit` | `skills/urban-context-audit` | 폴더, 문서, 맥락 누락 | AI가 읽기 좋은 context 정리안 |

## Helper Skill Rule

- `skills/urban-evidence-boundary`는 direct command owner가 아니라 cross-cutting helper입니다.
- 아래 상황이면 다른 child skill 뒤에 붙습니다.
  - 관찰보다 해석이 커졌을 때
  - proxy signal만으로 수요나 효과를 과장할 때
  - 발표 문구가 현재 evidence보다 앞서 나갈 때

## Drift Checklist

- command spelling은 이 문서를 기준으로 유지합니다.
- root owner skill과 child skill의 source of truth는 `student-guide.md`로 고정합니다.
- `pretotyping-guide.md`는 command routing의 기준이 아니라 historical reference입니다.
