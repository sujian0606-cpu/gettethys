# Tethys

Tethys offers AI-simulated consumer research for agents and developers. The official site is [gettethys.com](https://gettethys.com/). Use a simulated run as a directional preview before human research—not real respondents, market validation, or a sales forecast. Tethys does not promise accuracy, conversion, or other commercial outcomes.

This public repository is a developer entry point only. It is not a source-code release, an installable SDK, or a licensed open-source package, and it includes no credentials, payment addresses, or customer data.

## Official entry points

- Website: https://gettethys.com/
- Human workspace: https://gettethys.com/app/
- Order flow: https://gettethys.com/order/
- Recharge: https://gettethys.com/recharge/
- Agent console (keys and machine docs): https://gettethys.com/agents/
- OpenAPI: https://gettethys.com/openapi.yaml
- Health and route list: https://gettethys.com/api/health
- Research overview: https://gettethys.com/research/
- Method note: https://gettethys.com/method/ai-simulated-consumer/
- GEO visibility sampling (secondary, Beta): https://gettethys.com/geo/
- FAQ assistant: https://gettethys.com/support/
- Contact: gettethys@outlook.com

Humans work in `/app/` and place packages on the order page. Agents and developers should start at `/agents/` and the OpenAPI document above.

## Current scope

Paid research is a formula-priced package: a written persona / sampling frame, frozen prompts, a results table, and a re-testable method note. Log in, recharge, then deduct balance to submit an order. The order is recorded as an account ticket; checkout is not an instant public research API and does not auto-deliver a finished study.

Machine-readable status lives in the official OpenAPI and `GET /api/health`. Treat those as the source of truth. This README does not invent endpoints, SDK install commands, or copy-paste request examples.

Confirmed on the public site:

- A free, rate-limited simulated survey preview is documented at `GET /api/v1/sim-survey/demo` (n ≤ 10; question required). Output is labeled simulated, not a formal report.
- A free, rate-limited GEO demo can return a heuristic present/absent sample for a brand term. GEO is a secondary Beta, with no ranking, inclusion, or citation promises.
- `GET /api/v1/sim-survey` describes preview routes and states that full tiers are ordered through the business flow, not auto-unlocked.

Some documented paid preview routes may return HTTP 402 when unpaid. That is not a complete machine-payment integration, and paying a preview route does not fulfill a full research package.

An MCP descriptor is published at https://gettethys.com/mcp.json. This repository does not ship an MCP server or hosted gateway.

## Accounts, keys, and payment

Sign in at https://gettethys.com/login/, then use `/app/`. API keys are issued only through the official agent console at https://gettethys.com/agents/ after you have an account. The console documents the headers (`X-Tethys-Key` or `Authorization: Bearer`, with a `tth_…` key). The full key is shown once when you rotate it. Store it yourself; never commit it or paste it into issues, chat, or support mail.

Research, Web3 listing-readiness, and GEO packages use the same payment rule:

1. Log in first.
2. Recharge with Base USDC or Polygon USDT on the recharge page. Deposit addresses appear only there. After you submit a transaction hash, credit is usually applied within 24 hours on Asia/Shanghai weekdays.
3. When the balance covers the amount, return to the order page and deduct it.

Cards and PayPal are coming soon.

## Pricing

Verified on the official site:

- **$30 Base** — 30 simulated personas, 0 extra spans, one market and one concept, directional.
- **Custom** — total = `$1 × n` + `$1 × extra spans`.

The same formula applies to research, Web3, and GEO, on both the homepage quote form and the order page.

## Boundaries

- All research samples are AI-simulated, not real people.
- Deliverables are a directional preview and a method note, not a substitute for formal quantitative human research.
- No promises of accuracy, sales, conversion, listing approval, or AI citations.
- Validate important decisions with real respondents.
- Privacy policy and terms pages are not published yet (those URLs currently 404). Until they are, use the method note, the support page, or gettethys@outlook.com.

## This repository

The GitHub description matches the product: AI-simulated consumer research for agents and developers. There is no license file. Do not treat this repo as the production website.
