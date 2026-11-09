# Panda Public Funding Tools

<!-- mcp-name: io.github.pandadad0214/panda-public-funding-tools -->

Give Claude, Cursor or any MCP client 8 US federal money and filings tools: grants, contract awards and recompetes, SBIR/STTR topics, SEC financials, clinical trials, Federal Register, recalls and VIN decode. Each tool runs one public-data Apify Actor on your own Apify account and is priced per result. Part of the [Panda Federation](https://github.com/pandadad0214/panda-federation-tools) toolkit (36 tools in four focused servers).

[![PyPI](https://img.shields.io/pypi/v/panda-public-funding-tools)](https://pypi.org/project/panda-public-funding-tools/)
[![Latest Release](https://img.shields.io/github/v/release/pandadad0214/panda-public-funding-tools?label=latest%20release)](https://github.com/pandadad0214/panda-public-funding-tools/releases/latest)
[![Umbrella](https://img.shields.io/badge/index-panda--federation--tools-blue)](https://github.com/pandadad0214/panda-federation-tools)
[![Apify Store](https://img.shields.io/badge/Apify_Store-pandadad0214-00a3ff)](https://apify.com/pandadad0214)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

<a href="https://launchmcp.co?utm_source=badge&utm_medium=referral" target="_blank" rel="nofollow noopener noreferrer"><img src="https://launchmcp.co/featured-badge.png?v=1" alt="Featured on Launch MCP" width="200" height="52" /></a>

## How to use this

```bash
uvx panda-public-funding-tools
```

1. **Get a free Apify token** at [console.apify.com/settings/integrations](https://console.apify.com/settings/integrations) (the free plan includes $5 of monthly credit) and install [uv](https://docs.astral.sh/uv/).
2. **Add the server to your MCP client:** command `uvx`, args `["panda-public-funding-tools"]`, env `APIFY_TOKEN` (Cursor JSON below).
3. **Ask in plain words**, e.g. "Find open federal grants on wildfire sensors and the contracts in that NAICS ending in the next six months." Start with one or two inputs and read the `summary` / `agentSummary` line before widening.

```json
{"mcpServers": {"panda-public-funding-tools": {"command": "uvx", "args": ["panda-public-funding-tools"], "env": {"APIFY_TOKEN": "apify_api_YOUR_TOKEN"}}}}
```

## For AI agents

| Field | Value |
| --- | --- |
| Purpose | Focused MCP server with 8 US federal money and filings tools: grants, contract awards and recompetes, SBIR/STTR topics, SEC financials, clinical trials, Federal Register, recalls and VIN decode. |
| Use when | A task needs US federal funding, contract, filing, regulatory or safety-recall data from official government APIs. |
| Do not use when | The task is about papers and citations (use `panda-research-tools`), private-sector leads (`panda-leads-tools`) or site/email safety (`panda-web-security-tools`). |
| Install | `uvx panda-public-funding-tools` (stdio, Python 3.11+) |
| Auth | `APIFY_TOKEN` env var; runs bill to that Apify account. |
| Tools | 8, listed under [Tools](#tools-8) |
| Outputs | JSON rows plus a one-line `summary` / `agentSummary`; Excel/CSV files on the Apify run. |
| Side effects and cost | Starts Apify runs; pay per result; empty runs are not charged per result; `run_max_charge_usd` caps each call. Read-only toward third-party sites. |

## Other ways to install

From the umbrella package (same tools):

```bash
uvx --from panda-federation-tools panda-public-funding-tools
```

From this repo instead of PyPI:

```bash
uvx --from git+https://github.com/pandadad0214/panda-public-funding-tools panda-public-funding-tools
```

Cursor / Claude / VS Code: command `uvx`, args `["panda-public-funding-tools"]`, env `APIFY_TOKEN`.

Official MCP Registry name for this stdio package: `io.github.pandadad0214/panda-public-funding-tools` ([server.json](server.json)). Registry clients install the PyPI package with `uvx panda-public-funding-tools`. The git command above stays the install path from this repo.

## Use with Gemini CLI

Install this repo as a [Gemini CLI extension](https://geminicli.com/docs/extensions/) (adds the MCP server plus a short `GEMINI.md` context file). Needs [Gemini CLI](https://geminicli.com/), [uv](https://docs.astral.sh/uv/), and a free [Apify token](https://console.apify.com/settings/integrations).

```bash
gemini extensions install https://github.com/pandadad0214/panda-public-funding-tools
```

The extension prompts for `APIFY_TOKEN` on install and launches the server with `uvx panda-public-funding-tools`. Gallery listing is automatic once this public repo carries the `gemini-cli-extension` topic and a root `gemini-extension.json` (crawled daily).

## Tools (8)

- `grants_finder`
- `federal_contract_finder`
- `sbir_sttr_topic_radar`
- `sec_financials_excel`
- `clinical_trial_leads`
- `federal_register_monitor`
- `product_recall_monitor`
- `vin_decoder_recalls`

Each tool runs one Apify Actor on your account. Empty runs are not charged per result; every call is capped by `run_max_charge_usd`. Full schemas and prices: [umbrella README](https://github.com/pandadad0214/panda-federation-tools#domain-tool-lists).

## Sibling domain servers

- [`panda-research-tools`](https://github.com/pandadad0214/panda-research-tools) — Scholarly integrity and papers: citation checks, literature and PubMed search, academic experts, PDF tables, Wayback Machine snapshots.
- [`panda-leads-tools`](https://github.com/pandadad0214/panda-leads-tools) — Public leads and enrichment: NPI providers, podcasts, local businesses, hiring signals, website enrichment, team pages, topic trends, trucking carriers, IRS nonprofits, building permits, new Florida, Texas and New York businesses, H-1B visa sponsors, EU tenders.
- [`panda-web-security-tools`](https://github.com/pandadad0214/panda-web-security-tools) — Site, email and agent safety: SPF/DKIM/DMARC audits, AI/SEO readiness, website change monitoring, hidden AI instructions scanner, bulk domain WHOIS/expiry, broken link checker.

Index / compatibility mega-server: [panda-federation-tools](https://github.com/pandadad0214/panda-federation-tools) (use only when you truly need every tool).

## TDQS standard

New tools join this domain only while the count stays in the 3–15 band. Descriptions follow the checklist in the umbrella repo. See [tdqs-standard](https://github.com/pandadad0214/panda-federation-tools) / project docs.

Built by Panda Federation. MIT licensed.
