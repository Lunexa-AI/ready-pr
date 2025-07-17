# ready-pr
**Make every pull request merge‑ready—automatically.**

[![Status Badge](#)](#) [![CI](#)](#) [![License: MIT](#)](#)

---

## What It Does
ready-pr watches new and updated GitHub pull requests, analyzes failures (lint, formatting drift, trivial code/style issues, policy checks), and pushes minimal fix commits so your PR goes green faster. Maintainers review the diff—merge when happy.

---

## Quick Start

1. **Install the ready-pr GitHub App** (coming soon).
2. Add a repo config file: `.readypr.yaml` (see below).
3. Grant permission to read PRs + write patch commits.
4. Open or update a PR—ready-pr suggests or auto-pushes fixes.

### Minimal Config
```yaml
# .ready-pr.yaml
mode: auto            # auto | suggest
fixes:
  - lint              # run linter --fix
  - format            # run formatter
  - typing            # stub / quick type fixes (experimental)
ci_blocking: true     # only act when PR is red
comment_summary: true # post what was fixed

