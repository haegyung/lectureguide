# Urban Command Skill Concept Map

이 문서는 `urban-prototyping-coach` 패키지의 owner skill, child skill, command surface가 어떻게 연결되는지 한눈에 보여 주는 정렬 표면입니다.

## Map

```mermaid
graph TD
  A["SKILL.md<br/>owner skill"] --> B["student-guide.md<br/>course source of truth"]
  A --> C["references/routing-contract.md<br/>canonical command names"]
  A --> D["commands/urban/*.md<br/>portable command prompts"]
  A --> E["skills/urban-*<br/>child skills"]

  C --> D
  C --> E

  D --> D1["/urban:help"]
  D --> D2["/urban:scope"]
  D --> D3["/urban:service-loop"]
  D --> D4["/urban:prototype"]
  D --> D5["/urban:demo-review"]
  D --> D6["/urban:pitch"]
  D --> D7["/urban:spec"]
  D --> D8["/urban:plan"]
  D --> D9["/urban:context-audit"]

  E --> E1["urban-scope"]
  E --> E2["urban-service-loop"]
  E --> E3["urban-prototype"]
  E --> E4["urban-demo-review"]
  E --> E5["urban-pitch"]
  E --> E6["urban-spec"]
  E --> E7["urban-plan"]
  E --> E8["urban-context-audit"]
  E --> E9["urban-evidence-boundary<br/>helper only"]

  D2 --> E1
  D3 --> E2
  D4 --> E3
  D5 --> E4
  D6 --> E5
  D7 --> E6
  D8 --> E7
  D9 --> E8
  E9 --> E4
  E9 --> E5
  E9 --> E6
```

## Reading Rules

- owner skill은 전체 수업 흐름과 출력 문법을 소유합니다.
- `student-guide.md`는 개념과 수업 흐름의 source of truth입니다.
- `references/routing-contract.md`는 command spelling과 child skill 연결의 source of truth입니다.
- `commands/urban/*.md`는 복사해 붙여 넣기 쉬운 portable command surface입니다.
- `skills/urban-*`는 각 단계의 좁은 작업 단위를 소유합니다.
- `urban-evidence-boundary`는 단독 단계가 아니라 다른 단계 뒤에 붙는 helper입니다.
