# FlyRank Capstone

Setup phase for the capstone track: establishing a working Node.js, Git, and AI-assisted (Claude Code) development environment.

## Status

🚧 In progress — environment and toolchain setup.

## Stack

- Git / GitHub
- Claude Code (AI-assisted development)

## Goal

Verify a complete, working AI-assisted dev toolchain before moving into later phases of the capstone project.

## Getting started

When every item in the [Done checklist](#done-checklist) is checked, this setup phase is complete.

### Prerequisites

Install **Node.js (LTS)** and **Git**, then verify:

```bash
node --version   # expect v22.x.x or newer LTS
git --version    # expect 2.x or newer
```

Configure Git once per machine:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Clone the repo

```bash
git clone <repo-url> flyrank
cd flyrank
```

### Folder structure

```
flyrank/
├── .cursor/
│   └── rules/
│       └── project.mdc    # Cursor AI project rules
├── .gitignore
├── CLAUDE.md              # Claude Code project context
├── LICENSE
└── README.md
```

### Configure Claude Code / Cursor

1. Open the `flyrank/` folder as your workspace root (Cursor or VS Code with Claude Code).
2. The assistant reads **`CLAUDE.md`** (stack, conventions, purpose) and **`.cursor/rules/project.mdc`** (Cursor-specific rules) for project context.
3. When secrets are needed later, use **`.env`** at the repo root — it is gitignored and must never be committed.

### Smoke-test

Ask the assistant to summarize `CLAUDE.md` or propose a small README edit. Confirm it references repo files and follows [Conventional Commits](https://www.conventionalcommits.org/).

### Done checklist

- [ ] Node.js LTS and Git installed (`node --version`, `git --version` succeed).
- [ ] Repo cloned; Git identity configured.
- [ ] Cursor or Claude Code opens this folder and reads project context.
- [ ] Smoke-test passes — assistant summarizes `CLAUDE.md` or proposes a sensible edit.
- [ ] `.env` policy understood — local secrets only, never committed.
