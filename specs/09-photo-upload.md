# 09-photo-upload

> Epic: Photo Upload
> Dependencies: 06-restaurant-form

Lägg till foto-uppladdning för restauranger.

## Krav
- Uppladdning i restaurant form
- Supabase Storage för bilder
- Visa thumbnail på lista och detalj
- Max filstorlek 5MB
- Acceptera jpg, png, webp

## E2E Test
Skriv `e2e/photo-upload.spec.ts` som verifierar:
- Upload-knapp visas
- Felmeddelande vid för stor fil

## Klart när
- [ ] `npm run build` passerar
- [ ] E2E-test passerar
- [ ] Bild visas efter uppladdning
