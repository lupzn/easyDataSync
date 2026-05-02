# Frequently Asked Questions

## General

### What is easyDataSync?

A local Windows desktop app that maps columns between two spreadsheet files (Excel or CSV) and generates an import file containing only the changed and new rows. It exists to replace the chain of VLOOKUPs, helper sheets, and manual copy-paste that data-import workflows usually become.

### Is the source code available?

The Software is proprietary. Binaries are distributed via this GitHub repository, but the source code is not published. See [LICENSE](../LICENSE) for the full EULA.

### Does easyDataSync upload my data anywhere?

No. The app runs 100 % locally. Network requests are limited to:

1. **License activation / re-validation** against the official licensing service (no file content sent).
2. **Update checks** against the GitHub Releases API for this repository.

Your source files, target files, mapping profiles, and processed output never leave your machine.

### Why is there a SmartScreen warning on first launch?

The binaries are not yet code-signed. Code-signing certificates start at around €200 / year, and as a small project we haven't reached the volume to justify it. To run anyway: right-click the .exe → Properties → "Unblock" → OK. Or in PowerShell: `Unblock-File path\to\easyDataSync.exe`.

[Donations](https://www.paypal.com/donate/?hosted_button_id=X8MG6CZK2PETS) help us afford code signing in the future.

---

## Licensing & Pricing

### What are the tiers?

| Tier | Price | Highlights |
|------|-------|------------|
| Free | 0 € | 1 mapping profile, GUI only, personal use |
| Pro | 29 € one-time | Unlimited profiles, validations, CLI · 1 year of updates |
| Business | 99 € / year per seat | Watch-folder, commercial license, priority support |
| Enterprise | from 499 € / year | 5 + seats, custom validations, SLA |

→ [Buy a license](https://easydatasync.lupzn.de#pricing)

### How does the trial work?

The first launch starts a 30-day Pro trial automatically. All Pro features are unlocked. After the trial expires, the app reverts to Free tier — no nag screens, no forced uninstall. Buy a license to keep Pro features.

### Can I use the Free tier in my company?

The Free tier is for **personal, non-commercial use only**. Any use in a commercial or business context — including freelancers, contractors, employees on company time, and non-profits — requires a paid license. See [LICENSE](../LICENSE), section 1.

### What if my license expires?

- **Pro (perpetual)** — the version you bought keeps working forever; you only stop receiving updates after 1 year. Renew to get future updates.
- **Business / Enterprise (annual)** — at the end of the subscription period, Pro features lock; the Free tier remains. Renew to keep Pro features.

### Refunds?

14-day money-back guarantee, no questions asked. Email info@lupzn.de with your order ID.

### Does the license work offline?

Yes. After activation, the license is cached locally and re-validated online every 30 days. If the machine is offline at re-validation time, the app stays activated for a 7-day grace period.

---

## Technical

### Which file formats are supported?

- Excel: `.xlsx`, `.xlsm`
- Delimited text: `.csv`, `.tsv`

### How big can the source / target files be?

Practically tested up to ~500 000 rows × 50 columns. Above that, expect higher memory usage. The app loads the full files into memory for cell-by-cell diffing — this is intentional for accuracy and is not designed for million-row workloads.

### Is there a CLI?

Yes — included in **Pro and above**. Subcommands: `sync`, `validate`, `watch` (Business+).

```cmd
easyDataSync-CLI.exe sync ^
    --source data.xlsx ^
    --target schema.xlsx ^
    --profile customer_sync ^
    --output import.xlsx
```

### Can I run easyDataSync headlessly / on a server?

Yes via the CLI (Pro). The Watch-folder mode (Business) is built specifically for this: drop a file in a folder, the watcher picks it up, processes it, and archives it.

### Does it work on macOS / Linux?

Not yet. The codebase is portable Python, but the installer, file dialogs, and update mechanism are Windows-specific. macOS support is on the roadmap if there's enough demand — please [open a feature request](https://github.com/lupzn/easyDataSync/issues/new?template=feature_request.yml) if you'd buy it.

---

## Support

### How do I report a bug?

[Open an issue](https://github.com/lupzn/easyDataSync/issues/new?template=bug_report.yml). Please include the version, edition, Windows version, and reproduction steps.

### How do I request a feature?

[Open an issue](https://github.com/lupzn/easyDataSync/issues/new?template=feature_request.yml). The clearer the use case, the faster it lands.

### How long until I get an answer?

| Tier | Response time |
|------|---------------|
| Free | Best-effort, GitHub issues only |
| Pro | Email, ~3 working days |
| Business | Email, ~24 hours |
| Enterprise | SLA per contract |

### Where can I find the change log?

In the [Releases section](https://github.com/lupzn/easyDataSync/releases) of this repository.
