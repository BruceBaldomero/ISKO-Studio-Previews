# ISKO Studio — Claude Code Context

You are helping Bruk run ISKO Studio, a web design side hustle based in London (Surbiton area).
Every session read this file first. This is the source of truth for how ISKO operates.

---

## Who I am

- **Name:** Bruk
- **Business:** ISKO Studio — I design and build websites for local businesses
- **Stack:** Static HTML/CSS/JS, GitHub Pages hosting, Formspree (contact forms), GoCardless (payments), GA4 + Google Search Console, Namecheap (domains)
- **My site:** iskostudio.com (hosted on GitHub Pages)
- **Positioning:** "Digital architect for local businesses — get found, look credible, win more customers"

---

## Tiers & Pricing

| | Starter | Standard | Premium |
|---|---|---|---|
| Price | £500 | £850 | £1,400 |
| Deposit (50%) | £250 | £425 | £700 |
| Balance (50%) | £250 | £425 | £700 |
| Care plan /mo | £50 | £75 | £100 |
| Pages | 1–3 | up to ~5 | 6–8 |
| Copywriting | They provide | I polish | I write it |
| Revisions | 2 rounds | 2 rounds | 3 rounds |
| Build time | 1–2 weeks | 2–3 weeks | 3–4 weeks |

**Pricing rules:**
- Always quote build price WITH the care plan, never separately
- 50% deposit before starting, 50% before launch
- Round numbers only, no charm pricing (no £499, no £847)

**Tier decision:**
- Just needs to exist online, has own content → **Starter**
- Wants proper multi-page presence, needs polish → **Standard**
- Wants premium/bespoke, hands-off, wants me to write it → **Premium**

---

## Tech stack — use this on every build

- **Hosting:** GitHub Pages (deploy to brucebaldomero.github.io/[repo-name] for preview, then custom domain)
- **Forms:** Formspree (each client gets their own form ID)
- **Payments:** GoCardless one-off paylinks for deposit + balance; subscription for care plan
- **Analytics:** GA4 + Google Search Console (client's account, me as Manager)
- **Domains:** Namecheap — buy on client's behalf, push to their account at handover
- **Fonts default:** Fraunces (display) + Inter Tight (body) — vary per client so sites don't all look the same
- **Models:** Sonnet by default. Opus only for genuinely complex/bespoke sections.

---

## File structure — use this on every client build

```
/client-repo
  index.html
  services.html (Standard/Premium)
  about.html (Standard/Premium)
  gallery.html (if needed)
  privacy.html
  terms.html (Premium, or if client wants it)
  thankyou.html (if they take bookings/payments)
  404.html
  robots.txt
  sitemap.xml
  CNAME (their custom domain)
  CLAUDE.md (this client's design system — write before building)
  /css
  /img
  /js
```

---

## SEO baseline — every page, every build

- Unique `<title>` + meta description
- Open Graph + Twitter card tags + OG image
- JSON-LD LocalBusiness structured data (correct subtype for their niche) — name, address, phone, hours, geo, sameAs socials
- `sitemap.xml`, `robots.txt`, custom `404.html`, favicon
- Privacy + cookie page (+ terms for Premium)

---

## Design rules

1. **Write a per-client CLAUDE.md BEFORE generating anything.** Extract palette from their logo/Instagram, pick fonts, write a one-line vibe. This file goes in the client repo root.
2. **Never ship the same layout twice.** Deliberately pick a different hero style and section order each time.
3. **Vary fonts per client.** Fraunces + Inter Tight is my house default — don't use it unchanged for every client.
4. **Regulated niches (aesthetics, medical, finance, food):** flag to client. Medical aesthetics = no naming injectables, no before/after of POMs, no price promotions. Build around "book a consultation."

---

## The 13-stage client process

1. Enquiry lands (inbound or outbound preview)
2. Reply & book discovery chat — **Email A**
3. Discovery chat — gather: what they do, what site needs to do, pages needed, existing assets, budget, timeline, reference sites they like
4. Send proposal — tier-matched template — **Email B (proposal)**
5. Contract agreed (email reply = legally sufficient in England & Wales) + deposit link sent → **wait for deposit to clear before starting**
6. Onboarding form sent — **Email C** — set content deadline (2 weeks)
7. Design direction: palette, fonts, vibe, layout — write per-client CLAUDE.md
8. Build in Claude Code — Sonnet default
9. Preview link sent — **Email D** — "send ALL feedback in one go"
10. Revisions (2 rounds Starter/Standard, 3 Premium) → explicit sign-off
11. Balance payment sent → **wait for balance to clear before launching**
12. DNS: 4 × A records + www CNAME at Namecheap, remove parking records, Enforce HTTPS after propagation
13. Post-launch: Search Console, Google Business Profile, GA4 confirmed
14. Handover email — **Email F** — care plan link, Google review request, referral ask, portfolio permission

**Gate rules (never break these):**
- No work starts until deposit clears
- Site does not go live until balance clears

---

## Outbound preview method

This is the primary way I find clients:

1. Find a local business on Google Maps with no website (or a terrible one), good reviews
2. Build a quick 1–3 hour preview using their real brand cues (logo, colours, Instagram photos)
3. Deploy to a `brucebaldomero.github.io/previews/[business-name]` URL
4. Reach out: "Hi [Name] — I'm a web designer based near you. I built a quick homepage concept for [Business] — want the link?"
5. If they bite → straight into Stage 3 with a huge head start

**When I say "build an outbound preview" for a business:**
- Create folder `/previews/[business-name]/`
- One page: hero, about, what they do, hours + map, footer
- Use their real brand colours and feel from Instagram
- Placeholder images where needed — I'll swap in real photos
- Deploy to github.io preview URL
- Warm, human tone — not corporate

**Deployment rule — always do this after every preview build:**
1. Commit the files
2. Push to `main` (not a feature branch) so GitHub Pages serves it immediately
3. Preview URL is live at: `brucebaldomero.github.io/previews/[business-name]/`

---

## My existing work / portfolio

- **iskostudio.com** — my own site (Standard scope)
- **mukhafaceyoga.com** — yoga instructor, Standard–Premium scope, free client (my sister)

---

## Care plan — what's included monthly

- Uptime monitoring (UptimeRobot)
- Monthly contact form test
- PageSpeed check
- Small edits within tier's included time
- Monthly care report email to client
- Domain renewal watch

Static sites (no WordPress) mean: no plugin updates, no database backups, no malware scans. Low effort, high value to client.

---

## When starting any new session

If I say "new client" or "new outbound preview" — ask me for:
1. Business name + type
2. Location
3. Instagram handle (if they have one)
4. Any brand colours or vibe notes
5. Their Google Maps / review link if I have it

Then get building.
