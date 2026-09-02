# RCT Ecology Workshop

Interactive conference portal, schedule explorer, and registration platform for the Relational-Cultural Theory (RCT) Ecology Gathering, examining relational ecology, environmental sustainability, and embodied ecological connection.

---

## Architecture & Component Map

```
+-------------------------------------------------------------------------------+
|                            RCT Ecology Gathering SPA                          |
|                                                                               |
|  +-------------------------------------------------------------------------+  |
|  | Navbar (Navigation, Branding, Smooth Scroll Anchors)                   |  |
|  +-------------------------------------------------------------------------+  |
|                                       |                                       |
|  +------------------------------------+------------------------------------+  |
|  | Hero Section                       | AboutSection                       |  |
|  | - Event Theme & Call to Action     | - Relational-Cultural Theory Context|  |
|  +------------------------------------+------------------------------------+  |
|                                       |                                       |
|  +------------------------------------+------------------------------------+  |
|  | WorkshopDetails                    | SpeakerCard                        |  |
|  | - Dual Schedules (MA & MN)        | - Facilitator & Scholar Profiles   |  |
|  | - Location & Timing Matrix         | - Research Specializations         |  |
|  +------------------------------------+------------------------------------+  |
|                                       |                                       |
|  +------------------------------------+------------------------------------+  |
|  | BirdPhotography                    | RegistrationForm                   |  |
|  | - Ecological Species Gallery       | - Participant Intake & Validation  |  |
|  | - Field Notes & High-Res Media     | - React Hook Form + Zod Schema     |  |
|  +------------------------------------+------------------------------------+  |
|                                       |                                       |
|  +-------------------------------------------------------------------------+  |
|  | Footer (Institutional Credits, Community Links, Copyright)              |  |
|  +-------------------------------------------------------------------------+  |
+-------------------------------------------------------------------------------+
```

---

## Core Capabilities

* **Multi-Regional Schedule Management**: Interactive timeline presenting multi-track gathering sessions across Massachusetts and Minnesota cohorts.
* **Ecological Media & Field Photography**: High-resolution avian photography gallery with responsive aspect ratios and field observations.
* **Participant Registration**: Validated registration intake form powered by `react-hook-form` and `zod`.
* **Accessible Design System**: Built with Tailwind CSS, custom earth-tone palettes, and accessible Radix UI primitives.

---

## Repository Structure

```
RCT-ecology-workshop/
├── src/
│   ├── components/           # Modular page sections and UI controls
│   │   ├── AboutSection.tsx  # Relational-Cultural Theory context
│   │   ├── BirdPhotography.tsx # Avian media gallery and species notes
│   │   ├── Footer.tsx        # Institutional footer and navigation
│   │   ├── Hero.tsx          # Main conference banner and CTA
│   │   ├── Navbar.tsx        # Responsive header and navigation
│   │   ├── RegistrationForm.tsx # Registration intake and validation
│   │   ├── SpeakerCard.tsx   # Facilitator biographies
│   │   ├── WorkshopDetails.tsx # Detailed dual-location schedule matrix
│   │   └── ui/               # Radix UI primitive wrappers
│   ├── hooks/                # Custom React hooks (toast, mobile detection)
│   ├── lib/                  # Utility functions (class merging, formatters)
│   ├── pages/                # Route views (Index, NotFound)
│   ├── App.tsx               # App router and React Query client provider
│   └── main.tsx              # DOM root mount
├── docs/
│   └── adr/                  # Architectural Decision Records (ADRs 0001 - 0002)
├── public/                   # Static assets, fonts, and icons
├── index.html                # HTML entry document
├── package.json              # Project dependencies and build scripts
├── tailwind.config.ts        # Design tokens and styling configuration
└── vite.config.ts            # Vite bundler configuration
```

---

## Prerequisites

* **Node.js**: 18.x or higher
* **Package Manager**: `npm`, `pnpm`, or `bun`

---

## Quickstart

### 1. Installation

```bash
git clone https://github.com/kaushalbalagurusamy/RCT-ecology-workshop.git
cd RCT-ecology-workshop

npm install
```

### 2. Running Development Server

```bash
npm run dev
```

The application will start locally at `http://localhost:8080`.

### 3. Production Build

```bash
# Build optimized static bundle
npm run build

# Preview production build locally
npm run preview
```

---

## Technical Documentation & ADRs

All foundational architectural decisions are recorded in [`docs/adr/`](docs/adr/):

* [`docs/adr/0001-single-page-conference-portal-architecture.md`](docs/adr/0001-single-page-conference-portal-architecture.md) — Single-Page Workshop Portal Architecture
* [`docs/adr/0002-shadcn-tailwind-design-system.md`](docs/adr/0002-shadcn-tailwind-design-system.md) — Tailwind CSS & Radix UI Design System

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
