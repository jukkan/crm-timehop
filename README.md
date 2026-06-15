# CRM Timehop of the Day

A Timehop-style page for [CRM Tip of the Day](https://crmtipoftheday.com) — the legendary Microsoft Dynamics CRM community blog by [@CRMTipOfTheDay](https://twitter.com/mscrmtipoftheday).

Visit the current day's tips at **[crmtimehop.jukkan.com](https://crmtimehop.jukkan.com)**.

## What it does

Shows every tip ever posted on today's date, grouped by year — "On this day, X years ago…" — with full post content and images. Navigate backwards (and forwards) one day at a time using the toolbar.

The UI is styled as a retro Windows XP / Dynamics CRM 4.0-era desktop application, in tribute to the era when most of the tips were written.

## How it works

A single static HTML file with no build step. On load, it queries the [WordPress REST API](https://developer.wordpress.org/rest-api/) at `crmtipoftheday.com` for posts matching the current month/day across every year from 2011 to present, fetches them in parallel, and renders them with full content and featured images embedded via `?_embed=wp:featuredmedia`.

No backend, no dependencies, no framework. Deploys directly to GitHub Pages.

## Deploy

1. Fork or clone this repo
2. Enable GitHub Pages: **Settings → Pages → Source: main branch / root**
3. The site is live at `https://<your-username>.github.io/crm-timehop/`

### Custom domain

To use a custom domain, update `CNAME` with your domain and point a DNS `CNAME` record at `<your-username>.github.io`.

DNS for `crmtimehop.jukkan.com`:
```
crmtimehop.jukkan.com  CNAME  jukkan.github.io
```

GitHub Pages will handle HTTPS automatically once the DNS propagates.

## Credits

All content belongs to [CRM Tip of the Day](https://crmtipoftheday.com) and its authors. This page fetches and displays their content live — no content is stored in this repository.
