# /urban:scope

## Purpose

막연한 Urban테크 아이디어를
한 명의 행위자, 한 상황, 한 장소, 한 마찰, 한 학습 질문으로 줄입니다.

## Prompt Template

```text
/urban:scope

현재 아이디어:

조건:
- 너무 큰 플랫폼으로 키우지 말 것
- 하루 안에 검증 가능한 작은 실험으로 줄일 것
- 지속가능성 또는 공공가치 가설은 구체 효과로 적을 것
```

## Expected Output

1. 아이디어 재정의 1문장
2. 첫 행위자와 상황
3. 장소 / 서비스 접점
4. 현재 우회 방식
5. 학습 질문
6. 첫 프로토타이핑 방식 추천
7. 볼 증거 2~3개

## Routing

- owner: `../../SKILL.md`
- child skill: `../../skills/urban-scope/SKILL.md`
- helper if needed: `../../skills/urban-evidence-boundary/SKILL.md`
