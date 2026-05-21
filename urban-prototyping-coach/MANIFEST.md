# Manifest

- build_date: 2026-05-21
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
- `domain-alignment-map.md`는 `generate-skill`, `vector-language-cognition`, `cogarch`의 기준이 이 패키지에 어떻게 들어왔는지 기록합니다.
- `multi-skill-system.md`는 여러 기준을 쓰더라도 학생에게는 하나의 코칭 흐름으로 보이게 하는 방식을 설명합니다.
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
- 2026-05-21 multi-skill system verification: `skills-ref validate .` passed after system-surface additions
- 2026-05-21 multi-skill system verification: `quick_validate.py .` passed after system-surface additions
- 2026-05-21 multi-skill system verification: `skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators` returned ready, 120/120
- 2026-05-21 multi-skill system verification: `audit_three_layer_separation.py .` reported fixed/flexible/decisional signals present, smells 0
- 2026-05-21 Korean surface verification: `phrase_lint.py SKILL.md README.md multi-skill-system.md domain-alignment-map.md` returned no findings
- 2026-05-21 Korean surface verification: `skills-ref validate urban-prototyping-coach` passed
- 2026-05-21 Korean surface verification: `quick_validate.py urban-prototyping-coach` passed
- 2026-05-21 Korean surface verification: `audit_three_layer_separation.py urban-prototyping-coach` reported smells 0
- 2026-05-21 Korean surface CAA profile: ready, 120/120, no blocking findings

## Validation Commands

Run from this folder:

```bash
skills-ref validate .
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py .
PYTHONPATH=/Volumes/Extend/labs/SkillAnalysis/src python3 -m skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators
```

## Change History

- 2026-05-21: generate-skill / CAA 정합성 보강으로 배포 메타데이터, 기준 문서 고정, 호환성 상태, 예전 문서 처리 방식, 충돌 우선순위, 3층 분류, 자체 점검, 검증 명령을 추가했습니다. 이 패키지 안에서 같은 보강 패턴은 N=1입니다.
- 2026-05-21: generate-skill + vector-language-cognition + cogarch 정렬로 지속가능한 Urban테크 초점, 행위자 우선 규칙, 증거와 주장 범위 규칙을 추가하고 `domain-alignment-map.md`를 만들었습니다.
- 2026-05-21: 여러 기준을 하나의 코칭 흐름으로 쓰기 위해 `multi-skill-system.md`를 추가했습니다.
- 2026-05-21: `ChatGPT / Claude / Claude Code` 호환 문구를 추가하고, 호환성 상태는 `shared-core only / no-delta`로 유지했습니다.
- 2026-05-21: 한국어 표면 정리로 사람이 읽는 설명을 내부 태그보다 앞에 두었습니다. 검증과 분석에 필요한 태그만 괄호나 기록 항목으로 남겼습니다.
