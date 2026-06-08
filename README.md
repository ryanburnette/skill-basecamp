# skill-basecamp

Interact with Basecamp via the Basecamp CLI (`basecamp` v0.7.2). Full API coverage: projects, todos, cards, messages, files, schedule, check-ins, timeline, recordings, templates, webhooks, subscriptions, lineup, chat, gauges, assignments, notifications, and accounts.

Personal fork of [basecamp/basecamp-cli skill](https://github.com/basecamp/basecamp-cli). Tracks known bugs in v0.7.2 and reflects personal content and workflow preferences.

**Known bugs tracked (v0.7.2):**
- `basecamp search` is broken — times out, returns nothing ([#470](https://github.com/basecamp/basecamp-cli/issues/470))
- `basecamp todos update --due` silently fails ([#474](https://github.com/basecamp/basecamp-cli/issues/474))
- `basecamp todos list` misses listless todos (Basecamp 5 Todoset-level todos)
- `basecamp todos show` / `basecamp show` strip the `steps` field — subtasks not visible

## Usage

This is an [Agent Skills](https://agentskills.io/) compatible skill. Load it with your agent harness and invoke via `skill:basecamp`.

## Structure

- `SKILL.md` — Skill instructions and frontmatter
