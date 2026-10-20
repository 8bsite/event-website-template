# AGENTS.md: event website template

Event website for a music or culture festival, with lineup, schedule, venue zones and tickets. One file, `index.html`, with inline CSS and scripts (GSAP, ScrollTrigger, Lenis from jsDelivr); no build step, and none is needed for copy, colour or photo edits.

## Files
Edit these files, not a page fetched by URL (that arrives as a summary).
```bash
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/CREDITS.md
```
Upload `index.html`, LICENSE and CREDITS.md; not this file, README.md or `previews/`.

## Keep
- Every `id`, `data-8b-section`, `data-8b-motion` and `data-8b-part` (`section:<id>` styles, `scene:<id>` animation).
- Selectors the scripts use:
  - `section-script:navigation`: `.menu` `.nav__menu` `.menu__close`
  - `section-script:opening`: `.op-one`
  - `scene:opening`: `.op-rings` `.m-ring` `.op-veil__lid` `.op-zoom` `.op-word--a` `.op-word--c` `.op-word--b` `.op-upper` `.op-lower` `.op-veil`
  - `scene:lineup`: `.lu-row` `.lu-face` `.lu-name`
  - `scene:battle`: `.bt-stage` `.bt-name--a` `.bt-name--b` `.bt-round`
  - `scene:zones`: `.zn-map` `.zn-spot` `.zn-items`
  - `scene:looks`: `.lk-scroll` `.lk-track` `.lk-photo`
  - `scene:partners`: `.pt-pane` `.pt-man`
  - `scene:fanwall`: `.fw-item` `.fw-wall` `.fw-grade`
  - `scene:tickets`: `.tk-pass` `.tk-passes`
  - `scene:contact`: `.ct-rings`
- `style="--len:N"` = characters in that display line, spaces included: `Heat of Seoul` is 13, `Nova Nine` is 9, `Seora Kim` is 9, `Halo Kids` is 9, `Moon June` is 9, `Parallel` is 8, `ONDO 온도` is 7.
- The rings, the venue plan, the passes and the audience panes are HTML and CSS, not images: restyle them through the tokens. Each audience pane's height comes from style="--share:N" on its column.
- Korean text (온도 and the dish names) is marked lang="ko"; the font covers Latin and Hangul.
- Colours and fonts are variables in `:root` (`data-8b-part="tokens"`): `--color-1` #6e0a1e (deep crimson page and slides), `--color-2` #c8102e (red slides and photo tint), `--color-3` #fcfafb (white text, buttons, light slides), `--color-4` #1c0509 (near-black slides), `--color-5` #ff5c7a (pink hot edge, hover sweeps), `--color-6` #d9331f (orange-red in gradients); body text needs 4.5:1 contrast.
- With reduced motion the page must read in full.
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace
- `data-8b-placeholder` (og-image, favicon, email, phone, social): real value in, attribute out; no value, remove the row (no image: drop `og:image`, set `twitter:card` to `summary`).
- Choose day / Choose weekend / Choose pit buttons on the three passes: now #contact; owner's target: your ticket shop URL for each pass.
- Tickets (nav) and Get tickets (first screen): now #tickets; owner's target: your ticket shop URL, or keep them on the passes section.
- Enter your crew for 2027 (battle): now a mailto: link; owner's target: your sign-up form URL or a real e-mail address.
- Request the partner deck (partners): now a mailto: link; owner's target: your partner deck PDF or a real e-mail address.
- The name ONDO (any letter case); the favicon letter and colours in `<link rel="icon">`.
- Photos (29, Unsplash: opening 1, lineup 5, battle 2, zones 4, looks 3, food 2, partners 4, fanwall 8): `src`, no `srcset`/`sizes`, `width`/`height` to the ratio, `alt`, CREDITS.md.
- `<title>`, meta description, og tags.

## Ask the owner for
All demo text, never to be invented:
- Dates 12–13 June 2027, Saturday 12 June and Sunday 13 June (title, meta description, phone menu, opening, lineup).
- Venue and address: Pier Arena, Maashaven, Riverside Quay 2, Rotterdam; trams 20 and 23, "four minutes on foot", bike parking at the north gate; "Step-free from the tram stop" (opening, zones, contact, FAQ, footer).
- The day schedule: nine times 12:00–22:30 in CEST, "same schedule both days" (opening).
- Acts and set times: Nova Nine, Seora Kim, Halo Kids, Moon June, Parallel with their days, stages and times; "five headline acts", "fourteen crews, DJs and rookies", "announced in May", "set times go live two weeks before" (lineup).
- Battle: Saturday 14:30, "Last year's final, rematched", eight crews, three rounds (Footwork, Choreo, Freestyle), the crowd votes with lightsticks, crews Red Line (Rotterdam) and Night Shift (Seoul), entries for 2027 (battle).
- Zones: hours 12:00–23:00, 14:30–18:30, 12:30–20:00, 12:00–23:30; a standing floor for 6,000 and a raised deck; workshops and random play dance at six; twelve chairs and Korean skincare brands in the beauty lab; twenty stalls and a tea bar (zones, food).
- Beauty lab sessions: times 12:30 · 16:00, 13:30 · 17:00, 14:30 · 18:30, "twenty minutes each", products "to try and take home" (looks).
- Food prices €4–€9 for six dishes; "cards and phones only", "costs less than a lightstick"; a top-up point for prepaid cards (food, FAQ).
- Audience and reach: "Eighteen thousand visitors over two days", shares 40% / 30% / 20% / 10% with age ranges, "more than a hundred others" in the creators avatar list (hidden text) and its label "Creators who covered ONDO last year" (partners).
- Photo wall: lights up at 21:00, photos "land on this page by midnight", hashtag #ondoheat, and the caption "Photos from last year's wall, shared with permission" — the photos are stock photos, so change or remove this line (fanwall).
- Passes: €69, €119, €189, "400 only", early entry 11:30, Saturday soundcheck 16:00, wristbands posted three weeks before, "Prices include all fees", under-12s free with a paying adult, groups of eight or more (tickets, FAQ).
- Rules and policies: under-16s need an adult on the standing floor, lightsticks, A3 banners and one small bag allowed, no poles, chairs or cameras with detachable lenses; quiet room, companions go free; an app with live schedule and push notes; refunds up to 30 days before minus a €5 fee and an official resale exchange (FAQ).
- Contacts and service: hello@, battle@ and partners@ondo.example (replaced), phone +31 10 000 0000 (replaced), ticket desk "daily 10:00–18:00", "answers within a day" (FAQ, battle, partners, contact).
- Company and year: "© 2027 ONDO Festival B.V. · Rotterdam" (footer).

## Known limits
- The photo wall is static: nothing collects tagged photos; connect a feed or reword the paragraph.
- In the looks track, while it slides, one look's text sits beside the next look's photo for a moment.
- Without JavaScript the phone menu button cannot open the overlay, and the top links are hidden at 860 px and below; on phones the first screen links Get tickets and See the lineup and the footer links Tickets, Partners and Contact, but Battle, Zones and FAQ have no other link.

## Check
375 and 1440 px, reduced motion on, console clean; `data-8b-placeholder` and ONDO left only in class names.
