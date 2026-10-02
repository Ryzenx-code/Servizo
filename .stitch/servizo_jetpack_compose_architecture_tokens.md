# Servizo — Production Jetpack Compose Design System & Specifications
**Brand Anchor Logo:** `{{DATA:IMAGE:IMAGE_13}}`  
**Primary Accent:** `#0d5cde` (Electric Royal Blue) | **Secondary:** `#10b981` (Emerald Green) | **Dark Brand:** `#0a2540` (Navy Slate)

---

## 1. Design Token Matrix (Jetpack Compose Tokens)

### 1.1 Color Tokens (`Color.kt`)
```kotlin
package com.servizo.ui.theme

import androidx.compose.ui.graphics.Color

val ServizoPrimary = Color(0xFF0D5CDE)          // Main interactive, primary buttons
val ServizoPrimaryContainer = Color(0xFFEBF2FD) // Tinted chips, active tabs
val ServizoSecondary = Color(0xFF10B981)        // Growth, success, reminders
val ServizoSecondaryContainer = Color(0xFFE8FAF0)
val ServizoNavy = Color(0xFF0A2540)             // Headers, deep branding
val ServizoSurface = Color(0xFFF7F9FB)          // Android window background
val ServizoSurfaceCard = Color(0xFFFFFFFF)      // Cards, bottom sheets
val ServizoSurfaceHigh = Color(0xFFF1F4F9)      // Sub-containers, input fields
val ServizoTextPrimary = Color(0xFF1E293B)      // Slate 800 - high contrast
val ServizoTextSecondary = Color(0xFF64748B)    // Slate 500 - meta info
val ServizoBorder = Color(0xFFE2E8F0)           // Slate 200 - hairline borders
val ServizoDestructive = Color(0xFFEF4444)       // Red 500 - critical actions
val ServizoDestructiveContainer = Color(0xFFFEE2E2)
val ServizoWarning = Color(0xFFF59E0B)           // Amber 500 - AMC/overdue badge
val ServizoWarningContainer = Color(0xFFFEF3C7)
```

### 1.2 Spacing & Radii (`Dimensions.kt`)
- **Spacing Units:** `Grid4 = 4.dp`, `Grid8 = 8.dp`, `Grid12 = 12.dp`, `Grid16 = 16.dp`, `Grid20 = 20.dp`, `Grid24 = 24.dp`, `Grid32 = 32.dp`
- **Corner Radii:**
  - `CardRadius = 14.dp` (All standard customer, record, and metric cards)
  - `ButtonRadius = 12.dp` (Touch targets with height `52.dp` for primary, `44.dp` for secondary)
  - `InputRadius = 10.dp` (Outlined text fields with `56.dp` standard height)
  - `ChipRadius = 8.dp` (Status badges, tags, and category chips)
  - `BottomSheetTopRadius = 24.dp` (Modal presentation surface)

### 1.3 Typography Scale (Plus Jakarta Sans)
- `DisplayLarge`: 28sp / Bold (Splash, Key Milestone counts)
- `HeadlineMedium`: 20sp / Bold (App bar titles, customer names)
- `TitleMedium`: 16sp / SemiBold (Card headers, form labels)
- `BodyMedium`: 14sp / Regular (Details, address, transaction descriptions)
- `LabelSmall`: 11sp / SemiBold (Badge labels, metadata timestamps)

---

## 2. Multi-Screen Flow Inventory (18 Core Surfaces)

1. **Splash & Welcome:** Full-bleed brand gradient, centered `{{DATA:IMAGE:IMAGE_13}}`, animated entrance.
2. **Setup - Business Info:** Company name, owner details, water purifier / appliance domain tagger.
3. **Setup - Location & Map Pin:** Geolocation picker, city/locality bounds with service radius.
4. **Setup - 4-Digit Security PIN:** Numpad entry, biometrics toggle with quick haptic feedback.
5. **Setup - Completion & Launch:** Verified credentials checklist, instant database initialization.
6. **Executive Dashboard:** Live metrics (Today's Due, Revenue INR, Overdue), offline banner, action bar.
7. **Smart Service Reminders:** Categorized overdue vs upcoming AMC schedules, 1-tap WhatsApp trigger.
8. **Customer Directory:** Filterable search, alphabetical group index, dynamic count chips.
9. **Filter & Sort Bottom Sheet:** Multi-select criteria (AMC Active, TDS Tested, Expiring in 7 Days).
10. **Add New Customer Form:** Progressive sections, Indian phone contact picker integration, validation inline.
11. **Customer Profile (Rajesh Sharma):** TDS metrics, machine model, service timeline, direct dialer handoff.
12. **Edit Customer Profile:** Non-destructive image replacement, address updater, safe cancellation.
13. **Service Records Timeline:** Chronological list, complaint type, parts replaced, INR invoice badge.
14. **Add Service Record:** Date picker, complaint selector, parts replacement cost calculator, technician assignment.
15. **WhatsApp-Style Voice Note Dialog:** Audio visualizer wave, recording timer, instant play/pause & discard.
16. **Technician Directory & Analytics:** Active load indicators, skill tags, performance rating stars.
17. **Technician Profile:** Contact actions, service completion rate, current route inspection.
18. **Settings & Backup:** Grouped preferences, AES-256 `.servizo` backup export, danger zone factory reset modal.

---

## 3. Ergonomics & Android Safe Area Compliance Checklist
- **System Navigation Insets:** Every primary action button (e.g. Save, Record, Call) uses `WindowInsets.navigationBars.asPaddingValues()` with a minimum bottom offset of `16.dp` above system gesture pills or 3-button navbars.
- **Touch Target Integrity:** Every clickable icon or row guarantees a minimum bounding box of `48.dp × 48.dp`.
- **Keyboard IME Collision:** Add customer & Add service record forms utilize `Modifier.imePadding()` wrapped inside `rememberScrollState()`. Primary action buttons remain sticky above the virtual keyboard.
- **Offline & Empty States:** Lightweight local cache indicator banner with instant offline queuing status.
