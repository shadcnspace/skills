# ShadcnSpace Skills

[![Website](https://img.shields.io/badge/Website-shadcnspace.com-black?style=flat-square)](https://shadcnspace.com)
[![Registry](https://img.shields.io/badge/Registry-Shadcn%20CLI-blue?style=flat-square)](https://shadcnspace.com/r)
[![MCP Server](https://img.shields.io/badge/MCP%20Server-mcp.shadcnspace.com-purple?style=flat-square)](https://mcp.shadcnspace.com/mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

Official AI agent skill and developer guide for [ShadcnSpace](https://shadcnspace.com) - the premier open-source distribution and registry of 1000+ Shadcn resources for React, Next.js App Router, Tailwind CSS v4, Base UI, and Radix UI.

---

## What is Inside?

| Resource Type | Count | Highlights |
| :--- | :--- | :--- |
| **UI Blocks** | **521 Blocks** | Marketing (328), Dashboard UI (141), Ecommerce (42), Applications (10) |
| **UI Components** | **511 Components** | Apple Dock, Orbiting Circles, Canvas Shaders, Marquees, Micro-interactions |
| **Pre-designed Pages** | **29 Pages** | Full production pages for SaaS, Agency, Portfolio, and Dashboards |
| **Full Templates** | **13 Templates** | 10 Landing Page templates + 3 Application Dashboards (Next.js, Astro) |
| **Block Categories** | **60 Categories** | Hero sections, Pricing tables, Bento grids, AI Ops, Feature cards, FAQs |
| **Component Categories** | **68 Categories** | Animated text, Buttons, Docks, Orbiting circles, Shaders, Loaders |
| **Primitive Variants** | **Dual Variant** | Full parity across **Base UI** and **Radix UI** primitives |

---

## Quick Start - Install the Skill

Install this skill into your AI coding assistant (Cursor, Claude Code, Windsurf, Copilot, etc.):

```bash
# npm
npx skills add shadcnspace

# pnpm
pnpm dlx skills add shadcnspace

# bun
bunx skills add shadcnspace
```

### Recommended Pairing

For the best AI developer experience, install the official `shadcn/ui` skill alongside this one:

```bash
npx skills add shadcn/ui
```

- **`shadcn/ui` skill**: Gives the AI deep knowledge of core primitives, configuration, CSS variables, and theming.
- **`shadcnspace` skill**: Gives the AI deep knowledge of 1000+ ready blocks, components, pages, templates, and MCP commands.

---

## Using ShadcnSpace in Your Projects

### 1. Configure the Registry

Add the official `@shadcn-space` registry to your project's `components.json`:

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "base-nova",
  "registries": {
    "@shadcn-space": "https://shadcnspace.com/r/{name}.json"
  }
}
```

*For Pro users with a license key, pass `params` with `${EMAIL}` and `${LICENSE_KEY}`.*

### 2. Install Blocks & Components

ShadcnSpace supports both **Base UI** and **Radix UI** primitives:

#### Base UI (Recommended Default)
```bash
# Blocks
npx shadcn@latest add @shadcn-space/hero-01
npx shadcn@latest add @shadcn-space/bento-grid-01
npx shadcn@latest add @shadcn-space/pricing-01

# Full Pages
npx shadcn@latest add @shadcn-space/pages/landing-page-01
```

#### Radix UI
```bash
# Blocks
npx shadcn@latest add @shadcn-space/radix/hero-01
npx shadcn@latest add @shadcn-space/radix/bento-grid-01
npx shadcn@latest add @shadcn-space/radix/pricing-01

# Full Pages
npx shadcn@latest add @shadcn-space/pages/radix/landing-page-01
```

---

## MCP Server Integration

Connect the official ShadcnSpace MCP server to your AI IDE (Cursor, Windsurf, Claude Code, Lovable, Bolt) for instant live block search and installation during chat sessions:

### Cursor (`~/.cursor/mcp.json`)
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
*(Free tier users can omit the `headers` field).*

### Claude Code
```bash
claude mcp add shadcnspace https://mcp.shadcnspace.com/mcp
```

---

## Full Templates Directory

| Template Name | Tech Stack | Type |
| :--- | :--- | :--- |
| **Saazio** | Next.js 16, React 19, Tailwind CSS v4 | SaaS Product Landing |
| **Atomist** | Next.js & Astro versions, Tailwind CSS | Minimal SaaS Landing |
| **Awake** | Next.js & Astro versions, Tailwind CSS v4 | Agency & Portfolio |
| **Digital Arc** | Next.js & Astro versions, Tailwind CSS | Creative Agency |
| **Crypgo** | Next.js & Astro versions, Tailwind CSS | Crypto & Web3 Platform |
| **Studiova** | Next.js & Astro versions, Tailwind CSS | Design Studio Portfolio |
| **Typefolio** | Next.js 16, React 19, Tailwind CSS v4 | Developer Portfolio |
| **Resume** | Next.js 16, React 19, Tailwind CSS v4 | Interactive Resume |
| **Homely** | Next.js 16, React 19, Tailwind CSS v4 | Real Estate & Property |
| **Gleamer** | Next.js 16, React 19, Tailwind CSS v4 | Cleaning & Services |
| **AI Chatbox** | Next.js 16, React 19, Base UI | AI Chat Application |
| **AI Agent Ops** | Next.js 16, React 19, Recharts | AI Monitoring Dashboard |
| **PMS** | Next.js 16, React 19, TanStack Table | Project Management System |

---

## Helpful Links & Resources

- **Website**: [https://shadcnspace.com](https://shadcnspace.com)
- **Blocks Gallery**: [https://shadcnspace.com/blocks](https://shadcnspace.com/blocks)
- **Components Catalog**: [https://shadcnspace.com/components](https://shadcnspace.com/components)
- **Templates**: [https://shadcnspace.com/templates](https://shadcnspace.com/templates)
- **Documentation**: [https://shadcnspace.com/docs](https://shadcnspace.com/docs)
- **CLI Builder**: [https://shadcnspace.com/cli](https://shadcnspace.com/cli)
- **MCP Docs**: [https://shadcnspace.com/docs/getting-started/mcp-server-docs](https://shadcnspace.com/docs/getting-started/mcp-server-docs)
- **GitHub**: [https://github.com/shadcnspace/shadcnspace](https://github.com/shadcnspace/shadcnspace)

---

## License

This project is licensed under the [MIT License](LICENSE).
