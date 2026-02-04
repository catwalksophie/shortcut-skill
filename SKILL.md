---
name: shortcut
version: 1.0.0
description: Manage stories on Shortcut.com kanban boards. Use when creating, updating, or listing tasks/stories on Shortcut project management boards. Supports creating stories with descriptions and types (feature/bug/chore), updating story status, and listing active/completed stories.
---

# Shortcut Kanban Integration

Manage tasks and stories on Shortcut.com project boards via API.

## Prerequisites

- Shortcut API token at `/root/secrets/shortcut-api-token`
- Workspace: `coalface`
- Team: `dev`

## Available Operations

### List Stories

```bash
scripts/shortcut-list-stories.sh [--active|--completed|--all] [--json]
```

Options:
- `--active` - Show only incomplete stories (default)
- `--completed` - Show only completed stories
- `--all` - Include archived stories
- `--json` - Output raw JSON

### Create Story

```bash
scripts/shortcut-create-story.sh "Story name" [--description "text"] [--type feature|bug|chore]
```

Story types:
- `feature` (default) - New functionality
- `bug` - Bug fix
- `chore` - Maintenance task

### Update Story

```bash
scripts/shortcut-update-story.sh <story-id> [--state started|done|unstarted] [--description "new text"]
```

Common workflow states:
- `500000006` - Unstarted
- `500000007` - Started  
- `500000008` - Done

## Workflow

1. List existing stories to understand current board state
2. Create new stories with descriptive names and appropriate types
3. Update story status as work progresses

## Notes

- All scripts require sudo access to read the API token
- Stories are created in "Unstarted" state by default
- The workspace and team are pre-configured in the scripts
