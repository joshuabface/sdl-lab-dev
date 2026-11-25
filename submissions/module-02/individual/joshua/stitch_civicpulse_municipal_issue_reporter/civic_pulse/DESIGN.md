---
name: Civic Pulse
colors:
  surface: '#f8f9ff'
  surface-dim: '#ccdbf3'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e6eeff'
  surface-container-high: '#dce9ff'
  surface-container-highest: '#d5e3fc'
  on-surface: '#0d1c2e'
  on-surface-variant: '#434655'
  inverse-surface: '#233144'
  inverse-on-surface: '#eaf1ff'
  outline: '#747686'
  outline-variant: '#c4c5d7'
  surface-tint: '#2151da'
  primary: '#0037b0'
  on-primary: '#ffffff'
  primary-container: '#1d4ed8'
  on-primary-container: '#cad3ff'
  inverse-primary: '#b7c4ff'
  secondary: '#565e74'
  on-secondary: '#ffffff'
  secondary-container: '#dae2fd'
  on-secondary-container: '#5c647a'
  tertiary: '#8f000b'
  on-tertiary: '#ffffff'
  tertiary-container: '#bb0112'
  on-tertiary-container: '#ffc7c1'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dce1ff'
  primary-fixed-dim: '#b7c4ff'
  on-primary-fixed: '#001551'
  on-primary-fixed-variant: '#0039b5'
  secondary-fixed: '#dae2fd'
  secondary-fixed-dim: '#bec6e0'
  on-secondary-fixed: '#131b2e'
  on-secondary-fixed-variant: '#3f465c'
  tertiary-fixed: '#ffdad6'
  tertiary-fixed-dim: '#ffb4ab'
  on-tertiary-fixed: '#410002'
  on-tertiary-fixed-variant: '#93000b'
  background: '#f8f9ff'
  on-background: '#0d1c2e'
  surface-variant: '#d5e3fc'
typography:
  headline-xl:
    fontFamily: Inter
    fontSize: 36px
    fontWeight: '700'
    lineHeight: 44px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Inter
    fontSize: 30px
    fontWeight: '600'
    lineHeight: 38px
    letterSpacing: -0.015em
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Inter
    fontSize: 22px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-lg:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '600'
    lineHeight: 14px
    letterSpacing: 0.04em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 1.5rem
  gutter-mobile: 1rem
  margin: 2rem
  margin-mobile: 1rem
  space-xs: 0.5rem
  space-sm: 1rem
  space-md: 1.5rem
  space-lg: 2rem
  space-xl: 3rem
---

## Brand & Style

This design system delivers a civic utility infrastructure designed for municipal service tracking, public works reporting, and resident communication. The aesthetic fuses **Institutional Precision** with **Public Sector Modernism**—eschewing decorative excess in favor of legibility, immediacy, and trust.

### Brand Personality & Emotional Objectives
- **Authoritative & Trustworthy:** Communicates governmental accountability and institutional stability without feeling monolithic or bureaucratic.
- **Utilitarian & Transparent:** Prioritizes immediate readability and rapid operational comprehension in critical situations (e.g., utility failures, hazards, road obstructions).
- **Equitable & Inclusive:** Built around absolute accessibility, predictable interaction zones, and uncompromising WCAG AA contrast standards.

### Aesthetic Paradigm: Modern Institutional
The visual style relies on crisp structural hierarchy, defined dividing planes, and deliberate tonal surfaces. Rather than floating glassmorphic or playful neo-brutalist tropes, the interface uses clean white planar surfaces elevated slightly over cool slate canvases, framed by balanced dividers.

## Colors

The 60-30-10 palette distribution anchors municipal reports in visual calm while directing user attention unambiguously to critical alerts and actionable items.

### Palette Architecture
- **60% Base / Canvas Foundations:** 
  - Application Canvas: `Slate 50` (`#F8FAFC`)
  - Recessed Wells, Map Frame Backdrops, and Inactive Panels: `Slate 100` (`#F1F5F9`)
- **30% Structural Elements & Typography:**
  - Elevated Container / Header Backgrounds: `Pure White` (`#FFFFFF`)
  - Primary Structural Headings: `Slate 900` (`#0F172A`)
  - Body Text: `Slate 700` (`#334155`)
  - Metadata & Secondary Labels: `Slate 600` (`#475569`)
  - Structural Borders & Hairline Dividers: `Slate 300` (`#CBD5E1`)
- **10% Brand Accent & Interactive States:**
  - Primary Action / Civic Blue: `Civic Blue 700` (`#1D4ED8`)
  - Hover Action: `#1E40AF`
  - Pressed Action: `#1E3A8A`
  - Accessibility Focus Ring: 2px solid `#1D4ED8` offset by 2px `#FFFFFF`

### Semantic Systems
- **Success (Resolved / Verified):** Text `#065F46`, Fill `#D1FAE5`, Border `#059669`.
- **Warning (Under Review / Scheduled):** Text `#92400E`, Fill `#FEF3C7`, Border `#D97706`.
- **Hazard / Critical (Immediate Threat / Emergency Outage):** Text `#991B1B`, Fill `#FEE2E2`, Border `#DC2626`.

## Typography

The type hierarchy utilizes `Inter` across all structural roles to maximize character discrimination and optical clarity in high-stress reporting environments.

### Rules & Hierarchy
- **Strict WCAG Compliance:** All typography pairings must strictly satisfy AA (4.5:1 for normal text, 3:1 for large text) against canvas and card surfaces.
- **Numbers & Metrics:** Tabular figures (`tnum`) must be enforced for ticket tracking numbers, geographic coordinates, and time-lapse duration values.
- **Headings:** Always set in `Slate 900` (`#0F172A`) to ensure structural clarity across incident logs.
- **Metadata:** Rendered using `label-md` or `body-sm` in `Slate 600` (`#475569`).

