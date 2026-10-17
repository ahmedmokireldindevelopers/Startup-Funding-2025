# Startup Funding & Build System

A unified founder workspace that combines a practical startup-building library with a source-first directory of startup credits, grants, accelerators, discounts, and ecosystem programs.

## What is included?

This repository now combines two complementary projects:

### 1. Founder operating system

The React/Vite dashboard at `/` turns the learning library into a seven-phase workflow:

1. Discover the customer problem and business model.
2. Validate assumptions and define the MVP.
3. Build and learn through an iterative delivery cycle.
4. Monetize with pricing, revenue, and SaaS economics.
5. Go to market and build repeatable demand.
6. Operate with finance, people, risk, and KPI systems.
7. Fundraise with a pitch deck, model, data room, and investor pipeline.

Open the dashboard to search the work table, filter by phase or status, mark outcomes complete, and open the exact PDF, spreadsheet, CSV, or DOCX reference attached to each outcome.

### 2. Startup programs directory

The directory is a source-first, apply-ready catalog researched from official provider, fund, government, and accelerator pages. It covers:

- Cloud and AI credits.
- SaaS discounts and startup perks.
- Grants and non-dilutive funding.
- Accelerators and ecosystem programs.
- Global, China, Ukraine, and open-source resources.
- Coupon assessments and community leads clearly separated from verified official sources.

The current research snapshot is maintained in [`programs.csv`](programs.csv), with 38 active program records. Always re-check the official application page before applying because eligibility, benefits, and dates can change.

## Repository map

| Area | Purpose |
|---|---|
| `src/` | React dashboard and visual system |
| `Business Models - Super Guides Bundle/` | 54 PDFs covering business models, MVP, pricing, GTM, metrics, and fundraising |
| `Business Explained/` | Management, finance, operations, marketing, people, and technology references |
| `SAAS Toolkit/` | SaaS spreadsheets, CSVs, investor lists, templates, and operating models |
| `programs.csv` | Canonical machine-readable startup-program catalog |
| `categories/` | Program views by category |
| `global/` | Global credits, accelerators, and additional programs |
| `china/` | China cloud and AI programs |
| `ukraine/` | Ukraine grants and ecosystem programs |
| `open-source/` | Open-source alternatives and supporting directory |
| `communities/` | Public Reddit and Telegram discovery communities |
| `imports/` | Imported research inputs and source notes |
| `archive/` | Programs not currently verified as open or active |
| `.github/link-check-workflow.yml` | Ready-to-enable link and freshness check workflow |
| `MERGE_NOTES.md` | Decisions made during the two-repository merge |

The exact-duplicate `data/catalog.csv` was intentionally not retained because it was byte-for-byte identical to `programs.csv`. See [`data/README.md`](data/README.md).

## Run the dashboard locally

```bash
git clone https://github.com/ahmedmokireldindevelopers/Startup-Funding-2025.git
cd Startup-Funding-2025
npm install
npm run dev
```

Open `http://localhost:5173`.

To create a production build:

```bash
npm run build
```

## How to use the unified system

Start with the dashboard and complete the outcomes in order. For each outcome, read only the linked references needed for the current decision, create the deliverable, record the metric, and keep the evidence in your project workspace. Once the business has evidence of customer demand and operating discipline, use the programs directory to match the company against credits, grants, accelerators, and ecosystem support.

Use `programs.csv` to filter by provider, region, type, stage, status, and category. Use the linked Markdown pages for the detailed eligibility and application roadmap. The official application link is the source of truth; the directory is a research aid, not a guarantee of eligibility or funding.

The dashboard's **Big Funnel roadmap** is the main sequence: problem clarity → evidence of need → usable proof → economic proof → repeatable demand → company readiness → investor conversion. Each gate includes the user action, exit evidence, and the funnel movement expected before advancing.

For document access and password protection, read [`docs/SECURE-FILES.md`](docs/SECURE-FILES.md). Public GitHub files cannot be securely protected by a front-end password; use a private repository, AES-256 archive, or controlled data room instead.

## Updating the directory

The directory follows these quality rules:

- Prefer a primary official source.
- Do not infer eligibility, deadlines, amounts, or documents.
- Keep the README tables, category pages, detail pages, and `programs.csv` synchronized when changing an active entry.
- Use the exact status badges: `✅ Open`, `🔄 Rolling`, `⏳ Opens soon`, or `❌ Closed`.
- Move expired, closed, or insufficiently verified entries to `archive/`.
- Update `last_verified` whenever a row changes.
- Treat Reddit, Telegram, and community references as discovery leads only, never as proof of a working coupon or offer.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for the complete entry and coupon-field rules.

## Licensing and source rights

The root MIT license covers the project code unless a resource states otherwise. The PDFs, spreadsheets, DOCX files, and third-party directory content may have separate copyrights or terms. Review the source and usage rights before redistributing, selling, or placing any resource in a paid product.
