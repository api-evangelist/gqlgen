# gqlgen Rate Limits

## Overview

gqlgen is a client-side Go library — it runs within the developer's own Go application and does not connect to any external API or managed service. As such, there are no externally imposed rate limits from the gqlgen project itself.

Rate limiting in a gqlgen-powered GraphQL server is entirely the responsibility of the application developer.

## Built-in Complexity Controls

gqlgen provides query complexity analysis that developers can use to protect their servers from expensive or abusive queries:

- **Query Complexity Limiting:** Developers can configure a maximum allowed complexity score per query. Requests that exceed the threshold are rejected before execution.
- **Concurrent Resolver Limits:** The framework supports configurable worker pool sizes for concurrent field resolution, giving operators control over server-side parallelism.

### Example: Query Complexity Configuration

```go
srv := handler.NewDefaultServer(generated.NewExecutableSchema(generated.Config{Resolvers: &resolver{}}))
srv.Use(extension.FixedComplexityLimit(100))
```

## Recommended Rate-Limiting Patterns

For production deployments, the following approaches are commonly used alongside gqlgen:

| Layer | Approach | Notes |
|-------|----------|-------|
| Application | Query complexity limits | Built into gqlgen via extension |
| Application | Field-level depth limits | Configurable in gqlgen middleware |
| Infrastructure | API Gateway throttling | AWS API Gateway, Kong, Nginx |
| Infrastructure | Network-level rate limiting | Cloudflare, Fastly WAF rules |
| Application | Token bucket / sliding window | Custom Go middleware |

## GitHub API (Source Repository)

If automating access to the gqlgen GitHub repository (https://github.com/99designs/gqlgen) via the GitHub API, standard GitHub rate limits apply:

- **Unauthenticated:** 60 requests/hour
- **Authenticated (PAT):** 5,000 requests/hour
- **GitHub Apps:** Up to 15,000 requests/hour

## References

- Query Complexity Docs: https://gqlgen.com/reference/complexity/
- GitHub API Rate Limits: https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api
- gqlgen Middleware: https://gqlgen.com/reference/middlewares/
