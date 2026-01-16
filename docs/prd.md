# Product Requirements Document: Restaurant Tracker

## Overview

**Project Name:** restaurant-tracker
**Type:** Greenfield (new project)
**Description:** Restaurant Tracker is a lightweight web application that allows users to record, review, and manage restaurants they have visited. The product focuses on speed, clarity, and personal value rather than social or discovery features.

## Tech Stack

- **Frontend:** React + Vite + Tailwind CSS
- **Backend:** Supabase (Auth, Database, Storage)
- **Template:** react-supabase

## Features

### Core Features

1. **User Authentication**
   - User registration and login
   - Secure session management via Supabase Auth

2. **Restaurant Management**
   - Add new restaurant entries
   - Edit existing restaurant details
   - Delete restaurants from collection

3. **Personal Ratings & Reviews**
   - Rate restaurants (e.g., 1-5 stars)
   - Write personal notes/reviews for each visit

4. **Cuisine Categories**
   - Categorize restaurants by cuisine type
   - Filter restaurants by category

5. **Location Tracking**
   - Store restaurant address
   - Link to maps for directions

6. **Visit Date Tracking**
   - Record date of each visit
   - View visit history

7. **Price Range Indicator**
   - Mark restaurants by price level (e.g., $, $$, $$$, $$$$)
   - Filter by price range

8. **Favorites / Want to Revisit**
   - Mark restaurants as favorites
   - Create "want to revisit" list

9. **Search & Filter**
   - Search by restaurant name
   - Filter by cuisine, rating, price range
   - Sort by date visited, rating, name

10. **Photo Uploads**
    - Upload photos for each restaurant
    - Store images via Supabase Storage

## Design

- Use sensible defaults
- Focus on speed and clarity
- Clean, minimal UI
- Mobile-responsive design

## Constraints

- None specified

## Infrastructure

- **VM Provider:** SSH
- **VM Name:** ralph-sandbox
- **Region:** eu-west-1
- **GitHub User:** lbsa71
- **Notifications:** ntfy enabled (topic: ralph-1768566655969)

## Supabase Setup Required

Before deploying, add to `.env.local`:
```
VITE_SUPABASE_URL=your-project-url
VITE_SUPABASE_ANON_KEY=your-anon-key
```

## Success Criteria

- Users can create an account and log in
- Users can add, edit, and delete restaurant entries
- Users can rate and review restaurants
- Users can search and filter their restaurant collection
- Users can upload photos for restaurants
- Application is fast and responsive
- Data persists in Supabase database
