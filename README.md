# Free HTML event and festival website template with GSAP scroll animations — ONDO

**Event website for a music or culture festival, with lineup, schedule, venue zones and tickets: a free HTML template in one file, with GSAP scroll animations, no build step, MIT license. Made by [8B](https://8b.com/), the AI website builder.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/event-website-template/)** · **[Use this template](https://github.com/new?template_name=event-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/event-website-template/archive/refs/heads/main.zip)** · **[Template page on 8b.com](https://8b.com/templates/ondo/)**

<a href="https://8bsite.github.io/event-website-template/"><img src="previews/desktop.png" alt="ONDO, a free HTML template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/event-website-template/"><img src="previews/phone.png" alt="ONDO, a free HTML template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/event-website-template/"><img src="previews/scroll.gif" alt="ONDO, a free HTML template: scrolling through the first sections on a desktop" width="40%"></a><br><sub>Scroll animation</sub></p>

A one-page site for a two-day K-culture festival in Rotterdam: lineup, a crew battle, four zones, a beauty lab, a food board, partner info, a photo wall and three passes. Crimson and red slides with big type that heats from dim to white-hot as you scroll; the first screen's face closes into nine round windows that become the day's schedule.

Good for: music or culture festival; concert, fan meeting or convention; club night or event series with a lineup; any event with a schedule, several areas and ticket tiers.

## Use it with an AI coding agent

Download the files into your project (in Windows PowerShell type `curl.exe`):

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

Give the agent the downloaded file, not a link: from a link it would rebuild a different page. No agent? Click **[Use this template](https://github.com/new?template_name=event-website-template&template_owner=8bsite)**, edit `index.html` and turn on **Settings → Pages**.

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

## Design

Palette: ![#6e0a1e](https://img.shields.io/badge/-%236e0a1e-6e0a1e?style=flat-square) ![#c8102e](https://img.shields.io/badge/-%23c8102e-c8102e?style=flat-square) ![#fcfafb](https://img.shields.io/badge/-%23fcfafb-fcfafb?style=flat-square) ![#1c0509](https://img.shields.io/badge/-%231c0509-1c0509?style=flat-square) ![#ff5c7a](https://img.shields.io/badge/-%23ff5c7a-ff5c7a?style=flat-square) ![#d9331f](https://img.shields.io/badge/-%23d9331f-d9331f?style=flat-square)  
Fonts: Asta Sans (Google Fonts). Change both through the CSS variables in the `:root` block at the top of `<head>`. A big display line with `style="--len:N"` fills its width: set N to its new number of characters.

- The rings, the venue plan, the passes and the audience panes are HTML and CSS, not images: restyle them through the tokens. Each audience pane's height comes from style="--share:N" on its column.
- Korean text (온도 and the dish names) is marked lang="ko"; the font covers Latin and Hangul.

## Before you publish

- Replace everything marked `data-8b-placeholder` (social preview image, favicon, email, phone, social) and the invented demo facts: prices, dates, address. [AGENTS.md](AGENTS.md) lists them.

## Tech

GSAP 3.13.0, ScrollTrigger, Lenis 1.3.27 from jsDelivr, 152 KB, no build step. Chrome and Edge 111+, Safari 16.2+, Firefox 113+ (it uses color-mix(), container query units, cascade layers, small/dynamic viewport units). With "reduce motion" on, the page is complete and still.

## License

MIT, see [LICENSE](LICENSE); the "Design: 8B" footer link is welcome, not required. Photos, fonts and libraries keep their own licences: [CREDITS.md](CREDITS.md). More free templates: [8b.com/templates](https://8b.com/templates/) · [github.com/8bsite](https://github.com/8bsite).
