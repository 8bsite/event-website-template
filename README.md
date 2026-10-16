# Free HTML event and festival website template with GSAP scroll animations — ONDO

**Event website for a music or culture festival, with lineup, schedule, venue zones and tickets: a free HTML template in one file, with GSAP scroll animations, no build step, MIT license. Made by [8B](https://8b.com/), the AI website builder.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/event-website-template/)** · **[Use this template](https://github.com/new?template_name=event-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/event-website-template/archive/refs/heads/main.zip)**

<a href="https://8bsite.github.io/event-website-template/"><img src="previews/desktop.png" alt="ONDO, a free HTML template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/event-website-template/"><img src="previews/phone.png" alt="ONDO, a free HTML template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/event-website-template/"><img src="previews/scroll.gif" alt="ONDO, a free HTML template: scrolling through the first sections on a desktop" width="40%"></a><br><sub>Scroll animation</sub></p>

A one-page site for a two-day K-culture festival in Rotterdam: lineup, a crew battle, four zones, a beauty lab, a food board, partner info, a photo wall and three passes. Crimson and red slides with big type that heats from dim to white-hot as you scroll; the first screen's face closes into nine round windows that become the day's schedule.

Good for: music or culture festival; concert, fan meeting or convention; club night or event series with a lineup; any event with a schedule, several areas and ticket tiers. Free for personal and commercial use (MIT), made by [8B](https://8b.com/).

## Quick start

Pick one:

- **With an AI coding agent** (Claude Code, Codex, Cursor, Windsurf…). Download the files into your project (in Windows PowerShell type `curl.exe`):
  ```bash
  curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/index.html
  curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/AGENTS.md
  curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/LICENSE
  curl -LO https://raw.githubusercontent.com/8bsite/event-website-template/main/CREDITS.md
  ```
  Then give your agent this prompt:
  ```text
  Read AGENTS.md, then edit index.html. Use this template as the base for an event site for <your event: what it is, dates, venue and address, lineup or programme, areas, ticket types and prices, how to buy>. Keep the layout, the motion and the single-file format; replace the event name, copy, photos, schedule, prices, links and contacts, and recolour it through the CSS variables if needed.
  ```
  Give the agent the downloaded file, not a link: an agent reads a link as a summary and would rebuild a different page.
- **No code.** Download the ZIP, unzip it, replace the contacts and texts in `index.html`, put `index.html` into an empty folder and drag that folder onto [Netlify Drop](https://app.netlify.com/drop). The page is online in a minute.
- **On GitHub.** Click **[Use this template](https://github.com/new?template_name=event-website-template&template_owner=8bsite)** to get your own copy, then **Settings → Pages → Deploy from a branch → main**. Your site appears at `https://<you>.github.io/<repo>/`.

## What's on the page

- **Navigation** — top bar: wordmark, section links, Tickets button; phone menu overlay with dates and venue
- **Heat of Seoul** — two-screen opening: a full-bleed photo under a huge title, then nine round windows onto it with the day's schedule
- **On the bill** — the bill: five act names set full width, each with a round portrait and day, stage and time
- **Crew battle** — split screen: two sides with a moving VS line (demo: a dance crew battle)
- **One hall, four heats** — venue plan with four round zone windows and a description of each
- **Idol looks** — sideways track of three items, each a tall photo with times, name, text and three steps (demo: make-up looks)
- **Food street** — menu board with prices, names in two languages, two photos
- **Who fills the hall** — for sponsors: audience in four columns with bars sized by share, a portrait and a deck button
- **The photo wall** — photo wall: eight photos, rectangles and circles, red-tinted
- **Passes** — three ticket tiers as wristband passes with prices and buttons
- **Before you come** — questions and answers (native &lt;details&gt;) with a contact e-mail
- **See you on the river** — contact block framed by rings: e-mail, venue address, travel, phone, press e-mail
- **Footer** — width-filling ONDO 온도 wordmark, links, copyright and the Design: 8B credit

## Before you publish

- Replace everything marked `data-8b-placeholder` (social preview image, favicon, email, phone, social) and the invented demo facts — prices, dates, address. [AGENTS.md](AGENTS.md) lists them.

## Customize

- **Colours and fonts**: CSS variables in the `:root` block at the top of `<head>`.
- **Text**: edit it in place. A big display line with `style="--len:N"` fills its width: set N to its new number of characters.
- **Photos**: replace `src`, delete `srcset` and `sizes` (they list Unsplash sizes) and update the `alt` texts.
- **Animations**: each section's animation is one `<script data-8b-part="scene:<id>">` block at the end of the file. For native scroll, delete the Lenis block in `page-init`.

## For developers

- **Stack.** HTML and CSS (custom properties, cascade layers) with GSAP 3.13.0, ScrollTrigger, Lenis 1.3.27 from jsDelivr. No build step, no framework, no npm. 152 KB.
- **Layout of the file.** `<head>`: CSS variables, shared classes, then one style block per section. Then the markup, one element per section with a one-line comment above it. End of `<body>`: small behaviour scripts, the libraries, smooth scroll (`page-init`), the effects, one animation script per section.
- **Browsers.** Chrome and Edge 111+, Safari 16.2+, Firefox 113+ (it uses color-mix(), container query units, cascade layers, small/dynamic viewport units).
- **Accessibility.** Motion runs only when the visitor's system allows it; with "reduce motion" the page is complete and still. FAQ answers use native `<details>` and open without JavaScript. Every photo has alt text.
- **External requests.** images.unsplash.com, fonts.gstatic.com, cdn.jsdelivr.net. No analytics, no cookies. To self-host everything (offline use, or Google Fonts and GDPR in the EU), download those files and change the URLs.
- **Licences of the parts.** GSAP is free, commercial use included, under its own standard licence (not MIT); Lenis is MIT; fonts are SIL OFL; photos are under the Unsplash License. See [CREDITS.md](CREDITS.md).

## FAQ

**Can I use it for a client or a commercial site?** Yes. The code is MIT: use it, change it, sell the site you build with it.

**Do I have to keep the "Design: 8B" link?** No. It is welcome, not required.

**Can I use it in React, Next.js, Astro or Vue?** Yes. Move each section's markup and style block into a component and run its animation script in `useGSAP()` (React) or `onMounted` (Vue); start Lenis once. Or keep it as a separate static landing page next to your app (`example.com` for the landing, `app.example.com` for the app).

**Where are the photos from?** Unsplash; they load from Unsplash's servers. Replace them with your own when you can.

## More free templates

[More 8B templates on GitHub](https://github.com/8bsite) · [8b.com](https://8b.com/)

## License

The template code is MIT licensed — see [LICENSE](LICENSE). Photos, fonts and libraries keep their own licences — see [CREDITS.md](CREDITS.md).
