# GDPR Starter Kit — First B2B Customer

> First product of Marcus Orlov, Season 1. Status : **in production** —
> v0 target 2026-04-18.

---

## Target audience

Small European SaaS companies (≤ 50 people) who have just closed — or are
about to close — their first B2B customer, and whose prospect is asking for :

- a signable **Data Processing Agreement** (DPA),
- an Article 30 **record of processing activities** (registre de traitements),
- a credible public **privacy policy**,
- a minimal position on **international data transfers** (SCC, adequacy
  decisions, sub-processors like AWS / Google / OpenAI).

These founders are typically in a squeeze : the prospect wants to sign next
week, a lawyer quotes 2 000-5 000 €, free templates are generic enough to be
unsignable without rework, and nobody on the team has the bandwidth to write
it themselves.

## What the kit is, and is not

**It is** a set of editable documentary templates, pre-filled with realistic
SaaS defaults, shipped with a playbook that explains what to adapt, what to
negotiate, and what not to concede.

**It is not** individual legal advice. It is not a substitute for a
certified DPO or a lawyer. The kit is explicitly marketed as a documentary
template to be adapted, and each document carries that disclaimer in its
header. For complex situations — health data, minors, adtech with profiling,
regulated industries — customers are directed to a professional.

## Contents

1. **DPA template** — Data Processing Agreement, bilingual FR / EN,
   controller → processor, applicable EU. `.docx` and `.md` source.
2. **Register of processing activities** — Article 30 RGPD template,
   pre-filled with 8-10 standard SaaS processing activities (customer
   accounts, billing, support, product analytics, marketing ops, recruitment,
   HR, employee monitoring), columns left to customize. `.xlsx` and `.md`
   source.
3. **Public privacy policy** — FR and EN, website format (Markdown + rendered
   HTML), with placeholders for company-specific details.
4. **Note on international transfers** — short briefing on SCC module 1-4,
   adequacy decisions, and standard sub-processor cases (AWS, Google Cloud,
   OpenAI, Stripe, Intercom, Sentry). PDF + Markdown source.
5. **Playbook** — 6-8 pages : how to adapt each document, the 5-8 clauses
   clients most commonly push on, what to negotiate, what to refuse. PDF +
   Markdown source.

All files shipped together as a single ZIP. Customers keep their files. No
proprietary platform dependency.

## Pricing

**€149 TTC** (entry-level test price).

Pricing strategy (Season 1, aligned with the week-6 invalidation gate set in
`00-foundations/season-01-thesis.md`) :
- **Weeks 1-3** at 149 €. If zero sales at end of week 3, drop to 99 € for
  weeks 4-5.
- **Week 6** : if still zero sales, the thesis is reclassified as
  `invalidated` and a pivot is decided in weekend session.
- **199 €** is not tested pre-invalidation. It is reserved as a post-pivot
  hypothesis, only explored if a pivot reveals a willingness-to-pay signal
  above 149 €.

## Distribution

Canonical source : this repository, directory `05-products/gdpr-starter-kit/`.

Distribution channels (in order of priority) :
1. Gumroad storefront (primary — opened at v0 release, target 2026-04-18).
2. Targeted presence in 2-3 EU SaaS founder communities (Indie Hackers EU,
   Product Hunt makers, selected Slack / Discord).
3. Reseller partnerships with freelance DPOs (Season 1 stretch goal).

## Boundaries and disclaimers

- **Not legal advice.** Each document in the bundle carries a visible
  disclaimer in its header : *"Ce kit est un modèle documentaire à adapter à
  votre situation. Il ne constitue pas un conseil juridique individuel. Pour
  une situation complexe ou sensible, consultez un avocat ou un DPO
  certifié."*
- **Not audit-grade.** This kit is designed for a founder signing their
  first B2B customer, not for an ISO / SOC 2 audit file.
- **EU scope only.** The kit targets EU GDPR. Not UK DPA 2018 specifics, not
  US state laws (CCPA / CPRA etc.). V1 may expand.
- **Subject to CGV** validated by Bac before publication.

## Production state

See `outline.md` for the detailed work breakdown. See `STATUS.md` for
current progress.
