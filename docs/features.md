# Features - Poke X Junior Portfolio

This document summarizes the main feature areas planned and developed in the private Poke X Junior project.

The public repository does not include operational source code, real database access, payment credentials, or internal server logic.

---

## Public Website

The public website was designed to give players a cleaner and more professional entry point into the game server.

Main areas:

- Landing page
- Ranking page
- News page
- Download page
- Community page
- Rules page
- Terms page
- Privacy policy page
- Donate overview page
- Free support page
- Package support page

---

## Player Account Area

The private project includes a player account area connected to the game account structure.

Planned/developed features:

- Login
- Logout
- Register
- Account dashboard
- Character listing
- Character creation
- Password change
- Character deletion with confirmation flow
- Session validation
- Blocked account handling

---

## Ranking

The ranking area was planned to display competitive player information in a clean format.

Main goals:

- Show player position
- Show character name
- Show level
- Show online/offline status
- Show equipped Pokemon information where available
- Keep technical database fields hidden from the public UI

---

## News System

The project includes a news system for server communication.

Public side:

- Dynamic news listing
- News detail page
- Category display
- Image support
- Published/draft separation

Admin side:

- Protected admin dashboard
- Create news
- Edit news
- Delete news
- Draft/publish workflow
- Image upload
- Preview before publishing

---

## Donate/Pix Planning

The private project separates support flows into two models:

### Free Support

- Player chooses an amount
- Amount maps to account points/diamonds
- Selected character is used as visual/support reference
- No direct item delivery

### Package Support

- Player chooses a predefined package
- Player selects a target character
- The system creates a package order
- Package items are stored for later delivery
- Delivery is designed for a safe internal storage/depot flow
- First-purchase rewards are handled separately

Real payments are not active in this public portfolio.

---

## Admin Features

Administrative features are protected in the private project.

Main areas:

- Admin-only news dashboard
- News management
- Secure upload handling
- Manual package delivery route planning
- Role-based admin checks

---

## Security-Oriented Features

The private project includes:

- HTTP-only session cookie handling
- Rate limiting on sensitive routes
- Upload validation
- Magic byte validation for uploaded files
- Path traversal protection
- Basic security headers
- Private environment variables
- Payment flow disabled until production deployment
- Separate private and public repository strategy

---

## Public Portfolio Scope

This public repository is documentation-focused.

It is designed to show:

- Project scope
- Feature planning
- Security awareness
- Architecture decisions
- Product thinking
- Screenshots and visual result

It intentionally does not expose the full operational implementation.