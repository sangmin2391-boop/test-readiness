# Codex 작업 환경 설정 모음

Codex 작업 규칙, 검증 리포트 스킬, MCP 설정을 모은 저장소입니다. 완성된 앱 코드는 들어 있지 않습니다.

## 파일 구성

| 파일 | 역할 |
|---|---|
| `AGENTS.md` | 작업 규칙 (Codex가 자동으로 읽음) |
| `WORKLOG.md` | 기획, 제작, 검증, 실행 기록 양식 |
| `.agents/skills/verify-report/SKILL.md` | 검증 리포트 스킬 (`$verify-report`로 호출) |
| `.codex/config.toml` | Codex 프로젝트 MCP 설정 (신뢰한 프로젝트에서만 적용) |
| `mcp-servers.json` | JSON 가져오기 칸이 있는 환경에 넣는 MCP 설정 |
| `mcp-windows.json` | Windows에서 `npx`를 바로 실행하지 못할 때 쓰는 JSON 설정 |

## 사용 방법

1. 이 저장소의 파일을 프로젝트 폴더 맨 위에 복사합니다.
2. 작업 환경에 JSON 가져오기 칸이 있으면 `mcp-servers.json`의 내용을 넣습니다. 칸이 없으면 프로젝트를 신뢰해 `.codex/config.toml`이 적용되게 합니다.
3. Codex를 다시 시작하고 입력창에 `/mcp`를 입력해 연결을 확인합니다.
4. 아래 문장을 입력해 규칙, 스킬, 브라우저를 확인합니다.

```text
AGENTS.md의 규칙을 요약하고 환경 점검을 진행해 줘. $verify-report 스킬이 보이는지 확인하고, Playwright MCP로 about:blank를 열어 브라우저가 실행되는지도 확인해 줘.
```

## 명령어로 MCP를 추가할 때

```bash
codex mcp add playwright -- npx -y @playwright/mcp@0.0.83 --headless --isolated
```

```bash
codex mcp add context7 -- npx -y @upstash/context7-mcp@4.4.4
```

## 브라우저가 없다는 오류가 나올 때

```bash
npx playwright install chromium
```

Linux에서 브라우저 샌드박스 오류가 나오면 playwright 인자에 `--no-sandbox`를 추가합니다.
