---
name: app-design
description: Strict application design guidelines, UX/UI rules, ergonomic principles, and visual standards to craft clean, modern, dense, solid, and responsive interfaces.
---

# 🎨 App Design Skill

This skill provides a set of strict guidelines and design standards to build modern, professional, ergonomic, and clutter-free application interfaces (Web, SaaS, Mobile, Dashboards).

---

## 🚫 Golden Rules & Strict Constraints (Non-Negotiable)

These rules must be systematically applied by the agent when designing and generating UI code (React, Vue, Svelte, HTML/CSS, Tailwind, etc.):

### 1. 🎨 Strict Color Palette Adherence
- **Rule:** Use **exclusively** the color palette provided or requested by the user.
- **Prohibition:** Never invent any new accent color or unspecified secondary tint.
- **Structural Neutrals:** For backgrounds, texts, and borders, stick strictly to sober neutrals (pure white, deep black, shades of gray/slate/zinc).
- **Semantic State Colors:** Restrict red (error/danger), green (success), and amber (warning) to subtle status indicators (badges, alert texts), without tinting the entire interface.

### 2. ⬛ Zero Gradients & Zero Transparency
- **Rule:** Use **100% solid color surfaces** (*Solid Surfaces / Flat Clean Design*).
- **Strict Prohibitions:**
  - No gradients (`linear-gradient`, `radial-gradient`, `bg-gradient-to-...`).
  - No transparency or frosted glass effects (`backdrop-blur`, `backdrop-filter`, awkward `bg-opacity-*`, glassmorphism).
  - No translucent text or semi-invisible elements that compromise contrast and readability.

### 3. 📏 Subtle & Minimal Borders
- **Rule:** Separate content blocks primarily through surface background contrast (*surface separation*) or via a **subtle 1px border**.
- **Prohibition:**
  - No thick borders (`2px`, `3px`, etc.) or aggressive black outlines around every container.
  - No heavy or dark drop-shadows (*heavy shadows*). If a shadow is required for a modal or dropdown, use a very soft, diffused shadow (`shadow-sm` or discreet `shadow-md`).

### 4. 🏹 No Parasite / Redundant Arrows
- **Rule:** Buttons and cards must display clear, direct labels without superfluous decorative icons.
- **Prohibition:** Do not attach directional arrows (`→`, `ChevronRight`, `ArrowRight`, `->`) systematically to action buttons or navigation cards, unless the action is explicitly pagination (*Next / Previous*) or a back navigation.

### 5. 🚫 Zero Fake Reviews & Zero Cliché Dummy Content
- **Rule:** The interface must be product/utility-focused with realistic domain data.
- **Prohibition:**
  - Never insert fake testimonial cards ("*John Doe, 5 stars: Great tool!*").
  - Avoid generic *Lorem Ipsum*: use realistic, domain-specific terminology relevant to the application.

### 6. 📐 Optimal Space Density & Visual Rhythm
- **Rule:** The layout must use screen real estate efficiently with well-controlled information density.
- **Prohibition:**
  - No oversized margins or massive empty vertical gaps that force unnecessary scrolling.
  - Key information and actions must be immediately accessible (*Above the fold* optimization).
  - Maintain consistent spacing based on a modular scale (multiples of 4px / 8px: `p-3`, `p-4`, `gap-3`, `gap-4`).

### 7. 📱 Native Responsive Layout & Adaptive Navigation
- **Rule:** The layout must adapt seamlessly across all viewport sizes (Mobile, Tablet, Desktop).
- **Adaptive Navigation:**
  - **Desktop:** Fixed sidebar (*sidebar*) or clean horizontal header with quick access.
  - **Mobile / Tablet:** Accessible slide-over drawer (*drawer*), bottom navigation bar (*bottom nav*), or compact header with hamburger menu.
  - **Grid & Flexbox:** Tables and lists with contained horizontal scrolling or transformed into compact card stacks on mobile.

### 8. 🚫 Zero Emojis & Smileys
- **Rule:** The interface must maintain a sleek, elegant, and professional appearance.
- **Strict Prohibition:**
  - No emojis or smileys in titles, buttons, badges, menus, or body copy (e.g., ❌ `🚀`, `✨`, `🔥`, `💡`, `👋`).
  - Use exclusively crisp, monochrome vector icons (SVG, Lucide Icons, Heroicons).

### 9. 📁 Local & Real Assets Only
- **Rule:** If a logo or image is required, use **only** files already present in the project's asset directories (e.g., `public/`, `assets/`, `static/`, `images/`).
- **Strict Prohibition:**
  - Never generate unsolicited external URLs (no external Unsplash, Placehold.co, or third-party hotlinks that will eventually break).
  - If an expected asset does not exist, use a clean neutral placeholder (*minimalist SVG placeholder without external image*) or ask the user for the asset path.

### 10. 🔘 Strict Action Hierarchy (Single Primary Button per View)
- **Rule:** **Only 1 primary action** per view, card, or modal form (the main action the user is expected to take).
- **Prohibition:**
  - Never place multiple primary buttons side by side with the same accent color (e.g., "Save" and "Cancel" both styled in vivid primary colors).
  - Secondary actions must remain understated (neutral, bordered, or ghost).

### 11. ⚠️ Systematic Protection for Destructive Actions
- **Rule:** Any irreversible action (permanent deletion, reset, purge) must require explicit confirmation:
  - Clean confirmation dialog with explicit phrasing (*"Delete project"*).
  - Red semantic alert button strictly reserved for confirming the destructive step.
- **Prohibition:** Never trigger an irreversible destructive action on a single direct click without confirmation.

