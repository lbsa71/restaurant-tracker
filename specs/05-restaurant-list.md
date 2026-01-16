# 05-restaurant-list

> Epic: Core Restaurant CRUD
> Dependencies: 04-auth-pages

Skapa huvudsida som visar användarens restauranger.

## Krav
- Lista alla restauranger för inloggad user
- Visa namn, cuisine, rating, price range
- Klickbar rad → detalj-sida
- "Lägg till" knapp
- Empty state om inga restauranger

## E2E Test
Skriv `e2e/restaurants.spec.ts` som verifierar:
- Sidan laddar för inloggad user
- Empty state visas utan data

## Klart när
- [ ] `npm run build` passerar
- [ ] E2E-test passerar
- [ ] Restauranger hämtas från Supabase
