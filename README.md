# Codex 작업 환경 설정 모음

Codex 작업 규칙, 검증 리포트 스킬, MCP 설정을 모은 저장소입니다. 완성된 앱 코드는 들어 있지 않습니다.

## 사용 방법

이 저장소를 작업 폴더 밖에 내려받고, 필요한 파일만 프로젝트로 가져옵니다. 기존 파일은 덮어쓰지 않습니다.

```bash
git clone https://github.com/sangmin2391-boop/test-readiness.git /tmp/kit
```

```bash
cp -rn /tmp/kit/AGENTS.md /tmp/kit/.agents .
```

```bash
cat /tmp/kit/mcp-servers.json
```

MCP 설정 JSON은 작업 환경의 MCP 설정 화면에 넣습니다. 그다음 `codex`를 실행합니다.

## 파일 구성

| 파일 | 역할 |
|---|---|
| `AGENTS.md` | 작업 규칙 |
| `.agents/skills/verify-report/SKILL.md` | 검증 리포트 스킬 |
| `mcp-servers.json` | Linux 환경의 MCP 설정 |
| `mcp-windows.json` | Windows 환경의 MCP 설정 |
| `.codex/config.toml` | 직접 설정할 수 있는 환경에서 쓰는 Codex MCP 설정 |
| `WORKLOG.md` | 작업 기록 양식 |
