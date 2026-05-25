# /urban:plan

## Purpose

작은 구현 범위를
하루 단위의 빌드 순서와 검증 순서로 나눕니다.

## Prompt Template

```text
/urban:plan

현재 spec:

사용 가능한 시간:

먼저 검증해야 할 것:
```

## Expected Output

1. build order
2. 각 단계 산출물
3. 각 단계 검증 포인트
4. 오늘 안 해도 되는 것
5. 막히면 줄일 축

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-plan/SKILL.md`
