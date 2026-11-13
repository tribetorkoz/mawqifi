---
name: Mawqifi
description: Campus wayfinding for CMC Guelmim — a chalk board, pine ink, and orange earned only by estimates.
colors:
  chalk-ground: "#EDE9DC"
  plate-paper: "#FCFAF2"
  plate-paper-2: "#F4F0E3"
  ink: "#13241D"
  ink-soft: "#33463C"
  muted-ink: "#55655B"
  rule: "#C9C2B0"
  rule-soft: "#DDD7C8"
  pine: "#0B4C3A"
  pine-deep: "#073326"
  pine-soft: "#E4EBE2"
  pine-line: "#A9BFAF"
  signal-orange: "#A54E0F"
  orange-soft: "#F6E5D4"
  orange-line: "#E0C1A1"
  timetable-blue: "#33566B"
  danger: "#962C1D"
  chalk: "#F7F3E6"
  muted-ink-dark: "#9FAEA2"
  rule-dark: "#2E3D34"
  toast-scrim: "#000000A6"
typography:
  display:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "clamp(1.65rem, 6vw, 2.15rem)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  headline:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "clamp(1.35rem, 3.4vw, 1.7rem)"
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Readex Pro, Changa, Tahoma, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.85
  label:
    fontFamily: "Readex Pro, Changa, Tahoma, Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 500
    lineHeight: 1.6
  button:
    fontFamily: "Readex Pro, Changa, Tahoma, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 600
    lineHeight: 1.4
  utility:
    fontFamily: "Readex Pro, Changa, Tahoma, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.7
  input:
    fontFamily: "Readex Pro, Changa, Tahoma, Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.7
  display-compact:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "clamp(1.5rem, 7.2vw, 1.9rem)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  display-narrow:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "1.45rem"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  display-near:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "clamp(1.05rem, 3.6vw, 1.3rem)"
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: "-0.015em"
  direction-time-compact:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "21px"
    fontWeight: 600
    lineHeight: 1
  tab-compact:
    fontFamily: "Changa, Readex Pro, Tahoma, Arial, sans-serif"
    fontSize: "20px"
    fontWeight: 600
    lineHeight: 1
rounded:
  square: "0px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "24px"
  xxl: "32px"
components:
  button-primary:
    backgroundColor: "{colors.pine}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.square}"
    padding: "12px 18px"
    height: "48px"
    typography: "{typography.button}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.pine}"
    rounded: "{rounded.square}"
    padding: "11px 17px"
    height: "48px"
  plate:
    backgroundColor: "{colors.plate-paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "28px"
  direction-switch:
    backgroundColor: "{colors.plate-paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    height: "64px"
  gps-chip:
    backgroundColor: "{colors.plate-paper-2}"
    textColor: "{colors.ink-soft}"
    rounded: "{rounded.square}"
    padding: "7px 10px"
    height: "44px"
  fact:
    textColor: "{colors.ink}"
    padding: "16px 12px 4px"
  stop-row:
    textColor: "{colors.ink}"
    padding: "9px 2px"
    height: "56px"
  sheet:
    backgroundColor: "{colors.plate-paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "18px"
    width: "560px"
---

# Design System: Mawqifi

## Overview

**Creative North Star: "The Campus Noticeboard" (لوحة الحرم)**

Mawqifi is a wayfinding plate, not a map. The page borrows the grammar of a printed campus board: a chalk ground, a warm paper plate, pine enamel for institutional ink, hairline rules, square tick marks, and numbers large enough to read at arm's length. The interface answers one question — which stop, how far, when — and then shows its work. Nothing is decorated; everything that looks like a measurement is one.

The world was chosen by the user from three direction cards. It replaces an indigo product-sheet direction with something rooted in place: CMC's green is the ink of the institution, the chalk field is the walk to the curb, and orange is a signal that has to be earned. The page is deliberately dense at the answer and quiet everywhere else: one plate holds the result and its provenance, a slim sidebar holds the timetable and the reading key, and expandable rows hold the full stop list.

