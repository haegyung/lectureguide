# How to build with LLM Markdown Kit

이 폴더는 수업 배포용 일반 Markdown 묶음입니다.
현재 기준은 **지속가능한 Urban테크 문제를 작은 프로토타이핑 실험으로 다루는 동반 패키지**입니다.

## 구성

- `student-guide.md`: 우리가 합의한 기준을 반영한 통합 학생용 문서입니다. 프로토타이핑을 상위 개념으로 두고, LLM 활용과 증거 수집, 설계 연결까지 한 흐름으로 설명합니다.
- `pretotyping-guide.md`: 초기 원문을 참고용으로 보존한 문서입니다. 용어 비교나 수업 맥락 확인이 필요할 때 참고합니다.
- `SKILL.md`: `student-guide.md`를 주 기준으로 삼고, 지속가능한 Urban테크 수업에 맞게 행위자와 증거를 보는 방식을 덧댄 동반 스킬 파일입니다.
- `domain-alignment-map.md`: 이 스킬이 어떤 기준 문서와 어떤 도메인 규칙을 받아들였는지 짧게 정리한 메모입니다.
- `multi-skill-system.md`: 이 패키지 안에서 여러 보조 기준이 어떻게 함께 쓰이는지 정리한 운영 문서입니다.
- `MANIFEST.md`: 배포 파일 목록과 검증 기록입니다.

## 사용 순서

1. 먼저 `student-guide.md`를 읽고 아이디어를 질문, 프로토타입, 증거, 설계의 흐름으로 정리합니다.
2. `SKILL.md`를 읽고 `행위자 + 상황 + 장소 + 마찰`과 `evidence_state + claim_boundary` 기준을 현재 아이디어에 붙입니다.
3. `multi-skill-system.md`를 읽고 각 보조 기준이 언제 들어오는지 확인합니다.
4. 필요할 때 `domain-alignment-map.md`를 확인해 왜 이런 구조를 쓰는지 빠르게 복기합니다.
5. 문서 안의 프롬프트 예시를 자기 아이디어에 맞게 바꿔 씁니다.
6. 필요할 때 `pretotyping-guide.md`를 참고해 원문 표현이나 초기 수업 맥락을 비교합니다.
7. 스킬 파일을 지원하지 않는 도구에서는 `SKILL.md`의 기준과 출력 형식을 작업 기준으로 붙여 넣어도 됩니다.

## 어떤 도구에서 쓰나

- `ChatGPT`: `SKILL.md`와 `student-guide.md`를 함께 읽히고 현재 아이디어를 붙여 요청합니다.
- `Claude`: `SKILL.md`를 기준으로 코칭 규칙을 따르게 하고, 필요할 때 `student-guide.md` 예시를 같이 읽힙니다.
- `Claude Code`: skills-compatible 경로에 이 폴더를 두거나 현재 작업 폴더에서 `SKILL.md`를 직접 읽게 합니다.
- 일반 LLM 채팅: 스킬 자동 활성화가 없으면 `SKILL.md`의 `Working Position`, `Evidence and Claim Boundary`, `Default Workflow`, `Output Format`만 복사해도 됩니다.

## 배포 기준

- 별도 웹 서버나 빌드 과정이 필요 없습니다.
- 학생에게 전달할 최소 묶음은 `student-guide.md`, `SKILL.md`입니다.
- 지속가능한 Urban테크 수업 맥락을 함께 전달하려면 `domain-alignment-map.md`까지 같이 두는 편이 좋습니다.
- 멀티 스킬 운영까지 전달하려면 `multi-skill-system.md`를 함께 둡니다.
- `pretotyping-guide.md`는 역사적 참고 문서이며, 현재 실행 기준은 아닙니다.
- 프롬프트 예시는 `SKILL.md`에 중복하지 않고 학생용 문서 안에만 둡니다.
