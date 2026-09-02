# ADR 0002: Tailwind CSS & Radix UI Design System

* **Status**: Accepted & Implemented
* **Date**: 2026-09-02
* **Deciders**: Frontend & Design Team

---

## Context & Problem Statement

An ecology-themed portal requires a cohesive natural visual identity (earth tones, custom typography, smooth transitions) while maintaining full WAI-ARIA accessibility across modal dialogs, carousels, and accordion schedules.

---

## Decision Drivers

1. **Accessibility (a11y)**: Complete keyboard navigation, focus management, and screen reader announcements.
2. **Design Cohesion**: Semantic Tailwind theme tokens for natural palette (e.g. `primary-500`, `cream-500`, `muted-foreground`).
3. **Component Modularity**: Unstyled headless Radix UI primitives wrapped in customized styling.

---

## Decision Outcome

Adopt Tailwind CSS v3 paired with Radix UI headless components:

* **Primitives**: `@radix-ui/react-*` (Dialogs, Tooltips, Separators, Accordions, Tabs).
* **Styling**: `tailwind.config.ts` defining responsive breakpoints, color scales, and custom typography utilities.
* **Icons**: `lucide-react` for crisp vector iconography.

### Positive Consequences
* 100% accessible interactive controls out of the box.
* Zero runtime CSS overhead via ahead-of-time utility class compilation.
