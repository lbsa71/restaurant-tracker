# 06-login-register

> Epic: Database & Auth
> Dependencies: 05-auth-context

## Goal

Create login and register pages with email/password auth.

## Requirements
- /login page with email + password form
- /register page with email + password + display name
- Error messages for invalid credentials
- Redirect to / after successful auth
- Dark mode minimalist design (polestar style)

## E2E Test
Write `e2e/auth.spec.ts` that verifies:
- User can register with email/password
- User can login after registering
- Invalid login shows error

## Done when
- [ ] `npm run build` passes
- [ ] E2E auth test passes
- [ ] Can register and login as new user