Trust is the leading visual problem. Every number carries its source in the same viewport: distance and walking time are modelled on a saved street graph, departure and arrival are given by the supplied timetable, intermediate stop times are estimated. The design encodes that vocabulary in small square nodes on a measured rule, in source lines under each value, and in a standing legend — then uses the orange only where an estimate or an attention state is present. The result should feel inspected, not marketed.

**Key Characteristics:**

- Chalk ground (`#EDE9DC`) and warm plate (`#FCFAF2`); no gradients, glass, photography, or fake paper texture.
- Pine (`#0B4C3A`) is institutional ink: masthead, primary action, rules, selected states.
- Orange (`#A54E0F`) is reserved for estimates, attention, and focus. It is never decorative.
- Type is Changa for display and numbers, Readex Pro for reading; digits are tabular without needing OpenType features.
- Geometry is square: 0px radii, 1px rules, 8–9px square nodes, 50×54 stop tabs.
- The signature is the measured rule: a full-width 1px line with square nodes over three facts — distance, walk, bus time — each with a provenance line.
- Arabic-first RTL layout, Western tabular digits, and bidi isolation for times, margins, and Latin tokens.

## Colors

A chalk-and-enamel palette: warm neutrals carry the page, a single dark green carries authority, and two accents carry meaning. Light and dark schemes are token swaps; the semantic roles do not change.

### Primary

- **Pine** (`#0B4C3A`): the masthead field, primary buttons, selected stop tabs, active direction segment, rule nodes, focus-adjacent marks, and the start of the measured rule. On light it is the darkest institutional voice; on dark it lifts to `#0E5A45` so it remains a field rather than a hole.
- **Pine Deep** (`#073326`): pressed/hover states on pine and the masthead hairline. Never a text color on light.
- **Pine Soft** (`#E4EBE2`): selected rows, pending fields, and quiet fills. Dark scheme uses `#172A22`.
- **Pine Line** (`#A9BFAF`): the pulsing “waiting” line and the inactive timeline spine.

### Secondary

- **Signal Orange** (`#A54E0F`): earned by estimates, attention, and focus only — the estimated bus-time node, the trip-window notice, coarse-GPS warnings, the estimate legend mark, and the focus ring. It is not an accent for links or decoration.
- **Orange Soft** (`#F6E5D4`) and **Orange Line** (`#E0C1A1`): tinted notice blocks and borders. The tint must always accompany a message; never use it as a generic card background.

### Tertiary

- **Timetable Blue** (`#33566B`): the given timetable — departure/arrival facts, the “from the table” legend mark, and manual/reference chips. It is a provenance color, not a link color.
- **Blue Soft** (`#E4EBEE`): reference fields and manual chips.

### Neutral

- **Chalk Ground** (`#EDE9DC`): the page field. Dark scheme: `#0C1511`.
- **Plate Paper** (`#FCFAF2`): the answer plate and sheets. Dark scheme: `#13201A`.
- **Plate Paper 2** (`#F4F0E3`): secondary fields, GPS chips, inset blocks.
- **Ink** (`#13241D`): headings and measured numbers. Dark scheme: `#F1EDDE`.
- **Ink Soft** (`#33463C`): body copy and secondary values. Dark scheme: `#D2D8CC`.
- **Muted Ink** (`#55655B`): source lines, labels, metadata, footer. All shipped text pairs are at least 5.0:1.
- **Rule** (`#C9C2B0`) and **Rule Soft** (`#DDD7C8`): borders, dividers, table rules. The strong rule is used for the facts baseline and sheet headers; the soft rule for everything else.
- **Chalk** (`#F7F3E6`): type on pine. Dark scheme: `#F3EFE1`.
- **Danger** (`#962C1D`): only the error state mark. Never a generic alert color.
- **Dark counterparts** (`#9FAEA2` muted ink, `#2E3D34` rule): named tokens so dark-scheme values are documented rather than drift. The toast scrim is `#000000A6`; it is an overlay, not a text color.

