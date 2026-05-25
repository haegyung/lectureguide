# /urban:demo-review

## Purpose

시연 전에
무엇을 보여주고 무엇을 관찰할지 점검합니다.

## Prompt Template

```text
/urban:demo-review

현재 실험물:

누구에게 보여줄 것인가:

확인하고 싶은 행동:
```

## Expected Output

1. 시연 목표
2. 시연 흐름 3~5단계
3. 멈출 가능성이 높은 지점
4. 확인할 행동 증거
5. 다음 수정 1순위

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-demo-review/SKILL.md`
- helper if needed: `../../skills/urban-evidence-boundary/SKILL.md`
