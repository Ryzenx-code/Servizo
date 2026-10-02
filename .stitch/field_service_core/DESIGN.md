---
name: Field Service Core
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#424654'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#737686'
  outline-variant: '#c3c6d7'
  surface-tint: '#0055d3'
  primary: '#0046b0'
  on-primary: '#ffffff'
  primary-container: '#0d5cde'
  on-primary-container: '#dbe2ff'
  inverse-primary: '#b2c5ff'
  secondary: '#475f86'
  on-secondary: '#ffffff'
  secondary-container: '#b7d0fd'
  on-secondary-container: '#40597f'
  tertiary: '#00593c'
  on-tertiary: '#ffffff'
  tertiary-container: '#00744f'
  on-tertiary-container: '#70fcbf'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2ff'
  primary-fixed-dim: '#b2c5ff'
  on-primary-fixed: '#001848'
  on-primary-fixed-variant: '#0040a2'
  secondary-fixed: '#d5e3ff'
  secondary-fixed-dim: '#afc7f4'
  on-secondary-fixed: '#001b3c'
  on-secondary-fixed-variant: '#2f476d'
  tertiary-fixed: '#6ffbbe'
  tertiary-fixed-dim: '#4edea3'
  on-tertiary-fixed: '#002113'
  on-tertiary-fixed-variant: '#005236'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '800'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 26px
    fontWeight: '800'
    lineHeight: 34px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 22px
    fontWeight: '700'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '700'
    lineHeight: 24px
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '500'
    lineHeight: 24px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 10px
    fontWeight: '700'
    lineHeight: 14px
    letterSpacing: 0.04em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1rem
  margin: 1rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system is tailored for high-frequency service operations, client scheduling, and technician workflow orchestration on Android. The aesthetic blends Corporate Modern reliability with crisp tactile digital surfaces, projecting authority, speed, and trust. 

Designed for independent trade specialists, field technicians, and operations managers working under varying lighting conditions, the interface prioritizes immediate legibility, high contrast, and rapid one-handed tap navigation. The emotional tone evokes operational clarity, verified precision, and calm control amidst chaotic schedules. Visual elements derive their identity directly from dynamic curved service ribbons, rounded industrial tool silhouettes, and affirmative task completion cues.

## Colors

The palette establishes a clear operational hierarchy optimized for daylight readability:

