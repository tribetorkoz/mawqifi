# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Students and staff travelling to and from the Cité des Métiers et des Compétences (CMC) in Guelmim, Morocco, plus visitors who do not know the city. They open the app on an Android or iOS phone, usually while walking, often one-handed, and mostly around the 07:30–08:00 outbound window; the return trip matters too. They read Arabic (Modern Standard Arabic with light Darija phrasing) right-to-left.

## Product Purpose

Mawqifi answers one question with as little uncertainty as the available data allows: which bus stop is actually nearest to me, how long the walk takes, and when the next bus is expected. It exists because an unfamiliar city turns a normal commute into a chain of small uncertainties, and because a confident wrong answer is worse than an honest approximate one. Success is a person who knows which stop to walk to, how many minutes that walk costs, and whether the published bus time is still plausible.

## Positioning

The product refuses to perform certainty it does not have. It gates GPS quality in the browser, ranks stops by real walking distance over a cached OSM street graph, shows walking minutes without inventing arrival clock times, and labels every intermediate bus time as an arithmetic estimate rather than live tracking. Device location never leaves the phone.

## Operating Context

- The outbound journey is a fixed morning window (07:30–08:00) with a supplied departure and arrival time; return-trip arrival is not published.
- Hands are busy, light is bright, and the network may be absent. The app installs as a PWA and prepares its files for offline use.
- Operating days are unknown, intermediate stop times are estimated from distance, and stop positions are suggested street-front points, not surveyed stops. The interface must keep those distinctions visible without drowning the answer.
- Users compare two or three nearby stops when GPS accuracy is marginal, and can fall back to choosing a stop manually by name.
- Data covers Guelmim only; outside coverage the app must say so instead of routing.

## Capabilities and Constraints

- Vanilla JavaScript, HTML/CSS, a service worker, and static hosting; the whole app is one `public/index.html` with inline data, plus `public/sw.js` and JSON/GeoJSON fixtures in `public/data/`.
- Location is read with the Geolocation API, scored for age/accuracy/stability, and rejected when stale, outlying, or too coarse. Explicit opt-in exists for coarse readings.
- Routing runs locally: Dijkstra over a cached walking graph; stops rank by walking distance, not straight-line distance.
- Bus times come from `TRIP_ESTIMATES`: operator-supplied endpoints, computed intermediate stops. No live vehicle data, no service-calendar inference.
- The app has distinct states that must remain: boot/offline preparation, idle (permission prompt), locating, coarse signal, manual stop choice, routing, ready/result, unroutable/outside coverage, error (denied, unavailable, timeout, insecure, embedded, unsupported).
- Outbound/inbound direction switch changes the whole journey and result.
- No accounts, no analytics, no server-side routing. Share output contains public stop information only.
- No build step or framework may be introduced: deployment is static, and the page must stay installable and self-contained.

## Brand Commitments

- The name **موقفي** and the CMC (مدن المهن والكفاءات) emblem are binding and must remain, with the CMC campus attribution intact.
- The interface is Arabic-first, RTL, and the copy voice is plain, respectful, and explicit about uncertainty.
- The user granted full latitude over palette, typography, and layout; the current forest-green and sage palette is not binding.

## Evidence on Hand

- `public/data/`: route data, stops, landmarks, walking graph, road in/out, frontages, arrival estimates, walking access, context polygons.
- `public/assets/cmc-logo.svg`, `cmc-mark.svg`, `public/icon.svg`, app icons.
- Real Arabic copy in `public/index.html` describing GPS policy, estimates, privacy, and installation.
- Absent and not to be fabricated: live bus positions, confirmed operating days, surveyed stop coordinates, official route geometry, user counts, testimonials, or an operator partnership claim.

## Product Principles

1. State the confidence, not just the answer: every number carries its provenance (measured, modelled, or estimated) in plain language.
2. Answer first, explain on demand: the nearest stop, walk, and bus time are legible in seconds; the caveats follow.
3. A refusal is a feature: when the data cannot support an answer, say so and offer the nearest honest alternative.
4. The phone in one hand outdoors is the design target; every control is reachable and legible in sunlight.
5. Nothing about the person leaves the device.

## Accessibility & Inclusion

Arabic RTL screen-reader semantics, visible keyboard focus, 44px minimum touch targets, text that survives 200% zoom and bright outdoor light, and reduced-motion support. Numerals are Latin digits with tabular figures, as used on Moroccan signage and timetables.
