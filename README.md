# agentkit-template

새 프로젝트용 AI 세팅 기본틀. 언어/프레임워크 상관없이 쓰고, 스택별 스킬·플러그인은 `/stack-setup` 이 **그 주 GitHub 트렌드 기준**으로 붙여줌.

추천 엔진: [agentkit](https://github.com/alscjf1329/agentkit)

## 시작하기

```bash
# 1. 템플릿으로 새 레포 생성 (또는 GitHub 에서 "Use this template")
gh repo create my-app --template alscjf1329/agentkit-template --private --clone
cd my-app

# 2. Claude Code 실행 → 폴더 신뢰(trust) 수락
claude
```

```
# 3. 스택 정하고 추천·설치
/stack-setup
```

신뢰 수락하면 `.claude/settings.json` 에 등록된 `stack-setup` 플러그인이 자동 설치됨.
안 뜨면: `/plugin marketplace add alscjf1329/agentkit` → `/plugin install stack-setup@agentkit`

## 들어있는 것

| 파일 | 역할 |
|---|---|
| `.claude/settings.json` | 마켓플레이스 등록 + stack-setup 활성화, `.env` 읽기 차단 |
| `.claude/stack-setup.lock.json` | 설치한 스킬/플러그인 기록 (롤백·재설치용) |
| `AGENTS.md` | 모든 AI 에이전트 공통 규칙 (단일 소스) |
| `CLAUDE.md` | `@AGENTS.md` import 한 줄 |
| `.mcp.json.example` | MCP 설정 예시 (키는 `.env` 참조) |
| `.env.example` | 환경변수 예시 |
| `.gitignore` | 시크릿·로컬 설정 제외 |

## 템플릿 쓴 뒤 할 일

- [ ] `AGENTS.md` 의 `<...>` 채우기 (프로젝트명, 명령어)
- [ ] `/stack-setup` 으로 스킬·플러그인 설치
- [ ] MCP 쓰면 `.mcp.json.example` → `.mcp.json` 복사 후 `.env` 에 키
- [ ] 이 README 를 프로젝트 README 로 교체

## 원칙

- 템플릿엔 **스택별 내용 안 넣음** → 스택 맞춤은 `/stack-setup` 담당
- 카테고리당 스킬 1개 (중복·컨텍스트 낭비 방지)
- 서드파티 훅/스크립트는 설치 전 검토
