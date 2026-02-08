# Shortcut Skill v1.3.0 - ClawHub Submission

**Repository:** https://github.com/catwalksophie/shortcut-skill
**Version:** 1.3.0
**Category:** Productivity

## What's New in v1.3.0

Fixed workflow state IDs to match actual Shortcut workspace configuration:
- Corrected To Do state (500000007, was 500000006)
- Corrected In Progress state (500000008, was 500000007)
- Added support for all workflow states (Backlog, To Do, In Progress, In Review, Done)
- Added documentation for finding workspace-specific state IDs via API
- Added CHANGELOG.md for version tracking

## Description

Manage stories on Shortcut.com kanban boards via API. Create, update, and track tasks with full support for:
- Story creation with types (feature/bug/chore) and descriptions
- Workflow state management (backlog → todo → in progress → review → done)
- Checklist task management
- Comments
- Story listing and filtering

Perfect for AI agents managing project boards autonomously.

## Setup

1. Get API token from Shortcut.com (Settings → API Tokens)
2. Store in `~/.config/shortcut/api-token` or `SHORTCUT_API_TOKEN` env var
3. Optionally customize workflow state IDs for your workspace

## Links

- GitHub: https://github.com/catwalksophie/shortcut-skill
- Tag: https://github.com/catwalksophie/shortcut-skill/releases/tag/v1.3.0
