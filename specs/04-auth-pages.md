# 04-auth-pages

> Epic: Authentication
> Dependencies: 03-auth-context

Skapa login och register sidor.

## Krav
- Login sida med email/password
- Register sida med email/password
- Redirect till /restaurants efter login
- Protected route wrapper

## E2E Test
Skriv `e2e/auth.spec.ts` som verifierar:
- Kan navigera till login
- Formulär validering visas
- Kan växla mellan login/register

## Klart när
- [ ] `npm run build` passerar
- [ ] E2E-test passerar
- [ ] Routes: /login, /register, /restaurants
