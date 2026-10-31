# Rajan Malik — VIP Telegram Access

A single, mobile-first landing page that invites visitors to join the Rajan Malik VIP Telegram channel. It is built for paid social traffic and tracks visits and join clicks with Meta Pixel.

## Features

- A gold-on-dark "luxury" design with an avatar, a stats card, and a list of perks
- A countdown banner and a pulsing "Join Now" Telegram button
- A bottom-sheet popup that opens after 1.5 seconds and sends visitors to Telegram automatically 3 seconds later, unless they close it
- Meta Pixel `PageView` on load, plus `Lead` events for button clicks, popup clicks and auto-redirects

## Technologies

- Plain HTML, CSS and JavaScript in one file (`index.html`), with no build step
- Google Fonts (Cinzel, Montserrat) and Font Awesome, both loaded from CDNs
- Hosted on Netlify as a static site

## Running locally

Open `index.html` in a browser, or run:

```bash
netlify dev --port 8889
```

## Common edits

- **Telegram link:** search `index.html` for `telegram.me`. It appears three times: the main button, the popup button and the auto-redirect.
- **Meta Pixel ID:** change it in the `fbq('init', ...)` call and in the `<noscript>` image URL.
- **Countdown length:** change the `duration` value, which is in seconds.
