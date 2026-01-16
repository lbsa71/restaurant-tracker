# 18-visit-history

> Epic: User Profiles
> Dependencies: 17-profile-page

## Goal

Show user's restaurant visits and reviews on profile.

## Requirements
- "My Visits" tab on profile page
- List of restaurants user has reviewed
- Shows: restaurant name, rating given, visited_at date
- Click to go to restaurant detail
- Sorted by visited_at descending

## E2E Test
Write `e2e/profile.spec.ts` that verifies:
- User can see their visit history
- Visit links to restaurant detail

## Done when
- [ ] `npm run build` passes
- [ ] E2E test passes
- [ ] Visit history displays correctly
