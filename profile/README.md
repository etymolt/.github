# Etymolt

### The fact-check layer for LLM-generated names.

Trademark · domain · cultural · sound · pronunciation — signed verdicts across five canonical axes.

[Product](https://etymolt.com) · [Methodology](https://etymolt.com/methodology) · [Protocol](https://github.com/etymolt/evp-spec) · [Security](https://etymolt.com/security)

---

## Try it

```bash
curl -X POST https://api.etymolt.com/v1/verify \
  -H "content-type: application/json" \
  -d '{"name":"Stratagem"}'
```

The response is a signed [EVP/1](https://github.com/etymolt/evp-spec) verdict. Free tier, no signup.

## Use it from your stack

| | |
|---|---|
| **MCP** — Claude, Cursor, ChatGPT, Windsurf | [`@etymolt/mcp-server`](https://github.com/etymolt/mcp-server) |
| **OpenAPI** — generate any client | [`etymolt/openapi`](https://github.com/etymolt/openapi) |
| **Recipes** — examples for every surface | [`etymolt/cookbook`](https://github.com/etymolt/cookbook) |
| **Brand & design** — as installable agent skill | [`etymolt/design-skills`](https://github.com/etymolt/design-skills) |

## Read the protocol

EVP/1 is the open ([CC-BY-4.0](https://github.com/etymolt/evp-spec/blob/main/LICENSE)) wire format for signed brand-name clearance verdicts. Five canonical axes, Ed25519 signatures over JCS-canonicalized payloads, verbatim disclaimer, temporal-validity fields. In [public comment](https://github.com/etymolt/evp-spec/issues) until 2026-09-10.

→ **[etymolt/evp-spec](https://github.com/etymolt/evp-spec)**

## What a verdict is

A clearance signal compiled from records of record. **Not** legal advice. **Not** a recommendation. **Not** a name generator. We report what the registries show; counsel decides what to do about it.

## Naming, attested.

`hello@etymolt.com` · [`@etymolt`](https://twitter.com/etymolt)
