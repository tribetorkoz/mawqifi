---
version: 1
slug: "public-index-html"
primary_target: "public/index.html"
related_targets: []
---

# Surface brief — mawqifi app screen

Surface: the single app screen in `public/index.html` (web, RTL Arabic PWA).
Visitor mode: Operate. Job: find the nearest bus stop, the walk to it, and the next bus estimate, then leave with justified confidence. Frequency: daily, short sessions, outdoors, one hand.

## Audience, task, constraints

Students and staff of CMC Guelmim around 07:30–08:00 and the 13:45 return; visitors who do not know the city. The screen owns the GPS status, direction switch, idle/locating/coarse/manual/routing/ready/unroutable/error states, the stop comparison, the full trip stop list, the accuracy sheet, install and share. No live bus data, no surveyed stops, no operating days. Location never leaves the device. Single static file, no build step, offline via service worker. The emblem and the موقفي name are fixed; palette and type are free.

## Direction contract

THESIS: A stop-finding instrument that shows how every number was obtained, and refuses the category default of a dark map card with one cheerful ETA.

OWN-WORLD: Chalk-enamel plate #F4F1E7; CMC pine #0B4C3A carries header, primary action and rule marks; estimate orange #A9500F is earned only by estimates and attention; provided-timetable blue-grey #33566B; hairline rules, square nodes and ruler ticks; Changa for stop numbers, times and headings, Readex Pro for reading text.

STORY: The visitor sees the closest stop, walk and bus time in one plate, reads each fact's provenance on the rule beneath it, knows what is measured versus estimated, and walks to the stop.

FIRST VIEWPORT: Slim green header with emblem and wordmark; a two-segment direction control showing each direction's departure time; on phones a full-width answer plate, on ≥900px the plate occupies the right seven of twelve columns with the route schedule and stop list in the left five. Plate order: stop-number tab, stop name, street, GPS status; three-fact measured rule (distance, walk, bus time) with provenance lines; remaining-wait status; primary "تحديث الموقع" action; provenance note. The state screens (idle, locating, coarse, manual, error, unroutable) use the same plate. Footer carries privacy and OSM attribution.

FORM: Campus wayfinding (لوحة الحرم), ranked first of seven grounded directions; built after the user picked it over the concept-seed assignment (#4 indigo selvedge), which the roll ran degraded on a code-led path. seed:1a8ea355e2f39e9a

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance.

## Unresolved

No browser or screenshot tool in this sandbox, so the finish review runs against the rendered live preview by the user plus static and jsdom checks. Real stop names, times and caveats come from the committed data; none may be invented.
