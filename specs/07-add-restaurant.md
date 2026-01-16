# 07-add-restaurant

> Epic: Restaurant CRUD
> Dependencies: 06-login-register

## Goal

Create form to add new restaurants.

## Requirements
- /restaurants/new page (protected, requires auth)
- Form fields: name, address, city, cuisine_type, category, booking_url (optional)
- Save to Supabase with created_by = current user
- Redirect to restaurant detail after save

## E2E Test
Write `e2e/restaurant-add.spec.ts` that verifies:
- Logged in user can add restaurant
- Restaurant appears in list after adding

## Done when
- [ ] `npm run build` passes
- [ ] E2E test passes
- [ ] New restaurant saves to database
