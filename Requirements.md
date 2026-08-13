# FASTIANS — Requirements

## 1. Functional Requirements

### FR1 — Listings
| ID | Requirement |
|---|---|
| FR1.1 | Users can create a listing with: title, type, category, description, price (if applicable), availability (if bookable), and a contact option. |
| FR1.2 | Image and tags are optional fields on a listing. |
| FR1.3 | Listing creation must be completable in under one minute (small form, no more than the required fields above). |
| FR1.4 | Users can edit or close/cancel their own listings. |
| FR1.5 | Users cannot modify a listing they do not own. |
| FR1.6 | Each listing belongs to one of the core categories: Resources, Tutoring, Services, or Bookings. |

### FR2 — Search & Discovery
| ID | Requirement |
|---|---|
| FR2.1 | Users can search listings by keyword. |
| FR2.2 | Users can filter listings by category, type, price range, and availability. |
| FR2.3 | The system displays a "For You" style opportunity feed of relevant/recent/available listings without requiring AI (rule-based ranking). |
| FR2.4 | A search with no matches shows a clear no-results state with a suggestion to try another keyword or category. |

### FR3 — Trust & Profiles
| ID | Requirement |
|---|---|
| FR3.1 | Every user has a profile showing name, program/batch, avatar, average rating, number of completed exchanges, and reviews received. |
| FR3.2 | Profiles display a verification/status indicator (no complex identity verification required). |
| FR3.3 | A listing card and listing detail page must surface the owner's rating and completed-exchange count. |

### FR4 — Contact Requests
| ID | Requirement |
|---|---|
| FR4.1 | A user can send a "Request Contact" to a listing owner. |
| FR4.2 | The listing owner can accept or decline a contact request. |
| FR4.3 | Contact information is revealed to the requester only after the owner accepts. |
| FR4.4 | The system does not require or provide full in-app messaging. |
| FR4.5 | Users can view the status of their own sent and received contact requests (pending/accepted/declined). |

### FR5 — Booking
| ID | Requirement |
|---|---|
| FR5.1 | Bookable listings expose a slot picker showing available and booked time slots. |
| FR5.2 | Users can select and confirm an available slot. |
| FR5.3 | The system must prevent double-booking: a confirmed booking cannot overlap another confirmed booking for the same listing. |
| FR5.4 | Already-booked slots are visibly disabled in the UI. |
| FR5.5 | Users can view and, where appropriate, cancel their own bookings. |
| FR5.6 | The system does not assume authority to book official university-owned resources (e.g., official study rooms) without an explicit integration; demo/prototype bookings use peer-managed or clearly fictional resources. |

### FR6 — Exchange Completion
| ID | Requirement |
|---|---|
| FR6.1 | An exchange or booking can be marked as completed by the relevant participant(s). |
| FR6.2 | Completion is a prerequisite for leaving a review (no pre-completion reviews). |

### FR7 — Reviews & Ratings
| ID | Requirement |
|---|---|
| FR7.1 | Reviews consist of a 1–5 star rating and an optional comment. |
| FR7.2 | A review can only be submitted after the related exchange/booking is marked completed. |
| FR7.3 | Submitted reviews appear on the recipient's profile. |
| FR7.4 | The recipient's average rating updates based on all received reviews. |

### FR8 — Dashboard
| ID | Requirement |
|---|---|
| FR8.1 | Users have a personal dashboard showing: My Listings, My Bookings, My (Contact) Requests, and Completed Exchanges. |
| FR8.2 | From the dashboard, users can edit/close listings, accept/decline requests, cancel bookings, mark exchanges complete, and leave reviews. |

### FR9 — Navigation & Screens
| ID | Requirement |
|---|---|
| FR9.1 | The application provides these screens at minimum: Home, Discover, Listing Detail, Create Listing, Booking, Contact Requests, My Dashboard, Profile. |
| FR9.2 | The homepage must communicate what the platform does and how to use it without requiring explanation. |

---

## 2. Non-Functional Requirements

### NFR1 — Usability
| ID | Requirement |
|---|---|
| NFR1.1 | A first-time user must understand what the product does and how to use it within seconds of landing on the homepage. |
| NFR1.2 | Listing creation must be fast enough to complete in under one minute. |
| NFR1.3 | Search must return a useful result faster than manually searching a WhatsApp group. |
| NFR1.4 | Availability (booked vs. available) must be visually unambiguous at a glance. |
| NFR1.5 | The UI must avoid clutter: no oversized forms, no excessive filters, no unnecessary animation. |

### NFR2 — Trust & Integrity
| ID | Requirement |
|---|---|
| NFR2.1 | Trust indicators (rating, completed exchanges) must be visible wherever a listing owner is shown. |
| NFR2.2 | The review system must not allow reviews outside the completed-exchange flow, preventing fabricated or premature reviews. |

### NFR3 — Reliability / Correctness
| ID | Requirement |
|---|---|
| NFR3.1 | Booking logic must reliably prevent overlapping confirmed bookings for the same resource. |
| NFR3.2 | The system must handle edge cases gracefully and visibly: no listings, no search results, invalid search, already-booked slot, expired listing, cancelled booking, missing optional fields, duplicate booking attempts, and review-before-completion attempts. |

### NFR4 — Performance
| ID | Requirement |
|---|---|
| NFR4.1 | The application should feel fast and responsive across browsing, search, and booking actions. |
| NFR4.2 | Core interactions (search, filter, book) should not require a full page reload. |

### NFR5 — Responsiveness / Platform
| ID | Requirement |
|---|---|
| NFR5.1 | The application must be mobile-friendly and usable on small screens, since many students will access it on mobile. |
| NFR5.2 | The design should scale cleanly between desktop and mobile layouts. |

### NFR6 — Simplicity of Scope
| ID | Requirement |
|---|---|
| NFR6.1 | The system must not attempt to become a full e-commerce platform, social network, university ERP, chat application, payment platform, or AI chatbot. |
| NFR6.2 | Feature scope should be limited to what supports the core discovery → trust → action → completion → reputation loop. |

### NFR7 — Branding / Compliance
| ID | Requirement |
|---|---|
| NFR7.1 | The product must use original branding and must not use official FAST-NUCES logos or imply official university endorsement without explicit authorization. |
| NFR7.2 | A disclaimer should be shown if appropriate, noting the project is independent and not affiliated with or endorsed by FAST-NUCES. |

### NFR8 — Buildability (Hackathon Constraint)
| ID | Requirement |
|---|---|
| NFR8.1 | All features must be achievable within a 24-hour build window. |
| NFR8.2 | Any feature that threatens the timeline should be cut in favor of a smaller, fully working feature set. |
