# /urban:help

## Purpose

현재 아이디어와 진행 상태를 보고
지금 써야 할 `/urban:*` command를 하나 추천합니다.

## Use This When

- 어디서부터 시작해야 할지 모르겠을 때
- `scope` 다음에 무엇을 해야 할지 헷갈릴 때
- 지금이 `prototype` 단계인지 `plan` 단계인지 모를 때

## Prompt Template

```text
/urban:help

현재 아이디어:

지금까지 한 것:

막힌 지점:
```

## Expected Output

1. 현재 단계 진단 1문장
2. 지금 써야 할 command 1개
3. 그 command를 써야 하는 이유 2~3줄
4. 바로 붙여 넣을 다음 prompt 초안

## Routing

- owner: `../../SKILL.md`
- routing contract: `../../references/routing-contract.md`
