# Apie documentation

Official documentation for [Apie](https://apie.sh) — runtime visibility and guardrails for AI agents.

## Local development

```bash
npx mintlify dev
```

Preview at `http://localhost:3000`.

## Structure

Documentation is organized by what users want to accomplish — not by programming language. Code examples show TypeScript and Python side by side via `<CodeGroup>`.

| Section | Pages |
| --- | --- |
| Start here | Introduction, connect, choose integration tier, how Apie works |
| See what your agent does | Runs, tool calls, telemetry, multi-agent pipelines |
| Define boundaries | Capabilities, metadata, drift |
| Guard your agent | Monitor, enforce, templates, approval |
| MCP | Proxy, instrumented client |
| Integrations | LangChain, OpenAI Agents, platform connectors |
| Recipes | Full example walkthroughs |
| Production | Telemetry, redaction, diagnostics, reports |
| Reference | Configuration, events, CLI, errors |

## Authoring

See [AGENTS.md](./AGENTS.md) for voice, terminology, and content boundaries.

## Deployment

Connect the `apie-sh/docs` repo to Mintlify and set custom domain `docs.apie.sh`.
