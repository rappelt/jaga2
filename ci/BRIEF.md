# JAGA – Corporate Identity V2 (shared brief for all mockups)

## Company (facts from the current site)
JAGA Trendy Sp. z o.o., Gdańsk (ul. Chrobrego 79F, gdansk@jagatrendy.pl). Phone not published yet → show "[phone to add]".
B2B contract-furniture sourcing & specification partner. Does NOT manufacture. Curates 13 manufacturers:
- Café/Restaurant: Pedrali, Magis, Plust, Thonet, Infiniti
- Wooden chairs: Paged, TON
- Sofas/lounge: Alias, Softline
- Office chairs: Wilkhahn (premium), Profim, Bejot
- Office systems: LAS
Logos (PNG) in assets/logos/{alias,bejot,infinity,las,magis,paged,pedrali,plust,profim,softline,thonet,ton,wilkhahn}.png
Audience: architects, interior designers, planners, hotel/restaurant operators, office/fit-out clients. Markets PL (primary), DE, international. Languages PL/EN/DE (show switch; mockups written in English).
Services (sequence, numbering allowed): 1 Brief & site plan → 2 Specification & tender docs (manufacturer advice, CAD/BIM, FF&E schedule) → 3 Samples & finishes (fabric, wood, frame colours) → 4 Ordering, logistics, delivery → 5 Installation & acceptance.
Reference projects (real seed data):
- Hard Rock Cafe, Warsaw – lounge & dining, 200+ chairs, bar stools, upholstered seating – PAGED, Fameg
- Premium Office, Berlin – open space & meeting, 120+ workstations, ergonomic chairs, height-adjustable desks
- Boutique Hotel, Kraków – lobby & breakfast area, 80+ chairs, armchairs, lounge furniture
Claims to AVOID (unverified): "100%", "24h response", "verified partners", client logos, testimonials, invented numbers. Use only the facts above. Where a fact is missing, show a bracketed placeholder.

## Positioning (from competitor analysis)
"The specification partner between architects and Europe's contract manufacturers."
Tagline: EN "From plan to place." · DE "Vom Plan zum Platz." · PL "Od planu do miejsca."
Gaps competitors leave open (JAGA should own them visibly): architect service desk with CAD/BIM + samples; one project list / RFQ across all brands (instead of a shop cart); sector-first entry (Hospitality, Workplace, Retail, Public); projects credited with architect, city, scope; brand pages with a one-line statement per brand; lead with expertise, never with sales/discounts.

## Brand story hook
Gdańsk = world capital of amber (bursztyn), Baltic sea, Gothic brick. The logo already uses amber. The palette comes from that.

## Colour tokens
--ink     #16232B  Baltic Ink (text, dark surfaces)
--amber   #E2891C  Amber (accent, marks, highlights; use on ink or as fill; NOT as small text on light bg)
--amber-d #A65E0B  Amber deep (amber text/links on light bg, AA)
--brick   #8E3B2B  Gdańsk brick (secondary accent, sparingly)
--fog     #ECEEEC  Fog (light page background, cool)
--pier    #C9CFCB  Pier grey (hairlines, borders)
--paper   #FFFFFF
--stone   #55626A  secondary text on light
Never use cream #F4F1EA, terracotta #D97757, purple gradients.

## Typography
One family: **Archivo** (Google Fonts variable: wdth 62..125, wght 100..900):
<link href="https://fonts.googleapis.com/css2?family=Archivo:ital,wdth,wght@0,62..125,100..900;1,62..125,100..900&display=swap" rel="stylesheet">
- Display: Archivo, font-stretch 125%, weight 700–800, tight tracking (-0.02em), line-height 0.95–1.05. The wide stance is the brand's voice.
- Body: Archivo 100%, 400/500, 17–18px, line-height 1.6, max 65ch.
- Spec codes / data: Archivo font-stretch 75%, weight 600, tabular-nums (e.g. CH-04, 200+ seats). NO monospace.
Fallback: "Archivo", "Helvetica Neue", Arial, sans-serif.
Avoid: ALL-CAPS eyebrow labels over every heading, "A · B · C" meta strings, "→" glued to every button, single italic/coloured word in headlines.

## Signature device: the spec tag
Architects mark furniture on plans and FF&E schedules with callout codes. JAGA's tag = a small pill with a code (CH-01 chair, ST-02 stool, TB-03 table, SO-04 sofa, LG-05 lounge) + optional thin leader line + dot. Used for photo hotspots, list markers, project scopes. Code in Archivo 75% width 600.

## Logo
ci/logo.svg (copy inline into pages): amber plan-corner bracket + outlined square (a chair in elevation / a room corner) + "JAGA" wordmark in Archivo Expanded 800. Descriptor under/next to it: "Contract furniture, Gdańsk". "Trendy" is dropped from the brand mark (kept in legal name).

## Motion (user loved these effects from his previous site – reuse the technique)
One vanilla-JS scroll loop with requestAnimationFrame that writes CSS custom properties; CSS does the drawing. No GSAP/Lenis needed.
- parallax: el centre offset × data-depth → translate3d(0,var(--py),0) rotate(var(--pr))
- SVG line draw: pathLength="1", stroke-dasharray:1, dashoffset 1→0
- vertical progress line through the 5-step process: --progress scaleY, steps get .is-reached when they cross 60% of viewport
- sticky horizontal strip: section height ~240vh, inner sticky 100svh, track translateX(-p*max)
- sticky header gets .is-scrolled (blur, background) after 24px
- easing cubic-bezier(0.22,0.61,0.36,1); html{scroll-behavior:smooth}
- prefers-reduced-motion: disable everything (html.reduced), strips fall back to overflow-x:auto with scroll-snap.
- Content must be visible at rest (no opacity:0 waiting for observers).

## Common page structure (homepage mockup)
Sticky header (logo, Sectors, Manufacturers, Projects, For architects, Contact, phone/email, PL|EN|DE, "Project list (0)" button) → Hero → Sector entry → Manufacturers → For architects (service desk: CAD/BIM, samples, tender specs) → Process (5 steps) → Projects → Contact/RFQ form (company, role select: Architect/Designer/Operator/Developer, project type, city, timing, seats/pieces, message; "Commercial clients only") → Footer (legal name JAGA Trendy Sp. z o.o., address, Impressum/Privacy links).

## Images (assets/, Unsplash, 1800px wide)
restaurant.jpg (dark restaurant, many chairs – best hero), cafe.jpg, cafe-lounge.jpg, dining-top.jpg (overhead dining), office-glass.jpg, office-lounge.jpg (white shell chairs), office-dark.jpg, hotel-room.jpg, resort.jpg, sofa-green.jpg, chair-white.jpg (white shell chair on white), chair-black.jpg (black chair on teal), stool.jpg (stool on blue). Old site images: none needed.
