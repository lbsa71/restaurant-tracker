# 05-auth-context

> Epic: Database & Auth
> Dependencies: 04-database-schema

## Goal

Create React context for authentication with Supabase.

## Requirements
- AuthProvider wrapper component
- useAuth hook returning: user, loading, signIn, signUp, signOut
- Automatic session refresh on mount
- Profile creation on first sign up

## Done when
- [ ] `npm run build` passes
- [ ] useAuth hook works in components
- [ ] Session persists on refresh
