# Urban Prototyping Coach / 도시 프로토타이핑 코치

이 폴더는 수업 배포용 일반 Markdown 패키지입니다. 학생과 강사는 이 문서를 읽고, 필요한 프롬프트와 스킬 파일을 LLM 도구에 붙여 아이디어를 작은 실험으로 줄일 수 있습니다.

This folder is a plain Markdown course package. Students and instructors can read the guide, then paste the relevant prompts and skill files into an LLM tool to turn an idea into a small experiment.

## 한국어 사용 설명

### 핵심 목표

큰 서비스를 한 번에 완성하는 것이 목표가 아닙니다. 먼저 확인할 질문을 정하고, 작은 프로토타입으로 실제 반응이나 관찰 기록을 남긴 뒤, 다음 설계 판단으로 이어 가는 것이 목표입니다.

### 처음 쓰는 순서

1. `student-guide.md`를 읽고 아이디어를 `상황 -> 작은 실험 -> 증거 -> 다음 설계` 흐름으로 봅니다.
2. `SKILL.md`를 LLM 도구에 넣어 이 패키지의 코칭 기준을 알려 줍니다.
3. `commands/urban/help.md`를 먼저 넣어 현재 단계에 맞는 명령을 고릅니다.
4. 필요한 경우 `references/routing-contract.md`에서 명령과 하위 스킬 연결을 확인합니다.
5. 현재 단계와 맞는 `skills/urban-*/SKILL.md`를 추가해 더 좁은 작업으로 진행합니다.
6. 결과를 발표 문장으로 끝내지 말고, 클릭, 신청, 질문, 재사용, 관찰 메모 같은 증거로 다시 확인합니다.

### 명령별 사용법

| 명령 | 사용 장면 | 함께 보면 좋은 파일 |
| --- | --- | --- |
| `/urban:help` | 어떤 단계인지 모르겠을 때 | `commands/urban/help.md`, `SKILL.md` |
| `/urban:scope` | 문제를 작게 줄이고 싶을 때 | `commands/urban/scope.md`, `skills/urban-scope/SKILL.md` |
| `/urban:service-loop` | 서비스 흐름을 정리할 때 | `commands/urban/service-loop.md`, `skills/urban-service-loop/SKILL.md` |
| `/urban:prototype` | 작은 실험물을 정할 때 | `commands/urban/prototype.md`, `skills/urban-prototype/SKILL.md` |
| `/urban:demo-review` | 시연을 점검할 때 | `commands/urban/demo-review.md`, `skills/urban-demo-review/SKILL.md` |
| `/urban:pitch` | 발표 문장을 만들 때 | `commands/urban/pitch.md`, `skills/urban-pitch/SKILL.md` |
| `/urban:spec` | 구현 범위를 정할 때 | `commands/urban/spec.md`, `skills/urban-spec/SKILL.md` |
| `/urban:plan` | 하루 단위 계획을 잡을 때 | `commands/urban/plan.md`, `skills/urban-plan/SKILL.md` |
| `/urban:context-audit` | 프로젝트 폴더와 설명이 흩어졌을 때 | `commands/urban/context-audit.md`, `skills/urban-context-audit/SKILL.md` |

`skills/urban-evidence-boundary/SKILL.md`는 직접 명령이 아니라 보조 기준입니다. 관찰보다 해석이 커지거나, 아직 약한 증거로 발표 문장이 앞서 나갈 때 함께 씁니다.

### 도구별 사용

- ChatGPT: `SKILL.md`, 필요한 `commands/urban/*.md`, 필요한 `skills/urban-*/SKILL.md`를 함께 넣고 현재 아이디어를 붙입니다.
- Claude: `SKILL.md`를 먼저 넣고, 현재 단계에 맞는 command와 child skill을 이어서 넣습니다.
- Claude Code 또는 로컬 에이전트: 이 폴더를 작업 경로에 두고 `SKILL.md`, `commands/urban/`, `skills/`를 읽게 합니다.
- 일반 LLM 채팅: 스킬 자동 활성화가 없으면 command 파일의 본문을 복사해 쓰면 됩니다.

### 파일 구성

