---
title: Rules
description: WCAG rules, policy rules, and the What/Why/Fix format.
sidebar:
  order: 2
---

## WCAG rules

Rules mapped to specific WCAG success criteria. Violations may constitute accessibility barriers.

| Rule | Code | WCAG | Description |
|------|------|------|-------------|
| `no-color-only` | CLR001 | 1.4.1 | Don't convey information only through color |

## Policy rules

Best practices for cognitive accessibility. Not WCAG requirements, but improve usability for users with cognitive disabilities.

| Rule | Code | Description |
|------|------|-------------|
| `line-length` | FMT001 | Lines should be 120 characters or fewer |
| `no-all-caps` | LNG002 | Avoid all-caps text (hard to read) |
| `plain-language` | LNG001 | Avoid technical jargon (EOF, STDIN, etc.) |
| `emoji-moderation` | SCR001 | Limit emoji use (confuses screen readers) |
| `punctuation` | LNG003 | Error messages should end with punctuation |
| `error-structure` | A11Y003 | Errors should explain why and how to fix |
| `no-ambiguous-pronouns` | LNG004 | Avoid starting with "it", "this", etc. |

## Error message format

All messages follow the What/Why/Fix structure:

```
[ERROR] CODE: What happened
  Why: Explanation of why this matters
  Fix: Actionable suggestion

[WARN] CODE: What to improve
  Why: Why this matters
  Fix: How to improve (optional)

[OK] CODE: What was checked
```

## Grades vs CI gating

Letter grades (A-F) are informational summaries. For CI pipelines, gate on specific rule failures, error count thresholds, or regressions from a baseline — not on letter grades.
