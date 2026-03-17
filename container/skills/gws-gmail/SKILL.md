---
name: gws-gmail
version: 1.0.0
description: "Gmail: Send, read, and manage email."
metadata:
  openclaw:
    category: "productivity"
    requires:
      bins: ["gws"]
    cliHelp: "gws gmail --help"
---

# gmail (v1)

> **PREREQUISITE:** Read `../gws-shared/SKILL.md` for auth, global flags, and security rules.

```bash
gws gmail <resource> <method> [flags]
```

## Helper Commands

| Command | Description |
|---------|-------------|
| [`+send`](../gws-gmail-send/SKILL.md) | Send an email |
| [`+triage`](../gws-gmail-triage/SKILL.md) | Show unread inbox summary (sender, subject, date) |

## Key Resources

### users

  - `getProfile` — Gets the current user's Gmail profile.
  - `messages` — Operations on messages (list, get, send, delete, modify, trash, untrash)
  - `threads` — Operations on threads (list, get, modify, trash, untrash, delete)
  - `labels` — Operations on labels (list, get, create, update, patch, delete)
  - `drafts` — Operations on drafts (list, get, create, update, send, delete)
  - `history` — List history of mailbox changes
  - `settings` — Manage user settings

## Discovering Commands

```bash
gws gmail --help
gws schema gmail.<resource>.<method>
```
