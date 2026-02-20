---
name: init
description: Create or improve AGENTS.md by analyzing repository commands, architecture, and existing guidance files
metadata:
  tags: initialization, agents, onboarding, repository-analysis, documentation
---

## When to use

Use this skill when you need to create an initial `AGENTS.md` for a repository, or improve an existing one for AI coding agents.

## Instructions

Analyze the repository and produce (or improve) an `AGENTS.md` file that gives future AI coding agents a concise, actionable operating guide.

### Required content

1. Common development commands for this codebase:
   - Build
   - Lint
   - Tests
   - Running a single test
   - Any additional commands required for normal development in this repository

2. High-level architecture and structure:
   - Focus on the big-picture organization that requires reading multiple files to understand
   - Do not dump discoverable directory listings

### Source files to check first

- Existing `AGENTS.md`
- `README.md`
- `PROJECT.md` (if present)
- Cursor rules (`.cursor/rules/` or `.cursorrules`)
- Copilot instructions (`.github/copilot-instructions.md`)
- `GEMINI.md`

If `AGENTS.md` already exists, improve it instead of replacing it blindly.

### Mandatory header

Prefix `AGENTS.md` with this exact text:

```text
This file provides guidance to AI coding agents like Claude Code (claude.ai/code), Cursor AI, Codex, Gemini CLI, GitHub Copilot, and other AI coding assistants when working with code in this repository.
```

### Constraints

- Keep guidance focused, specific, and scoped to the repository
- Avoid generic best-practice filler
- Do not invent sections or information not supported by repository files
- Avoid repetition
- Keep the document under 500 lines
