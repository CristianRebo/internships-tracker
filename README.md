# 📗 Internships Tracker

A single-file internship application tracker. One HTML file — no build step, no server, no dependencies, no sign-up. Open it and it works.

Built for finance, quant and consulting recruiting, where you're running 30+ applications across cycles and portals and losing track of which ones are actually live.

**[→ Live demo](https://capoheladero.github.io/internships-tracker/)**

---

## Why

Spreadsheets work until they don't. Links get truncated, statuses turn into inconsistent free text, and you can never answer the only question that matters: *what needs my attention today?*

This gives you that in one screen — colour-coded stages, live counters, and a deadline column that makes an overdue assessment impossible to miss.

## Features

- **Nine pipeline stages** — Interview, Assessment, Accepted, Waiting, To Apply, Verify, Networking, Rejected, Closed. `Verify` is for applications you *think* you submitted but never got a confirmation for; `Closed` keeps withdrawals separate from real rejections so your stats stay honest.
- **Live counters** — total, in process, accepted, waiting, to apply, to verify, closed.
- **Company logos** fetched automatically from each company's domain, with coloured initials as fallback.
- **Search and filter** by company, role, location, comments, status or recruiting cycle.
- **Sortable columns** — click any header.
- **Click-to-edit** — click a row to open it, change any field, save or delete.
- **Deadline column** — assessment dates and next actions, highlighted.
- **Direct links** — one click straight to the application portal.
- **Autosave** in your browser (localStorage). Nothing is uploaded anywhere, ever.
- **Export / import** — JSON for backups and moving between machines, CSV for spreadsheets.
- **Responsive** — works on a phone.

## Getting started

**Option A — use it online.** Open the live demo. Your data is saved in your own browser and never leaves it.

**Option B — run it locally.** Download `index.html` and double-click it. That's the whole install.

Then:

1. Click **Reset** to clear the three example rows
2. Add your applications with **+ Add application**
3. Click **Export JSON** occasionally to keep a backup

## Fields

| Field | Notes |
|---|---|
| Company | Required |
| Role / programme | e.g. "Summer Analyst — Global Markets" |
| Location | Free text: city, region, or Remote |
| Cycle | 2026 / 2027 / 2028 — filter by recruiting season |
| Status | One of the nine stages |
| Dates / assessment | Deadlines and next actions — shown highlighted |
| Application link | Direct link to the portal; renders as "Open ↗" |
| Company website | Domain only (e.g. `jpmorgan.com`) — used to fetch the logo |
| Comments | Recruiter names, referral notes, anything else |

## Backups and syncing

Data lives in `localStorage`, which is per-browser and per-device. To move it or keep history:

- **Export JSON** → save the file (commit it to a private repo if you want version history)
- **Import JSON** on another machine or browser to restore it

## Privacy

Everything stays in your browser. No backend, no analytics, no tracking, no account. The only outbound request is to Google's favicon service for company logos — it sends nothing but the company domain, and fails gracefully offline.

## Tech

Plain HTML, CSS and vanilla JavaScript in a single file. No frameworks, no build tooling, around 500 lines. Fork it and change what you like — the status list, colours and fields all sit near the top of the `<script>` block.

## Contributing

Issues and pull requests welcome. If you want it for another field — law, medicine, engineering, grad schemes — the stage names are a single array, easy to swap.

## Licence

MIT — do whatever you like with it.
