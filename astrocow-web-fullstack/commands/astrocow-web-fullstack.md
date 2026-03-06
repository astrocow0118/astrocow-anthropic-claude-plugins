---
name: astrocow-web-fullstack
description: PO 에이전트를 시작점으로 전체 개발 워크플로우를 실행합니다.
---

`/astrocow-web-fullstack` 커맨드가 실행되었습니다.

po 에이전트로서 다음을 수행하세요:

1. 프로젝트 루트의 CLAUDE.md를 읽어 기술 스택을 확인합니다.
2. 기술 스택 확인 또는 질문 후 사용자에게 개발하려는 기능이나 요구사항을 질문합니다.
3. 요구사항을 프론트엔드 / 백엔드 / UI / 인프라 작업으로 분류합니다.
4. TodoWrite로 전체 작업 계획과 에이전트 간 의존성을 작성합니다.
5. architect 에이전트에게 시스템 설계서 작성을 요청합니다. (산출물은 docs/architecture.md에 기록하도록 지시)
6. 설계서 완료 후 즉시 1단계 병렬(ui-designer + backend)을 시작하고, 완료되면 2단계 병렬(frontend + infra)을 진행합니다.
7. 에이전트 간 정보 공유는 **파일 경로 전달**로 합니다. 에이전트 결과 텍스트를 다른 에이전트에게 복사하지 않습니다.
   - architect 산출물: docs/architecture.md
   - ui-designer 산출물: docs/ui-design.md
   - backend 산출물: docs/api-spec.md
   - infra 산출물: docs/infra-guide.md
8. 에이전트에게 작업 배정 시 반드시 전달: "PO에게 반환하는 보고는 간결한 요약만. 코드/설계서/명세 본문은 포함하지 말고 파일에만 기록."
9. 최종 결과를 사용자에게 요약 보고합니다.