# Clarifying questions — developer

Questions that block or meaningfully shape implementation. Grouped by what they unblock.

## 1. Stack & framework

The brief names "Webflow / Next.js / Sanity-tier shops" as the audience but doesn't specify what *we're* building with.

- **Framework:** Next.js (App Router, assumed 15+) — confirm? Or are we building in Webflow as a meta-flex ("the audience's tool")?
- **CMS:** Sanity for blog posts and structured content? Or MDX in-repo? (The "repo *is* the demo" framing leans MDX, but Sanity demonstrates the agency-relevant skillset better.)
- **Styling:** Tailwind v4? CSS modules? Something more bespoke? Any existing design tokens to inherit?
- **Hosting:** Vercel?
- **Package manager:** pnpm / bun / npm?

## 2. "Book a call" — the primary CTA

This is the conversion point, so it needs to actually work end-to-end.

- Booking provider: Cal.com, Calendly, or custom?
- Embedded inline, modal, or redirect?
- What happens after booking — confirmation page, email, anything else?
- Is the calendar live (real availability on Mike's calendar) or a mock for launch?

## 3. Lead capture & CRM

The brief says "lead-capture, CRM hand-off, nurture sequence — all mocked but production-quality."

- "Mocked but production-quality" — does that mean: real form → real CRM (HubSpot/Attio/Notion?) → real nurture (Loops/Resend/Customer.io?) but without paid traffic? Or: UI flows + fixtures + Storybook-style demo, no live integrations?
- If real: which CRM and which email provider should I wire up?
- Where do form submissions land for *actual* inbound leads from organic traffic during the job search?

## 4. Paid channel mocks

- Are the landing variants real routes (e.g., `/agency-founders`, `/hiring-managers`) or static design mocks?
- Ad creative — do you have copy/visuals, or am I generating placeholder concepts?
- A/B framework needed, or just static variants we can point ads at later?

## 5. SEO posts

- Three foundational posts — do you have topics/drafts, or am I drafting from scratch based on the audience?
- Reading time, length target, code samples?
- Author bio / OG images / structured data — full SEO treatment, or basic?

## 6. The "repo is the demo" constraint

This shapes how we work, not just what we build.

- Commit hygiene: conventional commits? Signed? PR-per-feature so `git log` reads as a narrative?
- Should the README double as a case study, or is there a separate `/case-study` route?
- Are Linear-style issues, Figma links, design docs, RFCs *also* in the repo (markdown files), or just code + commits?
- Public repo from day one, or private until launch?

## 7. Analytics & measurement

- Provider: GA4, Plausible, PostHog, Vercel Analytics?
- Are we tracking the full funnel (ad → landing → form → booking) for the demo, or just page views?

## 8. Design system

- Starting from existing tokens / Figma library, or building from scratch?
- Dark mode required for launch?
- Motion/animation budget — opinionated and bold, or restrained?

## 9. Quality bar for T+24h

- Lighthouse / Core Web Vitals targets?
- Accessibility: WCAG AA non-negotiable?
- Browser/device support floor?

## 10. Domain, infra, and the boring stuff

- Is `heggie.design` already registered and pointed somewhere?
- Email on the domain (for form replies / "from" address)?
- Any existing repo content from prior iterations to migrate, or fully greenfield?

---

**Top 3 I'd want answered before writing a single line of code:** 1 (stack), 3 (real vs. mocked integrations), 6 (repo-as-demo workflow rules).
