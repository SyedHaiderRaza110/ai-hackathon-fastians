# FASTIANS — Hackathon Product Strategy

> **The trusted student exchange platform for FAST students.**
> **Tagline:** Everything FAST students share, in one place.

---

## 1. Vision

FASTIANS replaces the fragmented way students discover and coordinate resources — WhatsApp groups, noticeboards, scattered messages — with a **trusted, organized exchange layer for a university community**.

Students can:
- Find academic resources
- Buy or sell useful items
- Offer or discover peer tutoring
- Offer student-to-student services
- Book peer-provided services or resources
- Contact other students through controlled requests
- Build trust through completed exchanges and reviews

This is **not** another OLX or a full e-commerce platform. The challenge brief rewards simplicity, trust, fast browsing, clear availability, and conflict-free booking over a marketplace clone with hundreds of features.

---

## 2. The Problem

Students currently rely on scattered WhatsApp groups, physical noticeboards, and individual messages to sell/find textbooks and equipment, find tutors, offer peer services, coordinate resources, and check slot availability. This causes:

1. Listings buried in chat history
2. No easy way to browse what's available right now
3. Individual back-and-forth messaging to coordinate
4. Unclear availability and double-booking
5. Little structured trust between students

**Core problem statement:** Students need a fast, trustworthy way to discover, exchange, and book resources within their own university community without digging through scattered group chats.

---

## 3. Positioning

**Don't pitch it as:** "A marketplace for FAST students."

**Pitch it as:** *FASTIANS is a trusted student exchange platform that helps FAST students discover resources, book peer services, and connect with opportunities without relying on scattered WhatsApp groups.*

A generic marketplace looks like OLX. A community exchange platform adds: university-specific context, student-to-student trust, academic resources, tutoring, peer services, booking, reputation, and campus-focused discovery.

**Guiding principle: Community first, marketplace second.** Users should be able to discover things that don't belong on OLX — *"A senior is offering DSA tutoring," "A student can review your CV," "A mentor has two slots tomorrow."*

### What FASTIANS is NOT
Not a full e-commerce platform, social network, university ERP, chat app, payment platform, room-management system, AI chatbot, or feature-collection.

---

## 4. Core Experience & Categories

The homepage answers one question immediately: **"What can I find or offer here?"**

| Category | Examples |
|---|---|
| 📚 **Resources** | Textbooks, calculators, notes, electronics, academic equipment |
| 🎓 **Tutoring** | Course tutoring, exam prep, peer mentoring |
| 💼 **Services** | CV review, graphic design, programming help, portfolio help |
| 📅 **Bookings** | Tutoring/mentorship sessions, peer-provided resources, society resources where appropriate |

---

## 5. Trust System

Every user has a simple profile:

- Name, program/batch (demo data acceptable)
- Profile image/avatar
- Average rating + number of completed exchanges
- Reviews
- Verification/status indicator

```text
Haider Raza — FAST Student
★★★★★ 4.9 · 14 completed exchanges
"Very reliable and item was exactly as described."
```

Don't build identity verification during the hackathon — a simple profile/status system is sufficient.

---

## 6. Core Exchange Flow

The platform facilitates the exchange; it does not control the physical handoff.

```text
Discover → View → Request Contact / Book → Owner Accepts / Slot Confirmed
   → Contact revealed → Students coordinate offline → Exchange completed → Review
```

**Contact system:** a lightweight request/accept flow, not full messaging.
```text
Request Contact → Owner Accepts/Declines → If accepted: contact info revealed
   → Students coordinate outside the platform
```

**Reviews** unlock only after a completed exchange or booking (1–5 stars + optional comment), and appear on the recipient's profile.

**Booking** requires a simple calendar/slot picker with clear available/booked status and no double-booking. Prioritize resources students can realistically offer (tutoring, mentorship, peer consultation, society resources). Don't claim students can book university-owned rooms — the same engine could support that later via an official integration; for the demo, use peer-managed or clearly fictional bookable resources.

```text
DSA Tutoring — Ali Ahmed — ★★★★★ 4.8
Monday: 10:00 AM Available · 11:00 AM Available · 12:00 PM Booked
[ Book a Slot ]
```

---

## 7. The "Wow" Feature — Opportunity Feed

