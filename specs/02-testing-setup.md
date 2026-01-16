# 02-testing-setup

> Epic: Foundation
> Dependencies: 01-project-setup

## Goal

Set up Playwright for E2E tests and Vitest for unit tests.

## Requirements
- Playwright installed with `npx playwright install`
- playwright.config.ts configured for localhost:5173
- Vitest configured for unit tests
- e2e/smoke.spec.ts that loads the app

## E2E Test
Write `e2e/smoke.spec.ts` that verifies:
- App loads at /
- Page has content visible

## Done when
- [ ] `npx playwright test` passes
- [ ] `npm test` runs unit tests
- [ ] Smoke test verifies app loads
