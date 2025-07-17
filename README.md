# ReadyPR
**Make every pull request merge‑ready—automatically.**

[![Status Badge](#)](#) [![CI](#)](#) [![License: MIT](#)](#)

---

## What It Does
ReadyPR watches new and updated GitHub pull requests, analyzes failures (lint, formatting drift, trivial code/style issues, policy checks), and pushes minimal fix commits so your PR goes green faster. Maintainers review the diff—merge when happy.

---

## Quick Start

1. **Install the ReadyPR GitHub App** (coming soon).
2. Add a repo config file: `.readypr.yaml` (see below).
3. Grant permission to read PRs + write patch commits.
4. Open or update a PR—ReadyPR suggests or auto-pushes fixes.

### Minimal Config
```yaml
# .readypr.yaml
mode: auto            # auto | suggest
fixes:
  - lint              # run linter --fix
  - format            # run formatter
  - typing            # stub / quick type fixes (experimental)
ci_blocking: true     # only act when PR is red
comment_summary: true # post what was fixed

