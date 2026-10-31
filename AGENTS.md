# AGENTS.md

## Architecture

This is a static, single-page site with no framework, no package.json and no build step. Netlify publishes the repository root (`publish = "."` in `netlify.toml`).

- `index.html`: the whole site. Its CSS is inline in `<style>`, its JS is inline in `<script>`, and the Meta Pixel snippet is in `<head>`.
- `netlify.toml`: the publish directory and basic security headers.

## Conventions and non-obvious decisions

- Keep everything in one file unless the owner asks otherwise. The page is an ad landing page, so load speed and simplicity matter.
- The Telegram invite URL is repeated in three places (main CTA, popup CTA, auto-redirect). Keep them in sync.
- `trackLead(source)` fires a Meta `Lead` event. The `content_category` values are `Button_Click`, `Popup_Click` and `Auto_Redirect`, and the ad reporting may depend on them, so don't rename them.
- The popup timing (opens after 1.5s, redirects 3s later) is intentional owner behaviour.
- The page doesn't store any data, so no backend or database is needed.
