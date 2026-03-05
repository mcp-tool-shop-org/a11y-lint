---
title: Python API
description: Programmatic scanning, scorecards, and reports.
sidebar:
  order: 4
---

## Quick scan

```python
from a11y_lint import scan

messages = scan("ERROR: It failed")
```

## Custom scanner

```python
from a11y_lint import Scanner

scanner = Scanner()
scanner.disable_rule("line-length")
messages = scanner.scan_text(text)
```

## Create messages programmatically

```python
from a11y_lint import A11yMessage

msg = A11yMessage.error(
    code="APP001",
    what="Configuration file missing",
    why="The app cannot start without config.yaml",
    fix="Create config.yaml in the project root"
)
```

## Validate against schema

```python
from a11y_lint import is_valid, validate_message

assert is_valid(msg)
```

## Generate scorecard

```python
from a11y_lint import create_scorecard

card = create_scorecard(messages)
print(card.summary())
print(f"Score: {card.overall_score}% ({card.overall_grade})")
```

## Generate markdown report

```python
from a11y_lint import render_report_md

markdown = render_report_md(messages, title="My Report")
```

## Environment variables

| Variable | Description |
|----------|-------------|
| `NO_COLOR` | Disable colored output (any value) |
| `FORCE_COLOR` | Force colored output (any value) |