Instead of a generic marketplace grid, show a campus-focused discovery feed. Purely rule-based, no AI required.

```text
For You
📚 PF Book — Rs. 1,500
🎓 DSA Tutor — Tomorrow, 4 PM
💼 CV Review — 3 slots available
🧮 Scientific Calculator — Rs. 2,800
```

---

## 8. Search, Discovery & Listing Creation

Search: keyword, category, type, price range, availability filter — kept simple so a student can find something in seconds.

Listing creation should take under a minute:
- **Required:** title, type, category, description, price (if applicable), availability (if bookable), contact option
- **Optional:** image, tags

No 20-field forms.

---

## 9. Screens

1. **Home** — communicates what FASTIANS does immediately
2. **Discover** — search, categories, filters, listing cards
3. **Listing Detail** — description, price, owner trust, availability, CTA
4. **Create Listing** — fast form
5. **Booking** — calendar/slot picker with live availability
6. **Contact Requests** — pending and accepted connections
7. **My Dashboard** — my listings, bookings, requests, completed exchanges
8. **Profile** — rating, reviews, completed exchanges

*(Data model lives in the [architecture doc](./architecture_readme.md) — Users, Listings, Bookings, ContactRequests, Reviews.)*

---

## 10. Visual Identity

**Name:** FASTIANS
**Tagline:** Everything FAST students share, in one place.
**Alternates:** *Buy. Book. Learn. Connect.* / *The trusted exchange for FAST students.* / *Your campus, connected.*

Use original branding — do not use official FAST-NUCES logos or imply university endorsement unless explicitly authorized. Consider a disclaimer: *"Independent student project for hackathon purposes. Not affiliated with or endorsed by FAST-NUCES."*

Design direction: fast, clean, modern, mobile-friendly, spacious, obvious, trustworthy. Avoid excessive animation, huge forms, cluttered dashboards, and fake enterprise complexity.

---

## 11. Feature Priority

| Must Have | Nice to Have | Cut First |
|---|---|---|
| Listing creation, search, categories, filters | Image uploads | AI chatbot |
| Listing detail, contact request | Opportunity feed | Payments |
| Booking slots, double-booking prevention | Saved listings | Full messaging |
| My Listings / My Bookings | Availability badges | Complex authentication |
| Basic profile, rating/review | Simple notifications | Admin panel, social feed, mobile app, university room integration |

---

## 12. 24-Hour Execution Plan

| Hours | Focus |
|---|---|
| 1–2 | Product definition: name, flow, data model, screens, demo story |
| 3–8 | Core product: home, discover, listing cards, search, filters, listing details, create listing |
| 9–13 | Booking: availability, slot picker, creation, booked/available state, double-booking prevention |
| 14–17 | Trust: profiles, contact requests, completion state, reviews, rating display |
| 18–20 | Polish: empty/loading/error states, mobile responsiveness, visual consistency |
| 21–22 | Deployment + full-flow testing |
| 23–24 | Demo prep: 3-minute demo, problem/solution slides, backup screenshots, stable demo data |

**The one rule: finish the loop.** A smaller feature set that works flawlessly beats a large one that breaks.

```text
Discover → View → Request/Book → Connect → Exchange → Complete → Review → Trust
```

---

## 13. Demo Story & Pitch

**Scenario:** a student needs a PF textbook, a DSA tutor, and a CV review.

Open FASTIANS → search "PF" → open textbook → show owner trust + details → request contact → open Tutoring → select DSA → choose a slot → book it → complete a prior transaction → leave a 5-star review → show the updated profile.

> "What previously required multiple WhatsApp groups and individual messages now takes seconds."

**Pitch:**
- *Problem:* Useful resources already exist for students — they're just scattered across WhatsApp groups, noticeboards, and private conversations.
- *Solution:* FASTIANS puts those student-to-student exchanges into one organized community.
- *Difference:* Not trying to become OLX — building a trusted exchange layer for FAST students' academic and community life.
- *Result:* Find something in seconds, book a slot without conflicts, connect with the other student, build trust through completed exchanges.

Judges should leave thinking *"That actually solves a problem we have,"* not *"They used a cool AI model."* The strongest story is real student pain + a simple solution + a complete workflow.

