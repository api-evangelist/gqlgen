# gqlgen

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
