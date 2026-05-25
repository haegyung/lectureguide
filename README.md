# Lecture Guide

수업 배포용 `urban-prototyping-coach` Markdown/Skill 패키지 저장소입니다.

## Current Release

- release_date: 2026-05-25
- package_root: `urban-prototyping-coach/`
- zip: `dist/urban-prototyping-coach-20260525.zip`
- checksum: `dist/urban-prototyping-coach-20260525.zip.sha256`

## Contents

- `urban-prototyping-coach/`: 검증 가능한 스킬 패키지 원본입니다.
- `urban-prototyping-coach/commands/urban/`: portable `/urban:*` command prompt 묶음입니다.
- `urban-prototyping-coach/skills/`: 단계별 하위 스킬 세트입니다.
- `dist/urban-prototyping-coach-20260525.zip`: 학생 또는 운영자에게 전달할 ZIP 배포본입니다.
- `dist/urban-prototyping-coach-20260525.zip.sha256`: ZIP 무결성 확인용 SHA256 체크섬입니다.
- `verification/`: 패키지 검증 요약과 반응형 화면 증거입니다.

## Quick Check

```bash
skills-ref validate urban-prototyping-coach
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py urban-prototyping-coach
cd dist && shasum -a 256 -c urban-prototyping-coach-20260525.zip.sha256
```

## Distribution

현재 배포 기준은 `urban-prototyping-coach/` 폴더와 `dist/` ZIP이 같은 내용을 가리키는 것입니다. ZIP은 macOS 메타데이터를 제외하고 생성했습니다.
