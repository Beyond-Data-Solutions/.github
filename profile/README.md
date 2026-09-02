# Beyond Data Solutions

Data engineering, automation, and custom software for small and mid-sized businesses. Phoenix, Arizona.

We take the systems a business already runs on (QuickBooks, spreadsheets, Microsoft 365, job trackers, SaaS exports, vendor PDFs) and turn them into one reliable set of numbers. Then we automate the work that was being done by hand around them.

## What we build

**BPO Autopilot** ([bpoautopilot.com](https://www.bpoautopilot.com)). A production B2B tool for broker price opinion work. It reads MLS order packets, extracts subject and comparable data into an editable review grid, and drives the vendor form field by field. It fills and stops; the agent reviews and submits. Built with a design partner who runs real orders through it, hosted on our own infrastructure, multi-tenant with row-level security. Login-gated because it holds customer data.

**Beyond Ops.** The Node.js and PostgreSQL platform that runs our own back office. An agent workforce drafts, scores, and files work under human approval. A bid engine triages the freelance pipeline with deterministic verdict gates before any language model sees a job post. A CRM built from ten years of email history. Security and cost gates keep the AI parts from doing anything unsupervised. It is also the test bed for how we build for clients.

**Beyond Assets.** A personal financial tracking application with TOTP two-factor enrollment, versioned migrations, nightly encrypted off-box backups, and a design system tuned for reading numbers on screen.

**Systematic trading research.** A public-data ingest and backtesting platform for spot crypto on Kraken. Cost-aware walk-forward testing against real tiered fees, deterministic signals only, no live execution.

**Client reporting and automation.** Power BI and DAX dashboards, Power Query and Power Automate pipelines, Python ETL, and the SQL underneath all of it. Recent work includes multi-source executive dashboards, an ERP data migration with fuzzy-matched customer deduplication, a price-list pipeline that normalizes dozens of vendor file formats into one schema with a golden-file regression harness, and a HIPAA-aware referral tracker on Microsoft 365.

## Track record

- An LLM-powered jurisdiction resolver for solar permitting that checks multiple authoritative sources, requires agreement, and escalates to a human when they disagree. Tracked at ~98% accuracy in production.
- An insurance claims pipeline in Python, SQL, and Power Automate that peaked at ~500,000 claims in a single month across a fleet of 52 virtual machines, with a live Power BI monitor on the database.
- Scheduled Claude agents doing real operational work: a twice-daily server security audit that compares against trend and flags new risks, and an inbox-scanning agent that classifies three years of sales leads over MCP.
- A layered server defense that blocked ~53,000 attack and probing attempts over four months.

## How we work

- Every change ships through a pull request or a gated deploy script. Nothing reaches production on a red gate.
- Agents propose, people approve. No AI-generated change executes without a human approval on record.
- Deterministic logic first, language models second. Rules decide what ships. The LLM handles the ambiguous middle.
- Schema changes are numbered migrations from day one.
- Databases run with separate owner and application roles, and row-level security where tenants share a schema.
- Safety-layer code is mutation-tested. Gates fail closed.
- A test count is pasted runner output, never a number from memory.
- Secrets live on the server, not in repos, not in chat logs.

## Stack

Node.js, TypeScript, React, Next.js, Python, PostgreSQL, Power BI, Power Query, Power Automate, Power Apps, SharePoint, Excel/VBA, Claude API and MCP, Playwright, Linux on AWS Lightsail behind nginx and fail2ban.

## Repositories

The code here is client and internal production work, so the repositories are private. This is the map.

| Repository | What it is | Status |
|---|---|---|
| `BDS_server` | Beyond Ops: agent supervisor, war room task board, bid engine, CRM, deploy and migration tooling | Production |
| `BDS_bpo` | BPO Autopilot web application and fill engine | Production |
| `BDS_website` | Marketing site (Next.js) | Live |
| `BDS_vault` | Obsidian knowledge base: doctrine, proof registry, night-run specs | Active |
| `<assets-repo>` | Beyond Assets financial tracker | Production |
| `<trading-repo>` | Kraken spot ingest and backtesting platform | Research |
| `<poshtracker-repo>` | Resale inventory and listing tracker | Rebuild in progress |
| `<repo>` | | |
| `<repo>` | | |
| `<migrating-1>` | | Migrating |
| `<migrating-2>` | | Migrating |

If you are evaluating us for a project, we are glad to walk through any of it live.

## Contact

Logan Spiers, founder
lspiers@beyonddatasolutions.co · [BeyondDataSolutions.co](https://www.BeyondDataSolutions.co) (coming soon)
