# 12-review-form

> Epic: Reviews & Ratings
> Dependencies: 11-star-rating

## Goal

Form to submit a review for a restaurant.

## Requirements
- ReviewForm component on restaurant detail page
- Fields: star rating (required), review text (optional), visited_at date
- Submit saves to reviews table with user_id
- One review per user per restaurant (upsert)
- Only visible when logged in

## E2E Test
Write `e2e/review.spec.ts` that verifies:
- User can submit review with rating
- Review appears on restaurant page

## Done when
- [ ] `npm run build` passes
- [ ] E2E test passes
- [ ] Review saves to database