- **Primary Interactive (#0D5CDE / #0066FF):** The high-visibility cobalt tone reserved strictly for primary calls-to-action, key state toggles, active bottom navigation indicators, and direct transactional commands.
- **Authority / Navigation Chrome (#08264A):** Deep navy used for prominent top app bars, primary header typography, high-level status summary containers, and foundational branding marks.
- **Success & Verification (#10B981 / #059669):** Sourced directly from the checkmark glyph and ribbon accent, applied to verified customer badges, completed job tags, live calendar schedules, and positive balance states.
- **Neutral & Canvas (#F8FAFC, #F1F5F9, #E2E8F0, #0F172A):** Pure `#FFFFFF` for elevated interactive cards, resting on a dual-tier cool canvas backdrop (`#F8FAFC` base, `#F1F5F9` structural wells), framed by subtle `#E2E8F0` micro-borders to maintain structural contrast without heavy visual noise. High-contrast slate `#0F172A` acts as primary body text for AA/AAA accessibility compliance.

## Typography

Typographic scale is powered by Plus Jakarta Sans to deliver an approachable yet geometric, highly legible technical structure. Display and headline weights leverage bold geometric apertures that mirror the circular curves of the app mark. 

Body copy favors weights 400 and 500 with generous x-heights suited for reading customer addresses, tool checklists, and invoice line items outdoors. Labels use tighter tracking and elevated semi-bold/bold weights to guarantee visual recognition on status tags, timestamps, and compact data badges.

## Layout & Spacing

Layout architecture follows a strict 8dp spatial rhythm aligned with Android Material guidelines:

- **Mobile Grid (up to 599dp):** Single-column layout with 16dp outer screen margins (`margin: 1rem`) and 16dp element gutters (`gutter: 1rem`). Bottom navigation and Floating Action Buttons (FABs) adhere strictly to Android system safe insets and gesture zones.
- **Tablet / Large Foldable Grid (600dp+):** Expands to a master-detail split (list view at 360dp, details fluid) or an 8-column layout with 24dp margins and 16dp gutters.
- **Touch Target Integrity:** Every interactive node—from list items to icon actions—enforces a minimum bounding box of 48×48dp, even when the visible glyph or chip is visually more compact.

## Elevation & Depth

Visual depth is achieved through layered tonal surfaces combined with soft, tinted ambient occlusion shadows:

- **Level 0 (Flat Canvas):** `#F8FAFC` base application background.
- **Level 1 (Card & Content Blocks):** `#FFFFFF` surfaces paired with a crisp 1px stroke in `#E2E8F0` and an ambient shadow: `box-shadow: 0 1px 3px 0 rgba(8, 38, 74, 0.04), 0 1px 2px -1px rgba(8, 38, 74, 0.03)`.
- **Level 2 (Active/Hover/Pressed Cards):** Lifted cards introduce subtle depth with `box-shadow: 0 4px 6px -1px rgba(8, 38, 74, 0.07), 0 2px 4px -2px rgba(8, 38, 74, 0.05)`.
- **Level 3 (Bottom Navigation & App Bar Chrome):** Fixed navigation surfaces use pure `#FFFFFF` with an upward soft shadow (`0 -2px 8px rgba(8, 38, 74, 0.05)`) or deep navy chrome (`#08264A`) for context headers.
- **Level 4 (Floating Action Buttons & Bottom Sheets):** Elevated utilities use `box-shadow: 0 10px 15px -3px rgba(13, 92, 222, 0.2), 0 4px 6px -4px rgba(13, 92, 222, 0.15)`.

## Shapes

The shape system expresses the fluid, continuous ribbons of the brand mark, counterbalanced with structured ergonomics:

- **Small Interactive Targets (Inputs, Buttons, Chips):** Use 10px to 12px radii (`rounded-md` to `rounded-lg`) for a friendly, modern grip.
- **Primary Content Cards & Task Modules:** Use 16px to 20px radii (`rounded-lg` to `rounded-xl`) to establish distinct visual containment for scheduling and service jobs.
- **Modals, Floating Sheets, and Action Badges:** Employ 24px (`rounded-2xl`) for top sheet corners, while status pill badges leverage full 9999px pills.

## Components

### Buttons
- **Primary Action:** Solid electric cobalt `#0D5CDE` fill, white text, 48dp minimum height, 12px border radius, semi-bold 14px typography. Includes a 12% darkened state on press.
- **Secondary Action:** Light cobalt tint `#EFF6FF` with `#0D5CDE` label and borderless contour for secondary steps.
- **Authoritative Action:** Deep navy `#08264A` fill for critical checkout, schedule submission, or high-tier administrative triggers.

### Chips & Badges
- **Status Pills:** 28dp height, 9999px pill radius. Verified/Active states feature a soft emerald tint background (`#ECFDF5`), deep emerald text (`#047857`), and a solid `#10B981` leading dot or checkmark.
- **Filter Chips:** 36dp height, white surface with `#E2E8F0` border, transitions to `#0D5CDE` surface with white text when selected.

### Input Fields
- Minimum 56dp height to accommodate glove or field use. 12px corner radius, background `#F8FAFC`, border `#E2E8F0`. Focus state shifts background to pure white, surrounded by a 2px active ring in `#0D5CDE`. Helper and error labels sit 4px beneath the container.

### Cards & Service Tiles
- Pure `#FFFFFF` background, 16px padding, 16px radius, enclosed in a 1px `#E2E8F0` border. Headers feature a left-aligned status badge alongside deep navy authority text (`#08264A`). Service action shortcuts sit docked at the bottom with explicit touch separation.

### Checkboxes & Radio Controls
- Minimum 24dp visual box with a 48dp hit zone. Active fill is `#0D5CDE` or `#10B981` (for completion status), holding a bold white checkmark icon.

### Service-Specific Elements
- **Job Status Indicator:** A vertical 4px left-border accent matching status color (emerald for completed, cobalt for scheduled, amber for pending) on white card modules.
- **Bottom App Bar / FAB:** Deep navy chrome or pure white with an elevated `#0D5CDE` quick-action circular FAB (56×56dp) for instant job and appointment creation.