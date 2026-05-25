# /urban:prototype

## Purpose

지금 질문에 맞는
가장 작은 실험물의 형식과 빌드 prompt를 만듭니다.

## Prompt Template

```text
/urban:prototype

학습 질문:

선택한 방식:

반드시 들어가야 할 입력 / 결과:

절대 넣지 않을 것:
```

## Expected Output

1. 오늘 만들 실험물 1개
2. 왜 이 형식이 가장 작은지
3. build prompt 초안
4. 관찰할 행동 2~3개
5. 실험 후 기록할 항목

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-prototype/SKILL.md`
- helper if needed: `../../skills/urban-evidence-boundary/SKILL.md`
