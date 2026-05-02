# easyDataSync

<p align="center">
  <img src="docs/screenshots/logo.png" alt="easyDataSync" width="128" height="128">
</p>

<p align="center">
  <b>Map columns between Excel/CSV files in seconds.</b><br>
  Local Windows app. No cloud, no login, no upload of your data.
</p>

<p align="center">
  <a href="https://github.com/lupzn/easyDataSync/releases/latest"><img src="https://img.shields.io/github/v/release/lupzn/easyDataSync?color=06b6d4&include_prereleases" alt="Latest Release"></a>
  <a href="https://github.com/lupzn/easyDataSync/releases"><img src="https://img.shields.io/github/downloads/lupzn/easyDataSync/total?color=10b981" alt="Total Downloads"></a>
  <img src="https://img.shields.io/badge/Platform-Windows-0078d4?logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Languages-EN%20%7C%20DE-blue" alt="EN | DE">
  <a href="https://easydatasync.lupzn.de"><img src="https://img.shields.io/badge/Website-easydatasync.lupzn.de-06b6d4" alt="Website"></a>
</p>

<p align="center">
  <a href="#-quick-start"><b>Quick Start</b></a> ·
  <a href="#-features"><b>Features</b></a> ·
  <a href="#-pricing"><b>Pricing</b></a> ·
  <a href="https://github.com/lupzn/easyDataSync/releases/latest"><b>Download</b></a> ·
  <a href="https://easydatasync.lupzn.de"><b>Website</b></a>
</p>

---

## 🎯 The problem

You have two spreadsheets:

- **Source** — your current data (an internal master sheet, a CRM export, a database dump)
- **Target** — the column schema of your destination system (an empty sample export)

The columns don't line up. Some target columns need a constant value. Some need a flag based on a condition. You've been chaining VLOOKUPs, helper sheets, and manual copy-paste for years. Every cycle, you redo it by hand.

**easyDataSync turns that chain into a saved mapping you click once.**

```
source.xlsx ──┐
              ├──► [ easyDataSync ] ──► import_file.xlsx
target.xlsx ──┘                         (only changed + new rows)
```

---

## 🚀 Quick Start

1. **Download** — [latest release](https://github.com/lupzn/easyDataSync/releases/latest)
   - `easyDataSync.Setup.X.Y.Z.exe` — installer (recommended)
   - `easyDataSync-X.Y.Z.exe` — portable GUI
   - `easyDataSync-CLI-X.Y.Z.exe` — portable CLI
2. **Pick** your source file and your target schema file
3. **Map** each target column: direct copy / constant / conditional flag / skip
4. **Save** the mapping as a profile (JSON) — reuse it next month
5. **Sync** — review changes per cell, generate the import file

> **Note:** Windows may show a SmartScreen warning the first time. Right-click the .exe → Properties → "Unblock" → OK. The binaries are unsigned because code-signing certificates start at €200/year — supporters via [PayPal donation](https://www.paypal.com/donate/?hosted_button_id=X8MG6CZK2PETS) help offset this.

---

## ✨ Features

### Core (Free Tier)

- 📊 **Excel + CSV** — read `.xlsx`, `.xlsm`, `.csv`, `.tsv`
- 🎯 **Per-column mapping** — direct copy, constant value, conditional flag, skip
- 🔍 **Cell-by-cell diff** — output contains only changed and new rows
- 🌍 **Bilingual UI** — English + German, switchable at runtime
- 🛡️ **Read-only sources** — your source files are never modified
- 🔒 **100 % local** — no cloud, no login, no telemetry, no data upload
- 1 mapping profile

### Pro (29 € · perpetual · 1 year of updates)

Everything in Free, plus:

- ♾️ **Unlimited mapping profiles**
- ✅ **Validations per column** — mandatory · allowed values · regex · numeric range
- 🖥️ **CLI mode** — `sync`, `validate` subcommands · scriptable
- 🚦 **Strict mode** — non-zero exit code on validation failures (CI/CD-friendly)
- 📧 Email support

### Business (99 € / year · per seat)

Everything in Pro, plus:

- 👁️ **Watch-folder mode** — drop file, auto-process, archive
- 📦 **Commercial license** — use in any company, any project
- 🔄 **Continuous updates** — for the duration of your subscription
- ⚡ Priority email support (24 h response)

### Enterprise (from 499 € / year)

Everything in Business, plus:

- 5 + seats
- Custom validation rules
- Onboarding call
- SLA support
- Volume discount

→ **[See full pricing & buy](https://easydatasync.lupzn.de#pricing)**

---

## 📸 Screenshots

> Screenshots coming soon. See the [website](https://easydatasync.lupzn.de) for the latest visuals.

---

## 💼 Use cases

- **CRM migrations** — convert export from System A to import format of System B, only push deltas
- **Monthly inventory feeds** — supplier sends Excel, your ERP needs a specific schema
- **HR onboarding loads** — new-hire spreadsheet → HRIS bulk-import format
- **Legacy-system data feeds** — anything that demands a precise Excel template
- **Data normalization** — clean and validate flat files before warehouse ingestion

---

## 💰 Pricing

| Tier | Price | For whom |
|------|-------|----------|
| **Free** | 0 € | Personal use, evaluation, single-mapping workflows |
| **Pro** | 29 € one-time | Power users, freelancers, single workstations |
| **Business** | 99 € / year per seat | Companies, teams, recurring data work |
| **Enterprise** | from 499 € / year | 5 + seats, custom validations, SLA |

→ **[Buy a license](https://easydatasync.lupzn.de#pricing)**

A 30-day Pro trial is available on first launch.

---

## 🛟 Support

- 🐛 **Bug reports** — [open an issue](https://github.com/lupzn/easyDataSync/issues/new?template=bug_report.yml)
- 💡 **Feature requests** — [open an issue](https://github.com/lupzn/easyDataSync/issues/new?template=feature_request.yml)
- 📖 **Documentation** — [docs/](docs/)
- ❓ **FAQ** — [docs/faq.md](docs/faq.md)
- 📧 **Email** — info@lupzn.de
- 💛 **Donate** — [PayPal](https://www.paypal.com/donate/?hosted_button_id=X8MG6CZK2PETS)

---

## ❓ FAQ (short)

**Is it open source?**
The Software is proprietary. The binaries are free for personal use; commercial use requires a paid license. See [LICENSE](LICENSE).

**Does it phone home?**
Only for license activation, license re-validation (every 30 days), and update checks against this GitHub repo. No data, source files, or mapping profiles ever leave your machine.

**macOS / Linux?**
Not yet. The codebase is portable Python, but the installer and file dialogs are Windows-specific. macOS is on the roadmap if there's enough demand.

**What if my license expires?**
For Pro (perpetual), the version you bought keeps working forever — you just stop receiving updates after 1 year. For Business / Enterprise (subscription), Pro features lock after expiry; the Free tier remains.

**Refunds?**
14-day money-back guarantee, no questions asked. Just email info@lupzn.de.

→ **[Full FAQ](docs/faq.md)**

---

## 📜 License

Proprietary. Free for personal, non-commercial use. Commercial use requires a paid license.
See [LICENSE](LICENSE) for the full End User License Agreement.

---

<p align="center">
  <sub>Built with 🩵 by <a href="https://lupzn.de">LUPZN</a> — Made in Germany 🇩🇪</sub>
</p>
