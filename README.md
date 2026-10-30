# 작업 환경 설정 모음

Claude Code 작업 규칙, 검증 리포트 스킬, MCP 설정 예시를 모은 저장소입니다. 완성된 앱 코드는 들어 있지 않습니다.

## 파일 구성

| 파일 | 역할 |
|---|---|
| `CLAUDE.md` | 작업 규칙 |
| `WORKLOG.md` | 기획, 제작, 검증, 실행 기록 양식 |
| `.claude/skills/verify-report/SKILL.md` | 검증 리포트 스킬 |
| `.mcp.json` | MCP 설정 (macOS, Linux, 그리고 그냥 `npx`가 실행되는 환경) |
| `mcp-windows.json` | Windows에서 `npx`를 바로 실행하지 못할 때 쓰는 MCP 설정 |

## 사용 방법

1. 이 저장소의 파일을 프로젝트 폴더 맨 위에 복사합니다.
2. MCP 설정 JSON을 작업 환경의 가져오기 칸에 넣거나, `.mcp.json`을 프로젝트 폴더 맨 위에 둡니다.
3. Claude Code를 다시 시작하고 MCP 서버 사용을 승인합니다.
4. 아래 문장을 입력해 연결을 확인합니다.

```text
CLAUDE.md의 환경 점검을 진행해 줘. Playwright MCP로 about:blank를 열어 브라우저가 실행되는지도 확인해 줘.
```

## 브라우저가 없다는 오류가 나올 때

```bash
npx playwright install chromium
```

Linux에서 브라우저 샌드박스 오류가 나오면 `.mcp.json`의 playwright `args`에 `"--no-sandbox"`를 추가합니다.