### Named Rules

**The Earned Orange Rule.** Orange appears only when the interface is estimating, warning, or focused. If a screen has no estimate, no attention state, and no focus, it has no orange.

**The One Ground Rule.** The page is chalk. Do not add gradient washes, glass panels, photographic textures, or a second field color to create depth; depth comes from a hairline and one low shadow.

**The Institutional Ink Rule.** Pine is authority, not success. Do not use it for “valid”, “live”, or “confirmed” states; the interface never claims those.

## Typography

**Display Font:** Changa (with Readex Pro, Tahoma, Arial fallbacks)  
**Body Font:** Readex Pro (with Changa, Tahoma, Arial fallbacks)  
**Label Font:** Readex Pro at 12px, weight 500

**Character:** Changa gives the plate its signage voice: open counters, a slightly condensed rhythm, and numerals that sit squarely on the rule. Readex Pro carries the reading text without competing; it is quieter, wider, and built for Arabic paragraphs. Together they read as a campus sign and its printed key, not as a product landing page.

### Hierarchy

- **Display** (600, `clamp(1.65rem, 6vw, 2.15rem)`, 1.15): the three fact values. Values are the loudest type on the page; the stop name is one step below.
- **Headline** (600, `clamp(1.35rem, 3.4vw, 1.7rem)`, 1.5): the stop name and state titles (“أين أنت الآن؟”, “لم نتمكن من تحديد موقعك”).
- **Title** (600, 18px, 1.5): sheet titles and the route panel heading.
- **Body** (400, 16px, 1.85): default reading; lead copy is 14.5px/1.9 with a maximum of 56ch.
- **Label** (500, 12px, 1.6): fact labels, source lines, chips, counts, and metadata. This is the smallest type in the system; do not go below 12px.
- **Button** (600, 14px, 1.4): actions and the direction names. Buttons are the only place body-family text is deliberately bold at this size.
- **Supporting steps** (documented, not one-off): 13px/1.7 utility copy (timing line, panel summaries, stop rows, text buttons), 15px/1.7 inputs, 20–21px compact stop tab and direction time below 560px, and the compact display clamps for facts at 560/400px (`clamp(1.5rem, 7.2vw, 1.9rem)`, `1.45rem`) and long near values (`clamp(1.05rem, 3.6vw, 1.3rem)`). These are responsive renditions of the same roles, not new voices.

### Named Rules

**The Tabular Measure Rule.** Times, distances, stop numbers, and counts use `font-variant-numeric: tabular-nums`. Changa digits are a uniform 0.5em, so 07:30 and 08:00 align without letter-spacing or a mono face.

**The Two-Voice Rule.** Changa is for what the user came for — numbers, names, section headings. Readex Pro is for what explains it. Do not set long paragraphs in Changa or measured values in Readex Pro.

## Layout

The workspace is a 1080px canvas with a fluid gutter (`clamp(16px, 4vw, 32px)`). Above 920px it is a 7/5 grid: the primary plate sits on the reading edge (right in RTL), and the timetable, reading key, privacy note, and context note sit in a slimmer sidebar. Below 920px the plate comes first, then the timetable, then the legend and privacy notes. Reading order and DOM order agree: masthead → direction switch → plate → provenance → route → method → footer.

The vertical rhythm is 8/12/16/24/28/32px. The plate has a fluid 18–28px inset; the sidebar uses 15–22px panels separated by 18px. Rules, not extra cards, separate sections: the route panel is a card, the method panel is a ruled block on the ground, and the footer is a hairline. The stop rows use a 56px minimum height with a 30px number square, a flexible name, an auto time, and a 44px pick control.

Responsive behavior is not a scaled-down desktop: at ≤560px the plate heading takes the full row and the GPS chip moves to its own line; at ≤400px the direction meta hides and fact values get a smaller clamp; at ≤380px the two result actions stack full width. At 320px the facts keep their units inline (`white-space: nowrap`) and the three columns stay legible without horizontal scroll.

