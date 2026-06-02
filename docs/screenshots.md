# Screenshots - Poke X Junior Portfolio

This document defines the screenshot strategy for the public Poke X Junior portfolio repository.

Screenshots should demonstrate the visual quality and product structure without exposing private information, operational data, payment details, database information, or admin-only sensitive content.

---

## Screenshot Goals

Screenshots should show:

* Visual quality
* UI consistency
* Game website presentation
* Player-facing experience
* Admin workflow concept, if safely sanitized
* Ranking layout
* News layout
* Donate/Pix planning screen without real payment data
* Account dashboard with fake or blurred data

The goal is to sell the quality of the work without exposing the operational product.

---

## Recommended Screenshots

### 1. Home Page

Suggested file:

```txt
screenshots/home.png
```

Show:

* Hero section
* Main call-to-action
* Visual identity
* Server presentation
* Public navigation

Avoid:

* Real private URLs
* Debug overlays
* Admin-only data

---

### 2. Ranking Page

Suggested file:

```txt
screenshots/ranking.png
```

Show:

* Ranking cards/table
* Player position
* Level display
* Equipped Pokemon visual, if safe
* Clean competitive layout

Avoid:

* Internal database fields
* Raw IDs
* Technical debug values
* Sensitive player information

---

### 3. Account Dashboard

Suggested file:

```txt
screenshots/account-dashboard.png
```

Show:

* General account dashboard layout
* Character cards
* Buttons and navigation

Use only:

* Fake account names
* Fake character names
* Blurred private data
* Demo-only data

Avoid:

* Real account email
* Real account ID
* Real admin status
* Real private character details

---

### 4. News System

Suggested file:

```txt
screenshots/news.png
```

Show:

* News listing
* News card layout
* Category badges
* Image support

Avoid:

* Admin-only draft data
* Internal upload paths
* Private images

---

### 5. Admin News Panel

Suggested file:

```txt
screenshots/admin-news.png
```

Only include this if fully sanitized.

Show:

* News management concept
* Create/edit interface
* Preview layout

Avoid:

* Real admin account
* Real internal IDs
* Real private uploaded images
* Any tokens or backend errors

---

### 6. Donate Pages

Suggested files:

```txt
screenshots/donate-overview.png
screenshots/donate-packages.png
screenshots/donate-free-support.png
```

Show:

* Package presentation
* Support flow concept
* Safety notices
* Payment-disabled state

Avoid:

* Real Pix QR Code
* Real payment ID
* Mercado Pago details
* Buyer data
* Webhook data
* Internal item delivery IDs, if not meant to be public

---

### 7. Download Page

Suggested file:

```txt
screenshots/download.png
```

Show:

* Download card layout
* Platform choices
* Terms/rules acceptance concept

Avoid:

* Private client links
* Real unpublished download URLs
* Internal file paths

---

## Screenshot Naming Rules

Use simple lowercase names:

```txt
home.png
ranking.png
account-dashboard.png
news.png
admin-news.png
donate-overview.png
donate-packages.png
donate-free-support.png
download.png
community.png
```

Avoid spaces and special characters.

---

## Sanitization Checklist

Before adding screenshots, confirm:

* No real email is visible
* No payment token is visible
* No Pix QR Code is visible
* No payment ID is visible
* No admin-only secret is visible
* No internal database ID is visible
* No debug output is visible
* No local filesystem path is visible
* No real VPS/domain secret is visible
* No private Discord/admin channel is visible
* No private upload path is visible

---

## Editing Recommendations

Before publishing screenshots:

* Blur sensitive text
* Crop browser tabs if needed
* Remove bookmarks bar if visible
* Remove local filesystem paths
* Use fake/demo names when possible
* Prefer full-page clean captures
* Keep consistent image dimensions
* Use PNG for UI clarity

---

## Public Portfolio Rule

Screenshots are meant to prove the work visually.

They should not reveal how to clone, operate, exploit, or reproduce the private system.

Show the result. Do not expose the machinery.
