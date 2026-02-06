# Changelog

## Unreleased

- Add pi-powerbar support: emits `powerbar:update` segment (`⏸ plan`) when plan mode is active

## 0.1.0

Initial release.

- `/plan` command to toggle plan mode
- Configurable keyboard shortcut via `/extension-settings` (no shortcut bound by default)
- Read-only tool restriction when active (`read`, `bash`, `grep`, `find`, `ls`, `questionnaire`)
- `--plan` CLI flag to start in plan mode
- Session persistence via invisible messages
- Status bar indicator (`⏸ plan`)
