# AGENTS.md

모든 AI 에이전트(Claude Code, Codex, Cursor 등) 공통 규칙. 단일 소스 — CLAUDE.md 는 이 파일을 import 만 함.

## 프로젝트
- 이름: <PROJECT_NAME>
- 목적: <한 줄 설명>
- 스택: <`/stack-setup` 실행 후 채우기>

## 명령어
<!-- 스택 정해지면 채우기. 에이전트가 이 명령으로 검증함 -->
- 설치: `<install>`
- 실행: `<dev>`
- 테스트: `<test>`
- 린트/포맷: `<lint>`
- 빌드: `<build>`

## 작업 규칙
- 변경 후 테스트·린트 통과 확인하고 끝낼 것
- 요청 범위 밖 리팩터링 금지
- 새 의존성 추가 전 이유 설명
- 커밋 메시지: Conventional Commits (`feat:`, `fix:`, `chore:` ...)

## 보안
- `.env`, 키, 토큰 절대 커밋·출력 금지. 예시는 `.env.example` 에만
- MCP 키는 `.env` 참조로만 사용

## 디렉토리 구조
<!-- 코드 생기면 주요 폴더만 한 줄씩 -->
