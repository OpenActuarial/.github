# OpenActuarial

A dependency-light Python ecosystem for general actuarial workflows —
experience analysis, projection, rating and pricing, loss modeling, tail
estimation, simulation, and portfolio capital.

| Package | Role |
|---|---|
| [actuarialpy](https://github.com/OpenActuarial/actuarialpy) | Calculation primitives the workflow packages build on |
| [experiencestudies](https://github.com/OpenActuarial/experiencestudies) | Experience reporting, actual-vs-expected, claimant and concentration analysis |
| [projectionmodels](https://github.com/OpenActuarial/projectionmodels) | Claim, premium, and expense projection over a renewal horizon |
| [ratingmodels](https://github.com/OpenActuarial/ratingmodels) | Manual and experience rating, credibility, indication, GLM relativities |
| [lossmodels](https://github.com/OpenActuarial/lossmodels) | Severity and frequency fitting, aggregate loss distributions |
| [extremeloss](https://github.com/OpenActuarial/extremeloss) | Extreme-value tails: POT/GPD, GEV, return levels, splicing |
| [risksim](https://github.com/OpenActuarial/risksim) | Portfolio Monte Carlo, dependence, reinsurance contracts, risk measures | Portfolio Monte Carlo, dependence, risk measures |

```
pip install openactuarial
```

Docs and runnable end-to-end examples: **[openactuarial.org](https://openactuarial.org)**

Every package's test suite reruns nightly against current PyPI releases
(the [ecosystem smoke](https://github.com/OpenActuarial/docs/actions/workflows/ecosystem-smoke.yml)),
so cross-package drift surfaces within a day.
