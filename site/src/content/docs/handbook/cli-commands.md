---
title: CLI Commands
description: scan, validate, scorecard, report, list-rules, schema.
sidebar:
  order: 3
---

## scan

Check for accessibility issues.

```bash
a11y-lint scan [OPTIONS] INPUT
```

| Option | Description |
|--------|-------------|
| `--stdin` | Read from stdin instead of file |
| `--color [auto\|always\|never]` | Color output mode (default: auto) |
| `--json` | Output results as JSON |
| `--format [plain\|json\|markdown]` | Output format |
| `--disable RULE` | Disable specific rules (can repeat) |
| `--enable RULE` | Enable only specific rules (can repeat) |
| `--strict` | Treat warnings as errors |

## validate

Validate JSON messages against the CLI error schema.

```bash
a11y-lint validate messages.json
a11y-lint validate -v messages.json  # Verbose output
```

## scorecard

Generate an accessibility scorecard.

```bash
a11y-lint scorecard output.txt
a11y-lint scorecard --json output.txt     # JSON output
a11y-lint scorecard --badge output.txt    # shields.io badge
```

## report

Generate a markdown report.

```bash
a11y-lint report output.txt
a11y-lint report output.txt -o report.md
a11y-lint report --title="My Report" output.txt
```

## list-rules

Show available rules.

```bash
a11y-lint list-rules          # Simple list
a11y-lint list-rules -v       # Verbose with categories and WCAG refs
```

## schema

Print the JSON schema for CLI error messages.

```bash
a11y-lint schema
```
