# Third Culture Kid Run Club — Landing Page

Single source of truth for building the TCK Run Club website. Any agent picking up this project should read this file before touching anything.

---

## What This Is

A single-page scrolly landing site for **Third Culture Kid Run Club (TCK Run Club)** — a New York-based run club for the expat and international community. The club meets every Saturday at 10am on the West Side Highway. It's founded and run by two brothers: Felix and his brother.

**Core positioning: community and belonging — not fitness or performance.** That feeling must come through in every design and copy decision.

---

## Goal

Brand-first. Tell the story of who TCK is. Feature the brothers visually and personally. Link out to Instagram, Strava, and WhatsApp. No forms, no RSVPs, no backend. A beautifully designed static page — that's the whole brief.

---

## Design Direction

Hybrid of two references:
- **Roots Digital Studio** — bold, editorial, graphic, confident structure
- **Cassandra Tang** — warm, personal, someone's voice

Result: designed and intentional, not a casual meetup flyer. But when people land on it they should feel like they're meeting two brothers, not a corporate brand.

---

## Visual System

### Color

- Pure black and off-white only. No accent color. Ever.
- Background: warm off-white — `#F8F6F1` or `#FAF7F2` (not pure white)
- Text: near-black — `#0A0A0A` (not pure black)
- No color means type and layout do all the work. Discipline is the point.

### Typography

**Raleway is the only typeface used on the site.** Load from Google Fonts with weights: 100, 400, 500, 700, 900.

```
https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100;0,400;0,500;0,700;0,900;1,100;1,400&display=swap
```

Weight roles:
| Role | Weight | Notes |
|---|---|---|
| Display / hero headlines | Black (900) | Very large, tight line-height |
| Grammar words | Thin (100) | Often italic, letter-spaced, smaller scale |
| Body copy | Regular (400) or Medium (500) | Comfortable size, generous line-height |
| Place names / hard facts | Medium (500) or SemiBold (700) | Clean, no decoration |

**Type rules:**
- Big things should be really big. Small things stay quiet. The jump between sizes is the drama.
- Never use non-Raleway fonts — not for code, not for captions, not for anything.

### The "from / based" Grammar Motif

This is the conceptual and typographic hook of the entire site. "Where are you from?" is the defining Third Culture Kid question. The site turns it into a visual system used throughout every section.

**The rule:** grammar words (from, based, every, at, find us on, run with us on) are set in Raleway Thin; the content (places, names, platforms) is set in Raleway Black or Medium. The contrast does the work.

Examples in use:
- Hero: *from* everywhere, *based* New York
- Bio block: **Felix** / *from* Singapore, London, Jakarta / *based* New York
- Run info: *every* Saturday / *from* 10am / *at* West Side Highway
- Links: *find us on* **Instagram** / *run with us on* **Strava** / *join us on* **WhatsApp**

This pattern must appear consistently. It is the editorial voice of the brand.

### Layout Principles

- Generous margins — let things breathe. Don't crowd sections.
- Left-aligned, not centered (editorial rhythm, not flyer symmetry). Exception: the hero wordmark may be oversized or centered as a design statement.
- Thin black horizontal rules (`1px`, `#0A0A0A`) between sections — print-magazine rhythm.
- One hero photo: black-and-white, environmental, featuring both brothers. Leave a clearly labeled placeholder with exact dimensions if the image isn't ready.
- Desktop-first design but fully responsive. Test at 1440px, 768px, and 375px.
- On mobile, the from/based grammar stacks cleanly — one line per element, still readable.

---

## Page Structure (Top to Bottom)

### 1. Hero

- Huge Raleway Black wordmark: "Third Culture Kid Run Club"
- Immediately below, small Raleway Thin (optionally italic): *from* everywhere, *based* New York
- No image in the hero. Let the type land alone.
- Subtle scroll indicator at the bottom of the viewport (arrow or word "scroll", Thin weight).

### 2. Manifesto

Short, direct, editorial. 2–3 sentences. Something close to:

> "We grew up between places. This is a run club for people who did too — less about pace, more about finding your people on a Saturday morning in New York."

Treatment: pull one key phrase out at a larger size or set it in Raleway Thin for contrast. Not a paragraph dump — give it space and visual intention.

### 3. The Brothers

- Large black-and-white photograph of the two founders. Placeholder for now — use a clearly labeled box (see Placeholders section).
- Adjacent or below: the from/based grammar block for each brother, then a short personal paragraph — why they started it, what it means to them.

Structure per brother:
```
[NAME] — Raleway Black
from [City, City, City] — Raleway Thin
based New York — Raleway Thin

[Short bio paragraph — Raleway Regular]
```

