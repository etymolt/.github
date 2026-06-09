# Etymolt

### The fact-check layer for LLM-generated names.

Trademark · domain · cultural · sound · pronunciation — signed verdicts across five canonical axes, issued under the **Bureau Model** on the open **Etymolt Verdict Protocol (EVP/1)**.

[Product](https://etymolt.com) · [Methodology](https://etymolt.com/methodology) · [Protocol spec](https://github.com/etymolt/evp-spec) · [Security](https://etymolt.com/security)

---

## What we issue

A verdict is a JSON object conforming to [**EVP/1**](https://github.com/etymolt/evp-spec), our open CC-BY-4.0 protocol. Every verdict carries:

- A composite verdict — `PROCEED` / `ITERATE` / `DECIDE` / `ABANDON` / `INSUFFICIENT_SIGNAL`
- Five canonical axes — **trademark · domain · cultural · sound · pronunciation**
- A stated confidence interval and named uncertainty drivers
- A `coverage_caveat` per jurisdiction
- A verbatim disclaimer (the Bureau Model anchor)
- An Ed25519 signature over a JCS-canonicalized payload
- A deterministic `verdict_id` and permalink
- Temporal-validity metadata (`issued_at`, `valid_until`, `axis_freshness`)

A verdict is a clearance signal. It is not legal advice, not a recommendation, not an opinion.

## The Bureau Model

We report what the records of record show. We do not opine on infringement. We are not a law firm.

A verdict from Etymolt is to a brand name what a credit-bureau report is to credit history: a point-in-time signal compiled from authoritative sources, surfaced under a disclosed methodology, signed for downstream verification. The signal is not the decision.

## Public surfaces

| Repo | Purpose |
|---|---|
| [**evp-spec**](https://github.com/etymolt/evp-spec) | The protocol specification. CC-BY-4.0. v1.0.0 in [public comment](https://github.com/etymolt/evp-spec/issues) until 2026-09-10. |
| [**mcp-server**](https://github.com/etymolt/mcp-server) | The official Model Context Protocol server. Published as [`@etymolt/mcp-server`](https://www.npmjs.com/package/@etymolt/mcp-server) on npm. Drop-in for Claude, Cursor, ChatGPT, Windsurf, any MCP-compatible host. |
| [**llm-hallucination-benchmark**](https://github.com/etymolt/llm-hallucination-benchmark) | Public ground-truth corpus measuring how often frontier LLMs fabricate USPTO citations. Updated quarterly. |
| [**brand-assets**](https://github.com/etymolt/brand-assets) | Logos, marks, color tokens. CC-BY-4.0 except for trademarks. |
| [**forge-docs**](https://github.com/etymolt/forge-docs) | Etymolt Forge — the post-name automation product. |
| [**.github**](https://github.com/etymolt/.github) | This repo. Org-wide community-health files. |

## Coming soon

- **etymolt-node** — official TypeScript / JavaScript SDK (auto-generated from OpenAPI)
- **etymolt-python** — official Python SDK
- **etymolt-cli** — command-line interface
- **etymolt-mock** — hardcoded fake API for SDK tests, no quota burned
- **examples** — named per-framework starters (Next.js, MCP-in-Claude-Code, batch CSV, agent loop)
- **cookbook** — recipes for verifying at scale, wiring into a name generator, interpreting confidence
- **design-skills** — brand identity as installable `npx skills add etymolt/design-skills`

## Not public

The production server, the data corpora, the scoring weights, and the operational infrastructure stay closed. Like Stripe's API server, Anthropic's model weights, and Linear's sync engine — the protocol is open, the implementation is ours.

## Get started

```bash
# Verify a candidate name (free tier, no signup)
curl -X POST https://api.etymolt.com/v1/verify \
  -H "content-type: application/json" \
  -d '{"name":"Stratagem"}'
```

The response is a signed EVP/1 verdict. Take it to counsel, ship it to your downstream tools, or render it in your own UI — the spec governs the format, your implementation governs the experience.

## Naming, attested.

— Etymolt · `hello@etymolt.com` · [`@etymolt`](https://twitter.com/etymolt)