- `student-guide.md`: 현재 학생용 기준 문서입니다.
- `pretotyping-guide.md`: 초기 원문을 참고용으로 보존한 문서입니다.
- `SKILL.md`: 이 패키지의 대표 코칭 스킬입니다.
- `commands/urban/`: 복사 가능한 명령 프롬프트 묶음입니다.
- `skills/`: 단계별 하위 스킬 세트입니다.
- `references/routing-contract.md`: 명령 이름, 하위 스킬, 입력/출력 계약을 고정한 기준 문서입니다.
- `references/command-skill-concept-map.md`: 대표 스킬, 하위 스킬, 명령 연결을 한눈에 보는 문서입니다.
- `domain-alignment-map.md`: 이 패키지가 어떤 기준과 도메인 규칙을 받아들였는지 정리한 문서입니다.
- `multi-skill-system.md`: 여러 스킬을 하나의 코칭 흐름으로 쓰는 방법입니다.
- `MANIFEST.md`: 배포 파일 목록과 검증 기록입니다.

## English User Guide

### Core Goal

The goal is not to build a full service at once. The goal is to choose a question, test it with a small prototype, capture user reactions or observation notes, and use that evidence for the next design decision.

### First Use Flow

1. Read `student-guide.md` and frame your idea as `situation -> small experiment -> evidence -> next design`.
2. Add `SKILL.md` to your LLM tool so it understands the coaching rules.
3. Start with `commands/urban/help.md` to choose the right command for your current stage.
4. If needed, check `references/routing-contract.md` to see how commands and child skills connect.
5. Add the matching `skills/urban-*/SKILL.md` file for a narrower task.
6. Do not stop at a polished explanation. Check the result against evidence such as clicks, sign-ups, questions, reuse, or observation notes.

### Command Guide

| Command | Use it when | Helpful files |
| --- | --- | --- |
| `/urban:help` | You are unsure where to start | `commands/urban/help.md`, `SKILL.md` |
| `/urban:scope` | You need to narrow the problem | `commands/urban/scope.md`, `skills/urban-scope/SKILL.md` |
| `/urban:service-loop` | You need to clarify the service flow | `commands/urban/service-loop.md`, `skills/urban-service-loop/SKILL.md` |
| `/urban:prototype` | You need a small experiment artifact | `commands/urban/prototype.md`, `skills/urban-prototype/SKILL.md` |
| `/urban:demo-review` | You need to review a demo | `commands/urban/demo-review.md`, `skills/urban-demo-review/SKILL.md` |
| `/urban:pitch` | You need to explain the work | `commands/urban/pitch.md`, `skills/urban-pitch/SKILL.md` |
| `/urban:spec` | You need to define build scope | `commands/urban/spec.md`, `skills/urban-spec/SKILL.md` |
| `/urban:plan` | You need a day-level plan | `commands/urban/plan.md`, `skills/urban-plan/SKILL.md` |
| `/urban:context-audit` | Project context is scattered | `commands/urban/context-audit.md`, `skills/urban-context-audit/SKILL.md` |

`skills/urban-evidence-boundary/SKILL.md` is a helper, not a direct command. Use it when interpretation is running ahead of observation, or when a pitch claim is stronger than the current evidence.

### Tool Use

- ChatGPT: provide `SKILL.md`, the relevant `commands/urban/*.md`, the relevant `skills/urban-*/SKILL.md`, and your current idea.
- Claude: provide `SKILL.md` first, then the command and child skill for the current stage.
- Claude Code or local agents: put this folder in the workspace and let the tool read `SKILL.md`, `commands/urban/`, and `skills/`.
- Generic LLM chat: if skill activation is not supported, copy the relevant command file into the chat.

### File Map

- `student-guide.md`: current student-facing guide.
- `pretotyping-guide.md`: preserved early reference document.
- `SKILL.md`: representative coaching skill.
- `commands/urban/`: portable command prompts.
- `skills/`: step-specific child skills.
- `references/routing-contract.md`: canonical command, child skill, input, and output contract.
- `references/command-skill-concept-map.md`: map of representative skill, child skills, and command prompts.
- `domain-alignment-map.md`: source and domain alignment notes.
- `multi-skill-system.md`: how multiple skills work as one coaching flow.
- `MANIFEST.md`: package inventory and verification log.

## Distribution / 배포

- No web server or build step is required.
- 별도 웹 서버나 빌드 과정이 필요 없습니다.
- Minimum teaching bundle: `student-guide.md`, `SKILL.md`, `commands/urban/`, and `skills/`.
- 최소 수업 묶음: `student-guide.md`, `SKILL.md`, `commands/urban/`, `skills/`.
- Use `MANIFEST.md` when you need the package inventory or verification history.
- 배포 파일 목록과 검증 기록은 `MANIFEST.md`에서 확인합니다.
