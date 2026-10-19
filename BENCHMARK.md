# VBD-resilience4j: synthetic vulnerability benchmark

This fork is a **synthetic, openly labelled benchmark**. It is not the upstream project
and must not be used as one. Each sample is an isolated pair of branches off `baseline`:

- `baseline`: the pinned upstream commit plus any hardening; the common ancestor.
- `smpl/<NNN>/safe`: the genuine negative (validated control) of sample `NNN`.
- `smpl/<NNN>/vuln`: `safe` plus exactly one commit that weakens the control.

The class and the coordinates of every sample live only in `GROUND_TRUTH.csv` on this
orphan branch, never in the analysed branches.

| sample | file | class |
|---|---|---|
| 001 | `resilience4j-micronaut/src/main/java/io/github/resilience4j/micronaut/ratelimiter/RateLimiterInterceptor.java` | F115 Security controls bypass or absence |