## Layout & Spacing

Layout adheres to a strict 8pt spatial grid: `8px`, `16px`, `24px`, `32px`, `48px`, `64px`. A controlled 4px micro-grid exception is reserved solely for compact indicator badges, micro-icons, and inline status dots.

### Grid & Breakpoints
- **Mobile (0 – 767px):** 4-column fluid layout. Canvas margin: `16px` (`margin-mobile`), gutter: `16px` (`gutter-mobile`). Incident intake workflows compress into full-width linear step stacks.
- **Tablet (768px – 1023px):** 8-column layout. Margin: `24px`, gutter: `24px`. Maps and ticket streams split into 5/3 column pairings.
- **Desktop (1024px+):** 12-column fixed/fluid hybrid grid capped at `1280px` max-width. Margin: `32px` (`margin`), gutter: `24px` (`gutter`). Master-detail layouts split into side-panel ticket feeds and persistent interactive GIS mapping canvases.

### Spacing Tokens Application
- `space-xs` (8px): Internal gap between icon and text; inline tag padding.
- `space-sm` (16px): Compact card internal padding; field stack gaps.
- `space-md` (24px): Standard card container padding; distance between fieldsets.
- `space-lg` (32px): Distance between unrelated UI modules or distinct sections.
- `space-xl` (48px): Top-level layout segment spacing and hero section margins.

## Elevation & Depth

Visual separation relies on distinct surface color tiers and low-contrast perimeter definition rather than heavy drop shadows.

### Surface Tiers
- **Tier 0 (Recessed Background):** `Slate 100` (`#F1F5F9`) used behind embedded mapping controls, audit trails, and filters.
- **Tier 1 (Base Canvas):** `Slate 50` (`#F8FAFC`) underpinning global viewports.
- **Tier 2 (Elevated Plane):** `Pure White` (`#FFFFFF`) card surfaces, list containers, and standard dialogs, bordered with a 1px solid `Slate 300` (`#CBD5E1`) perimeter stroke.
- **Tier 3 (Floating Overlays):** Used for navigation bars, contextual tooltips, and modal sheets. Supported by a crisp 1px border (`#CBD5E1`) and an ambient, low-contrast shadow: `0 4px 6px -1px rgba(15, 23, 42, 0.07), 0 2px 4px -2px rgba(15, 23, 42, 0.05)`.

## Shapes

The design system adopts a restrained **Soft (`1`)** shape language (`4px` base radius), reflecting technical discipline and spatial reliability.

### Corner Radius System
- **Base Components (`rounded`, 4px):** Form inputs, buttons, status tags, table cell highlights, and interactive toggles.
- **Large Components (`rounded-lg`, 8px):** Issue cards, interactive map containers, data modals, and alert callouts.
- **Structural Containers (`rounded-xl`, 12px):** Top-level dashboard cards and global navigation sheets.
- **Exception (Fully Rounded / Pill):** Reserved exclusively for live circular status indicators, geolocation breadcrumb markers, and compact count badges.

## Components

### Buttons
- **Primary:** Background `#1D4ED8`, text `#FFFFFF`, radius `4px`, height `40px` (desktop) or `48px` (touch targets). Hover: `#1E40AF`. Active: `#1E3A8A`. Focus ring: 2px offset with `#1D4ED8`.
- **Secondary:** Background `#FFFFFF`, 1px border `#CBD5E1`, text `#334155`. Hover: background `#F8FAFC`, border `#0F172A`.
- **Destructive / Hazard Report:** Background `#DC2626`, text `#FFFFFF`. Hover: `#B91C1C`.

### Form Inputs & Selectors
- **Input Fields:** Pure White background, 1px border `#CBD5E1`, text `#0F172A`, placeholder `#64748B`. Focused state: border `#1D4ED8` with 2px outer outline.
- **Validation Messages:** Positioned 4px beneath the field in `body-sm` using semantic critical (`#991B1B`) or success (`#065F46`).
- **Checkboxes & Radios:** 16px dimensions aligned to the 8pt grid with 8px label clearance. Checked fill `#1D4ED8` with high-contrast `#FFFFFF` glyph.

### Status Chips & Badges
- **Dimensions:** Strict 24px height, horizontal padding of 8px (`space-xs`), font `label-sm`.
- **States:**
  - Open / Reported: Fill `#FEF3C7`, text `#92400E`, border 1px `#D97706`.
  - In Progress: Fill `#DBEAFE`, text `#1E40AF`, border 1px `#3B82F6`.
  - Hazard / Urgent: Fill `#FEE2E2`, text `#991B1B`, border 1px `#DC2626`.
  - Resolved: Fill `#D1FAE5`, text `#065F46`, border 1px `#059669`.

### Issue & Incident Cards
- **Geometry:** Elevated White container, 1px border `#CBD5E1`, 8px radius (`rounded-lg`), internal padding of 16px (`space-sm`) or 24px (`space-md`).
- **Layout:** Header zone with tracking ID (tabular numbers) and category badge; middle zone with incident description (`Slate 700`); footer zone with geostamp, timestamp, and status.

### Civic Utility Specific: Map Callout & Incident Pin
- **Map Incident Pin:** 32px teardrop or circular target with 2px white halo and centered category icon. Color-coded according to semantic severity (Blue, Amber, Red).
- **Map Floating Sheet:** Docked bottom on mobile devices (90% viewport width) or anchored as an offset pane on desktop (`Slate 50` background, 8px radius, subtle border).