# VIPROX Product Page — Content, UX & Design Brief

**Deliverable:** `viprox.html` (complete, responsive, implementation-ready)
**Price presented:** $250
**Brand reference:** `index.html` (approved GSH Complex homepage)

---

## What changed in this revision

The previous version borrowed the homepage's actual section components, which is why it read as a copy. That has been undone. The page now shares the brand system and nothing else.

**Shared with `index.html`:** colour tokens, Vollkorn and DM Sans, the button family, spacing scale, both utility bars, the header, the mobile drawer, the footer, the sticky mobile purchase bar, the toast, and the scroll-reveal behaviour.

**Not shared:** every internal composition. None of `.hero`, `.buy`, `.pillars`, `.bandR`, `.ritual`, `.sci__grid`, `.tst__grid`, `.plans`, `.faq` or `.final` is used. The homepage's section CSS is no longer even loaded, which is why the file dropped from 151 KB to 119 KB.

**The page's own motif** is the champagne gold band from the top of the carton. It recurs as the protocol timeline, the annotation leader lines, the hairline under the price, and the seal.

### Section by section, what makes each one its own

| Section | The composition |
|---|---|
| **Hero** | Copy and an open, ruled purchase rail on the left. On the right the carton stands on a lit plinth inside a tall arch, tilted in perspective with a contact shadow and a fading reflection, so it reads as an object in a room rather than a cut-out pasted on a page. The homepage uses a full-bleed photograph and a floating white card; this uses neither. |
| **The shift** | A narrow centred column. The six symptoms are set as two quiet italic columns divided by a single hairline, not as a bulleted or numbered list. |
| **What arrives** | The system photographed once and **annotated in place** with gold leader lines and dots, the way a product sheet does it, rather than listed in a column beside the picture. On tablet and mobile the callouts fall into a rule-topped stack under the image. |
| **The protocol** | Two beats hung on one continuous gold line, with ringed markers, set large in Vollkorn. On mobile the line rotates to vertical. |
| **The three formulas** | Three full-width rows on forest, read left to right: what it is, what it does, what you get. Ruled, never boxed, no icons. |
| **What it supports** | A heading held to the left with three hairline-divided columns beside it, so it reads as one statement rather than three cards. |
| **Proof** | The four numbers set **inside** a wide banner image under a forest wash, with the three credentials ruled beneath it. |
| **What people tell us** | Centred: a small round portrait, one large serif quote, then two shorter quotes divided by a vertical hairline. No cards, no star tiles, no badges. |
| **What $250 buys** | Set as a **receipt**, with dotted leaders running from each item to its price, a struck-through subtotal and the total in Vollkorn, beside the guarantee. |
| **FAQ** | Two columns, hairline rows, thin gold chevrons. |
| **Close** | Fully centred on forest, the carton tilted to match the hero. |

Also carried through from earlier rounds: light palette throughout with two dark sections, no eyebrow labels except the hero's, no em dash anywhere in visible copy, and the content roughly halved from the first draft (eleven short sections, page height about 8,200px at 1440).

---

## Positioning

Robert's note and the strategy review both landed in the same place, and the page follows it: a premium three-part daily system for adults whose energy, recovery and digestion are no longer what they were, not a product that treats many conditions.

Robert's two specific requests are both in:

- **"Tired, burnt out, not quite yourself?"** is the H1, with *"Take a holistic approach to restoring vitality, energy and a more youthful sense of well-being"* as the lead. "Depressed" was dropped because it reads as a mental-health claim; "burnt out" carries the same feeling without it.
- **"If you feel like you've tried everything, try VIPROX, backed by a 45-day money-back guarantee"** appears as a gold-ruled line in the hero and again as the closing headline.
- **No "guaranteed results".** The guarantee block says plainly that it applies to your purchase, not to a specific health outcome.

---

## Structure

Eleven short sections. Each answers the next question a cold visitor actually asks.

| # | Section | Question it answers | Ground |
|---|---|---|---|
| 1 | **Tired, burnt out, not quite yourself?** | What is this, and what does it cost? | Ivory |
| 2 | **Nothing goes wrong. Things just go quiet.** | Is this about me? | Cream |
| 3 | **One box. Three formulas.** | What do I actually get? | Ivory |
| 4 | **The protocol is the product.** | What do I do every day? | Cream |
| 5 | **What each one is actually for.** | What does each formula do? | Forest |
| 6 | **Support where the body quietly runs short.** | What will it help with? | Ivory |
| 7 | **Proof** | Can I trust these people? | Cream |
| 8 | **What people tell us** | Has it worked for anyone like me? | Ivory |
| 9 | **What $250 actually buys** + guarantee | Is it worth it, and what if I'm wrong? | Sage |
| 10 | **Questions worth asking** | Anything else? | Ivory |
| 11 | **If you feel like you've tried everything** | Buy | Forest |

