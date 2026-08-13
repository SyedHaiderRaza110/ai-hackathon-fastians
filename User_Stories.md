# FASTIANS — User Stories

Format: *As a [role], I want to [action], so that [benefit].*
Each story includes acceptance criteria drawn from the product requirements.

---

## Epic: Discovery

**US1 — Browse categories**
As a student, I want to see the main categories (Resources, Tutoring, Services, Bookings) on the homepage, so that I immediately understand what I can find or offer.
- Acceptance: Homepage displays all four categories within the first screen.
- Acceptance: Category tiles link to filtered discovery results.

**US2 — Search for a resource**
As a student, I want to search listings by keyword, so that I can find what I need in seconds instead of scrolling through a WhatsApp group.
- Acceptance: Search returns matching listings by title/keyword.
- Acceptance: A search with no matches shows a "No resources found — try another keyword or category" message.

**US3 — Filter results**
As a student, I want to filter listings by category, type, price range, and availability, so that I can narrow results to what's actually usable to me.
- Acceptance: Filters can be combined.
- Acceptance: Filter controls remain simple (no more than a handful of options).

**US4 — See a personalized feed**
As a student, I want to see a "For You" feed of relevant or recent opportunities, so that the platform feels immediately useful without me having to search.
- Acceptance: Feed surfaces a mix of item, tutoring, and service listings.
- Acceptance: Feed logic is rule-based (recency, category relevance, availability, popularity) — no AI required.

---

## Epic: Listings

**US5 — Create a listing**
As a student, I want to create a listing in under a minute, so that I can quickly offer an item, tutoring, or a service.
- Acceptance: Required fields are only title, type, category, description, price (if applicable), availability (if bookable), and contact option.
- Acceptance: Image and tags are optional.

**US6 — View listing details**
As a student, I want to view a listing's full details, so that I can decide whether to request contact or book it.
- Acceptance: Detail page shows image, title, category, price/free, availability, description, and owner trust info.
- Acceptance: Primary CTA is either "Request Contact" or "Book a Slot" depending on listing type.

**US7 — Manage my own listings**
As a student, I want to edit or close my own listings, so that I can keep my offerings accurate and current.
- Acceptance: Only the listing owner can edit or close it.
- Acceptance: Closed/expired listings show "This listing is no longer available."

---

## Epic: Trust & Profiles

**US8 — View a provider's trust profile**
As a student, I want to see a listing owner's rating and completed-exchange count, so that I can decide whether to trust them before reaching out.
- Acceptance: Rating (average of 1–5 stars) and completed-exchange count are visible on both the listing card and listing detail page.
- Acceptance: Recent reviews are visible on the owner's profile.

**US9 — View my own profile**
As a student, I want to see my own rating, reviews, and completed exchanges, so that I can track my reputation on the platform.
- Acceptance: Profile page shows name, program/batch, avatar, rating, completed exchanges, and reviews received.

---

## Epic: Contact

**US10 — Request contact with a listing owner**
As a student, I want to request contact with a listing owner, so that I can coordinate an exchange without exposing anyone's contact info by default.
- Acceptance: "Request Contact" sends a pending request to the owner.
- Acceptance: Requester sees a "Contact request pending" state until the owner responds.

**US11 — Respond to a contact request**
As a listing owner, I want to accept or decline incoming contact requests, so that I control who can reach me.
- Acceptance: Owner sees pending requests in their dashboard.
- Acceptance: Accepting reveals contact info to the requester; declining does not.

---

## Epic: Booking

**US12 — View availability**
As a student, I want to see which time slots are available or booked for a bookable listing, so that I know what I can select.
- Acceptance: Slot picker clearly marks each slot as Available or Booked.

**US13 — Book a slot**
As a student, I want to book an available time slot, so that I can secure a tutoring/mentorship/service session.
- Acceptance: Selecting and confirming an available slot creates a confirmed booking.
- Acceptance: Attempting to book an already-booked slot shows "This slot has already been booked" and offers other available times.

**US14 — Avoid double-booking**
As a platform, I need to prevent two confirmed bookings from overlapping on the same listing, so that providers and requesters never end up in a scheduling conflict.
- Acceptance: A new booking is rejected if it overlaps an existing confirmed booking for the same listing (same date, overlapping time range).
- Acceptance: Already-booked slots are disabled in the UI so conflicts are prevented before submission.

**US15 — Manage my bookings**
As a student, I want to view and cancel my own bookings, so that I can manage my schedule.
- Acceptance: Dashboard lists all bookings I've made or am providing.
- Acceptance: Cancelling a booking updates its status and frees the slot.

---

## Epic: Completion & Reviews

**US16 — Mark an exchange complete**
As a student, I want to mark an exchange or booking as completed, so that both parties can move to the review step.
- Acceptance: Completion is available only after contact was accepted (item exchange) or a booking was confirmed and occurred (service/tutoring).
- Acceptance: Completed items/bookings unlock the review action.

**US17 — Leave a review**
As a student, I want to leave a 1–5 star rating with an optional comment after a completed exchange, so that I can help build trust in the community.
- Acceptance: Review submission is blocked until the exchange/booking is marked completed ("Complete the exchange before leaving a review").
- Acceptance: Review appears on the recipient's profile and updates their average rating.
- Acceptance: Only one review is allowed per completed exchange.

---

## Epic: Dashboard

**US18 — See everything in one place**
As a student, I want a single dashboard showing my listings, bookings, contact requests, and completed exchanges, so that I don't have to hunt across the app to manage my activity.
- Acceptance: Dashboard has four sections: My Listings, My Bookings, My Requests, Completed Exchanges.
- Acceptance: From the dashboard I can edit/close a listing, accept/decline a request, cancel a booking, mark completion, and leave a review.

---

## Epic: Trust & Safety Guardrails

**US19 — Avoid overreach on university property**
As a platform, I should not let students book official university-owned resources (e.g., official study rooms) without an authorized integration, so that the product doesn't misrepresent authority it doesn't have.
- Acceptance: Bookable demo resources are peer-managed or clearly fictional.
- Acceptance: Any messaging about official rooms notes that support would require an official integration.

**US20 — See the platform is independent**
As a user, I want to know this is an independent student project, so that I don't mistake it for an official university service.
- Acceptance: No official FAST-NUCES logos are used without authorization.
- Acceptance: A disclaimer is shown where appropriate: "Independent student project for hackathon purposes. Not affiliated with or endorsed by FAST-NUCES."
