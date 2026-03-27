# Feature: Login

## Overview
Registered users can log in using their email address and password.

## Behaviour

### Happy Path
- User navigates to `/login`
- Enters valid email and password
- Clicks "Sign In"
- Is redirected to their account dashboard at `/account`

### Error States
- If email is not registered: show "No account found with that email"
- If password is wrong: show "Incorrect password"
- If either field is empty: show "Please fill in all fields"

### Password Rules
- Minimum 8 characters
- At least one number
- At least one uppercase letter

### Session
- User stays logged in for 30 days unless they log out
- "Remember Me" checkbox extends this to 90 days

## Out of Scope (not yet built)
- Social login (Google, Apple)
- Two-factor authentication
- Password reset flow
