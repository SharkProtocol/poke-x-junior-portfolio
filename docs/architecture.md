# Architecture - Poke X Junior Portfolio

This document describes the high-level architecture of the private Poke X Junior web project.

The public repository does not expose operational source code, real credentials, database dumps, internal server details, or payment implementation logic.

---

## Architecture Goals

The project was designed with the following goals:

* Provide a modern web interface for a game server
* Separate public pages from authenticated player features
* Provide protected administrative tools
* Integrate with an existing game database structure
* Prepare a safe Donate/Pix flow for future production use
* Avoid exposing sensitive environment variables
* Keep the operational project in a private repository
* Maintain a separate public portfolio repository

---

## High-Level Structure

The private implementation follows a web application structure similar to:

```txt
web application
|-- public pages
|-- player account area
|-- admin area
|-- server-side API routes
|-- database access layer
|-- authentication/session helpers
|-- donate/payment helpers
|-- upload handling
|-- security utilities
```

---

## Main Layers

### 1. Public Interface

The public interface contains pages for visitors and players.

Examples:

* Landing page
* Ranking
* News
* Download
* Community
* Rules
* Terms
* Privacy policy
* Donate overview

This layer focuses on presentation, onboarding, server information, and player trust.

---

### 2. Player Account Layer

The authenticated account layer allows players to manage their account-related actions.

Examples:

* Login
* Logout
* Register
* Account dashboard
* Character listing
* Character creation
* Password change
* Safe character deletion flow

This layer communicates with server-side API routes and validates session state before exposing private account data.

---

### 3. Admin Layer

The admin layer is protected and restricted to authorized accounts.

Examples:

* News management dashboard
* Create/edit/delete news
* Draft and publish workflow
* Secure image upload
* Manual package delivery planning

The goal is to give the server team operational tools without exposing admin functionality to regular players.

---

### 4. API Layer

The private implementation uses server-side API routes for controlled operations.

Main API areas:

* Authentication
* Account data
* Character actions
* Ranking
* Server status
* News management
* Uploads
* Donate/Pix status
* Package order planning
* Future payment webhook handling

The public portfolio does not expose the implementation of these routes.

---

### 5. Database Layer

The private project is designed to communicate with a MySQL/MariaDB database.

The database layer is responsible for:

* Reading account data
* Reading character data
* Reading ranking data
* Managing site news
* Managing admin permissions
* Registering donate-related orders
* Preparing safe delivery records

The public repository does not include real database dumps, real schema exports, user data, character data, payment history, or account records.

---

### 6. Donate/Pix Planning Layer

The Donate/Pix structure is separated into conceptual areas:

* Free support flow
* Package support flow
* Payment order registration
* Package item registration
* First-purchase reward rules
* Delivery status tracking
* Future webhook validation

In the private project, real payment activation is intentionally disabled until the final VPS/domain deployment is ready.

---

## Security Boundaries

The project separates public and private concerns:

```txt
public portfolio repository
|-- documentation
|-- screenshots
|-- architecture notes

private operational repository
|-- real source code
|-- API logic
|-- database access
|-- admin behavior
|-- payment planning

production environment
|-- real environment variables
|-- production database
|-- payment credentials
|-- webhook secrets
```

This separation reduces the risk of exposing sensitive implementation details.

---

## Repository Strategy

The project uses two different repository purposes.

### Private Repository

Used for:

* Real development
* Operational code
* Internal documentation
* Deployment planning
* Security checklists
* Git history of the actual project

### Public Portfolio Repository

Used for:

* Case study
* Screenshots
* Feature documentation
* Architecture overview
* Security notes
* Professional presentation

The public repository is not intended to be a cloneable production template.

---

## Deployment Strategy

The private project follows a cautious deployment order:

1. Finish and validate the local project
2. Keep the private repository synchronized
3. Prepare public portfolio documentation separately
4. Deploy only when VPS/domain are ready
5. Configure production environment variables
6. Configure HTTPS
7. Validate database access
8. Enable payment webhook only after production readiness
9. Keep payment flow disabled until all checks pass

---

## Future Improvements

Possible future improvements include:

* Production-ready deployment documentation
* External object storage for uploads
* Redis-based rate limiting
* Reverse proxy hardening
* Observability/logging strategy
* More complete CI checks
* Public screenshots and UI walkthroughs
* Mocked demo version without operational backend logic
