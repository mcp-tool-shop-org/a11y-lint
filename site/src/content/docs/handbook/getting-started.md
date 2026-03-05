---
title: Getting Started
description: Install, scan CLI output, and generate reports.
sidebar:
  order: 1
---

## Install

```bash
pip install a11y-lint
```

Requires Python 3.11+.

## Scan CLI output

```bash
# Scan a file
a11y-lint scan output.txt

# Scan from stdin
echo "ERROR: It failed" | a11y-lint scan --stdin

# JSON output for CI
a11y-lint scan output.txt --json
```

## Generate reports

```bash
# Markdown report
a11y-lint report output.txt -o report.md

# Scorecard with grade
a11y-lint scorecard output.txt

# shields.io badge
a11y-lint scorecard --badge output.txt
```

## What it catches

- Lines too long for magnified displays
- ALL-CAPS text that hinders readability
- Jargon with no explanation
- Color as the only signal (WCAG 1.4.1)
- Missing "why" and "fix" context
- Excessive emoji use
- Ambiguous pronouns
