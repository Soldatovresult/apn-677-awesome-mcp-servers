# MCP (Model Context Protocol) Servers - 종합 가이드

> MCP는 Anthropic이 2024년 11월에 발표한 오픈 프로토콜로, AI 모델이 외부 도구/데이터와 표준화된 방식으로 연결됩니다.
> 2026년 현재 10,000+ 공개 MCP 서버가 활성화되어 있으며, OpenAI, Google, Microsoft 등이 채택했습니다.
> Anthropic은 MCP를 Linux Foundation 산하 Agentic AI Foundation(AAIF)에 기부했습니다.

---

## 1. 개발 (Development)

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **GitHub** (Official) | [github.com/github/github-mcp-server](https://github.com/github/github-mcp-server) | GitHub 공식 MCP 서버 - PR, 코드 리뷰, 커밋, 리포 관리 | `npx -y @modelcontextprotocol/server-github` |
| **Git** | [github.com/modelcontextprotocol/servers/src/git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) | Git 리포지토리 읽기, 검색, 조작 도구 | `uvx mcp-server-git` |
| **Filesystem** | [github.com/modelcontextprotocol/servers/src/filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) | 안전한 파일 시스템 접근 및 조작 (접근 제어 설정 가능) | `npx -y @modelcontextprotocol/server-filesystem /path/to/dir` |
| **Playwright** (Microsoft) | [github.com/microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) | Microsoft 공식 브라우저 자동화 및 E2E 테스트 서버 | `npx -y @playwright/mcp@latest` |
| **Docker** | [github.com/docker/mcp-server](https://github.com/docker/mcp-server) | Docker 컨테이너 관리 및 Dockerfile 생성 | `npx -y @docker/mcp-server` |
| **Sentry** | [github.com/getsentry/sentry-mcp](https://github.com/getsentry/sentry-mcp) | 에러 트래킹 및 디버깅 통합 (공식 Sentry 서버) | `npx -y @sentry/mcp-server` |
| **Context7** (Upstash) | [github.com/upstash/context7](https://github.com/upstash/context7) | 최신 버전별 라이브러리 문서를 프롬프트에 직접 제공 | `npx -y @upstash/context7-mcp` |
| **Grafana** | [github.com/grafana/mcp-grafana](https://github.com/grafana/mcp-grafana) | Grafana 대시보드 검색 및 데이터소스 쿼리 | `uvx mcp-grafana` |

---

## 2. DB (Database)

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **PostgreSQL** | [github.com/modelcontextprotocol/servers/src/postgres](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) | PostgreSQL 데이터베이스 읽기 전용 접근 및 쿼리 실행 | `npx -y @modelcontextprotocol/server-postgres postgresql://localhost/mydb` |
| **SQLite** | [github.com/modelcontextprotocol/servers/src/sqlite](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) | SQLite 데이터베이스 조작 및 비즈니스 인사이트 분석 | `uvx mcp-server-sqlite --db-path /path/to/db.sqlite` |
| **MongoDB** (Official) | [github.com/mongodb-js/mongodb-mcp-server](https://github.com/mongodb-js/mongodb-mcp-server) | MongoDB 및 Atlas 클러스터 공식 MCP 서버 | `npx -y mongodb-mcp-server@latest` |
| **MySQL** | [github.com/designcomputer/mysql_mcp_server](https://github.com/designcomputer/mysql_mcp_server) | MySQL 데이터베이스 보안 연결 및 쿼리 실행 | `uvx mysql-mcp-server` |
| **Redis** (Official) | [github.com/redis/mcp-redis](https://github.com/redis/mcp-redis) | Redis 공식 MCP 서버 - 자연어 데이터 관리 및 검색 | `uvx --from redis-mcp-server@latest redis-mcp-server` |
| **Neo4j** | [github.com/neo4j-contrib/mcp-neo4j](https://github.com/neo4j-contrib/mcp-neo4j) | Neo4j 그래프 DB - 스키마 조회 및 Cypher 쿼리 지원 | `npx -y @neo4j/mcp-neo4j` |
| **Neon** (Serverless Postgres) | [github.com/neondatabase/mcp-server-neon](https://github.com/neondatabase/mcp-server-neon) | Neon 서버리스 Postgres 관리 및 쿼리 | `npx -y @neondatabase/mcp-server-neon` |
| **ClickHouse** | [github.com/ClickHouse/mcp-clickhouse](https://github.com/ClickHouse/mcp-clickhouse) | ClickHouse 자연어 쿼리 및 자동화된 DB 관리 | `uvx mcp-clickhouse` |
| **Qdrant** | [github.com/qdrant/mcp-server-qdrant](https://github.com/qdrant/mcp-server-qdrant) | Qdrant 벡터 검색 엔진 기반 시맨틱 메모리 레이어 | `uvx mcp-server-qdrant` |

---

## 3. 커뮤니케이션 (Communication)

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **Slack** | [github.com/modelcontextprotocol/servers-archived/src/slack](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/slack) | Slack 채널 읽기, 스레드 요약, 메시지 전송 | `npx -y @modelcontextprotocol/server-slack` |
| **Discord** | [github.com/elyxlz/discord-mcp](https://github.com/elyxlz/discord-mcp) | Discord 서버 메시지 읽기 및 상호작용 자동화 | `uvx --from git+https://github.com/elyxlz/discord-mcp.git discord-mcp` |
| **Gmail / Google Workspace** | [github.com/taylorwilsdon/google_workspace_mcp](https://github.com/taylorwilsdon/google_workspace_mcp) | Gmail, Calendar, Docs, Sheets, Drive 통합 관리 | `uvx google-workspace-mcp` |
| **Notion** (Official) | [github.com/makenotion/notion-mcp-server](https://github.com/makenotion/notion-mcp-server) | Notion 공식 MCP 서버 - 페이지/DB 검색 및 편집 | `npx -y @notionhq/notion-mcp-server` |
| **Linear** | [linear.app/docs/mcp](https://linear.app/docs/mcp) | Linear 이슈, 스프린트, 프로젝트 관리 | `npx -y mcp-remote https://mcp.linear.app/mcp` |
| **Atlassian (Jira/Confluence)** | [github.com/sooperset/mcp-atlassian](https://github.com/sooperset/mcp-atlassian) | Jira 이슈 및 Confluence 문서 통합 관리 | `uvx mcp-atlassian` |
| **Mailgun** | [github.com/mailgun/mailgun-mcp-server](https://github.com/mailgun/mailgun-mcp-server) | Mailgun API를 통한 이메일 전송 및 관리 | `npx -y @mailgun/mcp-server` |

---

## 4. 자동화 (Automation)

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **Playwright** (Microsoft) | [github.com/microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) | 크로스 브라우저 자동화 및 웹 스크래핑 (접근성 기반) | `npx -y @playwright/mcp@latest` |
| **Puppeteer** | [github.com/modelcontextprotocol/servers-archived/src/puppeteer](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/puppeteer) | Puppeteer 기반 브라우저 자동화 및 스크린샷 | `npx -y @modelcontextprotocol/server-puppeteer` |
| **Firecrawl** | [github.com/firecrawl/firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) | 웹 크롤링, 스크래핑 및 데이터 추출 | `npx -y firecrawl-mcp` |
| **Browserbase** | [github.com/browserbase/mcp-server-browserbase](https://github.com/browserbase/mcp-server-browserbase) | 클라우드 기반 브라우저 자동화 인프라 | `npx -y @browserbasehq/mcp-server-browserbase` |
| **Fetch** | [github.com/modelcontextprotocol/servers/src/fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) | 웹 콘텐츠 가져오기 및 LLM용 변환 | `uvx mcp-server-fetch` |
| **E2B** | [github.com/e2b-dev/mcp-server](https://github.com/e2b-dev/mcp-server) | 보안 클라우드 샌드박스에서 코드 실행 | `npx -y @e2b/mcp-server` |
| **Tavily** | [github.com/tavily-ai/tavily-mcp-server](https://github.com/tavily-ai/tavily-mcp-server) | AI 에이전트 전용 검색 엔진 및 데이터 추출 | `npx -y mcp-server-tavily` |
| **Brave Search** | [github.com/nichochar/brave-search-mcp](https://github.com/nichochar/brave-search-mcp) | Brave 검색 API를 통한 실시간 웹 검색 | `npx -y @nichochar/brave-search-mcp` |

---

## 5. AI

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **Memory** | [github.com/modelcontextprotocol/servers/src/memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) | 지식 그래프 기반 영구 메모리 시스템 | `npx -y @modelcontextprotocol/server-memory` |
| **Sequential Thinking** | [github.com/modelcontextprotocol/servers/src/sequentialthinking](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) | 분기/수정/검증을 통한 구조적 사고 프로세스 | `npx -y @modelcontextprotocol/server-sequential-thinking` |
| **Qdrant** | [github.com/qdrant/mcp-server-qdrant](https://github.com/qdrant/mcp-server-qdrant) | Qdrant 벡터 DB 위에 시맨틱 메모리 레이어 구축 | `uvx mcp-server-qdrant` |
| **Chroma** | [github.com/chroma-core/chroma-mcp](https://github.com/chroma-core/chroma-mcp) | 시맨틱 문서 관리 및 벡터 검색 (임베딩 기반) | `uvx chroma-mcp` |
| **ElevenLabs** | [github.com/elevenlabs/elevenlabs-mcp](https://github.com/elevenlabs/elevenlabs-mcp) | 텍스트-투-스피치(TTS) 및 음성 생성 AI | `npx -y @elevenlabs/mcp-server` |
| **Perplexity** | [github.com/ppl-ai/modelcontextprotocol](https://github.com/ppl-ai/modelcontextprotocol) | Perplexity Sonar API 연결 - AI 검색 및 답변 | `npx -y @anthropic/mcp-server-perplexity` |
| **Knowledge Graph** | [github.com/shaneholloman/mcp-knowledge-graph](https://github.com/shaneholloman/mcp-knowledge-graph) | 로컬 지식 그래프를 통한 Claude 영구 메모리 | `npx -y mcp-knowledge-graph` |
| **OpenAI** | [github.com/openai/mcp-server](https://github.com/openai/mcp-server) | OpenAI 모델 통합 및 API 연동 | `npx -y @openai/mcp-server` |

---

## 6. 비즈니스 (Business)

| 이름 | 링크 | 설명 | 설치 명령어 |
|------|------|------|-------------|
| **Google Drive** | [github.com/isaacphi/mcp-gdrive](https://github.com/isaacphi/mcp-gdrive) | Google Drive 파일 읽기 및 Google Sheets 편집 | `npx -y @isaacphi/mcp-gdrive` |
| **Google Sheets** | [github.com/xing5/mcp-google-sheets](https://github.com/xing5/mcp-google-sheets) | Google Sheets 생성 및 수정 통합 | `uvx mcp-google-sheets@latest` |
| **Notion** (Official) | [github.com/makenotion/notion-mcp-server](https://github.com/makenotion/notion-mcp-server) | Notion 공식 - 데이터베이스, 페이지 시맨틱 검색 | `npx -y @notionhq/notion-mcp-server` |
| **Agent Payment Node** | [github.com/nuanu-ai/agent-payment-node](https://github.com/nuanu-ai/agent-payment-node) | x402 제안 확인, 한도 내 결제 준비, 상태 및 영수증 조회용 로컬 stdio 도구; Apple Silicon macOS와 Node 24 전용 | `brew install nuanu-ai/tap/apn` |
| **Stripe** (Official) | [github.com/stripe/ai](https://github.com/stripe/ai) | Stripe 공식 결제 API - 고객, 상품, 결제 관리 | `npx -y @stripe/mcp --tools=all --api-key=SK_KEY` |
| **Salesforce** (Official) | [github.com/salesforcecli/mcp](https://github.com/salesforcecli/mcp) | Salesforce CRM 공식 - SOQL 쿼리, 메타데이터 관리 | `npx -y @salesforce/mcp` |
| **Linear** | [linear.app/docs/mcp](https://linear.app/docs/mcp) | 프로젝트/이슈 관리 - 스타트업에 최적화 | `npx -y mcp-remote https://mcp.linear.app/mcp` |
| **HubSpot** | [github.com/hubspot/hubspot-mcp-server](https://github.com/hubspot/hubspot-mcp-server) | HubSpot CRM 연동 - 연락처, 회사, 딜 관리 | `npx -y @hubspot/mcp-server` |
| **Datadog** | [github.com/DataDog/datadog-mcp-server](https://github.com/DataDog/datadog-mcp-server) | 애플리케이션 모니터링 및 인프라 관측 | `npx -y @datadog/mcp-server` |

---

## 빠른 시작 가이드

### Claude Desktop 설정 (claude_desktop_config.json)

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/Users/username/projects"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<YOUR_TOKEN>"
      }
    },
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"]
    },
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres", "postgresql://localhost/mydb"]
    },
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]
    }
  }
}
```

### Claude Code 설정

```bash
# 서버 추가 (scope: user = 전역, project = 프로젝트별)
claude mcp add --scope user memory -- npx -y @modelcontextprotocol/server-memory
claude mcp add --scope user github -- npx -y @modelcontextprotocol/server-github
claude mcp add --scope user filesystem -- npx -y @modelcontextprotocol/server-filesystem /path/to/dir
claude mcp add --scope user context7 -- npx -y @upstash/context7-mcp
claude mcp add --scope user playwright -- npx -y @playwright/mcp@latest

# 설치된 서버 목록 확인
claude mcp list
```

---

## 참고 리소스

- **공식 MCP 서버 레포**: [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- **MCP 레지스트리**: [github.com/modelcontextprotocol/registry](https://github.com/modelcontextprotocol/registry)
- **Awesome MCP Servers (punkpeye)**: [github.com/punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers)
- **Awesome MCP Servers (wong2)**: [github.com/wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers)
- **Awesome MCP Servers (appcypher)**: [github.com/appcypher/awesome-mcp-servers](https://github.com/appcypher/awesome-mcp-servers)
- **MCP 서버 디렉토리**: [mcpservers.org](https://mcpservers.org/)
- **MCP Awesome (1200+)**: [mcp-awesome.com](https://mcp-awesome.com/)
- **MCP 공식 사양**: [modelcontextprotocol.io](https://modelcontextprotocol.io/specification/2025-11-25)
