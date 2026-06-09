# Etymolt

### The fact-check layer for LLM-generated names.

Trademark · domain · cultural · sound · pronunciation — signed verdicts across five canonical axes, issued under the **Bureau Model** on the open **Etymolt Verdict Protocol (EVP/1)**.

[Product](https://etymolt.com) · [Methodology](https://etymolt.com/methodology) · [Protocol spec](./evp-spec) · [Security](https://etymolt.com/security)

---

## What we issue

A verdict is a JSON object conforming to [**EVP/1**](./evp-spec), our open CC-BY-4.0 protocol. Every verdict carries:

- A composite verdict — `PROCEED` / `ITERATE` / `DECIDE` / `ABANDON` / `INSUFFICIENT_SIGNAL`
- Five canonical axes — **trademark · domain · cultural · sound · pronunciation**
- A stated confidence interval and named uncertainty drivers
- A `coverage_caveat` per jurisdiction
- A verbatim disclaimer (the Bureau Model anchor)
- An Ed25519 signature over a JCS-canonicalized payload
- A deterministic `verdict_id` and permalink

A verdict is a clearance signal. It is not legal advice, not a recommendation, not an opinion.

## The Bureau Model

We report what the records of record show. We do not opine on infringement. We are not a law firm.

A verdict from Etymolt is to a brand name what a credit-bureau report is to credit history: a point-in-time signal compiled from authoritative sources, surfaced under a disclosed methodology, signed for downstream verification. The signal is not the decision.

## What's here

### Public

- **[evp-spec](./evp-spec)** — the Etymolt Verdict Protocol. CC-BY-4.0. In [public comment](https://github.com/etymolt/evp-spec/issues) until 2026-09-10.

### Coming soon

- **etymolt-node** — official TypeScript / JavaScript SDK
- **etymolt-python** — official Python SDK
- **etymolt-mcp** — Model Context Protocol server, already on [npm](https://www.npmjs.com/package/@etymolt/mcp-server) as `@etymolt/mcp-server`
- **etymolt-mock** — hardcoded fake API for SDK tests, no quota burned
- **etymolt-cli** — command-line interface
- **examples** — named per-framework starters (Next.js, MCP-in-Claude-Code, batch CSV, agent loop)
- **cookbook** — recipes for verifying at scale, wiring into a name generator, interpreting confidence
- **benchmarks** — `llm-hallucination-2026` ground-truth corpus

### Not public

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

— Etymolt · `evp@etymolt.com` · [`@etymolt`](https://twitter.com/etymolt)
