# EXPINFO — LEAD TERMINAL 🖥️

> **Bloomberg-style business development intelligence dashboard for trade show lead generation.**
> A self-contained HTML terminal that surfaces **IMTS-adjacent, non-exhibiting manufacturing technology companies** showing financial signals of imminent marketing budget expansion.

**© EXPINFO™ — Trademark property of ExpInfo.** Internal use only. Not for external redistribution.

---

## 📊 What It Does

The PG Exhibits Lead Terminal identifies **new business prospects for exhibit sales** by surfacing companies that:

- Operate in the same ecosystems as confirmed **IMTS 2026** exhibitors (competitors, adjacent players, distributors, integrators)
- Have **NOT yet committed to exhibiting** at a major trade show
- Show **2+ financial buy-signals** indicating an imminent marketing budget increase

Think of it as a radar for *"who is about to need a booth."*

---

## 🔍 Prospect Scoring Methodology

Each prospect is scored against trigger logic:

| Signal | Description |
|--------|-------------|
| 📈 **Revenue Growth** | >10% YoY revenue growth |
| 💰 **Funding Round** | Recent Series A–E funding (war chest for GTM spend) |
| 👥 **Hiring Push** | Announced expansion of sales/engineering headcount |
| 💰 **Capex Increase** | Stated or inferred capital investment ramp |
| 🔄 **Corporate Pivot** | Divestiture, merger, rebrand, or new product launch |
| 🌍 **Market Entry** | US / new-region market entry requiring brand awareness |

**Priority Classification:**
- 🔴 **HIGH** — 2 or more concurrent triggers, nearest to a buying decision
- 🟡 **MEDIUM** — 1 trigger present, monitor and nurture
- ⚪ **LOW** — Established exhibitor likely, upsell/expand footprint angle

---

## ✨ Features

- **📊 KPI Dashboard** — instant summary of total prospects, high-priority count, pipeline estimate
- **🔍 Live Search** — filter by company, sector, or HQ instantly
- **🎯 Priority Filter Buttons** — ALL / HIGH / MEDIUM / LOW one-click views
- **📋 Click-to-Expand Detail Rows** — reveals buy-signals and the recommended PG Exhibits pitch angle per company
- **📈 Scrolling Ticker Tape** — Bloomberg-style animated prospect tape
- **🕐 Live Central Time Clock** — aligned to Chicago (venue) time
- **💾 Fully Offline** — single HTML file, zero dependencies, zero telemetry
- **📱 Responsive** — collapses gracefully on mobile/tablet

---

## 🚀 Getting Started

No build step. No dependencies. Just open it.

```bash
git clone https://github.com/your-org/pg-exhibits-lead-terminal.git
cd pg-exhibits-lead-terminal
open pg_exhibits_leads.html   # macOS
# or double-click the file on Windows/Linux
