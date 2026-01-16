# 01-project-setup

> Epic: Foundation
> Dependencies: None

Sätt upp Vite + React + TypeScript + Tailwind + Playwright.

## Krav
- Vite React TypeScript projekt
- Tailwind CSS konfigurerat
- Playwright installerat med smoke test
- Supabase client installerat

## Kommandon
```bash
npm create vite@latest . -- --template react-ts
npm install
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm install -D @playwright/test
npx playwright install
npm install @supabase/supabase-js
```

## E2E Test
Skriv `e2e/smoke.spec.ts` som verifierar:
- App laddar utan errors

## Klart när
- [ ] `npm run dev` fungerar
- [ ] `npm run build` passerar
- [ ] `npx playwright test` passerar