TODO: bio copy for both brothers is a placeholder (see Placeholders section).

### 4. Saturdays

Oversized stacked type. One line per fact. Use the grammar system:

```
every Saturday
from 10am
at West Side Highway
```

Grammar words (every, from, at) in Raleway Thin. Content (Saturday, 10am, West Side Highway) in Raleway Black or Medium — significantly larger.

Below this block: one smaller line with any meeting-spot specifics or what to expect (e.g., "We meet at the Pier 84 entrance. All paces welcome.").

### 5. Come Run With Us

Three large links using the grammar system:

```
find us on Instagram →
run with us on Strava →
join us on WhatsApp →
```

- Grammar words in Raleway Thin
- Platform names in Raleway Black
- Arrow (→) in Raleway Black
- All links open in new tabs (`target="_blank" rel="noopener noreferrer"`)
- Leave `href="#"` as placeholders — real URLs will be swapped in

### 6. Footer

Quiet, minimal. One line:

```
Third Culture Kid Run Club. New York. © [YEAR]
```

Optional: small credit line ("Site by ..."). Raleway Regular, small size, low visual weight.

---

## Technical Requirements

- **Single static HTML page** — or Next.js/React if the project is already scaffolded that way. Match whatever's already set up.
- **Raleway from Google Fonts** — weights 100, 400, 500, 700, 900. Include italic variants for 100 and 400.
- **Fully responsive** — test at 1440px, 768px, 375px.
- **Smooth scroll behavior** — `scroll-behavior: smooth` on `html`.
- **No unnecessary JavaScript** — this is a static marketing page. If it doesn't need JS, don't add it.
- **Semantic HTML** — proper heading hierarchy (one `h1`, logical `h2`/`h3` use), `<nav>`, `<main>`, `<footer>`, `<section>`.
- **Accessible** — alt text on all images, focus states on all links, sufficient color contrast, no keyboard traps.
- **Performance** — optimize images, fast first paint, no render-blocking resources beyond the Google Fonts stylesheet.
- **Tailwind welcome** if already set up; otherwise clean CSS or CSS Modules. No UI component libraries needed.

---

## What NOT to Do

- Do not add color accents, gradients, shadows, or decorative elements beyond black rules and type.
- Do not use any typeface other than Raleway.
- Do not add stock photos of people running — the only photography on the page is the brothers' hero shot.
- Do not make it cute or casual — the design is intentional and grown-up. The club is warm; the design is confident.
- Do not add RSVP forms, email capture fields, newsletter signups, or any backend logic.
- Do not add sections that aren't in the page structure above. If something feels unnecessary, cut it.
- Do not center-align body text. Left-aligned throughout (hero wordmark is the only exception).
- Do not use pure `#FFFFFF` or pure `#000000` anywhere on the page.

---

## Placeholders

Leave the following clearly marked in the code and visually obvious in the rendered page:

| Placeholder | Location | Notes |
|---|---|---|
| Brothers' photo | The Brothers section | Placeholder box, suggest ~1200×800px, labeled "PHOTO: Felix + [brother] on West Side Highway, B&W" |
| Felix's "from" cities | Brothers bio block | TODO comment: `<!-- TODO: Felix's cities (e.g. Singapore, London, Jakarta) -->` |
| Brother's name | Brothers bio block | TODO comment: `<!-- TODO: Brother's name -->` |
| Brother's "from" cities | Brothers bio block | TODO comment: `<!-- TODO: Brother's cities -->` |
| Bio copy (both) | Brothers bio block | TODO: short personal paragraph per brother |
| Instagram URL | Come Run With Us | `href="#" <!-- TODO: Instagram URL -->` |
| Strava URL | Come Run With Us | `href="#" <!-- TODO: Strava URL -->` |
| WhatsApp URL | Come Run With Us | `href="#" <!-- TODO: WhatsApp URL -->` |
| Footer year | Footer | `<!-- TODO: founding year -->` |

---

## File Structure (if static HTML)

```
/
├── CLAUDE.md
├── index.html
├── styles.css        (or styles/ directory if modular)
└── assets/
    └── images/       (brothers photo goes here when ready)
```

If using Next.js, follow standard App Router conventions: `app/page.tsx`, `app/globals.css`, `public/images/`.

---

## Brand Voice (for copy)

- Direct, not flowery.
- Warm, not corporate.
- Specific, not vague — "West Side Highway" not "a park in New York."
- The grammar system (from/based) carries the emotional weight. Let it do its job; don't over-explain.
- No exclamation points. No emoji. No hashtags in body copy.
