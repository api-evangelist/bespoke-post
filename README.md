# Bespoke Post

Bespoke Post is a New York City direct-to-consumer men's lifestyle retailer founded in 2011
by Rishi Prabhu and Steven Szaronos. It sells curated menswear, gear and home goods through a
free-to-join membership — members answer an onboarding quiz, preview a personalized monthly
"Box of Awesome" they can swap or skip, and buy at member pricing. Alongside independent
third-party brands the company operates its own labels: Line of Trade and Fieldworth
(apparel), Halfday (travel), Wren (outdoor), Ash and Fir (home and fragrance) and Marcellin
(kitchen and bar).

- Website: https://www.bespokepost.com/
- Support: https://support.bespokepost.com/
- Field Guide (blog): https://www.bespokepost.com/field-guide
- GitHub: https://github.com/bespokepost
- Secondary market: https://forgeglobal.com/bespoke-post_stock/

## API posture

Bespoke Post publishes **no developer portal, no API documentation and no machine-readable
specification**. As of 2026-08-02 no OpenAPI, Swagger, AsyncAPI, GraphQL schema, MCP server
or A2A agent card was found on any host probed (`www.bespokepost.com`, `bespokepost.com`,
`support.bespokepost.com`; `api.bespokepost.com` does not resolve).

What it does have is more interesting than nothing: an **undocumented storefront API** under
`/api/`, eight of whose paths Bespoke Post names in its own `robots.txt` with explicit
`Allow:` directives for eight AI agents — GPTBot, ChatGPT-User, OAI-Searchbot, ClaudeBot,
anthropic-ai, PerplexityBot, meta-externalagent and cohere-ai — while `User-agent: *` is
`Disallow: /api/`. That is a provider-authored, machine-readable agent access policy on a
retailer with no developer program, captured in `agentic-access/`.

Note: `bespoke-api.readme.io` is a **different** company (an email-delivery API also called
"Bespoke") and is not associated with Bespoke Post.

## Artifacts

| Path | What it is |
|---|---|
| `apis.yml` | APIs.json 0.20 index — identity, link properties, the storefront API entry |
| `agentic-access/bespoke-post-agentic-access.yml` | The robots.txt AI-agent access policy, classified per path |
| `agentic-access/bespoke-post-robots.txt` | Verbatim `robots.txt` (the source of that policy) |
| `security/bespoke-post-domain-security.yml` | Probed TLS / HSTS / DNSSEC / CAA / SPF / DMARC |
| `well-known/bespoke-post-well-known.yml` | Result of probing every `/.well-known/` discovery path |
| `llms/bespoke-post-llms.txt` | Generated `llms.txt` for this provider |

Not present, and correctly so: `openapi/`, `mcp/`, `a2a/`, `skills/`, `packages/`,
`conventions/`, `errors/`, `lifecycle/`, `sandbox/`, `changelog/`. There is no published
contract to ground them in, and none were fabricated.
