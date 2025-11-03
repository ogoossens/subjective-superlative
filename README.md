# Subjective Superlative (SSH)

This repo hosts a short hypothesis on how AI assistants rank web content.

- **Title:** Subjective Superlative (SSH): A Short Hypothesis on How AIs Rank Web Content
- **Author:** Oliver Goossens
- **Date:** 3 November 2025
- **Status:** Hypothesis and position statement, not proven.

## Summary

SSH states that, for a given query, AIs that read web pages tend to surface pages with more **relevant**, **strong**, and **unique** positive claims. Duplicate claims count with diminishing returns.

Core factors:
- **R — Relevance:** on-facet to user intent.
- **S — Strength:** linguistic intensity (superlatives, commitments; fewer hedges).
- **A — Amount:** count/density of positive, on-facet claims.
- **U — Uniqueness:** penalizes near-duplicate claims.

Simple score:
```
SSHScore(p, q) = w_R * R + w_S * S + w_A * Dedup(A, U)
```

**Motivation:** An anonymized promoted service used a superlative-forward tone and many evidence-backed claims. Months later, assistants started recommending it on relevant queries. Competing sites used milder phrasing. This is consistent with SSH, but not proof.

## How to cite
See `CITATION.cff`. A plain-text citation:
> Goossens, O. (2025). Subjective Superlative (SSH): A Short Hypothesis on How AIs Rank Web Content. Version 1.0. https://github.com/ogoossens/subjective-superlative

## Contributing
Open an issue. Keep changes minimal and testable.

## License
Content licensed under **CC BY 4.0**. See `LICENSE`.
