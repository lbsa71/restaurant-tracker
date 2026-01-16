# 02-database-schema

> Epic: Foundation
> Dependencies: 01-project-setup

Skapa Supabase databasschema för restaurants.

## Krav
- `restaurants` tabell med alla fält
- Row Level Security (RLS) policies
- SQL migration fil

## Datamodell
```sql
CREATE TABLE restaurants (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES auth.users NOT NULL,
  name TEXT NOT NULL,
  cuisine TEXT,
  address TEXT,
  price_range INT CHECK (price_range BETWEEN 1 AND 4),
  rating INT CHECK (rating BETWEEN 1 AND 5),
  review TEXT,
  visited_at DATE,
  is_favorite BOOLEAN DEFAULT false,
  want_to_revisit BOOLEAN DEFAULT false,
  photo_url TEXT,
  created_at TIMESTAMPTZ DEFAULT now()
);

ALTER TABLE restaurants ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Users can CRUD own restaurants"
  ON restaurants FOR ALL
  USING (auth.uid() = user_id);
```

## Klart när
- [ ] SQL fil skapad i `supabase/migrations/`
- [ ] Schema dokumenterat
