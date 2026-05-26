# Manifest

- build_date: 2026-05-26
- package_type: plain Markdown distribution
- publishable_sot_path: `dist/urban-prototyping-coach/`
- source_documents:
  - `ai-pretotyping-gemini-cli-student-guide-ko.md`
  - `How to build with LLM.md`
- companion_skill: `SKILL.md`
- owner: lecture-works prototyping course package
- license: internal course distribution; confirm before public redistribution
- dependencies: none
- backend_required: no
- build_required: no
- runtime_targets: ChatGPT, Claude, Claude Code, generic manual fallback

## Files

- `README.md`: 패키지 입구 문서
- `pretotyping-guide.md`: 프롬프트 예시를 포함한 초기 프리토타이핑 학생용 문서
- `student-guide.md`: 프로토타이핑과 설계 연결을 다루는 현재 학생용 기준 문서
- `SKILL.md`: `student-guide.md`에 맞춘 AI 코칭 스킬 파일
- `commands/urban/`: portable `/urban:*` command prompt 묶음
- `skills/urban-*/SKILL.md`: 분리된 단계별 하위 스킬 세트
- `references/routing-contract.md`: command와 skill 연결 계약
- `references/command-skill-concept-map.md`: owner skill, child skill, command surface 정렬 문서
- `domain-alignment-map.md`: 원문, 도메인 규칙, 문서별 역할을 짧게 정리한 메모
- `multi-skill-system.md`: 여러 보조 기준을 하나의 코칭 흐름으로 쓰는 방식을 설명한 문서
- `MANIFEST.md`: 이 배포 기록 문서

## Source Mapping

- `ai-pretotyping-gemini-cli-student-guide-ko.md` -> `pretotyping-guide.md`
- `How to build with LLM.md` -> `student-guide.md`

## Distribution Notes

- `pretotyping-guide.md`는 참고 문서로 보존하고, 현재 학생용 기준 문서는 `student-guide.md`로 둡니다.
- 프롬프트 예시는 학생용 Markdown 문서 안에만 둡니다.
- `SKILL.md`는 `student-guide.md`를 기준으로 삼고, 지속가능한 Urban테크 초점을 덧붙입니다.
- `commands/urban/`는 runtime 특정 문법이 아니라 plain Markdown prompt로 배포합니다.
- `skills/urban-*`는 root owner skill 아래에 붙는 child skill이며, command 이름과 routing contract를 단독으로 바꾸지 않습니다.
- `references/routing-contract.md`는 command spelling, primary child skill, input/output contract의 단일 기준입니다.
- `references/command-skill-concept-map.md`는 owner skill, child skill, command surface 연결을 한 번에 보여 주는 정렬 표면입니다.
- `domain-alignment-map.md`는 `generate-skill`, `vector-language-cognition`, `cogarch`의 기준이 이 패키지에 어떻게 들어왔는지 기록합니다.
- `multi-skill-system.md`는 여러 기준을 쓰더라도 학생에게는 하나의 코칭 흐름으로 보이게 하는 방식을 설명합니다.
- `README.md`는 한국어와 영어 사용 설명을 함께 제공하며, root README와 같은 명령 흐름을 가리킵니다.
- ChatGPT, Claude, Claude Code는 같은 `SKILL.md`를 읽어 사용합니다. 일반 채팅 도구는 필요한 섹션을 붙여 넣어 사용할 수 있습니다.
- 이 폴더는 그대로 배포할 수 있습니다.
- 호환성 상태는 `SKILL.md`에 `shared-core only / no-delta`로 기록했습니다.

## Verification

- source parity: `student-guide.md` matches `How to build with LLM.md`
- source parity: `pretotyping-guide.md` matches `ai-pretotyping-gemini-cli-student-guide-ko.md`
- skill validation: `skills-ref validate dist/urban-prototyping-coach/` passed
- plain Markdown check: no HTML wrapper tags detected in the distribution folder
- 2026-05-21 hardening verification: `skills-ref validate .` passed
- 2026-05-21 hardening verification: `quick_validate.py .` passed
- 2026-05-21 CAA generate-skill profile: ready, 120/120, runtime compatibility `shared-core only / no-delta`, no blocking findings
- 2026-05-21 three-layer audit: fixed/flexible/decisional signals present, smells 0
- 2026-05-21 멀티 스킬 구조 검증: `skills-ref validate .` 통과
- 2026-05-21 멀티 스킬 구조 검증: `quick_validate.py .` 통과
- 2026-05-21 multi-skill system verification: `skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators` returned ready, 120/120
- 2026-05-21 multi-skill system verification: `audit_three_layer_separation.py .` reported fixed/flexible/decisional signals present, smells 0
- 2026-05-22 표현 점검: `phrase_lint.py SKILL.md README.md multi-skill-system.md domain-alignment-map.md MANIFEST.md`에서 추가 경고 없이 마감
- 2026-05-22 hardening verification: `skills-ref validate .` passed
- 2026-05-22 hardening verification: `quick_validate.py .` passed
- 2026-05-22 hardening verification: `audit_three_layer_separation.py .` reported smells 0
- 2026-05-22 package completion: actual `commands/urban/` and `skills/urban-*` surfaces added, root guide path generalized from `.gemini/` to portable `commands/` + `skills/`
- 2026-05-22 child skill verification: each `skills/urban-*` folder passes `skills-ref validate` and `quick_validate.py`
- 2026-05-26 bilingual README verification: root README and package README include Korean/English usage sections and command names match `references/routing-contract.md`

## Validation Commands

Run from this folder:

```bash
skills-ref validate .
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py .
PYTHONPATH=/Volumes/Extend/labs/SkillAnalysis/src python3 -m skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators
find skills -mindepth 1 -maxdepth 1 -type d -exec sh -c 'skills-ref validate "$1" && python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py "$1"' sh {} \;
```

## Change History

- 2026-05-21: generate-skill / CAA hardening pass added portable metadata, source-of-truth contract, runtime compatibility closeout, legacy distillation owner split, conflict resolution, Fixed/Flexible/Decisional layering, self-application gates, and runnable validation commands. Pattern repetition count: N=1 for this package-local hardening pattern.
- 2026-05-21: generate-skill + vector-language-cognition + cogarch alignment pass specialized the companion skill for sustainable urban tech, added actor-first/evidence-boundary rules, and added `domain-alignment-map.md` for source and ownership traceability.
- 2026-05-21: 멀티 스킬 구조 정리로 `multi-skill-system.md`를 추가하고, 하나의 코칭 흐름 안에서 역할 분담이 보이게 정리했습니다.
- 2026-05-21: `ChatGPT / Claude / Claude Code` 호환 문구를 추가하면서도 `shared-core only / no-delta` 상태와 로컬 전용 어댑터 없음 원칙을 유지했습니다.
- 2026-05-22: 학생이 읽는 표면에서 내부 운영 용어 노출을 줄이고, 같은 구조를 더 자연스러운 한국어 설명으로 정리했습니다.
- 2026-05-22: `commands/urban/`, `skills/urban-*`, `references/routing-contract.md`를 추가해 문서에만 남아 있던 command/skill 구조를 실제 배포 파일로 복원했습니다.
- 2026-05-22: `references/command-skill-concept-map.md`를 추가해 owner skill, child skill, command surface 정렬 증거를 패키지 안에 남겼습니다.
- 2026-05-26: 루트 README와 패키지 README를 한국어/영어 병기 사용 설명서로 정리하고, 배포 ZIP과 checksum을 새 릴리즈 기준으로 갱신했습니다.
