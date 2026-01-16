# CLAUDE.md - restaurant-tracker

## Project

A restaurant discovery and review platform where users can register restaurants they've visited, give ratings and reviews, and search for recommendations. Includes a Slack integration with an AI agent for recommendations.

## Stack

- Frontend: React 18+ with Vite
- Styling: Tailwind CSS (dark mode, minimalist like polestar.com)
- Backend: Supabase (PostgreSQL, Auth, Realtime)
- Language: TypeScript
- Testing: Vitest for unit tests, Playwright for E2E

## Project Structure

```
src/
├── components/
│   ├── ui/           # General UI components (Button, Input, Card, etc.)
│   ├── auth/         # Auth-related components
│   ├── restaurant/   # Restaurant components (Card, List, Form, etc.)
│   ├── review/       # Review components
│   └── search/       # Search and filter components
├── hooks/            # Custom React hooks
├── contexts/         # React contexts
├── lib/              # Utilities (supabase client, etc)
├── pages/            # Route components
└── types/            # TypeScript types
```

## Code Rules

### Components

- One component per file
- Named exports (not default)
- Each folder has `index.ts` that re-exports all components

```typescript
// src/components/ui/index.ts
export { Button } from './Button'
export { Input } from './Input'
export { Card } from './Card'
```

### Hooks

- Prefix with `use`
- Return object with named values
- Handle loading and error states

```typescript
export function useRestaurants() {
  const [restaurants, setRestaurants] = useState<Restaurant[]>([])
  const [loading, setLoading] = useState(true)
  const [error, setError] = useState<string | null>(null)

  // ...

  return { restaurants, loading, error, addRestaurant, updateRestaurant, deleteRestaurant }
}
```

### Supabase

- Client in `src/lib/supabase.ts`
- Types in `src/lib/database.types.ts`
- RLS policies for all data
- Use `user_id` for row-level access

### Styling

- Use Tailwind utility classes
- Dark mode by default (like polestar.com)
- Minimalist design with clean typography
- Define design tokens in `tailwind.config.js`
- Use CSS variables for themes

### Testing

- **Unit tests required** for all components and hooks
- Use Vitest for unit testing
- Use Playwright for E2E tests
- Run tests before completing each epic

## Verification

After each epic, run:
```bash
npm run build          # No compile errors
npm test               # Unit tests pass
npx playwright test    # E2E tests pass
```

## E2E Tests (Playwright)

E2E tests should test **entire user flows**, not just that the page loads.

**Requirements for auth apps:**
- Test login flow
- Fetch magic link from Mailpit (`localhost:54324`) if needed
- Verify user reaches correct page after login
- Test CRUD operations as logged-in user

## Supabase Setup

Before auth development:
```bash
supabase start                    # Start local instance
supabase db reset                 # Run migrations
# Update .env.local with credentials from 'supabase status'
```

## Port Exposure for Testing

For external testing (browser outside VM):
```bash
# Dev server on all interfaces
npm run dev -- --host 0.0.0.0

# Supabase is already exposed on 0.0.0.0:54321
```

**Important for E2E tests:**
- Playwright runs headless on VM
- Mailpit for magic links: `http://localhost:54324`
- API for fetching mail programmatically: `http://localhost:54324/api/v1/messages`

## Security Rules

CRITICAL - NEVER do:
- rm -rf / or sudo rm
- curl | bash or wget | bash
- Expose credentials in code
- Commit .env files
- Hardcode API keys

SECRETS HANDLING:
- .env files NEVER in repo
- Use import.meta.env.VITE_* for frontend env vars
- .gitignore MUST contain .env*

## Common Mistakes

1. **Forgotten export** - New component must be added to index.ts
2. **Missing prop** - Check that all required props are passed
3. **Supabase not started** - Gives "Failed to fetch" in browser
4. **RLS blocking** - Check policies if data not showing
5. **Wrong redirect URL** - Check `supabase/config.toml` site_url

## Workflow

1. Read spec carefully
2. Implement step by step
3. Write unit tests for each component/hook
4. Run tests often
5. Output `<promise>DONE</promise>` when done
