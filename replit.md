# Everything Claude Code (ECC)

## Project Overview

ECC is a CLI toolkit and collection of battle-tested configurations for AI agent harnesses (Claude Code, Codex, Cursor, OpenCode, Gemini, etc.). It provides agents, skills, hooks, rules, and commands to improve AI-driven development workflows.

## Tech Stack

- **Node.js** (v18+): Primary runtime for all CLI scripts
- **Python 3.11**: Dashboard (Tkinter GUI) and LLM abstraction layer
- **Rust**: ECC 2.0 alpha control-plane (TUI in `ecc2/`)
- **Package Manager**: npm (also has yarn.lock)

## Project Structure

- `scripts/` — Core CLI scripts (ecc.js, install-apply.js, etc.)
- `agents/` — Markdown AI persona definitions
- `skills/` — Reusable skill modules (each with SKILL.md)
- `hooks/` — JSON/script hooks for agent action interception
- `rules/` — Language-specific coding standards
- `commands/` — Custom agent command definitions
- `manifests/` — Selective install profiles
- `src/llm/` — Python LLM abstraction layer
- `ecc2/` — Rust-based ECC 2.0 prototype
- `ecc_dashboard.py` — Tkinter GUI dashboard

## CLI Usage

```bash
node scripts/ecc.js --help
node scripts/ecc.js typescript
node scripts/ecc.js install --profile developer --target claude
node scripts/ecc.js catalog profiles
```

## Workflow

The "Start application" workflow runs `node scripts/ecc.js --help` as a console workflow, demonstrating the CLI is operational.

## Key Commands

- `npm test` — Run all CI validators
- `node scripts/ecc.js <subcommand>` — Main CLI entry point
- `python3 ecc_dashboard.py` — Launch Tkinter GUI dashboard
