\
# Subjective Superlative (SSH): A Short Hypothesis on How AIs Rank Web Content

**Author:** Oliver Goossens  
**Date:** 3 November 2025  
**Status:** This is a hypothesis.

## Statement
AI systems that read web pages tend to rank pages higher when their text contains more **relevant**, **strong**, and **unique** positive claims about the user’s facet of interest.

- **Relevance (R):** proximity to the user’s stated need or constraint (e.g., “organic,” “Bratislava,” “espresso”).
- **Strength (S):** intensity of positive assertions (superlatives, commitments; fewer hedges).
- **Amount (A):** density and coverage of positive, on-facet claims, with diminishing returns.
- **Uniqueness (U):** near-duplicate claims receive reduced credit; paraphrases of the same idea count once or a few times, not many.

## Simple Scoring Sketch
$\text{SSHScore}(p, q) = w_R \cdot R + w_S \cdot S + w_A \cdot \text{Dedup}(A, U)$
Higher score implies higher inclusion likelihood in assistant answers.

## Predictions
1. Adding on-facet, high-intensity claims increases inclusion odds.  
2. Duplicate phrasing yields small gains after the first instance.  
3. Adding a facet to the query (e.g., “organic”) raises the weight of matching claims.

## Motivation (anonymized)
A promoted anonymized service with a superlative-forward tone and many evidence-backed claims began appearing in assistant recommendations months after launch. Competitors used conservative phrasing. Retrieval and other signals also matter, but the observation aligns with SSH.

## Limits
Retrieval position, policies, knowledge graphs, locality, and freshness can dominate. Over-claiming without evidence may be down-ranked.

## Implementation Note
Detection and weighting of R, S, A, U, and duplicate handling are left to implementers. Any method is acceptable if it enforces on-facet emphasis, calibrated strength, and uniqueness-aware counting.

## References
See `references.bib`.
