# DecodeHer Landing Page — Context

This repo is the **marketing landing page** for DecodeHer (an Android app). It is a static site (`index.html`, `privacy-policy.html`, `terms.html`, `delete-account.html`) styled with Tailwind (CDN) + custom CSS, dark editorial aesthetic.

This file distills only what's needed to write/extend landing page copy and design — not full app internals. Full app context (if ever needed) lives in `.app_context/`.

---

## What DecodeHer Is

An Android app that translates a woman's indirect, emotion-driven messages into plain, factual language for men — bridging the "emotional language gap" (Mars/Venus thesis).

**Core loop (the thing to sell):** Paste her message → pick the relationship context → get back a translation, her likely tone, what to watch for, and suggested replies.

**Brand philosophy / voice:** "Building relationships through understanding, not manipulation." Warm, intimate, human — never clinical, never a pickup-artist / manipulation tool. This framing matters for App Store/ad compliance and for not coming across as creepy or exploitative. Lean into *empathy and clarity*, not "decode women like a hacking trick."

**Tagline used on site:** "Understand Her, Actually"

---

## Who It's For / Relationship Contexts

The app adapts its tone per relationship type — useful for landing page sections that show "works for every relationship in your life":

- `new_match` — just matched on a dating app
- `dating` — been on a few dates
- `girlfriend` — committed relationship
- `wife` — married / long-term partner
- Family: `daughter`, `mother`, `sister`

Dating contexts get direct/honest framing (signals, interest level); relationship contexts get empathetic, relationship-preserving framing; family contexts adapt per dynamic.

---

## Headline Features (good landing-page section material)

1. **Decode** — paste a message, get translation + tone + "watch for" + suggested replies, tailored to the relationship.
2. **Screenshot import (OCR)** — share or upload a chat screenshot; the app extracts the conversation automatically (WhatsApp, Instagram, Telegram, Tinder, Hinge, Bumble, iMessage, Snapchat, etc.).
3. **Voice note decoding** — transcribes a voice message and reads the emotional tone behind it (Plus/Pro).
4. **Ask About Her** — a relationship-aware Q&A assistant that knows the context of the relationship (Plus/Pro).
5. **Longitudinal profile summaries** — the app learns the relationship over time and gets sharper with use (every 5 decodes).
6. **Her Rhythm** — optional menstrual-cycle awareness for girlfriend/wife profiles, so advice accounts for where she is in her cycle.
7. **Multi-language support** — works across languages/scripts (e.g., responds in Tamil/Hindi/etc. with natural reply suggestions in her language).
8. **Behavioral flags** — gently flags potentially serious patterns (manipulation, gaslighting, betrayal, blame-shifting) — *only when clearly evidenced*, framed as protective, not paranoid.

---

## Privacy & Trust (strong selling point — emphasize on landing page)

This is a major differentiator and trust-builder; worth a dedicated section:

- **Everything stays on the phone.** Conversations are stored in an encrypted local database (SQLCipher). The backend is stateless and never stores message content.
- Each user gets their own encrypted, isolated database file.
- Use this to counter the obvious objection: *"Wait, am I uploading her private messages to some server?"* — Answer: no, it's encrypted and local, and the backend doesn't retain message content.

---

## Pricing / Tiers (for a pricing section)

| Tier | Price | Decodes/day | Ask | OCR/day | Voice/day | Profiles |
|------|-------|-------------|-----|---------|-----------|----------|
| Free | — | 5 | ✗ | 10 | ✗ | 1 |
| Plus | €4.99/mo | 30 | ✓ | 30 | 10 | 5 |
| Pro | €9.99/mo | 75 | ✓ | 75 | 30 | unlimited |

Sold via Google Play Billing / RevenueCat (Android only for now; iOS planned later).

---

## Design Language (keep landing page visually consistent with the app)

**Palette:**
| Token | Hex | Usage |
|---|---|---|
| Background | `#0D0F14` / `#1d1b25` (site bg) | base |
| Accent (amber) | `#F5A623` | primary brand accent — buttons, highlights, the "Her" wordmark |
| Surface/card | `#1A1E28` / `#11131A` | cards, panels |
| Warm card | `#1C1720` | profile-card style surfaces |
| Destructive/red | `#C0394F` | |
| Muted text | `#9CA3AF` | |
| Body text | `#E5E7EB` / `#f3f4f6` | |

**Relationship accent colors** (useful if showing relationship-type chips/cards):
`new_match` `#7C4DFF` · `dating` `#00E5FF` · `girlfriend` `#FF4081` · `wife` `#FF6E40` · `daughter` `#66BB6A` · `mother` `#FFB74D` · `sister` `#BA68C8`

**Typography:** `Fraunces` (serif, editorial) for display/headline type, system-ui for body. The site already uses an editorial "manifesto" style for the philosophy section (large ghost numerals, italic accent marks with amber underline highlight).

**Tone of visuals:** dark, warm, intimate — frosted glass cards, amber glow, soft shadows. Never cold/clinical blue-tech aesthetic.

---

## Links & Contact (for footer/CTAs)

- Play Store: https://play.google.com/store/apps/details?id=com.decodeher.decodeher
- Tester opt-in (currently in Closed Alpha): https://play.google.com/apps/testing/com.decodeher.decodeher
- Contact email: ligerragul@gmail.com
- Package name: `com.decodeher.decodeher`

**Current status:** Closed Testing (Alpha) on Play Store — if the landing page has a download CTA, it may need to point to the tester opt-in rather than a public listing until wider release.

---

## What NOT to Over-Index On

This is a marketing site, not the app — avoid pulling in implementation detail that doesn't serve persuasion/clarity:
- Backend architecture, API endpoints, database schemas, admin dashboard — irrelevant to visitors.
- Avoid making the "behavioral flags" feature sound alarmist/paranoid in marketing copy — frame as *gentle awareness*, not relationship-ending accusations.
- Don't oversell "decode women" in a manipulative/pickup-artist register — the brand philosophy explicitly rejects that framing in favor of empathy and understanding.
