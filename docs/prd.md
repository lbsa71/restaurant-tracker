# Product Requirements Document - restaurant-tracker

## Overview

**Project Name:** restaurant-tracker
**Type:** Greenfield (new project)
**Description:** A restaurant discovery and review platform where users can register restaurants they've visited, give ratings and reviews, and search for recommendations. Includes a Slack integration with an AI agent that provides restaurant recommendations based on criteria like type, rating, or popularity.

## Tech Stack

- **Frontend:** React 18+ with Vite
- **Styling:** Tailwind CSS
- **Backend:** Supabase (PostgreSQL, Auth, Realtime)
- **Language:** TypeScript
- **Testing:** Full unit test coverage required

## Design Requirements

- **Style Reference:** polestar.com
- **Theme:** Dark mode, minimalist
- **Aesthetic:** Clean, Scandinavian design with lots of white space, clean typography, dark/light contrast

## Features

### Core Platform Features

1. **User Authentication**
   - User registration
   - User login/logout
   - Session management via Supabase Auth

2. **Restaurant Management**
   - Add restaurants (name, location, type, cuisine)
   - Edit restaurant details
   - Delete restaurants

3. **Ratings & Reviews**
   - Rate restaurants (1-5 stars)
   - Write text reviews
   - View reviews from other users

4. **Search & Discovery**
   - Search restaurants by name, type, or cuisine
   - Browse and filter by rating, popularity, category
   - View restaurant details

5. **User Profiles**
   - User profile page
   - Visit history
   - User's reviews and ratings

6. **Book a Table**
   - Link to restaurant's own booking system
   - External redirect to booking page

### Slack Integration Features

7. **Slack Bot Integration**
   - Connect workspace to platform
   - Bot responds to commands in channels

8. **AI-Powered Recommendations**
   - Natural language queries in Slack
   - Fetch relevant restaurant data based on:
     - Type (lunch, dinner, etc.)
     - Rating threshold
     - Popularity
     - Cuisine type
   - Present concise, useful suggestions in Slack

## Constraints & Requirements

- **Testing:** Full unit test coverage required
- **Backend:** Must use Supabase
- **Security:** RLS policies for all data, no credentials in code

## Database Schema (Suggested)

```
users (managed by Supabase Auth)
  - id, email, created_at

profiles
  - id, user_id, display_name, avatar_url, created_at

restaurants
  - id, name, address, city, cuisine_type, category, booking_url, created_at, created_by

reviews
  - id, restaurant_id, user_id, rating (1-5), review_text, visited_at, created_at

slack_workspaces
  - id, workspace_id, access_token, created_at
```

## VM/Deploy Configuration

- **Provider:** ssh
- **Region:** eu-west-1
- **VM Name:** ralph-sandbox
- **GitHub User:** lbsa71

## Setup Notes

- Supabase credentials to be configured later in `.env.local`
- Required environment variables:
  - `VITE_SUPABASE_URL`
  - `VITE_SUPABASE_ANON_KEY`
  - Slack bot tokens (for Slack integration)
