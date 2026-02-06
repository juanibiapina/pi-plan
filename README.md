# @juanibiapina/pi-plan

A [pi](https://github.com/badlogic/pi-mono) extension for plan mode — read-only exploration and analysis.

## Features

- **`/plan` command** — Toggle plan mode on and off
- **Configurable shortcut** — Optional keyboard shortcut via `/extension-settings`
- **Read-only tools** — Only safe, non-modifying tools are available while in plan mode
- **Session persistence** — System reminders are kept in session history, so what the LLM sees is exactly what you see
- **Status indicator** — Shows `⏸ plan` in the status bar when active

## Installation

```bash
pi install npm:@juanibiapina/pi-plan
```

## Usage

### Entering Plan Mode

Use `/plan` to toggle plan mode. When enabled:

- Only read-only tools are available (`read`, `bash`, `grep`, `find`, `ls`, `questionnaire`)
- The agent is instructed to only observe, analyze, and plan — no modifications
- A `⏸ plan` indicator appears in the status bar

### Exiting Plan Mode

Use `/plan` again to return to normal mode with full tool access.

### Keyboard Shortcut

No shortcut is bound by default. To configure one, use `/extension-settings` and set the `shortcut` setting under `plan` (e.g. `tab`, `ctrl+p`).

> **Note:** The `/extension-settings` command is provided by the [`@juanibiapina/pi-extension-settings`](https://github.com/juanibiapina/pi-extension-settings) package, which must be installed separately:
>
> ```bash
> pi install npm:@juanibiapina/pi-extension-settings
> ```

### CLI Flag

Start pi directly in plan mode:

```bash
pi --plan
```

### How It Works

Plan mode works by injecting system reminder messages into the session when the mode changes. These messages instruct the LLM to operate in read-only mode (or restore full access when exiting). The messages are kept in the session history, so what is sent to the LLM is always exactly what you see in the session — no hidden prompt manipulation. When resuming a session that was in plan mode, the mode is automatically restored from these messages.

## License

MIT
