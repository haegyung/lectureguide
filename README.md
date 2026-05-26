# Lecture Guide / 수업 가이드

`urban-prototyping-coach`는 LLM을 써서 도시·서비스 아이디어를 작게 실험하고, 관찰한 증거를 다음 설계로 연결하는 수업용 Markdown/Skill 패키지입니다.

`urban-prototyping-coach` is a course-ready Markdown/Skill package for using LLMs to test urban or service ideas through small prototypes, collect evidence, and connect the result to the next design step.

## 한국어 사용 설명

### 1. 무엇을 받으면 되나요?

최신 배포본은 GitHub Releases에서 받습니다.

- Release: [Urban Prototyping Coach 2026-05-26](https://github.com/haegyung/lectureguide/releases/tag/urban-prototyping-coach-20260526)
- ZIP: `urban-prototyping-coach-20260526.zip`
- Checksum: `urban-prototyping-coach-20260526.zip.sha256`

저장소 안에서는 같은 파일이 `dist/`에 들어 있습니다.

### 2. 누가 쓰나요?

- 학생: 아이디어를 바로 크게 만들기 전에, 확인할 질문과 작은 실험을 정할 때 씁니다.
- 강사: 수업 진행, 실습 안내, 발표 점검, 피드백 기준을 맞출 때 씁니다.
- 운영자: `SKILL.md`, `commands/urban/`, `skills/`를 LLM 도구에 넣어 코칭 흐름을 재사용할 때 씁니다.

### 3. 빠른 시작

1. 릴리즈 ZIP을 내려받고 압축을 풉니다.
2. `urban-prototyping-coach/student-guide.md`를 먼저 읽습니다.
3. ChatGPT, Claude, Claude Code 같은 도구에 `SKILL.md`와 현재 단계에 맞는 `commands/urban/*.md`를 함께 넣습니다.
4. 아래 명령 흐름 중 하나를 골라 현재 아이디어를 붙여 요청합니다.
5. 나온 답을 그대로 완성품으로 보지 말고, 실제 사용자 반응이나 관찰 기록으로 다시 확인합니다.

### 4. 명령 흐름

| 명령 | 언제 쓰나 | 결과 |
| --- | --- | --- |
| `/urban:help` | 어디서 시작할지 모를 때 | 다음에 쓸 명령 1개 추천 |
| `/urban:scope` | 문제가 너무 클 때 | 학습 질문과 첫 실험 방향 |
| `/urban:service-loop` | 서비스 흐름이 흐릴 때 | 입력, 처리, 결과, 다음 행동 |
| `/urban:prototype` | 작은 실험물을 정할 때 | 빌드 프롬프트와 관찰 포인트 |
| `/urban:demo-review` | 시연 전후를 점검할 때 | 시연 체크리스트와 수정 우선순위 |
| `/urban:pitch` | 발표 문장을 정리할 때 | 1페이지 설명과 주장 경계 |
| `/urban:spec` | 구현 범위를 좁힐 때 | 작은 구현 명세 |
| `/urban:plan` | 작업 순서를 잡을 때 | 하루 단위 빌드 계획 |
| `/urban:context-audit` | AI가 읽을 맥락이 부족할 때 | 폴더와 문서 정리안 |

### 5. 파일 안내

- `urban-prototyping-coach/student-guide.md`: 학생용 주 문서입니다.
- `urban-prototyping-coach/SKILL.md`: LLM이 수업 기준을 따라 코칭하게 하는 대표 스킬입니다.
- `urban-prototyping-coach/commands/urban/`: 복사해 쓸 수 있는 명령별 프롬프트입니다.
- `urban-prototyping-coach/skills/`: 단계별 보조 스킬입니다.
- `urban-prototyping-coach/references/routing-contract.md`: 명령과 스킬 연결 기준입니다.
- `urban-prototyping-coach/MANIFEST.md`: 배포 파일 목록과 검증 기록입니다.
- `dist/`: 배포 ZIP과 checksum 파일입니다.
- `verification/`: 검증 요약과 화면 증거입니다.

### 6. 무결성 확인

```bash
cd dist
shasum -a 256 -c urban-prototyping-coach-20260526.zip.sha256
```

개발자가 패키지 자체를 검증할 때는 저장소 루트에서 아래 명령을 씁니다.

```bash
skills-ref validate urban-prototyping-coach
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py urban-prototyping-coach
```

## English User Guide

### 1. What should I download?

Use the latest package from GitHub Releases.

- Release: [Urban Prototyping Coach 2026-05-26](https://github.com/haegyung/lectureguide/releases/tag/urban-prototyping-coach-20260526)
- ZIP: `urban-prototyping-coach-20260526.zip`
- Checksum: `urban-prototyping-coach-20260526.zip.sha256`

The same release files are also stored in `dist/` in this repository.

### 2. Who is this for?

- Students: use it to turn a broad idea into a question, a small prototype, and observable evidence.
- Instructors: use it to guide workshops, reviews, demos, and feedback.
- Operators: use `SKILL.md`, `commands/urban/`, and `skills/` to reuse the coaching flow in LLM tools.

### 3. Quick Start

1. Download and unzip the release package.
2. Read `urban-prototyping-coach/student-guide.md` first.
3. In ChatGPT, Claude, Claude Code, or another LLM tool, provide `SKILL.md` plus the relevant `commands/urban/*.md` file.
4. Pick one command from the table below and add your current idea or project notes.
5. Treat the response as a draft for action, then check it against real user reactions or observation notes.

### 4. Command Flow

| Command | When to use it | Output |
| --- | --- | --- |
| `/urban:help` | You are unsure where to start | One recommended next command |
| `/urban:scope` | The problem is too broad | Learning question and first experiment direction |
| `/urban:service-loop` | The service flow is unclear | Input, processing, output, and next action |
| `/urban:prototype` | You need a small experiment artifact | Build prompt and observation points |
| `/urban:demo-review` | You need to review a demo | Demo checklist and fix priorities |
| `/urban:pitch` | You need to explain the work | One-page explanation and claim boundary |
| `/urban:spec` | You need a small build scope | Compact implementation spec |
| `/urban:plan` | You need a work sequence | Day-level build plan |
| `/urban:context-audit` | The AI lacks project context | Folder and document cleanup plan |

### 5. File Map

- `urban-prototyping-coach/student-guide.md`: main student guide.
- `urban-prototyping-coach/SKILL.md`: representative skill for LLM coaching.
- `urban-prototyping-coach/commands/urban/`: portable command prompts.
- `urban-prototyping-coach/skills/`: step-specific child skills.
- `urban-prototyping-coach/references/routing-contract.md`: command-to-skill contract.
- `urban-prototyping-coach/MANIFEST.md`: package inventory and verification log.
- `dist/`: release ZIP and checksum files.
- `verification/`: verification summary and visual evidence.

### 6. Verify the Package

```bash
cd dist
shasum -a 256 -c urban-prototyping-coach-20260526.zip.sha256
```

For maintainers, run these checks from the repository root:

```bash
skills-ref validate urban-prototyping-coach
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py urban-prototyping-coach
```

## Release Status

- current_release_date: `2026-05-26`
- package_root: `urban-prototyping-coach/`
- release_tag: `urban-prototyping-coach-20260526`
- package_zip: `dist/urban-prototyping-coach-20260526.zip`
- checksum: `dist/urban-prototyping-coach-20260526.zip.sha256`