**Where the urgency comes from.** Section 2 opens with the honest version of the problem, that nothing dramatic happens, it just goes quiet, and closes with the client's own line: *"There is no such thing as a quick fix when it comes to your health. Improving it is a commitment: an ongoing process of smart decisions, good habits and positive lifestyle choices. This is why we created VIPROX."* No countdowns, no fake stock, no invented deadlines. The pressure is the cost of another year of drift; the guarantee removes the reason to wait.

**CTAs.** Four: the hero rail, the sticky mobile bar, the price section, and the close.

---

## Interactions

| Interaction | Detail |
|---|---|
| Scroll reveal | IntersectionObserver, 26px rise and fade, staggered across paired elements. Shared with the homepage so the two pages feel the same in motion |
| Sticky mobile purchase bar | Appears once the hero scrolls past, hides at the page end |
| Segmented plan control | One-time or Smart Buy, filled forest when active |
| Buttons | 1px lift, arrow slides 3px |
| FAQ | One panel open at a time, gold chevron rotates |
| Quantity, add to cart | Same demo behaviour and toast as the homepage |
| Reduced motion | `prefers-reduced-motion: reduce` disables every reveal and smooth scrolling |

No external requests. Fonts are the self-hosted woff2 files already in `/fonts`. The carton is `fetchpriority="high"`; everything below the fold is `loading="lazy"`. The carton's tilt, contact shadow and reflection are pure CSS, so there is no extra image weight.

---

## Responsive behaviour

Rendered and checked at 390, 820 and 1440.

- **Mobile (≤820px).** The carton and its plinth move above the copy, so the product is the first thing seen. The purchase rail keeps the price, both plan options, quantity and Add to Cart visible without a tap, and the sticky bar carries $250 and Add to Cart for the rest of the page. The annotated diagram becomes a rule-topped stack; the protocol line turns vertical; the FAQ becomes one column.
- **Tablet (821–1080px).** Same stacking as mobile, wider measure, annotations in three columns under the image.
- **Desktop (≥1081px).** Copy and rail left, plinth right; annotations positioned around the photograph.

---

## Images

Everything upscaled from the presentation deck is gone. Five photographs now carry the page, renamed by what they are:

| File | Was | Used for |
|---|---|---|
| `viprox-hero.jpg` + `@half` | `hero-image-dextop.png` | **Hero, desktop.** Fills the section edge to edge. |
| `viprox-hero-mobile.jpg` + `@half` | `hero image-mobile.png` | **Hero, ≤560px.** The portrait frame. |
| `viprox-system.jpg` + `@700` | `image1.png` | **What arrives.** Annotated in place with gold leader lines. |
| `viprox-daily.jpg` + `@700` | `image2.png` | **The protocol.** The routine in use, beside the two beats. |
| `viprox-box.png` + `@430` | your original carton cut-out | **Closing band** and the mobile bar thumbnail. |

All JPEGs at quality 88 with half-size companions for `srcset`, roughly 245–285 KB at full size instead of ~2 MB per PNG. `viprox-box-open.jpg` was superseded by the wider hero frame and has been removed; `viprox-system-light.jpg`, the last deck crop, is gone too.

### How the hero is built

You were right that full-bleed was the way to go, and it turned out to be the technically correct choice as well: the 2:1 photograph crops badly inside a tall half-width column, but fills a full-width band with only a vertical crop, so the whole box stays in frame.

The photograph sits at `position: absolute; inset: 0` behind the section. The shading is a CSS gradient, not baked into the file, so it stays adjustable: solid ivory to 25%, then 0.9, 0.52, 0.14 and clear by 58%. Because the picture was generated with real empty surface on the left, the scrim lands on that emptiness rather than on the product, and the copy and purchase rail sit on what reads as flat ivory. No text is ever on top of the box.

Three breakpoints keep the framing honest:

- **≥1200px:** full-bleed. Above 1360 the frame is wider than the picture so it crops vertically only; between 1200 and 1360 `object-position: 40%` keeps the box and both bottles inside the frame.
- **561–1199px:** the picture becomes a 16:9 band above the copy, with the scrim turning vertical so it dissolves into the ivory beneath it.
- **≤560px:** the `<picture>` element swaps in the portrait frame at 5:5.2.

---

## Every claim on the page, and where it came from

