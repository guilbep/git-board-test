---
issue: a6661d9
status: draft
last_updated: 2026-10-22
summary: Add a line to README.md saying this repository is a scratch board for git-board live tests.
---

# Plan: README says this is a scratch board (a6661d9)

## Context
Issue a6661d9 asks that `README.md` state this repository is a scratch board for git-board live tests. The README currently opens with "A playground for git-board and the git-bug bridge-sync fork" but never says "scratch board" or "live tests".

## Change
One edit, `README.md` only: add a line right after the title (before the existing paragraph):

> This is a scratch board for git-board live tests.

No other files, no code, no tests (docs-only).

## Verification
- `grep -n "scratch board for git-board live tests" README.md` returns exactly one line.
- `git diff --stat` shows only `README.md`, one line added.
