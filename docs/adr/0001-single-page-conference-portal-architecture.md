# ADR 0001: Single-Page Workshop Portal Architecture

* **Status**: Accepted & Implemented
* **Date**: 2026-09-02
* **Deciders**: Frontend & Design Team

---

## Context & Problem Statement

The RCT Ecology Gathering requires an accessible, responsive, and aesthetically serene conference portal to present gathering details, multi-state workshop schedules (Massachusetts & Minnesota), facilitator profiles, interactive media, and participant registration.

---

## Decision Drivers

1. **Fast Initial Load**: Static single-page application (SPA) with minimal bundle size and immediate client-side hydration.
2. **Accessible Form Handling**: Interactive registration flow with robust validation (`react-hook-form`, `zod`).
3. **Mobile & Media Optimization**: High-quality ecological imagery and bird photography galleries with responsive aspect ratios.

---

## Decision Outcome

Adopt a modern React 18 + Vite SPA architecture:

* **Entry Point**: `src/pages/Index.tsx` composing modular section components.
* **State & Query Layer**: `@tanstack/react-query` for asynchronous interactions and server state caching.
* **Routing**: `react-router-dom` v6 for clean client-side navigation.

### Positive Consequences
* Sub-second load times across mobile and desktop devices.
* Clean separation of concerns between presentation components and registration logic.