### 12. 📦 Actionable Empty States
- **Rule:** Every empty table, list, or container must display a helpful empty state containing:
  1. A clear and concise explanation (e.g., *"No customers found"*).
  2. A **direct call-to-action button** to create or import the first record (e.g., *"[ + Add Customer ]"*).
- **Prohibition:** Never leave an empty blank white box or insert oversized decorative illustrations.

### 13. 👆 Compliant Touch Targets (≥ 44 × 44 px)
- **Rule:** On mobile and touch devices, every clickable area (buttons, icon triggers, pagination links) must have an interactive hit area of at least **44 × 44 px** (via padding or minimum dimensions), even if the visual icon is 16 px.
- **Prohibition:** No micro-buttons impossible to tap reliably on mobile screens.

### 14. ✂️ Clean Overflow & Truncation Handling
- **Rule:** Any dynamic or long text inside tables, lists, and cards must be truncated cleanly (`truncate` / `overflow-hidden text-ellipsis whitespace-nowrap`) with a native `title="..."` attribute to view the full text on hover.
- **Prohibition:** No unconstrained text breaking grid columns or creating accidental horizontal scrollbars.

### 15. ⌨️ Keyboard Navigation & Power-User Ergonomics
- **Rule:**
  - Immediate dismissal of all modals, drawers, and dropdowns with the `Escape` (`Esc`) key.
  - Standard form submission on `Enter` (or `Ctrl + Enter` / `Cmd + Enter` for multiline textareas).
  - Logical sequential focus navigation (`Tab`) with a clear visible focus ring on every interactive element.

### 16. 🏷️ Concise Microcopy & Consistent Case
- **Rule:** Labels must be concise, direct, and formatted as action verbs (*"Export CSV"*, *"Create Invoice"*).
- **Prohibition:** No wordy sentences (*"Click here to..."*), no unjustified language mixing, and maintain standard sentence case (avoid ALL-CAPS overload).

---

## 🏗️ Standards by UI Component

### Typography & Hierarchy
- **Single font family:** Modern sans-serif (Inter, Geist, SF Pro, or system font stack).
- **3 font weights maximum:** `font-normal` (body), `font-medium` (labels/buttons), `font-semibold` (headings).
- No novelty fonts, no excessive italics.

### Icons & Symbols
- Use a single, unified icon library (e.g., Lucide, Heroicons).
- Standardized, discrete sizing: `16px` (h-4 w-4) for buttons and tables, `20px` (h-5 w-5) for navigation.
- Uniform stroke weight (`stroke-width: 1.5` or `2`).

### Buttons & Actions
- **Primary:** 1 per section, solid user accent color + high-contrast text.
- **Secondary:** Subtle neutral surface (light gray / dark zinc) or 1px fine border.
- **Danger:** Discrete semantic red, reserved for deletions with confirmation.
- **Mandatory States:** Immediate visual feedback on hover (`hover`), click (`active`), keyboard focus (`focus-visible:ring-2`), and disabled state (`disabled:opacity-50 cursor-not-allowed`).

### Forms & Input Fields
- Visible label positioned above the field (`text-xs` or `text-sm`, `font-medium`).
- 1px border with a clean, precise focus ring.
- Specific error messages positioned directly beneath the relevant input field.
- Logical action button alignment (primary action given prominent placement).

### Data Tables & Lists
- Compact rows with subtle border separation (`border-b`).
- Column headers in subdued text or light uppercase (`text-xs font-semibold text-muted`).
- Alignment: text left-aligned, numbers & monetary values right-aligned, status badges centered.
- Explicit state handling: **Loading (skeleton)**, **Actionable empty state (with add button)**, **Error**.

### Animations & Transitions
- Understated and snappy: short color/opacity transitions only (`transition-colors duration-150`).
- **Prohibition:** No bouncy animations (`bounce`), aggressive pulse effects, or disruptive visual noise.

### Modals & Drawers
- Subtly dimmed backdrop (without extreme blur).
- Header with clear title and visible close button (`X` icon).
- Native closing via `Escape` key and backdrop click.
- Primary actions grouped at bottom-right (Desktop) or full-width stack (Mobile).

---

## 📋 Self-Verification Checklist for Agents

Before delivering any UI component or screen, verify each item:
- [ ] **Palette Adherence:** No colors invented outside the user's color scheme?
- [ ] **Solid Surfaces:** Zero gradients and zero transparency/frosted glass effects?
- [ ] **Borders:** Subtle 1px borders without heavy dark outlines?
- [ ] **Zero Emojis:** No emojis (`🚀`, `✨`, etc.) used in the UI?
- [ ] **Real Assets:** All logos/images sourced from local project folders without invented external URLs?
- [ ] **Action Hierarchy:** Exactly one primary button per view/form?
- [ ] **Destructive Safeguards:** Confirmation modal required before any permanent deletion?
- [ ] **Empty States:** Does every empty view include a direct creation/import action button?
- [ ] **Touch Targets:** Are interactive elements at least 44 × 44 px on mobile?
- [ ] **Overflow:** Long text truncated with `title="..."` without breaking the layout?
- [ ] **No Parasite Elements:** No redundant arrow icons on buttons?
- [ ] **Clean Content:** No fake customer testimonials or filler clichés?
- [ ] **Visual Density:** Screen space efficiently utilized without excessive empty gaps?
- [ ] **Responsive & Keyboard:** Adaptive navigation, modals close on `Escape`, no horizontal layout overflow?
- [ ] **Accessibility:** WCAG AA contrast compliance and visible keyboard focus rings?
