# Module 02: Lab Submission Report

**Mentee Name:** Joshua  
**GitHub Handle:** @joshuabface  
**Project Type:** Individual  
**Branch Name:** `feat/m02-ind-joshua`  
**Assigned Topic:** Civic Utility & Municipal Issue Reporter  
**Group Partner (if Group PR):** N/A  

---

## 1. Prototype & Pull Request Links

- **Google Stitch Prototype URL:** https://stitch.google.com/projects/3165976553559818779
- **Pull Request URL (created via `gh pr create`):** https://github.com/Skillodev/sdl-lab-dev/pull/new/feat/m02-ind-joshua

---

## 2. UI/UX Engineering Audit

### 8pt Spatial Grid
- **Base Grid:** `8px` (micro-grid: `4px` for badge padding and internal alignment)
- **Layout Columns / Gutter / Margin:**
  - Desktop (`1440px`): 12 columns, 24px gutter, 64px outer margin, 64px header height
  - Tablet (`768px`): 8 columns, 16px gutter, 32px outer margin
  - Mobile (`390px`): 4 columns, 16px gutter, 16px outer margin

### 60-30-10 Color Tokens & WCAG AA Contrast Audit

| Role | Share | Hex Token | Paired Foreground/Background | Contrast Ratio | WCAG AA Pass (`>= 4.5:1`) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Dominant / Neutral (Canvas)** | 60% | `#F8FAFC` / `#F1F5F9` | `#334155` text on `#F8FAFC` | `9.89:1` | Yes (AAA) |
| **Secondary Surface (Cards)** | 30% | `#FFFFFF` | `#0F172A` text on `#FFFFFF` | `17.74:1` | Yes (AAA) |
| **Secondary Metadata** | 30% | `#475569` | `#475569` text on `#FFFFFF` | `7.58:1` | Yes (AAA) |
| **Accent / Primary CTA** | 10% | `#1D4ED8` | `#FFFFFF` text on `#1D4ED8` | `6.70:1` | Yes (AA) |
| **Semantic Success** | 10% | `#065F46` / `#D1FAE5` | `#065F46` on `#D1FAE5` | `7.12:1` | Yes (AAA) |
| **Semantic Warning** | 10% | `#92400E` / `#FEF3C7` | `#92400E` on `#FEF3C7` | `6.48:1` | Yes (AA) |
| **Semantic Error** | 10% | `#991B1B` / `#FEE2E2` | `#991B1B` on `#FEE2E2` | `6.81:1` | Yes (AA) |
| **Component Boundary / Focus** | 10% | `#475569` / `#1D4ED8` | `#1D4ED8` on `#FFFFFF` | `6.70:1` | Yes (`>= 3.0:1`) |

### 5 Interactive Component States Checklist
- [x] **Default**
- [x] **Hover**
- [x] **Focus** (visible keyboard focus ring meeting >= 3:1)
- [x] **Active / Pressed**
- [x] **Disabled**

---

## 3. Four-Page Application Overview

1. **Page 1: Live Issue Map & Community Feed (`live_issue_map_community_feed/code.html`):** Interactive GIS map canvas, issue filters, real-time civic stream.
2. **Page 2: Guided Issue Reporting Wizard (`guided_issue_reporting_wizard/code.html`):** Multi-step incident intake form with geo-location pin, photo upload, category tagging.
3. **Page 3: Issue Detail & Resolution Timeline (`issue_detail_resolution_timeline/code.html`):** Dispatch crew assignment, SLA countdown, photo evidence, and audit timeline.
4. **Page 4: Resident Dashboard & Municipal Transparency (`resident_dashboard_transparency/code.html`):** Transparency metrics, ticket resolution rate, and ward MTTR analytics.
