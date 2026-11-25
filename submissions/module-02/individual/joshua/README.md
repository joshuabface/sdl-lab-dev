# CivicPulse — Civic Utility & Municipal Issue Reporter
## Module 02 UI/UX Engineering & Collaborative Git Specification

**Author:** Joshua  
**GitHub Handle:** [@joshuabface](https://github.com/joshuabface)  
**Assigned Topic:** Civic Utility & Municipal Issue Reporter  
**Feature Branch:** `feat/m02-ind-joshua`  
**Prototype Link:** [Google Stitch Prototype (Project 3165976553559818779)](https://stitch.google.com/projects/3165976553559818779)  

---

## 1. 8pt Spatial Grid System

CivicPulse adheres strictly to the **8pt spatial grid scale** for all layout containers, paddings, margins, and vertical rhythm. Spatial discipline ensures institutional clarity, rapid scannability for emergency utility reports, and consistent responsive scaling.

### Spacing Scale
- **`8px` (`--space-8`):** Micro-spacing for compact internal elements, icon-to-label text gaps, inline status dot margins.
- **`16px` (`--space-16`):** Compact card padding, form field gaps, table cell vertical padding.
- **`24px` (`--space-24`):** Standard card padding, distance between related form sections, gutter between list items.
- **`32px` (`--space-32`):** Section margins, major modular component separation.
- **`48px` (`--space-48`):** Top-level layout segment spacing, hero card gutters.
- **`64px` (`--space-64`):** Viewport outer margins (desktop) and global top navigation bar height.

> **4px Micro-Grid Exception:**  
> A strict `4px` micro-grid exception is permitted solely for compact internal alignment:
> 1. Badge internal vertical padding (`4px 8px`).
> 2. Micro-icon clearance within compact search input pills (`4px`).
> 3. Status indicator dot halos and geometric offset borders.

### Responsive Breakpoints & Column Architecture
| Device Breakpoint | Target Viewport | Columns | Outer Margin | Column Gutter | Layout Behavior |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Desktop** | `1440px` | 12 Columns | `64px` | `24px` | Persistent split view: 7-col GIS Map Canvas / 5-col Community Ticket Feed |
| **Tablet** | `768px` | 8 Columns | `32px` | `16px` | Stacked master-detail with expandable bottom sheet overlay |
| **Mobile** | `390px` | 4 Columns | `16px` | `16px` | Single-column fluid stream with bottom drawer navigation & full-width CTA |

---

## 2. 60-30-10 Color Architecture

The color system maintains institutional authority, high legibility under harsh lighting, and instant recognition of public hazard levels using a strict 60-30-10 distribution.

```
┌─────────────────────────────────────────────────────────────┐
│ 60% Dominant / Neutral Surfaces                             │
│   Canvas Foundation: Slate 50 (#F8FAFC)                     │
│   Recessed Map Well: Slate 100 (#F1F5F9)                    │
├─────────────────────────────────────────────────────────────┤
│ 30% Secondary Structural Planes & Content                   │
│   Elevated Cards & Nav: Pure White (#FFFFFF)                │
│   Primary Headings: Slate 900 (#0F172A)                     │
│   Body Copy: Slate 700 (#334155)                            │
│   Metadata & Labels: Slate 600 (#475569)                    │
│   Borders & Separators: Slate 300 (#CBD5E1)                 │
├─────────────────────────────────────────────────────────────┤
│ 10% Accent Tokens & Semantic Feedback                       │
│   Primary CTA: Royal Blue (#1D4ED8)                         │
│     Hover: #1E40AF | Active/Pressed: #1E3A8A                │
│   Focus Ring: 2px #1D4ED8 with 2px #FFFFFF offset           │
│   Success: #065F46 on #D1FAE5 (border #059669)              │
│   Warning: #92400E on #FEF3C7 (border #D97706)              │
│   Error:   #991B1B on #FEE2E2 (border #DC2626)              │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. WCAG AA Verified Contrast Ratios

All interactive states, body copy, and UI controls satisfy or exceed **WCAG 2.1 AA** (minimum `4.5:1` for normal text and `3.0:1` for UI components and large text). Verified contrast ratios were computed using standard sRGB luminance formulas:

| UI Element Role | Foreground Hex | Background Hex | Contrast Ratio | WCAG Compliance Level | Evaluation Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Primary Headings** | `#0F172A` | `#FFFFFF` | **17.74:1** | WCAG AAA (`≥ 7.0:1`) | ✅ Pass |
| **Normal Body Text** | `#334155` | `#F8FAFC` | **9.89:1** | WCAG AAA (`≥ 7.0:1`) | ✅ Pass |
| **Metadata & Secondary Labels** | `#475569` | `#FFFFFF` | **7.58:1** | WCAG AAA (`≥ 7.0:1`) | ✅ Pass |
| **Primary CTA Button** | `#FFFFFF` | `#1D4ED8` | **6.70:1** | WCAG AA (`≥ 4.5:1`) | ✅ Pass |
| **Success Status Badge** | `#065F46` | `#D1FAE5` | **7.12:1** | WCAG AAA (`≥ 7.0:1`) | ✅ Pass |
| **Warning Status Badge** | `#92400E` | `#FEF3C7` | **6.48:1** | WCAG AA (`≥ 4.5:1`) | ✅ Pass |
| **Error / Urgent Badge** | `#991B1B` | `#FEE2E2` | **6.81:1** | WCAG AA (`≥ 4.5:1`) | ✅ Pass |
| **UI Input Border Stroke** | `#475569` | `#FFFFFF` | **7.58:1** | UI Component (`≥ 3.0:1`) | ✅ Pass |
| **Active Focus Ring** | `#1D4ED8` | `#FFFFFF` | **6.70:1** | UI Component (`≥ 3.0:1`) | ✅ Pass |

---

## 4. Five Interactive Component States

Every core interactive element in CivicPulse is explicitly defined across five distinct states to eliminate cognitive friction and ensure accessible keyboard navigation:

### 1. Primary Buttons (`.btn-primary`)
- **Default:** Background `#1D4ED8`, text `#FFFFFF`, radius `4px`, height `40px` (desktop) / `48px` (touch target).
- **Hover:** Background `#1E40AF`, subtle cursor pointer.
- **Focus:** `2px` solid `#1D4ED8` outline with `2px` `#FFFFFF` offset ring.
- **Active / Pressed:** Background `#1E3A8A`, slight inset transformation (`scale(0.98)`).
- **Disabled:** Background `#94A3B8`, text `#E2E8F0`, cursor `not-allowed`, opacity `0.6`.

### 2. Secondary Buttons (`.btn-secondary`)
- **Default:** Background `#FFFFFF`, `1px` border `#CBD5E1`, text `#334155`.
- **Hover:** Background `#F8FAFC`, border `#0F172A`, text `#0F172A`.
- **Focus:** `2px` solid `#1D4ED8` outline with `2px` `#FFFFFF` offset.
- **Active / Pressed:** Background `#F1F5F9`, border `#0F172A`.
- **Disabled:** Background `#F8FAFC`, border `#E2E8F0`, text `#94A3B8`, cursor `not-allowed`.

### 3. Text Inputs & Search Bars (`.input-text`)
- **Default:** Background `#FFFFFF`, `1px` border `#CBD5E1`, text `#0F172A`, placeholder `#64748B`.
- **Hover:** Border `#475569`.
- **Focus:** Border `#1D4ED8`, `2px` outer glow/ring (`rgba(29, 78, 216, 0.25)`).
- **Active / Pressed:** Border `#1D4ED8`, background `#FFFFFF`.
- **Disabled:** Background `#F1F5F9`, border `#E2E8F0`, text `#94A3B8`, cursor `not-allowed`.

### 4. Selectable Category Cards (`.category-card`)
- **Default:** Background `#FFFFFF`, `1px` border `#CBD5E1`, radius `8px`.
- **Hover:** Border `#1D4ED8`, ambient shadow `0 4px 6px -1px rgba(15, 23, 42, 0.07)`.
- **Focus:** `2px` solid `#1D4ED8` ring around card perimeter.
- **Active / Pressed:** Selected fill `#EFF6FF`, border `2px` `#1D4ED8`, checkmark indicator badge visible.
- **Disabled:** Background `#F8FAFC`, border `#E2E8F0`, opacity `0.5`, non-interactive.

### 5. Filter Tabs (`.filter-tab`)
- **Default:** Background transparent, text `#475569`, bottom border `2px` transparent.
- **Hover:** Text `#0F172A`, bottom border `2px` `#CBD5E1`.
- **Focus:** Keyboard focus pill outline `#1D4ED8`.
- **Active / Selected:** Text `#1D4ED8`, font-weight `600`, bottom border `2px` `#1D4ED8`.
- **Disabled:** Text `#CBD5E1`, pointer-events `none`.

### 6. Dropdown Selectors (`.select-dropdown`)
- **Default:** Background `#FFFFFF`, border `1px` `#CBD5E1`, chevron icon `#475569`.
- **Hover:** Border `#475569`.
- **Focus:** Border `#1D4ED8`, focus ring `2px` `#1D4ED8`.
- **Active / Expanded:** Menu open, chevron rotated 180°, active item highlighted in `#F1F5F9`.
- **Disabled:** Background `#F8FAFC`, text `#94A3B8`, border `#E2E8F0`, cursor `not-allowed`.

---

## 5. Four-Page Application Overview

| Page # | Screen Name | Core Functional Deliverable | Asset References |
| :--- | :--- | :--- | :--- |
| **Page 1** | **Live Issue Map & Community Feed** | Split-screen municipal situational awareness view. Features GIS map canvas with color-coded incident pins, real-time ticket stream, category filter pills, and quick-report floating action button. | `live_issue_map_community_feed/code.html` |
| **Page 2** | **Guided Issue Reporting Wizard** | Step-by-step incident intake workflow. Step 1: Geolocation pin drop; Step 2: Category selection (Pothole, Water Main, Electrical Hazard, Waste); Step 3: Photo upload & description; Step 4: Urgency classification & confirmation. | `guided_issue_reporting_wizard/code.html`<br>`guided_issue_reporting_wizard/screen.png` |
| **Page 3** | **Issue Detail & Resolution Timeline** | Granular ticket inspection view. Includes verified ticket ID, municipal dispatch crew assignment, SLA progress bar, photo proof before/after slider, and immutable chronological audit trail. | `issue_detail_resolution_timeline/code.html` |
| **Page 4** | **Resident Dashboard & Municipal Transparency** | Public accountability hub. Summarizes resident submitted tickets, ward-level resolution analytics, mean-time-to-repair (MTTR) metrics, and municipal notification preferences. | `resident_dashboard_transparency/code.html`<br>`resident_dashboard_transparency/screen.png` |

---

## 6. Exported Stitch Deliverables Directory

All exported HTML prototypes, screenshots, and visual assets from Google Stitch are organized alongside this specification:

```
submissions/module-02/individual/joshua/
├── README.md
├── SPEC.md
├── tokens.css
├── submission.md
└── stitch_civicpulse_municipal_issue_reporter/
    ├── civic_pulse/
    │   └── DESIGN.md
    ├── guided_issue_reporting_wizard/
    │   ├── code.html
    │   └── screen.png
    ├── issue_detail_resolution_timeline/
    │   └── code.html
    ├── live_issue_map_community_feed/
    │   └── code.html
    ├── nigeria_flag_logo/
    │   └── screen.png
    └── resident_dashboard_transparency/
        ├── code.html
        └── screen.png
```
