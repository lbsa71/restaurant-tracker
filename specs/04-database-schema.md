# 04-database-schema

> Epic: Database & Auth
> Dependencies: 03-supabase-setup

## Goal

Create database migrations for profiles, restaurants, and reviews tables.

## Requirements
- profiles: id, user_id, display_name, avatar_url, created_at
- restaurants: id, name, address, city, cuisine_type, category, booking_url, created_by, created_at
- reviews: id, restaurant_id, user_id, rating (1-5), review_text, visited_at, created_at
- RLS policies for all tables (users can CRUD own data, read others)

## Done when
- [ ] `supabase db reset` runs migrations
- [ ] Tables visible in Supabase Studio
- [ ] RLS policies active
- [ ] src/lib/database.types.ts generated
