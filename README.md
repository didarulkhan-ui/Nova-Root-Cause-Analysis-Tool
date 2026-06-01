# Nova Audit Group — Root Cause Analysis (RCA) Tool

A single-page, browser-based tool for performing and documenting root cause analysis on audit quality findings. No install, no login, no dependencies — it runs entirely in the browser.

**Live tool:** served from `index.html` at the site root.

## What it does
Guides the user through a compliant RCA and exports a workpaper (print to PDF) for the audit file. Built around:
- **ASQM 1** (mandatory RCA on identified deficiencies)
- **ASIC REP 739** — Root cause analysis: Audit firm thematic review
- **ASIC INFO 222** — Improving and maintaining audit quality
- **CA ANZ / CPA** — An External Auditor's Guide to Improving Audit Quality Using Root Cause Analysis

## Built-in "smart" checks (live, bottom-right panel)
- Blocks the RCA preparer being the engagement partner (independence)
- Flags if the EQR or specialists were not interviewed
- Forces Five-Whys to a minimum depth and warns on symptom-vs-cause misclassification
- Errors if every action is "more training"; nags if no real-time review is planned

## Files
- `index.html` — the tool (this is what Vercel serves)
- `Nova-RCA-Tool.html` — identical copy for local/offline use

## Deploy (Vercel via GitHub)
1. Push this folder to a GitHub repository.
2. In Vercel: **Add New → Project → Import** the repo.
3. Framework preset: **Other**. No build command, no output directory (it's static).
4. Deploy. Vercel serves `index.html` at the project URL. Every push auto-redeploys.

## Notes
- Data stays in the user's browser (autosave) and in exported PDF/JSON files. No data is sent anywhere.
- Internal use only. © 2025 Nova Audit Group. All rights reserved.
