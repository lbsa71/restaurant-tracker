# 10-edit-delete-restaurant

> Epic: Restaurant CRUD
> Dependencies: 09-restaurant-detail

## Goal

Allow restaurant creator to edit or delete their restaurants.

## Requirements
- Edit button on detail page (only for creator)
- /restaurants/:id/edit page with pre-filled form
- Delete button with confirmation dialog
- RLS ensures only creator can edit/delete

## E2E Test
Write `e2e/restaurant-edit.spec.ts` that verifies:
- Creator can edit restaurant
- Creator can delete restaurant
- Non-creator cannot see edit/delete buttons

## Done when
- [ ] `npm run build` passes
- [ ] E2E test passes
- [ ] Only creator can modify restaurant