| Claim | Source |
|---|---|
| Component roles; "each component serves a very specific purpose"; "more energy, greater mental clarity, better overall well-being" | yourcym.com VIPROX product page |
| "There is no such thing as a quick fix…" and "Rather than attacking diseases and conditions, it empowers your body to do what it is naturally meant to do: protect itself" | yourcym.com VIPROX page, near-verbatim |
| GSH Complex description, Provida CVE, Dr. Robert Bender MD FAAFP, ingredients, NPN 800021489 | yourcym.com GSH Complex page |
| Triozyme: organic-certified spelt, kamut and rye; probiotics, prebiotics, fibres, vitamins, minerals, 1,000+ enzymes; 180 chewable tablets | yourcym.com VIPROX and Triozyme Chewables pages |
| Une Vie: structured water, excitation currents and quartz wavelength purification, delivery system, 500 ml | yourcym.com Une-Vie page |
| The protocol (one scoop before each meal in 500 ml diluted Une Vie; 2 Triozyme after each meal, followed by 500 ml diluted Une Vie) | Cymcorp published protocol |
| Contents: 2 × GSH Complex, 1 × Une Vie, 1 × Triozyme, 1 × shaker and eye-wash cup | yourcym.com VIPROX page |
| Prices $85.95 / $59.95 / $35.35, totalling $267.20 | yourcym.com individual product pages; the sum matches the site's own crossed-out VIPROX price exactly |
| Volume terms (25% at 6–11, 30% at 12+, not eligible for AutoShip; Smart Buy 6-month minimum) | yourcym.com |
| 4.6 from 58,564 VIPROX customers; 652,035 customers and 4.56 average across CYM; 20+ years | yourcym.com |
| Founded 2003 by Robert Gauthier after seven years of research in biology and human anatomy | Cymcorp press releases, 2021 |
| Health begins at the cellular level; patented; non-toxic; non-invasive | *Viprox Presentation ENGLISH.pptx* and `clinical-studies-3.pdf` |
| Randomised, double-blind, placebo-controlled survey; 115 participants; three months; ethics-committee review | `clinical-studies-3.pdf` |
| Not suitable with a milk-protein allergy | GSH Complex is whey-based; milk-protein allergy is an explicit exclusion criterion in the clinical study |
| Three testimonials (Dyan L., Debbie J., Martin N.) | yourcym.com VIPROX page, condensed, meaning unchanged |

### Claims deliberately left off
Each of these appears somewhere in the source material and needs product-specific substantiation before it can be published. Several are exactly what Robert flagged.

"98.9% effective" · "Clinically proven under WHO standards" · "Peer-reviewed by two U.S. universities" · "Backed by 170,000 peer-reviewed medical articles" · "Guaranteed results" · "No side effects" · "Safe for pregnant women and newborn infants" · "Treatment of a host of immune system and immune-related diseases" · "Repairs damaged cells" · "Detoxifies and cleans your whole system" · "Provides relief from acid reflux" · "Combats Leaky Gut Syndrome" · "Hydrates 10× more effectively than plain water" / "equivalent to 300 regular water bottles" · Dr. Ray Obomsawin's "natural immunity" quotation · any outcome figure from the clinical survey.

The proof section turns that restraint into an asset by describing what the documentation is and offering the report to health professionals, rather than printing a headline number. If any of the above is later substantiated, it can be added without touching the structure.

---

## Open questions for the client

1. **GSH Complex pack size inside VIPROX.** The website lists the standalone Family Pack as 450 g / 15.8 oz; the presentation artwork shows 2.20 lb (1 kg). The page never states a weight and the images were chosen so neither is contradicted, but this needs settling and it changes the value story.
2. **How long does one package last** on the full protocol versus a maintenance dose? The FAQ answers honestly and routes to the phone line. A real number is worth several paragraphs of copy.
3. **Is $250 one-time only, or also the AutoShip price?** Both options currently show $250.
4. **Volume tier prices at a $250 base.** The hero card currently says "volume pricing brings this to $175 a box", which is 30% off $250. The site's existing tiers were quoted against a different base and need confirming.
5. **Photography of the shaker and eye-wash cup.** No supplied image includes them, and they are part of what justifies the price.
6. **Sign-off on referencing the clinical survey** factually, with no outcome figures, and on offering the report to health professionals.
7. **Written permission and verification for the three testimonials**, and confirmation that "4.6 from 58,564" is current.
8. **Patent number**, if "patented" is to stay on the page.
9. Confirm the **nav and footer link targets**. They are carried over from `index.html`, where several are still `#` placeholders.

---

## Files

```
viprox.html                        the page, self-contained, no external requests
assets/viprox-box.png              carton, background removed   (1057 × 874)
assets/viprox-box@430.png          carton, half size            (528 × 437)
assets/viprox-system-light.jpg     the four components          (1236 × 622)
```

Also reused unchanged: `assets/science-graded.jpg`, `assets/customer-story.jpg`, `assets/logo-dark*.png`, and the six woff2 files in `/fonts`.

Single self-contained file in the same shape as `index.html`, so it drops into the same build with no new dependencies.
