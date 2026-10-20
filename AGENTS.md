# ONDO — notes for AI coding agents

One HTML file: markup, inline CSS and inline scripts; GSAP with ScrollTrigger, Lenis smooth scroll, all from jsDelivr. No build step, no framework.

## Files
Work from the files: a page read through a link comes back as a summary, and a page rebuilt from it would differ.
```bash
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/CREDITS.md
```
In Windows PowerShell type `curl.exe`. Publish `index.html` with LICENSE and CREDITS.md; this file, README.md and `previews/` are not part of the site.

## Do not break
- Keep it one file unless the user asks otherwise; no framework or bundler for copy, colour or photo changes.
- Keep the ids and the `data-8b-section` / `data-8b-motion` attributes. Each section has its styles in `<style data-8b-part="section:<id>">` and its animation, if any, in `<script data-8b-part="scene:<id>">`.
- The scripts find these classes and attributes; when you change a section's markup, keep them or update the script:
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
- Colours, fonts, radii and shadows are CSS variables in the `:root` block (`data-8b-part="tokens"`); change them there and keep body text at 4.5:1 contrast or more.
- Animations run only when the visitor allows motion (`prefers-reduced-motion: no-preference`); the page must stay readable without them.
- A display line with `style="--len:N"` is sized to fill its width: N is its number of characters, spaces included (`Heat of Seoul` → 13, `Nova Nine` → 9).
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace before publishing
- Everything marked `data-8b-placeholder` (og-image, favicon, email, phone, social); remove the attribute once the real value is in. With no real value: no preview image — delete the `og:image` tag and set `twitter:card` to `summary`; no phone, email or address — remove that link or row.
- Choose day / Choose weekend / Choose pit buttons on the three passes: link to #contact now; point them to your ticket shop URL for each pass.
- Tickets (nav) and Get tickets (first screen): link to #tickets now; point them to your ticket shop URL, or keep them on the passes section.
- Enter your crew for 2027 (battle): link to a mailto: link now; point them to your sign-up form URL or a real e-mail address.
- Request the partner deck (partners): link to a mailto: link now; point them to your partner deck PDF or a real e-mail address.
- Invented demo facts (ask the user for the real ones; do not make up prices, dates or addresses):
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
- `<title>`, the meta description and the og tags; photos (Unsplash, see CREDITS.md) when the user has their own.

## Notes
- The rings, the venue plan, the passes and the audience panes are HTML and CSS, not images: restyle them through the tokens. Each audience pane's height comes from style="--share:N" on its column.
- Korean text (온도 and the dish names) is marked lang="ko"; the font covers Latin and Hangul.
- The photo wall is static: nothing collects tagged photos; connect a feed or reword the paragraph.
- In the looks track, while it slides, one look's text sits beside the next look's photo for a moment.
- Without JavaScript the phone menu button cannot open the overlay; the links stay reachable in the footer.

## Common edits
- Rebrand: search the old name (`ONDO`) in any letter case and replace every match; change the favicon letter and colours in `<link rel="icon">`.
- Photos: replace `src` and delete `srcset` and `sizes` (they list Unsplash sizes), keep `width`/`height` to the new photo's ratio, update `alt` and CREDITS.md.
- Remove a section: delete its markup, its `section:<id>` and `scene-style:<id>` styles, its `scene:<id>` and `section-script:<id>` scripts, and links to `#<id>`.
- Native scroll instead of smooth scroll: delete the Lenis block in `page-init` and the Lenis `<script>` tag.

## Check and publish
- Open the page at 375 and 1440 px, with reduced motion on, with the console open.
- Search `data-8b-placeholder` and the old name: nothing should be left but class names.
