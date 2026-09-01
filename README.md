# EXPINFO — LEAD TERMINAL 🖥️

> **Bloomberg-style business development intelligence dashboard for trade show lead generation.**
> A self-contained HTML terminal that surfaces **IMTS-adjacent, non-exhibiting manufacturing technology companies** showing financial signals of imminent marketing budget expansion.

**© EXPINFO™ — Trademark property of ExpInfo.** Internal use only. Not for external redistribution.

---

## 🔗 Live Dashboard

**[View the Live Dashboard on GitHub Pages](https://bosquecounty.github.io/expInfo/)**

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
git clone https://github.com/BosqueCounty/expInfo.git
cd expInfo
open index.html   # macOS
# or double-click the file on Windows/Linux
```

### System Requirements

- **Browser**: Chrome, Firefox, Safari, Edge (all modern versions)
- **JavaScript**: Must be enabled
- **Storage**: ~500 KB disk space
- **Network**: None required (fully offline)

---

## 📖 User Guide

### Dashboard Layout

```
┌─────────────────────────────────────────────────────────┐
│ EXPINFO LEAD TERMINAL                    [🕐 2:45 PM CT] │
├─────────────────────────────────────────────────────────┤
│ KPI Summary:                                             │
│  Total Prospects: 487  |  HIGH Priority: 42  |  Est. Value: $2.1M
├─────────────────────────────────────────────────────────┤
│ [🔍 Search...] [ALL] [HIGH] [MEDIUM] [LOW]              │
├─────────────────────────────────────────────────────────┤
│ ▸ Acme Industries (HIGH) — Revenue Growth, Funding Round │
│   └─ Buy-signal details, sales angle, HQ location...    │
│ ▸ TechFlow Solutions (MEDIUM) — Hiring Push              │
│ ▸ QuantumX Corp (LOW) — Market Entry                     │
├─────────────────────────────────────────────────────────┤
│ 📺 Scrolling Ticker: 🔴 Acme expanding... 🟡 TechFlow... │
└─────────────────────────────────────────────────────────┘
```

### Interaction Guide

| Action | Result |
|--------|--------|
| **Click company row** | Expands to show all buy-signals, recommended pitch, and contact strategy |
| **Type in search box** | Filters prospects by company name, sector, or city in real-time |
| **Click priority button** | Filters dashboard to show only that priority tier |
| **Hover on KPI number** | Shows breakdown of how score was calculated |
| **Mobile view** | Collapses ticker tape; search and filters remain fully functional |

---

## 📋 Data Fields Reference

Each prospect record contains:

| Field | Type | Example | Notes |
|-------|------|---------|-------|
| **Company Name** | Text | Acme Industries Inc. | Full legal entity name |
| **Sector** | Category | Manufacturing / Automation | NAICS aligned |
| **HQ Location** | City, State | Chicago, IL | Primary office |
| **Website** | URL | https://acme.com | Clickable for research |
| **Annual Revenue** | Currency (2024) | $150–200M | Range or exact |
| **Headcount** | Integer | ~850 | Approximate current |
| **Buy-Signals** | Array | Revenue Growth, Hiring, Funding | 1–6 triggers |
| **Priority** | Enum | HIGH / MEDIUM / LOW | Computed from signals |
| **Last Updated** | Date | 2024-08-15 | Data freshness timestamp |
| **Sales Angle** | Text | Upsell new automation tier to existing customer base | Recommended pitch |
| **Contact Strategy** | Text | Target VP of Marketing; timing = Q4 budget cycle | Outreach recommendation |

---

## 🔧 Configuration & Customization

### Editing Prospect Data

The prospect database is embedded in the HTML. To add or modify prospects:

1. Open `index.html` in a text editor
2. Locate the `<script id="prospect-data">` section
3. Add/modify entries in the JSON array:

```json
{
  "id": "ACM001",
  "name": "Acme Industries Inc.",
  "sector": "Manufacturing / Automation",
  "hqCity": "Chicago",
  "hqState": "IL",
  "website": "https://acme.com",
  "revenueRange": "$150M–$200M",
  "headcount": 850,
  "buySignals": ["Revenue Growth", "Funding Round", "Hiring Push"],
  "priority": "HIGH",
  "lastUpdated": "2024-08-15",
  "salesAngle": "Upsell new automation tier to existing customer base.",
  "contactStrategy": "Target VP of Marketing; timing = Q4 budget cycle."
}
```

4. Save and refresh browser

### Styling & Theme

The dashboard uses embedded CSS. To customize:

- **Colors**: Modify CSS variables in `<style>` section (primary green: `#00a86b`)
- **Font**: Change `font-family` declaration (default: system sans-serif)
- **Layout**: Adjust grid widths and breakpoints for responsive design

### Exporting Data

Currently, no built-in export. To save filtered results:
1. Use browser DevTools → Console → `JSON.stringify(filteredProspects)`
2. Copy output and paste into Excel or Google Sheets
3. Future version will add CSV/JSON export button

---

## 🎯 Sales Workflow

### Recommended Outreach Sequence

1. **HIGH Priority** (First contact within 48h)
   - Most likely to exhibit soon
   - Budget likely approved
   - Timing: Outreach before competitor booth fills

2. **MEDIUM Priority** (Weekly nurture)
   - Building case for budget
   - Needs education on ROI
   - Timing: Monthly check-ins through Q4

3. **LOW Priority** (Quarterly review)
   - Already exhibiting or unlikely
   - Opportunity to upsell footprint
   - Timing: Q1 for next year's planning

### Pitch Template

```
Hi [Name],

We've seen [COMPANY] growing fast—especially with your recent [BUY-SIGNAL].

This year, we're hosting IMTS 2026 in Chicago. Given your expansion into [MARKET/PRODUCT], 
a booth with us could connect you with [TARGET AUDIENCE] who are actively buying.

Would a 15-min overview call make sense for your team?

Best,
[Your Name]
```

---

## 🔐 Privacy & Security

- **No external calls**: All data stored locally; no beacons or trackers
- **No cookies**: Dashboard does not store user preferences
- **Offline-first**: Works without internet connection
- **IP protection**: Trademark and business logic protected
- **Restricted access**: Internal use only; do not redistribute

---

## 🐛 Troubleshooting

### Dashboard Won't Load

**Problem**: Blank screen or error in browser console

**Solution**:
1. Ensure JavaScript is enabled
2. Clear browser cache: `Cmd+Shift+Delete` (Chrome/Firefox) or `Cmd+Option+E` (Safari)
3. Try a different browser
4. Check browser console for errors: `F12` → Console tab

### Search Not Working

**Problem**: Filter buttons or search box unresponsive

**Solution**:
1. Refresh page: `Cmd+R` (macOS) or `Ctrl+R` (Windows/Linux)
2. Check that prospect data is loaded (look for company names in table)
3. Ensure search query is not too restrictive (try "a" for all matches)

### Data Looks Stale

**Problem**: Prospect information seems outdated

**Solution**:
1. Check "Last Updated" timestamp in expanded row
2. Contact data owner to request refresh
3. Submit update via internal process (see Contributing section)

### Mobile Display Issues

**Problem**: Layout broken on phone/tablet

**Solution**:
1. Rotate device to landscape for better viewing
2. Use pinch-to-zoom to enlarge text
3. Tap + hold on row for mobile context menu
4. Use search to narrow prospects instead of scrolling

---

## 📊 Analytics & Reporting

### KPI Definitions

- **Total Prospects**: Count of all active opportunities in pipeline
- **HIGH Priority Count**: Companies with 2+ buy-signals and near-term buying intent
- **Pipeline Estimate**: Sum of potential contract values (based on company revenue * estimated booth tier)

### Metrics to Track

Track these weekly to measure pipeline health:

| Metric | Target | Formula |
|--------|--------|---------|
| **HIGH → Contacted** | 80% | Contacted HIGH prospects / Total HIGH |
| **Response Rate** | 20% | Replies received / Outreach sent |
| **Meeting Booked** | 15% | Demos scheduled / Responses |
| **Booth Conversion** | 5–10% | Exhibitors signed / Original prospects |

---

## 🤝 Contributing

### Submitting Updates

To add or correct prospect data:

1. Email raw data (CSV or JSON) to **[internal owner]**
2. Include sources for buy-signals (news link, SEC filing, job posting)
3. Data owner will merge into next release

### Reporting Bugs

Found an issue? 

1. Document the problem (screenshots, browser/OS, reproduction steps)
2. Post in internal Slack **#lead-gen** channel or email **[owner]**
3. Include console errors (`F12` → Console tab)

### Feature Requests

Ideas for the dashboard?

1. Post to **#lead-gen** channel with mockup or description
2. Owner will prioritize and add to roadmap
3. Expected turnaround: 1–2 weeks

---

## 📅 Release Notes

### Version 1.0 (Current)
- ✅ KPI dashboard with live clock
- ✅ Full-text search and priority filtering
- ✅ Clickable detail rows with buy-signal breakdown
- ✅ Bloomberg-style ticker tape
- ✅ Responsive mobile layout
- ✅ Offline-first, zero dependencies

### Planned (v1.1)
- ⏳ CSV/JSON data export
- ⏳ Bulk email template generator
- ⏳ Contact history tracking
- ⏳ Win/loss analytics dashboard

### Roadmap (v2.0+)
- 🚀 API integration with Salesforce
- 🚀 Automated web scraping for buy-signal updates
- 🚀 Predictive scoring (ML-based priority ranking)
- 🚀 Multi-event support (IMTS, Fabtech, etc.)

---

## 📞 Support & Contact

**Questions?** Reach out to:

- **Data Updates**: [internal owner email]
- **Technical Issues**: [technical lead email]
- **General Access**: Internal SharePoint group

---

## 📄 License & Terms

**Copyright © 2024 ExpInfo™**

This tool is proprietary and confidential. Intended for internal business development use only. Unauthorized reproduction, distribution, or external sharing is prohibited.

---

**Last Updated**: September 1, 2024  
**Maintained By**: BosqueCounty Team  
**Status**: ✅ Production
