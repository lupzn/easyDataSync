# Changelog

All notable user-facing changes to easyDataSync are documented here.
The format is loosely based on [Keep a Changelog](https://keepachangelog.com/).

---

## [v1.4.0] — Live licensing + Dark mode

- **Real license activation** — paid licenses (Pro / Business / Enterprise) now activate against the live Lemon Squeezy licensing service
- **Dark mode by default** — full dark theme; light theme switchable under Settings → Application → Theme
- Fix: flag-rule rows in mapping list and diff tree are now visible on dark theme
- Fix: License deactivate is local-only by default so single-seat licenses aren't permanently disabled when moving between machines
- Fix: License activation auto-fills `instance_name` with hostname when not supplied

→ [Download v1.4.0](https://github.com/lupzn/easyDataSync/releases/tag/v1.4.0) · [Buy a license](https://easydatasync.lupzn.de#pricing)

---

## [v1.3.0] — License system, tier-aware UI

- **Paid-license system** — Free / Pro (29 € one-time) / Business (99 € / yr per seat) / Enterprise (from 499 € / yr)
- **30-day Pro trial** auto-starts on first launch — every Pro feature unlocked
- **In-app license dialog** under Info → License — activate, deactivate, re-validate
- **Tier badge** in the header (top-right) shows current state
- **Trial-expiry banner** when ≤ 7 days remain
- **Pro feature gates** — multiple mapping profiles, validations, CLI mode, watch-folder mode now require a paid tier
- **Bilingual UI** for all license-related strings (EN + DE)

→ [Download v1.3.0](https://github.com/lupzn/easyDataSync/releases/tag/v1.3.0) · [Buy a license](https://easydatasync.lupzn.de#pricing)

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

[v1.4.0]: https://github.com/lupzn/easyDataSync/releases/tag/v1.4.0
[v1.3.0]: https://github.com/lupzn/easyDataSync/releases/tag/v1.3.0
[v1.2.1]: https://github.com/lupzn/easyDataSync/releases/tag/v1.2.1
[v1.2.0]: https://github.com/lupzn/easyDataSync/releases/tag/v1.2.0
