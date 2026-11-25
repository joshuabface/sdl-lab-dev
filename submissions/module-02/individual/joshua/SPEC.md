# Design Specification: CivicPulse UI/UX Design System

**Project:** CivicPulse — Civic Utility & Municipal Issue Reporter  
**Mentee:** Joshua (@joshuabface)  
**Topic:** Civic Utility & Municipal Issue Reporter  
**Prototype URL:** https://stitch.google.com/projects/3165976553559818779  

## Spatial System (8pt Grid)
- Base Unit: 8px
- Micro Grid: 4px (restricted to icon alignment, badge padding, and indicator halos)
- Scale: 8px, 16px, 24px, 32px, 48px, 64px
- Responsive Viewports:
  - Desktop (1440px): 12-column grid, 64px outer margins, 24px gutters, 64px header height
  - Tablet (768px): 8-column grid, 32px outer margins, 16px gutters
  - Mobile (390px): 4-column grid, 16px outer margins, 16px gutters

## Color Architecture (60-30-10)
- 60% Canvas / Neutral:
  - Canvas Primary: `#F8FAFC`
  - Recessed Well: `#F1F5F9`
- 30% Secondary Structural:
  - Elevated Container / Cards: `#FFFFFF`
  - Headings: `#0F172A`
  - Body Text: `#334155`
  - Metadata / Secondary Labels: `#475569`
  - Dividers / Structural Borders: `#CBD5E1`
- 10% Accent Tokens & Semantic States:
  - Primary CTA / Active: `#1D4ED8` (Hover: `#1E40AF`, Active: `#1E3A8A`, Disabled: `#94A3B8`)
  - Focus Ring: `2px` solid `#1D4ED8` with `2px` `#FFFFFF` offset
  - Success Badge: `#065F46` text on `#D1FAE5` fill (`#059669` border)
  - Warning Badge: `#92400E` text on `#FEF3C7` fill (`#D97706` border)
  - Error Badge: `#991B1B` text on `#FEE2E2` fill (`#DC2626` border)
