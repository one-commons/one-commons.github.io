# **O.N.E. WEB APPLICATION REDESIGN & ARCHITECTURAL REFACTORING SPEC (`webapp/TODO.md`)**

## **I. EXECUTIVE SUMMARY & STRATEGIC PIVOT**

The current web portal (`webapp/index.html`, `styles.css`, and `app.js`) historically evolved by continuous accumulation. While it successfully serves as a comprehensive archive of the project's intellectual depth, it currently suffers from **monolithic cognitive overload** (1,320 lines of dense HTML, 9 stacked sections, and 5 competing hero CTAs) and a visual language rooted in **dark cyberpunk / Web3 glassmorphism** that inadvertently signals "crypto token / sci-fi video game" rather than an authoritative, physical commons and constitutional foundation.

This specification outlines the comprehensive refactoring of the web portal toward **timeless architectural minimalism, editorial elegance, and focused user conversion**, drawing visual and spatial inspiration from benchmarks such as **[WikiHouse.cc](https://wikihouse.cc)** and **[Riverview Consulting](https://riverviewconsulting.co.nz)**, while **strictly preserving the complete 15-language multilingual engine (`i18n/`)** and zero-tracker privacy standards.

---

## **II. CORE OBJECTIVES & INVARIANTS**

1. **The Architectural Paradigm (WikiHouse / Riverview Consulting Benchmark):**
   * Transition from *deep-space carbon (`#06090e`), neon cyan/emerald glows, and frosted glass cards* to an **architectural, material, and editorial aesthetic**: warm chalk/paper background, crisp graphite/ink typography, 1px hairline grid structures, generous white space, technical line drawings, and authentic material textures (timber, earth, steel).
2. **From Monolithic Encyclopedia to "Grand Hall" Navigation:**
   * Break the single 15-scroll vertical dump into a clean, decisive **Front Door (Grand Hall)** leading to focused, modular rooms/views.
3. **Elevating the Call for Co-Stewards:**
   * Move the recruitment of the 4 Domain Co-Stewards (and the Media/Community Steward) from the very bottom (Section 9, line 1125) to a prominent, immediate position on the front door.
4. **Reduction of Choice Paralysis (Hero CTAs):**
   * Replace the 5 competing hero buttons with **2 decisive primary paths**:
     - `[ Discover Track B ]` (Orientation, 3-min explainer & core contrast).
     - `[ Join as Co-Steward / Builder ]` (Direct recruitment & technical RFCs).
5. **Preserving 100% of the Multilingual Infrastructure (`i18n/`):**
   * Retain all 15 localized language dictionaries (`en`, `it`, `de`, `fr`, `es`, `pt`, `ru`, `zh`, `ja`, `ko`, `hi`, `ar`, `id`, `tr`).
   * Preserve all existing `data-i18n` attributes, language selector dropdown, dynamic RTL support, and multi-script Google Font fallbacks.
6. **Class-0 Hard Constraints Compliance:**
   * 100% free software (AGPL-3.0), zero monetization, zero trackers (GoatCounter privacy analytics only), zero leak of personal workstation metadata (`Kyberlex` / `kyberlex@proton.me` exclusively).

---

## **III. DESIGN SYSTEM OVERHAUL: FROM CYBERPUNK TO ARCHITECTURAL ELEGANCE**

### **1. Color Palette & Materiality**
* **Primary Canvas:** Warm architectural white / matte chalk (`#fbfbfa` or `#f7f7f5`) for light mode, with an optional deeply muted, warm architectural slate/graphite for dark mode (`#121316` without neon dropshadows).
* **Typography & Ink:** Deep charcoal ink (`#18191b`), medium architectural slate (`#4b5563`), subtle technical captions (`#6b7280`).
* **Material Accents (Replacing Neon Glows):**
  - *Warm Terracotta / Cedar:* Earthy structural accent reflecting timber and habitat (`#c25e38` or `#b45309`).
  - *Engineering Blueprint Blue:* Crisp, understated technical contrast (`#1d4ed8` or `#2563eb`).
  - *Sage / Forest Patina:* Subtle ecological reference (`#2d6a4f` or `#059669`).
* **Borders & Dividers:** Clean 1px hairline grid dividers (`rgba(0, 0, 0, 0.08)` or `#e5e7eb`), eliminating fuzzy neon glows, blur filters, and multi-layer box shadows.

### **2. Typography & Layout**
* **Headings & Hierarchy:** High-contrast, elegant Grotesk sans-serif (`Inter`, `Outfit`, or system Swiss Grotesk) with tight tracking and deliberate scale.
* **Editorial & Literature:** Refined serif for philosophical/constitutional passages (`Newsreader`, Georgia).
* **Technical Metadata:** Monospace for articles, Leontief formulas, and RFC specs (`JetBrains Mono`).
* **Grid Discipline:** Asymmetrical, Swiss-style architectural grid with generous breathing room (padding and margins increased by 40-50%), allowing technical diagrams and typography to command the page.

---

## **IV. INFORMATION ARCHITECTURE (IA) RESTRUCTURING**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       O.N.E. FRONT DOOR (GRAND HALL)                        │
├─────────────────────────────────────────────────────────────────────────────┤
│ 1. Minimal Header & Nav (Brand Acrostic, Language Selector, Clean Links)    │
│ 2. Hero: "Deploy Track B: When Machines Work, Humanity Inherits the Earth"  │
│    - 2 Clear CTAs: [ Discover Track B ] & [ Join as Co-Steward ]            │
│    - Visual Hook: `one-wars-remastered.mp4` (2m 10s Civilizational Prologue)│
│ 3. The Visceral Contrast Matrix: Track A (Legacy Warfare/Debt) vs. Track B  │
│ 4. Immediate Call for Co-Stewards Banner (Phase 0 Genesis Hardening)        │
│ 5. The 4 Gateways (Modular Cards / Hubs):                                  │
│    ├── 🏛️ The Living Constitution & AI Benchmark                           │
│    │   └── Architectural Walkthrough: `O.N.E(8min)Easy_Master.mp4`          │
│    ├── 📚 The 6-Volume Novel Saga & Audio Archive                          │
│    ├── 🎮 The Thermodynamic Sandbox & Living Game (O-ASIS)                  │
│    └── 🛠️ The Seed Node Blueprint & Open Hardware (WikiHouse/MHU)           │
│ 6. Future Growth Tools (e.g., Debt Jubilee Calculator / Watershed Passport) │
│ 7. Sovereign Footer (AGPL-3.0, Swiss Foundation, Tor/Surge/GitHub Mirrors)  │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## **V. ACTIONABLE IMPLEMENTATION CHECKLIST (PHASED)**

### **Phase 1: Design Tokens & CSS Cleanup (`webapp/styles.css`)**
- [ ] **CSS Variable Audit:** Replace neon glow tokens (`--accent-cyan-glow`, `--shadow-glow`, glassmorphism blur) with architectural flat/hairline variables.
- [ ] **Background & Canvas:** Remove dark radial-gradient glow backdrops and pulsing watermark logo. Implement warm architectural canvas (`#fcfcfb`).
- [ ] **Card & Panel Reset:** Convert `.glass-panel` and `.hero-section` from translucent blur to solid paper panels with crisp 1px borders and refined hover states.
- [ ] **Button Simplification:** Standardize on minimal solid-fill primary buttons and architectural outlined secondary buttons.

### **Phase 2: HTML Structure & Front Door Pruning (`webapp/index.html`)**
- [ ] **Hero Section Cleanup & Video Re-allocation:**
  - Prune the 5 buttons down to the 2 primary actions (`#overview` and `#co-stewards`).
  - Feature **`one-wars-remastered.mp4`** (2m 10s) as the high-impact visual prologue right in the Hero/Contrast section (100,000 years of warfare transitioning into Track B).
- [ ] **Constitution Architectural Video:**
  - Move the 8-minute architectural explainer (**`O.N.E(8min)Easy_Master.mp4`**) to the header of the `#constitution` section as the foundational briefing before exploring the 10 chapters.
- [ ] **Promote Co-Stewards:** Relocate the `#co-stewards` section immediately below the core manifesto/overview to maximize visibility for prospective builders and media allies.
- [ ] **Create Modular Gateway Sections:** Condense the deep encyclopedic sections (Benchmark, Roadmap, Simulator, Books) into modular architectural cards that expand on demand or link cleanly to dedicated views.
- [ ] **Dialectic Chat Refinement:** Clean up the `#challenge` section into a sleek, editorial "Stress-Test Arena" with crisp typography and clear objection chips.

### **Phase 3: Multilingual & JavaScript Synchronization (`webapp/app.js` & `webapp/i18n/`)**
- [ ] **i18n Dictionary Integrity:** Ensure all 15 JSON files in `webapp/i18n/` maintain key parity for newly structured headlines, buttons, and gateway descriptions.
- [ ] **RTL & Multi-Font Verification:** Confirm Arabic (`ar.json`), East Asian (`zh`, `ja`, `ko`), and Indic (`hi`) typography scales cleanly under the new architectural grid.
- [ ] **State & Modal Logic:** Streamline `app.js` event listeners for modal views (e.g. ebook reader, blueprint viewer, constitution accordion) to ensure zero regressions.

### **Phase 4: Viral & Interactive Experience Enhancements (Future Sprints)**
- [ ] **Thermodynamic Debt Jubilee Calculator:** Design a clean, minimal slider widget calculating biological life-hours lost to fiat usury vs. O.N.E. baseline.
- [ ] **Bioregional Watershed Explorer:** Minimalist map widget mapping local hydrological catchments without national borders.

---

## **VI. VERIFICATION CRITERIA**

1. **Visual Test:** Does the site feel like an authoritative, timeless architectural and civic foundation (comparable to WikiHouse.cc or a Swiss design archive) rather than a crypto/gaming project?
2. **Speed & Lightweight Performance:** Page load remains instantaneous, zero layout shift, fully accessible, and mobile responsive.
3. **i18n Test:** Switching between all 15 languages seamlessly updates 100% of visible UI text without breaking layout grids.
4. **Conversion Clarity:** Can a new visitor understand what O.N.E. is within 10 seconds, and can a prospective Co-Steward find the application path within one scroll?
