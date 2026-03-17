---
name: gws-calendar
version: 1.0.0
description: "Google Calendar: Manage calendars and events."
metadata:
  openclaw:
    category: "productivity"
    requires:
      bins: ["gws"]
    cliHelp: "gws calendar --help"
---

# calendar (v3)

> **PREREQUISITE:** Read `../gws-shared/SKILL.md` for auth, global flags, and security rules.

```bash
gws calendar <resource> <method> [flags]
```

## Helper Commands

| Command | Description |
|---------|-------------|
| [`+insert`](../gws-calendar-insert/SKILL.md) | create a new event |
| [`+agenda`](../gws-calendar-agenda/SKILL.md) | Show upcoming events across all calendars |

## Key Resources

### calendarList

  - `list` — Returns the calendars on the user's calendar list.
  - `get` — Returns a calendar from the user's calendar list.

### events

  - `list` — Returns events on the specified calendar.
  - `insert` — Creates an event.
  - `get` — Returns an event based on its Google Calendar ID.
  - `patch` — Updates an event (supports patch semantics).
  - `delete` — Deletes an event.
  - `quickAdd` — Creates an event based on a simple text string.
  - `move` — Moves an event to another calendar.
  - `instances` — Returns instances of a recurring event.

### freebusy

  - `query` — Returns free/busy information for a set of calendars.

## Discovering Commands

```bash
gws calendar --help
gws schema calendar.<resource>.<method>
```
