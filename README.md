# 🚀 Next.js + shadcn/ui + Biome Template

This is a template repository based on Next.js (App Router), combining `shadcn/ui` and `Biome`.  
It is intended to reduce the initial setup needed when starting a new project.

## ✨ What This Repository Includes

- ⚡ Next.js 16 + React 19 + TypeScript
- 🎨 Tailwind CSS v4
- 🧩 shadcn/ui
- 🧹 Biome (formatting / linting)
- ✅ Biome CI with GitHub Actions

## 🧭 Intended Usage

- Duplicate this repository as a template to start a new project
- Add required shadcn/ui components as you build

## 📦 Requirements

- Node.js 20 or later
- pnpm

## 🏁 Getting Started

```bash
pnpm install
pnpm dev
```

Open [`http://localhost:3000`](http://localhost:3000) to check it is running.

## 🛠️ Commands

```bash
pnpm dev      # Start the development server
pnpm build    # Build for production
pnpm start    # Start in production mode
```

### 🧪 Code Quality Checks

```bash
pnpm exec biome check .         # Run format/lint checks
pnpm exec biome check --write . # Apply automatic fixes
pnpm exec biome ci .            # Run checks equivalent to CI
```

## 🧩 Adding shadcn/ui Components

`components.json` is already configured.

```bash
pnpm dlx shadcn@latest add button
```

A `cn` utility (`clsx` + `tailwind-merge`) is provided in `lib/utils.ts`.

## 🔄 CI

The following is run via `.github/workflows/biome.yml`.

- `pull_request`
- `push` to the `main` branch
- `pnpm exec biome ci .`

## 🗂️ Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── biome.yml            # Biome CI workflow
├── app/
│   ├── globals.css              # Global styles
│   ├── layout.tsx               # Root layout
│   └── page.tsx                 # Top page
├── lib/
│   └── utils.ts                 # `cn` utility
├── biome.json                   # Biome configuration
├── components.json              # shadcn/ui configuration
├── next.config.ts               # Next.js configuration
├── package.json                 # scripts / dependencies
├── pnpm-lock.yaml               # pnpm lockfile
├── postcss.config.mjs           # PostCSS configuration
└── tsconfig.json                # TypeScript configuration
```

## 🚀 How to Use as a Template

1. Click `Use this template` on GitHub and create a new repository
2. Clone the created repository
3. Run `pnpm install`
4. Replace the initial page (`app/page.tsx`) and start development

## 💡 Glossary

- `Use this template`:  
  A GitHub feature that creates a new, separate repository based on this one.
- `new-york`:  
  The name of a shadcn/ui style preset (`style` in `components.json`).

## 📚 References

- Next.js Docs: https://nextjs.org/docs
- shadcn/ui Docs: https://ui.shadcn.com/docs
- Biome Docs: https://biomejs.dev/guides/getting-started/
