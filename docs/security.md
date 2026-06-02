# Security - Poke X Junior Portfolio

This document summarizes the security decisions considered in the private Poke X Junior project.

The public repository does not include real source code, real credentials, payment tokens, production environment files, database dumps, or internal server details.

---

## Security Goals

The private project was designed with the following security goals:

- Keep operational code private
- Keep secrets outside Git
- Separate public portfolio from private production code
- Protect sensitive routes
- Reduce brute-force risk
- Harden upload handling
- Avoid exposing internal database details
- Keep payments disabled until production readiness
- Avoid publishing server-specific operational logic

---

## Repository Separation

The project uses a separation strategy:

```txt
Private repository:
- real source code
- backend logic
- database access
- admin logic
- payment planning
- internal documentation

Public repository:
- portfolio documentation
- feature overview
- architecture summary
- security summary
- screenshots without private data