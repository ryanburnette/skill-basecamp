# skill-basecamp

Interact with Basecamp via the Basecamp CLI (`basecamp` v0.9.0). Full API coverage: projects, todos, cards, messages, files, schedule, check-ins, timeline, recordings, templates, webhooks, subscriptions, lineup, chat, gauges, assignments, notifications, and accounts.

Personal fork of [basecamp/basecamp-cli skill](https://github.com/basecamp/basecamp-cli). Tracks CLI bugs and reflects personal content and workflow preferences.

**Known bugs tracked (v0.9.0):**
- `basecamp show` (generic) returns `steps: null` on todos with subtasks — use `basecamp todos show` instead
- `basecamp cards steps <todo_id>` fails with "Not Found" — it hits a card-table-specific endpoint

**Fixed in v0.9.0**, verified against a live Basecamp 5 account:
- `basecamp search` works ([#470](https://github.com/basecamp/basecamp-cli/issues/470))
- `basecamp todos update --due` persists ([#485](https://github.com/basecamp/basecamp-cli/issues/485))
- `basecamp todos list` finds listless todos, and `todos create --loose` makes them ([#474](https://github.com/basecamp/basecamp-cli/issues/474))
- `basecamp todos show` returns `steps`, and `--md` renders them
- `--notify-on-completion` exposes "let know when done", replacing the raw-PUT workaround

Note: v0.9.0 changed `basecamp auth login` to request `full` scope by default on Basecamp-hosted OAuth. New logins only; existing credentials are untouched.

## Usage

This is an [Agent Skills](https://agentskills.io/) compatible skill. Load it with your agent harness — Claude Code, opencode, pi, or another — and invoke via `skill:basecamp`. It gives the agent what it needs to write correct `basecamp` CLI commands.

Load it directly. Do not provision it with `basecamp setup claude` or `basecamp skill install`; those install upstream's copy over this fork. `basecamp doctor` reporting "Skill not linked" is expected.

## Structure

- `SKILL.md` — Skill instructions and frontmatter
