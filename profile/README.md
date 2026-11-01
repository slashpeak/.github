# SlashPeak

**The AI DBA for BigQuery.** See where every dollar goes, catch cost spikes early, and ship fixes as pull requests.

SlashPeak is a cost tool for data teams that run Google BigQuery. It reads your BigQuery metadata, prices every job and table the way you are billed, ranks each saving in dollars, and can open the pull request that fixes it.

[**Start a free 30-day trial**](https://app.slashpeak.com/signup) · [Book a demo](https://slashpeak.com/demo) · [Watch the 90-second tour](https://slashpeak.com/videos)

---

## Who it is for

- **Heads of data and data platform leads** who need to explain the BigQuery bill and bring it down.
- **Analytics and data engineers** who want to know which queries, tables and dbt models cost the most.
- **FinOps teams** who need spend by team, budgets and alerts before the invoice arrives.

## What you get

### 1. Cost analytics: see every dollar

- Spend by **project, team, user, table, query, label and tool**.
- Priced the way you are billed: **on-demand, Editions capacity, or a hybrid** of both.
- Checked against your **Cloud Billing export**, so the numbers match the invoice.
- **Cost centers and budgets**: group spend by team or product with match rules, and give each group a monthly budget.
- **Anomaly detection**: cost spikes are explained, not just flagged.
- **Airflow cost per DAG and task**, from the labels Airflow already puts on each job.
- Reservations and slot utilisation, multi-project views, saved filters.

### 2. Savings findings: a ranked list, not a score

- **23 documented cost rules** across queries, storage, schema design and capacity.
- Every finding has a **monthly dollar estimate**, with the evidence, a sample query and the math shown.
- The list is sorted by dollar impact, so the top item is always the best use of your next hour.
- Findings **close themselves** when the next scan no longer sees the problem, so savings are realized, not only promised.

Examples of what it finds:

| Area | Examples |
|---|---|
| Query waste | Missing partition filters, `SELECT *` on wide tables, the same heavy query run again and again |
| Storage | Wrong storage billing model, tables nobody has queried in months |
| Capacity and pricing model | On-demand vs. Editions per project, idle reservations, slot contention |
| dbt | Incremental models that keep rebuilding the whole table, expensive dbt tests |

### 3. Cognis AI DBA: ship the fix

- Opens a **GitHub pull request** for dbt and SQL fixes through the SlashPeak GitHub App.
- Your CI runs on it like on any other PR. **A person on your team reviews and merges. It never merges by itself.**
- Other actions wait for an **owner's approval** by default. Almost all of them can be undone.
- **Cognis AI chat** answers plain-English questions from your own cost data, and the **AI query optimizer** suggests cheaper SQL.

### 4. Alerts and reports

- Email, **Slack** and webhook alerts for cost spikes, budgets and new findings.
- Daily, weekly or monthly report emails, plus CSV and Excel exports.
- A read-only **REST API** on Growth and up.

## How it works

1. **Connect read-only access.** Create a BigQuery service account with metadata-only permissions. There is no agent to install and no key to upload.
2. **SlashPeak scans.** Each scan reads job history, table storage and reservations. Most first scans finish in under a minute.
3. **Fix and confirm.** Work down the ranked list yourself or with the Cognis AI DBA. Each finding closes once the fix shows up in the next scan.

## Security

- **Metadata only.** SlashPeak reads job history, table definitions, storage sizes and reservation usage. It never queries your table rows.
- **No service account key.** You give SlashPeak the Token Creator role on your read-only service account. Each scan gets a Google sign-in that ends within 1 hour. You can remove access at any time.
- **Every permission is listed** on the [Security page](https://slashpeak.com/security), with what each one is for.
- **Tenant isolation.** Every request is scoped to your account, and Postgres row-level security adds a second check.
- **SOC 2 is in progress.** We support vendor security reviews and sign DPAs.

## Pricing

Prices in USD, monthly or yearly (2 months free on yearly). Same numbers in euros in the euro area.

| Plan | Price | Best for |
|---|---|---|
| **Starter** | $199/mo | Small data teams that want to see where BigQuery spend goes. 2 seats, scans every 6 hours, all 23 rules. |
| **Growth** | $499/mo | Teams ready to fix waste with the Cognis AI DBA and dbt pull requests. 8 seats, scans every 3 hours, REST API. |
| **Pro** | $999/mo | Many teams at scale. 25 seats, hourly scans, 60-day history, slot and reservation right-sizing. |
| **Enterprise** | Custom | Companies above $50k a month in BigQuery spend. Unlimited seats, SLA, dedicated Slack channel. |

**Free 30-day trial, no credit card.** Full details on the [pricing page](https://slashpeak.com/pricing).

## Warehouses

- **BigQuery**: live today.
- **Snowflake** and **Databricks**: coming soon, on the same read-only, metadata-only model. [Join the waitlist](https://slashpeak.com/integrations).

## Learn more

- [Product overview](https://slashpeak.com/products)
- [Docs](https://slashpeak.com/docs)
- [FAQ](https://slashpeak.com/faq)
- [Compare SlashPeak to alternatives](https://slashpeak.com/compare)
- [Blog: BigQuery cost guides](https://slashpeak.com/blog)
- [Video walkthroughs](https://slashpeak.com/videos) · [YouTube](https://www.youtube.com/@slashpeak) · [X](https://x.com/slashpeak)

Questions? Write to [hello@slashpeak.com](mailto:hello@slashpeak.com) or [book a demo](https://slashpeak.com/demo).
