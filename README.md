# @juanibiapina/pi-plan

A [pi](https://github.com/badlogic/pi-mono) extension for plan mode — read-only exploration and analysis.

## Features

- **`/plan` command** — Toggle plan mode on and off
- **Tab shortcut** — Quick toggle with the Tab key
- **Read-only tools** — Only safe, non-modifying tools are available while in plan mode
- **Session persistence** — Plan mode state is persisted across session resume via invisible messages
- **Status indicator** — Shows `⏸ plan` in the status bar when active

## Installation

```bash
pi install npm:@juanibiapina/pi-plan
```

## Usage

### Entering Plan Mode

Use `/plan` or press `Tab` to toggle plan mode. When enabled:

- Only read-only tools are available (`read`, `bash`, `grep`, `find`, `ls`, `questionnaire`)
- The agent is instructed to only observe, analyze, and plan — no modifications
- A `⏸ plan` indicator appears in the status bar

### Exiting Plan Mode

Use `/plan` or press `Tab` again to return to normal mode with full tool access.

### CLI Flag

Start pi directly in plan mode:

```bash
pi --plan
```

### Session Persistence

Plan mode state is tracked via invisible messages in the session. When resuming a session that was in plan mode, the mode is automatically restored.

## License

MIT
