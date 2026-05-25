# /urban:service-loop

## Purpose

입력, 처리, 결과, 다음 행동의 흐름으로
서비스처럼 작동하는지 점검합니다.

## Prompt Template

```text
/urban:service-loop

아이디어 또는 현재 실험:

이미 정한 행위자 / 상황 / 장소:

보고 싶은 행동:
```

## Expected Output

1. 서비스 루프 4단계
2. 각 단계의 사용자 행동
3. 가장 막히기 쉬운 지점
4. 사람이 수동으로 대신해도 되는 부분
5. 지금 맞는 실험 방식

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-service-loop/SKILL.md`
