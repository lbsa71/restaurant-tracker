# 20-recommendation-api

> Epic: Slack Integration
> Dependencies: 19-slack-bot-setup

## Goal

API endpoint that returns restaurant recommendations based on criteria.

## Requirements
- Edge function: POST /recommendations
- Parameters: cuisine, min_rating, category, limit
- Returns top restaurants matching criteria
- Sorted by rating * review_count (popularity score)
- Returns: name, city, cuisine, avg_rating, review_count

## Done when
- [ ] Edge function returns recommendations
- [ ] Filters work correctly
- [ ] Results sorted by relevance
