# gqlgen Plans

## Overview

gqlgen is a free, open-source Go library maintained by the 99designs organization on GitHub. There are no paid plans or commercial tiers — the library is available to all users under the MIT license at no cost.

## Open Source (Free)

- **Cost:** Free
- **License:** MIT
- **Repository:** https://github.com/99designs/gqlgen
- **Availability:** Publicly available via Go modules

### Included Features

- Schema-first GraphQL server generation using the GraphQL Schema Definition Language (SDL)
- Automatic code generation for resolvers, models, and boilerplate
- Type-safe Go code without `map[string]interface{}` patterns
- DataLoader integration for optimized batch data fetching
- Subscription support for real-time GraphQL updates
- Middleware hooks for request/response processing
- Query complexity analysis
- Field collection utilities
- OpenTelemetry tracing integration
- Concurrent field resolver execution with configurable worker limits
- Custom model mapping via configuration
- Active community support via GitHub Issues

## Enterprise Considerations

Organizations using gqlgen in production environments typically supplement it with:

- **Observability:** Self-managed OpenTelemetry pipelines (Jaeger, Grafana Tempo, etc.)
- **Hosting:** Cloud compute costs for running Go GraphQL servers (AWS, GCP, Azure, Fly.io, etc.)
- **Support:** Community support through GitHub Issues; no commercial SLA is offered by the project

## References

- GitHub Repository: https://github.com/99designs/gqlgen
- Documentation: https://gqlgen.com/
- Go Package Registry: https://pkg.go.dev/github.com/99designs/gqlgen
