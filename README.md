# Bespoke Post

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
