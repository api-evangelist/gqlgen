# gqlgen FinOps

## Overview

gqlgen is a free, open-source library. There are no licensing fees, subscription costs, or API call charges associated with using gqlgen itself. All cost considerations relate to the infrastructure and services used to run a gqlgen-powered GraphQL server.

## Direct Costs: $0

| Item | Cost |
|------|------|
| gqlgen library license | $0 (MIT) |
| Code generation (gqlgen tool) | $0 |
| Library updates / releases | $0 |
| GitHub repository access | $0 (public) |

## Indirect Infrastructure Costs

Organizations deploying gqlgen-powered GraphQL servers should budget for the following infrastructure categories:

### Compute

Running Go GraphQL servers requires compute resources. gqlgen-generated servers are highly efficient (compiled Go binaries), resulting in lower compute costs compared to interpreted-language alternatives.

| Platform | Pricing Model |
|----------|--------------|
| AWS EC2 / Fargate | Per vCPU/hour |
| Google Cloud Run | Per request + CPU/memory |
| Azure Container Apps | Per vCPU/hour |
| Fly.io | Per VM/month |
| Kubernetes (self-managed) | Node cost + management overhead |

### Observability

gqlgen supports OpenTelemetry natively, enabling tracing to any compatible backend. Costs depend on chosen vendor:

| Tool | Pricing Model |
|------|--------------|
| Grafana Cloud | Free tier; usage-based above threshold |
| Datadog APM | Per host/month |
| Honeycomb | Event-volume based |
| Jaeger (self-hosted) | Infrastructure cost only |

### Data Storage

DataLoader patterns in gqlgen reduce N+1 query overhead, which can materially lower database costs. Consider:

- Database query volume reduction through batching
- Caching layer costs (Redis, Memcached) if deployed

## Cost Optimization Recommendations

1. **Leverage code generation:** gqlgen's generated code is optimized at compile time — prefer generated resolvers over reflection-heavy alternatives.
2. **Use DataLoaders:** Batch database calls to reduce query counts and database compute costs.
3. **Set query complexity limits:** Prevent runaway queries that spike compute and database load.
4. **Profile concurrent resolvers:** Tune the worker pool size to balance throughput and memory use.
5. **Compile to minimal Docker images:** Use multi-stage Go builds to produce small, efficient container images.

## References

- gqlgen GitHub Repository: https://github.com/99designs/gqlgen
- gqlgen DataLoader Docs: https://gqlgen.com/reference/dataloaders/
- OpenTelemetry Integration: https://gqlgen.com/reference/opentelemetry/
- MIT License: https://github.com/99designs/gqlgen/blob/master/LICENSE
