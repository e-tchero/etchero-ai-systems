# etchero-ai-systems

Vite + React + TypeScript scaffold with Tailwind and shadcn/ui.

## Status: scaffold only

This repository currently contains configuration and nothing to run:

- `vite.config.ts` (including a debug collector plugin that writes browser
  logs to disk), `tsconfig.json`, `tsconfig.node.json`
- `components.json` for the shadcn/ui CLI
- `.prettierrc` / `.prettierignore`
- `package.json`, `pnpm-lock.yaml`

There is no `index.html`, no `src/` directory and no entry point, so
`pnpm dev` and `pnpm build` have nothing to start or compile.

## Getting it running

```sh
pnpm install
```

Then add the missing pieces:

1. `index.html` with `<script type="module" src="/src/main.tsx"></script>`
2. `src/main.tsx` rendering your root component, and `src/App.tsx`
3. `src/index.css` imported from `main.tsx` (Tailwind is configured through
   `@tailwindcss/vite`)
4. `src/lib/utils.ts` with the `cn` helper that shadcn/ui components import

After that `pnpm dev` starts the dev server and `pnpm build` produces a
production bundle.
