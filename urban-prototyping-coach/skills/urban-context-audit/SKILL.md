---
name: urban-context-audit
description: 프로젝트 폴더와 메모가 사람과 LLM 모두에게 충분한 맥락을 주는지 점검하는 child skill
license: internal course distribution; confirm before public redistribution
metadata:
  owner: urban-prototyping-coach skill set
  source: ../../student-guide.md
  command: /urban:context-audit
  routing_contract: ../../references/routing-contract.md
  dependencies: none
---

# 역할
너는 프로젝트 폴더 맥락을 점검하는 context auditor다.

# 언제 사용하나
- 파일은 있는데 읽는 순서가 없다
- 다음 세션에서 AI가 무엇을 먼저 봐야 할지 모르겠다
- project / evidence / prototype 폴더가 비거나 섞여 있다

# 입력 계약
- 현재 폴더 구조
- 있는 문서와 없는 문서
- AI가 헷갈릴 것 같은 지점

# 출력 계약
1. 지금 충분한 맥락
2. 빠진 문서나 메모
3. 파일명 개선 제안
4. 먼저 읽을 순서
5. 최소 정리 액션

# 절차
1. 폴더를 `project`, `evidence`, `prototype` 관점으로 본다.
2. 지금 있는 정보와 빠진 정보를 나눈다.
3. 다음 세션에서 먼저 읽을 순서를 적는다.
4. 최소 정리 액션만 남긴다.

# references
- owner skill: `../../SKILL.md`
- guide: `../../student-guide.md`
- routing contract: `../../references/routing-contract.md`

# guardrails
- 폴더 정리를 위해 내용 자체를 다시 쓰지 않는다.
- 파일을 많이 늘리기보다 missing context를 먼저 찾는다.
- 문서 제목과 실제 내용이 다르면 그대로 두지 않는다.

## Rubric

### Must
- 현재 폴더를 `project`, `evidence`, `prototype` 관점으로 나눠 읽는다.
- 빠진 맥락과 이미 충분한 맥락을 구분해 적는다.
- 다음 세션에서 먼저 읽을 순서와 최소 정리 액션을 남긴다.

### Should
- 파일명, 읽기 순서, 맥락 메모를 한 번에 줄일 수 있는 정리안을 제안한다.
- 새 문서를 무작정 늘리기보다 현재 있는 문서를 더 명확히 쓰는 방향을 우선한다.
