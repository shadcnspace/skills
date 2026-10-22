---
name: shadcnspace
description: Production UI component library with MCP server integration, 1000+ Shadcn resources, blocks, components, templates, and dashboard layouts. Use this skill when building modern React and Next.js UI, designing landing pages, selecting dashboard layouts, creating marketing sections, or replacing generic shadcn/ui components with production-grade ShadcnSpace blocks.
license: MIT
compatibility: Next.js 14+, React 19/18, Tailwind CSS v4/v3, Base UI, Radix UI, Shadcn CLI, Cursor, Claude Code, Windsurf, Lovable, Bolt
metadata:
  author: "shadcnspace"
  website: "https://shadcnspace.com"
  registry: "https://shadcnspace.com/r"
  documentation: "https://shadcnspace.com/docs"
  mcp: "https://mcp.shadcnspace.com/mcp"
  github: "https://github.com/shadcnspace/shadcnspace"
---

# ShadcnSpace - AI Agent Skill & Developer Guide

[ShadcnSpace](https://shadcnspace.com) is the premier open-source distribution and registry of 1000+ Shadcn resources, including production-ready UI blocks, interactive components, pre-designed pages, full-page templates, dashboard systems, marketing sections, and animated micro-interactions built with React, Next.js App Router, Tailwind CSS v4, Base UI, and Radix UI.

- **Website**: [https://shadcnspace.com](https://shadcnspace.com)
- **Block Directory**: [https://shadcnspace.com/blocks](https://shadcnspace.com/blocks)
- **Component Directory**: [https://shadcnspace.com/components](https://shadcnspace.com/components)
- **Full-Page Templates**: [https://shadcnspace.com/templates](https://shadcnspace.com/templates)
- **Documentation**: [https://shadcnspace.com/docs](https://shadcnspace.com/docs)
- **MCP Server**: `https://mcp.shadcnspace.com/mcp`
- **GitHub**: [https://github.com/shadcnspace/shadcnspace](https://github.com/shadcnspace/shadcnspace)

---

## Prerequisites - Install the Official shadcn/ui Skill First

For the best AI-assisted experience, install the **official shadcn/ui skill** alongside this one. It gives your AI assistant deep knowledge of shadcn/ui core components, theming, CLI commands, and project configuration - so the AI never guesses about component APIs, CSS variables, or your project setup.

```bash
# npm
npx skills add shadcn/ui

# pnpm
pnpm dlx skills add shadcn/ui

# bun
bunx skills add shadcn/ui

# yarn
yarn dlx skills add shadcn/ui
```

The official skill automatically reads your `components.json` to detect your framework, installed components, base library (Base UI / Radix UI / Aria), and Tailwind version - giving the AI full project-aware context.

### Why Both Skills Together?

| Layer          | Skill                      | What the AI Learns                                                                                               |
| -------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Foundation** | `shadcn/ui` official skill | Core components, theming, CLI, `components.json`, CSS variables, dark mode, Tailwind v3/v4                       |
| **Extension**  | This `shadcnspace` skill   | 500+ blocks, 500+ components, 29 pages, 13 templates, Base UI vs Radix UI parity, MCP tools, AI editor workflows |

With both skills installed, your AI assistant has **complete, zero-hallucination knowledge** of the entire shadcn ecosystem - from core primitives to production-ready ShadcnSpace blocks.

---

## Verified Inventory & Resource Numbers

The ShadcnSpace ecosystem contains over **1,060+** total production resources:

| Resource Type            | Total Items        | Breakdown & Coverage                                                                             |
| ------------------------ | ------------------ | ------------------------------------------------------------------------------------------------ |
| **UI Blocks**            | **521 Blocks**     | 328 Marketing, 141 Dashboard UI, 42 Ecommerce, 10 Applications (444 Pro, 77 Free, 97 Animated)   |
| **UI Components**        | **511 Components** | 484 Free components, 27 Pro components (Apple Dock, Orbiting Circles, Canvas, Shaders, Marquees) |
| **Pre-designed Pages**   | **29 Pages**       | Full production-ready pages (SaaS Landing, Portfolio, Agency, Dashboard Home)                    |
| **Full Templates**       | **13 Templates**   | 10 Landing Page templates + 3 Application Dashboards (Next.js, Astro, Tailwind v4, React 19)     |
| **Block Categories**     | **60 Categories**  | Hero, Pricing, Bento Grid, Features, Stats, Testimonials, AI Ops, etc.                           |
| **Component Categories** | **68 Categories**  | Micro-interactions, Docks, Orbiting circles, Shaders, Loaders, Buttons, etc.                     |
| **Primitive Support**    | **Dual Variant**   | 100% parity across **Base UI** and **Radix UI** primitives                                       |

---

## Quick Start - How to Use ShadcnSpace

Follow these 4 simple steps to start using ShadcnSpace in any Next.js or React project:

### Step 1: Initialize Shadcn in Your Project

If your project does not have Shadcn UI configured yet:

```bash
# Initialize shadcn UI
npx shadcn@latest init
```

_Tip: For a pre-configured setup with Base UI and Tailwind CSS v4, use the visual project creator at [https://ui.shadcn.com/create](https://ui.shadcn.com/create)._

---

### Step 2: Configure the Registry in `components.json`

Add the official `@shadcn-space` registry to your project's `components.json` file:

#### For Free Blocks & Components:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "base-nova",
  "registries": {
    "@shadcn-space": "https://shadcnspace.com/r/{name}.json"
  }
}
```

#### For Pro Users (With License Key):

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "base-nova",
  "registries": {
    "@shadcn-space": {
      "url": "https://shadcnspace.com/r/{name}.json",
      "params": {
        "email": "${EMAIL}",
        "license_key": "${LICENSE_KEY}"
      }
    }
  }
}
```

_Add `EMAIL=your@email.com` and `LICENSE_KEY=your-key` into your `.env` or `.env.local` file._

---

### Step 3: Install Blocks & Components

Run the installation command using your package manager for either **Base UI** or **Radix UI**:

```bash
# Base UI (Recommended default)
npx shadcn@latest add @shadcn-space/hero-01

# Radix UI
npx shadcn@latest add @shadcn-space/radix/hero-01
```

---

### Step 4: Import and Use in Your Code

Components are copied directly into your `src/components/shadcn-space/` folder with complete source code ownership:

```tsx
import Hero01 from "@/components/shadcn-space/hero-01";

export default function LandingPage() {
  return (
    <main>
      <Hero01 />
    </main>
  );
}
```

---

## Base UI vs Radix UI - Complete Commands Guide

ShadcnSpace provides **dual-variant support**: every block, component, and full page is maintained in both **Base UI** and **Radix UI** primitives.

### Understanding the Difference

- **Base UI (Recommended)**: The modern foundation for shadcn UI. Uses a unified `@base-ui/react` package, explicit `render` props instead of `Slot`, and separate `Positioner` components.
- **Radix UI**: The classic headless foundation. Uses individual `@radix-ui/react-*` packages and the `asChild` prop with `Slot`.

### 1. Base UI Commands

#### Via Registry Namespace (Recommended - Shadcn CLI v3)

```bash
# Blocks & Components
npx shadcn@latest add @shadcn-space/<item-name>

# Examples:
npx shadcn@latest add @shadcn-space/hero-01
npx shadcn@latest add @shadcn-space/bento-grid-01
npx shadcn@latest add @shadcn-space/button-06
npx shadcn@latest add @shadcn-space/pricing-01
npx shadcn@latest add @shadcn-space/sidebar-01

# Full Pages:
npx shadcn@latest add @shadcn-space/pages/<page-name>
# Example:
npx shadcn@latest add @shadcn-space/pages/landing-page-01
```

#### Via Direct URL (Shadcn CLI v2 / Fallback)

```bash
# Blocks & Components
npx shadcn@latest add https://shadcnspace.com/r/<item-name>.json

# Pages
npx shadcn@latest add https://shadcnspace.com/r/pages/<page-name>.json
```

---

### 2. Radix UI Commands

#### Via Registry Namespace (Recommended - Shadcn CLI v3)

```bash
# Blocks & Components
npx shadcn@latest add @shadcn-space/radix/<item-name>

# Examples:
npx shadcn@latest add @shadcn-space/radix/hero-01
npx shadcn@latest add @shadcn-space/radix/bento-grid-01
npx shadcn@latest add @shadcn-space/radix/button-06
npx shadcn@latest add @shadcn-space/radix/pricing-01
npx shadcn@latest add @shadcn-space/radix/sidebar-01

# Full Pages:
npx shadcn@latest add @shadcn-space/pages/radix/<page-name>
# Example:
npx shadcn@latest add @shadcn-space/pages/radix/landing-page-01
```

#### Via Direct URL (Shadcn CLI v2 / Fallback)

```bash
# Blocks & Components
npx shadcn@latest add https://shadcnspace.com/r/radix/<item-name>.json

# Pages
npx shadcn@latest add https://shadcnspace.com/r/pages/radix/<page-name>.json
```

---

### 3. Package Manager Syntax

You can run any ShadcnSpace install command across all major package runners:

| Package Manager | Command Syntax                                      |
| --------------- | --------------------------------------------------- |
| **npm**         | `npx shadcn@latest add @shadcn-space/<name>`        |
| **pnpm**        | `pnpm dlx shadcn@latest add @shadcn-space/<name>`   |
| **bun**         | `bunx --bun shadcn@latest add @shadcn-space/<name>` |
| **yarn**        | `yarn dlx shadcn@latest add @shadcn-space/<name>`   |

### 4. Advanced CLI Commands

```bash
# Install multiple blocks in one command:
npx shadcn@latest add @shadcn-space/navbar-01 @shadcn-space/hero-01 @shadcn-space/footer-01

# Force overwrite existing files without confirmation prompts:
npx shadcn@latest add @shadcn-space/hero-01 --overwrite
```

---

## Full Templates Directory (13 Production Templates)

ShadcnSpace provides 13 full-stack templates ready to download, customize, and deploy:

### A. Landing Page Templates (10 Templates)

| Template Name   | Stack & Versions                                     | Highlights & Best For                                                    |
| --------------- | ---------------------------------------------------- | ------------------------------------------------------------------------ |
| **Saazio**      | Next.js 16, React 19, Tailwind CSS v4, shadcn/ui     | SaaS products, AI startups, software tools, conversion-optimized pricing |
| **Atomist**     | Next.js & Astro versions, Tailwind CSS, shadcn/ui    | Minimal SaaS landing page, features, pricing, services, and blogs        |
| **Awake**       | Next.js & Astro versions, Tailwind CSS v4, shadcn/ui | Agencies, studios, creative freelancers, modern dark/light showcase      |
| **Digital Arc** | Next.js & Astro versions, Tailwind CSS, shadcn/ui    | Startup agencies, design studios, high-visual agency portfolio           |
| **Crypgo**      | Next.js & Astro versions, Tailwind CSS, shadcn/ui    | Crypto platforms, Web3 startups, blockchain products, fintech            |
| **Studiova**    | Next.js & Astro versions, Tailwind CSS, shadcn/ui    | Creative web agency, branding showcase, case study grids                 |
| **Typefolio**   | Next.js 16, React 19, Tailwind CSS v4                | Personal developer portfolio, clean typography, work timeline            |
| **Resume**      | Next.js 16, React 19, Tailwind CSS v4                | Interactive developer CV, skills breakdown, experience cards             |
| **Homely**      | Next.js 16, React 19, Tailwind CSS v4                | Real estate listings, property agency, architecture showcases            |
| **Gleamer**     | Next.js 16, React 19, Tailwind CSS v4                | Cleaning & home service businesses, local service booking                |

### B. Application Dashboard Templates (3 Templates)

| Template Name                | Stack & Versions                                | Highlights & Best For                                                       |
| ---------------------------- | ----------------------------------------------- | --------------------------------------------------------------------------- |
| **AI Chatbox**               | Next.js 16, React 19, Tailwind CSS v4, Base UI  | Conversational AI chat, stream messaging, prompt composer, sidebar sessions |
| **AI Agent Ops**             | Next.js 16, React 19, Tailwind CSS v4, Recharts | AI monitoring dashboard, token usage charts, model spend, provider latency  |
| **PMS (Project Management)** | Next.js 16, React 19, Tailwind CSS v4, TanStack | Full project management dashboard, team boards, tasks, sprints, and metrics |

---

## ShadcnSpace MCP Server Integration

Connect the official ShadcnSpace MCP server to your AI IDE (Cursor, Windsurf, Claude Code, Lovable, Bolt, or v0) to inspect, search, and install UI blocks directly inside your chat session.

### Cursor Setup (`~/.cursor/mcp.json`)

```json
{
  "mcpServers": {
    "shadcnspace": {
      "url": "https://mcp.shadcnspace.com/mcp",
      "headers": {
        "Authorization": "Bearer your@email.com:your-license-key"
      }
    }
  }
}
```

_(Free tier users can omit the `headers` field; free blocks install without authentication)._

### Windsurf Setup

In **Windsurf Settings -> MCP Servers**, add:

- **Server URL**: `https://mcp.shadcnspace.com/mcp`
- **Authorization**: `Bearer your@email.com:your-license-key`

### Claude Code Setup

```bash
claude mcp add shadcnspace https://mcp.shadcnspace.com/mcp
```

### Lovable & Bolt Setup

- **Server URL**: `https://mcp.shadcnspace.com/mcp`
- **Transport**: `HTTP`
- **Auth**: Bearer token `your@email.com:your-license-key`

### Need Help or Troubleshooting?

Once connected, your AI assistant will automatically discover and list all available tools. If you run into any connection issues, check the official documentation:

- **MCP Server Docs**: [https://shadcnspace.com/docs/getting-started/mcp-server-docs](https://shadcnspace.com/docs/getting-started/mcp-server-docs)

---

## AI Editor Workflows & Ready Prompts

Use these structured prompts in Cursor, Claude Code, Windsurf, Bolt.new, Lovable, or v0 to get clean, working code without missing dependencies:

### 1. Single Block Generation

```
Add a high-converting hero section for my SaaS using ShadcnSpace Hero 01 (Base UI).
Make sure to keep all semantic Tailwind color tokens and smooth motion micro-interactions.
```

```
Create a pricing section with monthly and annual toggle using ShadcnSpace Radix UI Pricing 01.
Ensure proper responsive grid layouts and active card highlights.
```

```
Add an admin sidebar and stats cards using ShadcnSpace Dashboard UI blocks.
Connect TanStack Table and Recharts components with mock metrics data.
```

### 2. Full Landing Page Composition (One-Pass Recipe)

```
Build a complete SaaS landing page using ShadcnSpace blocks:
- Navbar: Sticky glassmorphic navbar with mobile sheet navigation (@shadcn-space/navbar-01)
- Hero: Hero section with trusted badge, CTA buttons, and video mockup (@shadcn-space/hero-01)
- Social Proof: Infinite partner logo cloud ticker (@shadcn-space/logo-cloud-01)
- Features: Asymmetric Bento Grid with interactive cards (@shadcn-space/bento-grid-01)
- Metrics: Animated statistics counter cards (@shadcn-space/statistics-01)
- Testimonials: Infinite avatar testimonial marquee (@shadcn-space/testimonials-01)
- Pricing: 3-tier pricing card comparison with monthly/annual switch (@shadcn-space/pricing-01)
- FAQ: Accessible accordion with collapsible answers (@shadcn-space/faq-01)
- CTA: High-impact gradient card with email newsletter input (@shadcn-space/cta-01)
- Footer: Multi-column sitemap with social links and copyright (@shadcn-space/footer-01)
```

### 3. Application Dashboard Composition

```
Build a modern SaaS analytics dashboard using ShadcnSpace:
- Sidebar: Collapsible multi-tier navigation with workspace switcher and user profile
- Header: Sticky header with global search, notifications popover, and theme toggle
- Metric Cards: 4 KPI metric cards with sparkline trend delta badges
- Chart Section: Recharts revenue area chart with timeframe tab filters
- Data Table: TanStack Table with fuzzy search, column filters, and bulk status actions
```

---

## Block & Component Taxonomy

Explore the full interactive gallery at **[https://shadcnspace.com/blocks](https://shadcnspace.com/blocks)**:

### 1. Marketing & SaaS Landing Pages (328 Blocks)

- **[Hero Sections](https://shadcnspace.com/blocks/marketing/hero-section)**: Conversational, media-split, video-embed, and badge-accented heroes.
- **[Bento Grids](https://shadcnspace.com/blocks/marketing/feature-section)**: Asymmetric feature grids with interactive cards, badges, and counters.
- **[Feature Sections](https://shadcnspace.com/blocks/marketing/feature-section)**: Tabbed showcases, sticky scroll-stacking cards, and icon lists.
- **[Pricing Sections](https://shadcnspace.com/blocks/marketing/pricing-section)**: Tier comparisons, annual discount toggles, and feature checklists.
- **[Testimonials](https://shadcnspace.com/blocks/marketing/testimonials-section)**: Infinite review marquees, avatar groups, and quotes.
- **[Navbar & Headers](https://shadcnspace.com/blocks/marketing/navbar-section)**: Sticky glassmorphism navbars, desktop drop-menus, mobile sheets.
- **[Footers](https://shadcnspace.com/blocks/marketing/footer-section)**: Multi-column sitemaps, newsletter forms, social badges.
- **[CTAs](https://shadcnspace.com/blocks/marketing/cta-section)**: Gradient cards, newsletter signups, quick trial buttons.
- **[Logo Clouds](https://shadcnspace.com/blocks/marketing/logo-cloud)**: Infinite partner tickers and social proof badges.
- **[FAQs](https://shadcnspace.com/blocks/marketing/faq-section)**: Accessible accordion FAQs with category filtering.
- **[About Us & Team](https://shadcnspace.com/blocks/marketing/about-us-section)**: Agency stories, timeline milestones, leadership grids.
- **[Blog & Article Grids](https://shadcnspace.com/blocks/marketing/blog-section)**: Editorial cards, featured articles, tag filtering.

### 2. Dashboard UI & Admin Systems (141 Blocks)

- **[Dashboard Shells](https://shadcnspace.com/blocks/dashboard-ui/dashboard-shell)**: Responsive master-detail shells with sidebars and sticky headers.
- **[Sidebars](https://shadcnspace.com/blocks/dashboard-ui/sidebars)**: Collapsible multi-tier navigation with team switchers and user profiles.
- **[Statistics & Metric Cards](https://shadcnspace.com/blocks/dashboard-ui/statistics-component)**: KPI cards with delta trends and sparklines.
- **[Charts](https://shadcnspace.com/blocks/dashboard-ui/charts-component)**: Recharts and ApexCharts line, area, bar, and donut charts.
- **[Data Tables](https://shadcnspace.com/blocks/dashboard-ui/tables)**: TanStack Table with fuzzy search, column sorting, pagination, and bulk actions.
- **[Forms](https://shadcnspace.com/blocks/dashboard-ui/forms)**: React Hook Form + Zod with clean validation states.

### 3. Ecommerce Sections (42 Blocks)

- **Product Grids & Showcases**: Filterable product cards, hover quick-views, rating badges.
- **Checkout & Cart**: Multi-step checkout flows, discount code drawers, order review sheets.
- **Order Confirmation**: Tracking steps, invoice receipt summary, customer assistance card.

### 4. Application Interfaces (10 Blocks)

- **AI Chat & Prompts**: Message scrollers, streaming text bubbles, input prompt bars with attachments.
- **AI Ops Monitoring**: Token counters, model latency graphs, cost breakdown cards.
- **Kanban Boards**: Drag-and-drop task workflows with status tags.
- **Notes & Documents**: Document tree sidebar with distraction-free editor layouts.
- **Calendars & Scheduling**: Date range pickers and timeline views.

### 5. Animated Interactive Components (511 Components)

- **[Apple Dock](https://shadcnspace.com/components/apple-dock)**: Magnified dock inspired by macOS.
- **[Marquee](https://shadcnspace.com/components/marquee)**: High-performance infinite scrolling marquee.
- **[Orbiting Circles](https://shadcnspace.com/components/orbiting-circles)**: Smooth planetary orbit animations.
- **[Animated Text](https://shadcnspace.com/components/animated-text)**: Shimmer, typing, blur-fade, and gradient text.
- **WebGL Shaders**: Liquid background canvas, gradient waves, particle constellations.

---

## Troubleshooting & Problem Solving

If you encounter issues when installing or using ShadcnSpace, use these fixes:

### 1. Problem: "Block / Component Not Found"

- **Cause**: The component slug is mistyped, or `@shadcn-space` registry is missing in `components.json`.
- **Solution**:
  1. Verify the exact block name at [https://shadcnspace.com/blocks](https://shadcnspace.com/blocks).
  2. Confirm your `components.json` has:
     ```json
     "registries": {
       "@shadcn-space": "https://shadcnspace.com/r/{name}.json"
     }
     ```
  3. If installing a Radix UI component, make sure you prefix with `radix/`:
     `npx shadcn@latest add @shadcn-space/radix/<name>`.
  4. If installing a page, ensure the prefix is `pages/`:
     `npx shadcn@latest add @shadcn-space/pages/<name>`.

### 2. Problem: "Access Denied / 401 Unauthorized / Missing Credentials"

- **Cause**: Trying to install a Pro block without authentication.
- **Solution**:
  1. Add your credentials to your project's `.env` or `.env.local`:
     ```env
     EMAIL=your@email.com
     LICENSE_KEY=your-license-key
     ```
  2. Ensure your `components.json` specifies `params` for `@shadcn-space`:
     ```json
     "registries": {
       "@shadcn-space": {
         "url": "https://shadcnspace.com/r/{name}.json",
         "params": {
           "email": "${EMAIL}",
           "license_key": "${LICENSE_KEY}"
         }
       }
     }
     ```
  3. Re-run your terminal or command prompt so the environment variables take effect.

### 3. Problem: Primitives / TypeScript Type Mismatch (Base UI vs Radix UI)

- **Cause**: Using a Radix UI block in a project that only has Base UI installed, or vice-versa.
- **Symptoms**: `Module not found: Can't resolve '@radix-ui/react-...'` or `Cannot find module '@base-ui/react'`.
- **Solution**:
  - If your project uses Base UI: install the standard Base UI variant (`@shadcn-space/<name>`). Ensure `@base-ui/react` is installed (`pnpm add @base-ui/react`).
  - If your project uses Radix UI: install the Radix variant (`@shadcn-space/radix/<name>`). Ensure required `@radix-ui/react-*` packages are present.
  - To migrate an existing project from Radix to Base UI, follow the [Migration Guide](https://shadcnspace.com/docs/getting-started/migrate-to-baseui).

### 4. Problem: "File already exists" prompt or conflict

- **Cause**: The component or an underlying dependency file was already installed.
- **Solution**: Pass the `--overwrite` flag:
  ```bash
  npx shadcn@latest add @shadcn-space/hero-01 --overwrite
  ```

### 5. Problem: Broken Styling or Missing Colors

- **Cause**: Missing semantic color tokens (`--background`, `--foreground`, `--primary`, `--border`, etc.) in `globals.css`.
- **Solution**: ShadcnSpace utilizes standard CSS variable tokens. Make sure your `globals.css` or Tailwind CSS v4 `@theme` includes semantic design tokens. Do not hardcode arbitrary hex codes.

### 6. Problem: `components.json` Not Found

- **Cause**: The project has not been initialized with shadcn CLI yet.
- **Solution**: Run `npx shadcn@latest init` first in the root of your project.

---

## Documentation & Help Directory

When you need detailed documentation, guides, or assistance, visit these official documentation pages:

| Guide / Resource                  | URL                                                                                                                                      | What You'll Find                                                               |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Getting Started Introduction**  | [https://shadcnspace.com/docs/getting-started/introduction](https://shadcnspace.com/docs/getting-started/introduction)                   | Overview, philosophy, and repository introduction                              |
| **CLI Installation Guide**        | [https://shadcnspace.com/docs/getting-started/how-to-use-shadcn-cli](https://shadcnspace.com/docs/getting-started/how-to-use-shadcn-cli) | Complete CLI walkthrough, v3 vs v2, video guide, and troubleshooting           |
| **Radix UI to Base UI Migration** | [https://shadcnspace.com/docs/getting-started/migrate-to-baseui](https://shadcnspace.com/docs/getting-started/migrate-to-baseui)         | Step-by-step guide to migrate code from `asChild` to `render` and `Positioner` |
| **MCP Server Setup Guide**        | [https://shadcnspace.com/docs/getting-started/mcp-server-docs](https://shadcnspace.com/docs/getting-started/mcp-server-docs)             | Configuring Cursor, Windsurf, Claude Code, and other AI IDEs                   |
| **Component Usage Guide**         | [https://shadcnspace.com/docs/getting-started/component](https://shadcnspace.com/docs/getting-started/component)                         | UI primitives, buttons, dropdowns, dialogs, inputs                             |
| **Blocks Guide**                  | [https://shadcnspace.com/docs/getting-started/blocks](https://shadcnspace.com/docs/getting-started/blocks)                               | Marketing, hero, pricing, testimonials, bento grids, and dashboards            |
| **AI Prompting Guide**            | [https://shadcnspace.com/docs/getting-started/copy-prompt](https://shadcnspace.com/docs/getting-started/copy-prompt)                     | Prompts for single-pass landing pages and dashboard composition                |
| **Interactive CLI Builder**       | [https://shadcnspace.com/cli](https://shadcnspace.com/cli)                                                                               | Custom visual command builder for styles, themes, and icons                    |
| **Open in v0 Guide**              | [https://shadcnspace.com/docs/getting-started/open-v0](https://shadcnspace.com/docs/getting-started/open-v0)                             | Opening and customizing ShadcnSpace blocks inside v0                           |
| **Interactive Blocks Gallery**    | [https://shadcnspace.com/blocks](https://shadcnspace.com/blocks)                                                                         | Visual live preview and copy code for all 500+ blocks                          |
| **Components Catalog**            | [https://shadcnspace.com/components](https://shadcnspace.com/components)                                                                 | Micro-interactions, animated text, dock, marquee                               |
| **Full Page Templates**           | [https://shadcnspace.com/templates](https://shadcnspace.com/templates)                                                                   | Complete production-ready page templates                                       |
| **GitHub Issues & Community**     | [https://github.com/shadcnspace/shadcnspace/issues](https://github.com/shadcnspace/shadcnspace/issues)                                   | Bug reports, feature requests, and community discussions                       |

---

## Design System & Anti-Slop Rules

1. **Semantic Design Tokens**:
   Use CSS variables and semantic Tailwind classes:
   `bg-background`, `bg-card`, `text-foreground`, `text-muted-foreground`, `border-border`, `bg-primary text-primary-foreground`.
   **Never** use arbitrary hardcoded hex codes (`bg-[#0a0a0a]`).
2. **Dual-Theme Parity**:
   All blocks must look polished in both Light and Dark mode without contrast issues.
3. **Primitives Compatibility**:
   Supports both **Base UI** (`render` prop) and **Radix UI** (`asChild` prop).
4. **Motion Restraint**:
   Use purposeful spring micro-interactions (`motion/react`). Always respect `prefers-reduced-motion`.
5. **Interactive Link Polish**:
   Every `<a>` element must feature an explicit hover state (`hover:underline`, `hover:text-primary`).
   Never nest `<button>` inside `<a>` or vice-versa.
