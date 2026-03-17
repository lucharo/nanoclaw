---
name: gws-calendar-insert
version: 1.0.0
description: "Google Calendar: Create a new event."
metadata:
  openclaw:
    category: "productivity"
    requires:
      bins: ["gws"]
    cliHelp: "gws calendar +insert --help"
---

# calendar +insert

> **PREREQUISITE:** Read `../gws-shared/SKILL.md` for auth, global flags, and security rules.

create a new event

## Usage

```bash
gws calendar +insert --summary <TEXT> --start <TIME> --end <TIME>
```

## Flags

| Flag | Required | Default | Description |
|------|----------|---------|-------------|
| `--calendar` | — | primary | Calendar ID (default: primary) |
| `--summary` | yes | — | Event summary/title |
| `--start` | yes | — | Start time (ISO 8601, e.g., 2026-03-17T10:00:00+00:00) |
| `--end` | yes | — | End time (ISO 8601) |
| `--location` | — | — | Event location |
| `--description` | — | — | Event description/body |
| `--attendee` | — | — | Attendee email (can be used multiple times) |

## Examples

```bash
gws calendar +insert --summary 'Standup' --start '2026-03-17T09:00:00+00:00' --end '2026-03-17T09:30:00+00:00'
gws calendar +insert --summary 'Review' --start ... --end ... --attendee alice@example.com
gws calendar +insert --calendar 'Workouts' --summary 'Gym' --start '2026-03-17T18:00:00+00:00' --end '2026-03-17T19:15:00+00:00'
```

## Tips

- Use RFC3339 format for times (e.g. 2026-03-17T09:00:00+00:00).
- For recurring events or conference links, use the raw API instead.

> [!CAUTION]
> This is a **write** command — confirm with the user before executing.
