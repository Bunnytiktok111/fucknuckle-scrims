# Fucknuckle Scrims

A responsive PUBG community scrims website starter for Cloudflare Pages.

## What's included

- Home page and stats overview
- Overall and season leaderboard views
- Upcoming scrims and match-results views
- Squad registration form with a local preview reference
- PayPal and Patreon links
- Dark esports styling that works on desktop and mobile

## Important: starter preview vs production

This first version is a **front-end preview**, not yet a live shared-data scrims system. Registration requests and preview data are saved in the visitor's browser only; they are not sent to an organiser and do not sync between devices. There is no secure admin login yet. Do not use this preview to store private information or to claim that a payment has been verified.

Before using it for real events, add a Cloudflare Worker/API, a Cloudflare D1 database, and secure organiser authentication. Store each player's payment status separately and only mark payments as paid after organiser verification or server-side PayPal verification. A PayPal.Me redirect is not proof of payment.

## Publish with Cloudflare Pages

1. Sign in to Cloudflare.
2. Open Workers & Pages (or Pages, depending on the dashboard layout).
3. Choose Create, then Pages, then Connect to Git.
4. Select the GitHub repository Bunnytiktok111/fucknuckle-scrims.
5. For a plain static site, leave the build command blank and set the build output directory to the repository root (use the option Cloudflare presents for a static site).
6. Deploy. Cloudflare will provide a public pages.dev address.
7. Each future commit to the connected branch can trigger a new deployment.

## Entry fee and links

- Entry fee: **$1 per player**; a four-player squad costs **$4**.
- PayPal: https://paypal.me/staffieg3
- Patreon: https://www.patreon.com/cw/u6489658

## Suggested next stage

Implement the shared D1 schema and API for teams, players, seasons, scrims, match results, registration references and per-player payment statuses, plus a protected admin area. Keep secrets in Cloudflare environment variables, never in front-end files.
