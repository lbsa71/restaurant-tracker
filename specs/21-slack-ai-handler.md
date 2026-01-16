# 21-slack-ai-handler

> Epic: Slack Integration
> Dependencies: 20-recommendation-api

## Goal

Parse natural language Slack messages and return recommendations.

## Requirements
- Parse queries like "good Italian for dinner" or "best rated lunch spots"
- Extract: cuisine, meal type (category), rating preference
- Call recommendation API with extracted params
- Format response as Slack blocks (cards with restaurant info)
- Handle "no results" gracefully

## Done when
- [ ] Bot parses natural language queries
- [ ] Returns formatted Slack message with recommendations
- [ ] Handles edge cases (no results, invalid query)
