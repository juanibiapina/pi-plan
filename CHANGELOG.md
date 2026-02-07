# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.0] - 2026-02-07

- Register `plan-mode` powerbar segment via `powerbar:register-segment` event for ordered multi-select settings

## [0.2.0] - 2026-02-06

- Add pi-powerbar support: emits `powerbar:update` segment (`⏸ plan`) when plan mode is active

## [0.1.0] - 2026-02-06

Initial release.

- `/plan` command to toggle plan mode
- Configurable keyboard shortcut via `/extension-settings` (no shortcut bound by default)
- Read-only tool restriction when active (`read`, `bash`, `grep`, `find`, `ls`, `questionnaire`)
- `--plan` CLI flag to start in plan mode
- Session persistence via invisible messages
- Status bar indicator (`⏸ plan`)
