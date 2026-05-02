# Changelog

All notable user-facing changes to easyDataSync are documented here.
The format is loosely based on [Keep a Changelog](https://keepachangelog.com/).

---

## [v1.2.1] — One-click in-app updates

- Auto-update is now fully in-app: download + install with one click
- Update dialog launches the installer via a PowerShell helper that waits for the running app to exit cleanly
- Auto-updater prefers the Setup installer asset over the portable .exe
- Browser-redirect fallback retained for releases without an installer asset

→ [Download v1.2.1](https://github.com/lupzn/easyDataSync/releases/tag/v1.2.1)

---

## [v1.2.0] — i18n, validations, watch-folder

- **Bilingual UI** — English (default) and German, switchable under Settings → Application → Language
- **Validations per column** — mandatory, allowed values, regex pattern, numeric range
- **Watch-folder mode (CLI)** — drop a file in a folder, it gets processed automatically
- **CLI** — new `validate` subcommand; `--strict` flag on `sync` and `watch` (exit code 4 on validation failures)
- License changed from MIT to a proprietary EULA — source remains visible for transparency, binaries free for personal use, redistribution requires consent

→ [Download v1.2.0](https://github.com/lupzn/easyDataSync/releases/tag/v1.2.0)

---

## [v1.1.0] — CLI mode, mapping profiles, CSV support

- **CLI mode** — scriptable `sync` subcommand
- **Mapping profiles** — save and reuse mappings as JSON
- **CSV / TSV support** — read `.csv` and `.tsv` files
- Performance improvements for large files

---

## [v1.0.0] — Initial public release

- GUI for column mapping between Excel files (`.xlsx`, `.xlsm`)
- Per-column mapping: direct copy, constant, conditional flag, skip
- Cell-by-cell diff — output contains only changed and new rows
- Read-only sources, no cloud, no login

---

[v1.2.1]: https://github.com/lupzn/easyDataSync/releases/tag/v1.2.1
[v1.2.0]: https://github.com/lupzn/easyDataSync/releases/tag/v1.2.0