**Success metrics to demonstrate:** listing in under a minute · a useful search result in seconds · a booked slot in a few clicks · a visible trust history · a clear path from discovery to review.

---

## 14. AI Builder Master Prompt

Use this prompt with a coding/vibe-coding AI to scaffold the build (pair with the [architecture doc](./architecture_readme.md) for schema and technical detail):

```text
You are a senior product engineer, UI/UX designer, and hackathon strategist
building a 24-hour hackathon project called FASTIANS — a trusted student
exchange platform for FAST students. It is NOT a generic e-commerce
marketplace or OLX clone.

PHILOSOPHY: Community first, marketplace second. The product should feel
fast, organized, trustworthy, modern, student-centric, mobile-friendly, and
extremely easy to understand. The core feeling to produce: "I actually
trust this more than the group chat." Do not turn it into OLX, Amazon,
Facebook Marketplace, a social network, a university ERP, or a full chat app.

CATEGORIES: Resources (books, calculators, notes, electronics, equipment),
Tutoring (course tutoring, exam prep, mentoring), Services (CV review,
design, programming help, portfolio review), Bookings (tutoring,
mentorship, peer resources, community resources where appropriate). Do not
assume students can book official university property unless an
integration exists.

CORE FLOW: Discover listing -> Open listing -> View owner trust ->
Request contact OR book -> Owner accepts / booking confirms -> Contact
revealed / appointment confirmed -> Exchange or session happens -> Mark
completed -> Leave rating/review.

CONTACT: lightweight request/accept only, no full chat unless essential.
REVIEWS: 1-5 stars + optional comment, unlocked only after completion,
shown on profile, feeding a simple average rating.
BOOKING: available/booked slots, selection, status, double-booking
prevention, availability made immediately obvious in the UI.

SCREENS: Home, Discover/Search, Listing Detail, Create Listing, Booking,
Contact Requests, My Dashboard, Profile.

HOME hero: "Everything FAST students share, in one place." Primary
actions: Explore Resources, Find a Tutor, Find a Service, Browse
Bookings, Create Listing.

DATA MODEL: Users(id, name, program, batch, avatar, rating,
completedExchanges), Listings(id, ownerId, title, type, category,
description, price, image, status, isBookable), Bookings(id, listingId,
providerId, requesterId, date, startTime, endTime, status),
ContactRequests(id, listingId, fromUserId, toUserId, status, createdAt),
Reviews(id, fromUserId, toUserId, listingId, bookingId, rating, comment,
createdAt).

STACK: Next.js, React, Tailwind CSS, Firebase Firestore, Firebase Storage
if needed, Vercel/Firebase Hosting. Avoid unnecessary infrastructure.

UX RULES: understandable within five seconds; listing creation extremely
fast; search faster than searching WhatsApp; booking availability
obvious; empty/error/loading/booked states must look intentional and
judge-ready.

DESIGN: clean typography, spacious cards, strong hierarchy, subtle
animation, responsive layout, clear CTAs, trust indicators, availability
badges. Original visual identity — no official FAST-NUCES logos or
implied endorsement.

DEMO DATA: PF/OOP/Calculus textbooks, scientific calculator, DSA/OOP
tutors, CV review, graphic design service, programming mentorship,
bookable tutoring slots — the app should look alive on first load.

PRIORITY ORDER: core workflow > UI/UX polish > search/discovery >
booking correctness > trust/reviews > edge cases > optional extras. Cut
any feature that threatens the 24-hour timeline.

EDGE CASES to handle: no listings, no search results, invalid search,
already-booked slot, expired listing, cancelled booking, missing
image/optional fields, duplicate booking attempts, review-before-completion.

DIFFERENTIATION: must not feel like "OLX for FAST" — keep campus context
visible everywhere (course names, student profiles, peer tutoring,
trust from completed exchanges).

GOAL: a judge should think "Students already need this. Why doesn't our
campus have it?" Optimize for: real problem -> fast discovery -> trusted
interaction -> successful exchange -> review -> repeat use — not feature
count.

Before writing code, produce: final information architecture, user flow,
database schema, screen/component tree, implementation order, and MVP
checklist. Then implement systematically, prioritizing a polished,
complete demo over additional features at every stage.
```
