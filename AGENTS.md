# Documentation project instructions

## About this project

- Mintlify documentation site for [Apie](https://apie.sh) — runtime visibility and guardrails for AI agents
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Documentation is **feature-driven**, not language-driven — organize by what users want to accomplish
- Use `<CodeGroup>` for TypeScript and Python on every instructional page

## Terminology

| Term | Usage |
|------|-------|
| Agent | The AI system you register and instrument (not "bot") |
| Run | One unit of work — a user request, a job, a handler invocation |
| Session | Container for related runs, especially multi-agent pipelines |
| Tool call | Agent invoking an external capability |
| Action | What the tool does (`read`, `execute`, `delete`, …) |
| Resource | What the action touches (`code_repository`, `pipeline_run`, `secret`, …) |
| Capability | Declared boundary of tools, actions, and resources |
| Guardrail | Policy evaluated before an action runs |
| Mode | `monitor` (observe) or `enforce` (block and wait for approvals) |
| Telemetry | Events batched and sent to Apie in the background |

## Writing voice

Every page follows this pattern:

1. **Open with intent** — what the user wants to accomplish
2. **State the outcome** — what works when they finish
3. **Show a decision** — table or flowchart when multiple paths exist
4. **Walk through it** — complete runnable examples; "What you'll see in the dashboard" after major steps
5. **Escalate to production** — simple path first, then Enforce mode and rich metadata

**Tone:** Direct, warm, confident. Write like a senior engineer pairing on day one.

- Use active voice and second person ("you")
- Sentence case for headings
- Bold for UI elements: Click **Dashboard**
- Code formatting for file names, commands, paths

## Content boundaries

- Document public `Apie` / `AsyncApie` APIs and CLI commands
- Do not document internal modules (`mcp_core/`, `guard.py`, etc.)
- Note SDK parity gaps honestly (e.g. `apie.wrap()` is JavaScript-only)

## SDK packages

| Language | Package | CLI |
|----------|---------|-----|
| TypeScript | `@apie-sh/sdk`, `@apie/cli` | `npx apie` |
| Python | `apie-sdk` | `apie` |
