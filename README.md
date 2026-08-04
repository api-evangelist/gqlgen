# gqlgen

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

gqlgen is a Go library for building GraphQL servers with a schema-first approach, automatic code generation for resolvers and models, DataLoader support, and OpenTelemetry tracing. Maintained by 99designs, gqlgen generates type-safe, production-ready GraphQL server code from GraphQL SDL schemas.

## Links

- **Website:** https://gqlgen.com/
- **Documentation:** https://gqlgen.com/getting-started/
- **GitHub:** https://github.com/99designs/gqlgen
- **Go Package:** https://pkg.go.dev/github.com/99designs/gqlgen

## Key Features

- Schema-first development using the GraphQL Schema Definition Language
- Automatic code generation eliminates repetitive boilerplate
- Strong type safety — no `map[string]interface{}` patterns
- DataLoader integration for batched, efficient data fetching
- Real-time subscriptions
- Middleware support for request/response processing
- Query complexity analysis to protect servers from expensive queries
- OpenTelemetry tracing built in
- Concurrent field resolver execution with configurable worker pools

## Repository Contents

| Path | Description |
|------|-------------|
| `apis.yml` | APIs.json 0.19 catalog entry |
| `plans/gqlgen-plans.md` | Licensing and plan information |
| `rate-limits/gqlgen-rate-limits.md` | Rate limit and complexity control details |
| `finops/gqlgen-finops.md` | Cost and FinOps guidance |

## Maintainer

**Kin Lane** — kin@apievangelist.com
