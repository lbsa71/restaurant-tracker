# 06-restaurant-form

> Epic: Core Restaurant CRUD
> Dependencies: 05-restaurant-list

Skapa formulär för att lägga till och redigera restauranger.

## Krav
- Fält: name, cuisine, address, price_range, rating, review, visited_at
- Checkboxar: is_favorite, want_to_revisit
- Validering (name required)
- Funkar för både create och edit mode
- Sparar till Supabase

## E2E Test
Skriv `e2e/restaurant-form.spec.ts` som verifierar:
- Formulär visas
- Validering fungerar
- Kan fylla i och spara

## Klart när
- [ ] `npm run build` passerar
- [ ] E2E-test passerar
- [ ] Create och edit fungerar