### Verification

The shipped surface was reviewed in headless Chromium at 390×844, 320×700, and 1280×900. No horizontal overflow at any width; no console or page errors; `document.fonts.status = loaded`; every tappable control is at least 44×44 CSS pixels; no rendered text is below 12px; reduced-motion users get effectively instant state changes. The interface runs from the built `public/index.html` with embedded fonts, a v9 service worker, and no external map or routing request.

## Elevation & Depth

This is a printed-sheet system, not a layered app. The chalk ground is flat. The answer plate is a sheet of paper laid on it: a 1px rule plus one long, low shadow (`0 1px 0 #13241d08, 0 26px 48px -40px #13241d66`). The sidebar panels are flat or rule-separated. Sheets are the only genuinely elevated layer, with a dark backdrop and a deeper shadow. There is no glass, blur, glow, or bevel anywhere.

### Shadow Vocabulary

- **Plate** (`box-shadow: 0 1px 0 #13241d08, 0 26px 48px -40px #13241d66`): the result plate at rest. In dark mode the shadow deepens and loses the light rim.
- **Sheet** (`box-shadow: 0 30px 80px -30px #00000080`): modal sheets over the `#07140f99` backdrop. The header is sticky inside the sheet.

### Named Rules

**The Printed Sheet Rule.** A surface earns a shadow only if it is a sheet of paper on the board. Do not add shadows to buttons, chips, rows, or the direction switch; state is color, border, and position.

## Shapes

The form language is square and ruled. All radii are 0. Borders are 1px. The recurring marks are 7–9px squares: provenance nodes on the measured rule, legend marks, status bullets, and the signal dot in the GPS chip. The stop tab is a 50×54 pine rectangle; the pick control is a 44×44 square; the timeline is a 1px spine with square nodes. There are no pills, no rounded cards, no circles except the icon set’s own geometry (location pin, info, close).

The measured rule is the signature silhouette: a full-width 1px ink line, held at both ends by the plate, with a square node over each fact. The node styles are the provenance key:

- **Filled pine**: a measured value (distance, walk) or the nearest-stop status.
- **Half-filled pine**: modelled from the saved street graph; half ink, half plate, so the mark reads as “computed” in the legend.
- **Solid orange**: an estimate (the bus time), always paired with the orange source line.
- **Solid blue**: a value given by the supplied timetable.
- **Outlined**: missing; the interface will not invent the value.

## Components

### Buttons

- **Shape:** square (0px), 48px minimum height, 1px border only on secondary variants.
- **Primary:** pine field, chalk type, 12×18px padding, Changa-family label size; full width in single-action states and in narrow layouts.
- **Hover / Focus:** primary deepens to `#073326`; ghost fills with `#E4EBE2`; focus is a 2px orange outline with 3px offset. Never remove the focus ring.
- **Secondary / Ghost:** transparent field, pine type, 1px rule border, share/download actions.
- **Text button:** 44px minimum height, underlined, full width inside the plate so the hit target matches the row; its underline is the affordance, not a filled background.
- **Disabled:** 0.5 opacity, no shadow, no color change beyond opacity.

### Chips

- **GPS chip:** `#F4F0E3` field, 1px rule border, 8px square signal dot, 12px muted label and a 13px tabular value. A fair signal turns the dot orange; a caution state tints the chip orange-soft and keeps the text ink; a manual/reference state uses a dashed blue border and blue dot.
- **Count chip:** a 24–30px square with a 1px rule border, tabular digits, and no fill; it reports how many stops are behind a panel summary.

### Cards / Containers

- **Plate:** `#FCFAF2` field, 1px `#C9C2B0` border, 0 radius, one shadow, fluid 18–28px inset. It holds the answer and its provenance; it is the only strong card on the page.
- **Route panel:** a smaller plate with 15–22px inset, a header with a 12px “حسب الجدول المقدم” label, and the bus mark between the two times.
- **Method panel:** no card; a 1px rule above, a heading, three legend rows, and a full-width text button. It reads as a key printed on the ground.
- **Quiet note:** a shield icon in muted ink, a 13px sentence, and a second line of muted text. No border.

