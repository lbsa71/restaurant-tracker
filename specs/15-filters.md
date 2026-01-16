# 15-filters

> Epic: Search & Discovery
> Dependencies: 14-search-bar

## Goal

Filter restaurants by cuisine, rating, and category.

## Requirements
- FilterBar component with dropdowns/chips
- Filter by: cuisine_type, category, minimum rating
- Multiple filters can be combined
- Filters persist in URL query params
- Clear all filters button

## E2E Test
Write `e2e/search-filter.spec.ts` that verifies:
- User can filter by cuisine
- User can filter by minimum rating
- Filters combine correctly

## Done when
- [ ] `npm run build` passes
- [ ] E2E test passes
- [ ] Filters update URL and persist on refresh
