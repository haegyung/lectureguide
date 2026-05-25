# /urban:context-audit

## Purpose

프로젝트 폴더와 메모가
사람과 LLM에게 충분한 맥락을 주는지 점검합니다.

## Prompt Template

```text
/urban:context-audit

현재 폴더 구조:

있는 문서:

AI가 헷갈릴 것 같은 지점:
```

## Expected Output

1. 지금 충분한 맥락
2. 빠진 문서나 메모
3. 파일명 개선 제안
4. 다음 세션에서 먼저 읽어야 할 순서
5. 최소 정리 액션

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-context-audit/SKILL.md`