### Inputs / Fields

- **Select:** full width, 48px minimum height, plate field, 1px rule border, 15px text, 0 radius. Focus is a 2px orange outline with 2px offset.
- **Textarea:** full width, 13px text, 1.7 line height, 150px minimum height, RTL explicit; used only for the share text. Do not round it.

### Navigation

- **Masthead:** pine field, 72px minimum height, chalk CMC mark at 34px, a 25px Changa wordmark, a 12px campus line, an install control and a tabular clock. On <420px the campus line is hidden; the emblem and wordmark remain.
- **Direction switch:** a two-up ruled switch on the plate field, 64px tall, with a 24px tabular time and a 14px direction name. The active segment is a solid pine field; the inactive one is paper. The switch is the navigation; there is no tab bar.
- **Panels:** native `<details>` with a ruled summary, a 12–13px title, a square count, and a chevron. The open state is a rotated chevron and a rule; the rows inside are not indented into a separate card.

### Signature: The Measured Rule

A full-width ink rule sits above three equal facts. Each fact has a square node on the rule, a 12px label, a display-size value, an optional unit, and a 12px source line. The rule is the visual promise that these numbers are measurements, not marketing; the nodes and source lines are the promise that each one knows where it came from. On mobile the three columns remain side by side; the labels shorten to «المسافة», «المشي», «موعد الحافلة» so they never wrap into the value.

### Signature: Stop Rows

Two variants share a grid: a 30px number square, a flexible name, an auto metric/time, and a 44px control. Nearby rows are one big button with a check or arrow mark and a selected pine-soft fill; the full route is a 1px vertical spine with square nodes, estimated times prefixed by `≈` in orange, and a terminal row that carries «نهاية الاتجاه · ليست للصعود» and no pick button. Rows are 56px minimum and never shrink below a 44px target.

### Sheets

A native `<dialog>`: 560px maximum width, 86vh maximum height (90vh on phones), plate field, sticky header with an 18px title and a 44px close control, and 16–18px content padding. The backdrop is `#07140f99`. Sheets hold the method, improve-signal, install, and share content; the share text is selectable, never hidden behind a custom control.

### Boot

A full-screen chalk field with the CMC mark at 52px, a 24px “التطبيق جاهز” title, a 12px brand line, a 2px file-count meter, and a privacy line. The meter is honest: it advances with the seven public files, not with a timer. The screen closes after the offline check and removes itself from the accessibility tree with `hidden` + `display:none`.

## Do's and Don'ts

### Do:

- **Do** put provenance in the same viewport as the number: a node on the rule, a source line under the value, and a note under the facts.
- **Do** use the orange only for estimates, attention, and focus; pair every orange fill with a message.
- **Do** keep the three facts side by side at 320px; shorten labels rather than stacking the table.
- **Do** use `dir="ltr"` and tabular numerals for times, margins, and Latin tokens inside the RTL page.
- **Do** let the plate be the only strong card; separate the sidebar with rules and spacing.
- **Do** keep tappable controls at 44×44 or larger, with a visible 2px focus ring.
- **Do** preserve the CMC emblem, the «موقفي» name, and the campus attribution on the surface.

### Don't:

- **Don't** add pills, rounded cards, gradients, glassmorphism, or a second ground color.
- **Don't** use orange as a link color, a decorative accent, or a success badge.
- **Don't** use pine to claim “live”, “confirmed”, or “official”; the product has none of those.
- **Don't** invent an arrival time, a walking minute, or a stop number to fill a column. Missing is an outlined node and an em dash.
- **Don't** put a whole live region around the plate; announce a concise state summary and keep the visible structure stable.
- **Don't** let an animation re-run on every render in a way that makes measured values flicker; reduced motion must be honored.
- **Don't** hide the campus line on desktop or drop the CMC mark on mobile.
