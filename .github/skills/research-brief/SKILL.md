---
name: research-brief
description: Create a concise, decision-ready research brief with claims supported by citations and clearly labeled uncertainty.
---

# Research Brief

Use this skill when the user needs a focused investigation, comparison, landscape scan, or evidence-backed recommendation.

## Workflow

1. Clarify the research question, audience, decision to support, scope, date range, and desired depth. Ask only the questions that materially affect the result; otherwise state assumptions and proceed.
2. Break the question into answerable sub-questions and define what would count as useful evidence.
3. Gather information from authoritative and diverse sources appropriate to the topic. Prefer primary sources, official documentation, standards, peer-reviewed research, government data, and direct statements from involved organizations.
4. Cross-check important claims with independent sources and record publication dates, access dates when relevant, and source limitations.
5. Separate facts, interpretations, estimates, and recommendations. Do not present an inference as a sourced fact.
6. Synthesize the findings around the user's decision instead of producing an unstructured source dump.
7. Flag conflicting evidence, gaps, stale sources, and assumptions.

## Output

Return a concise Markdown brief with:

- **Question and scope**
- **Executive summary**: the answer in a few sentences.
- **Key findings**: the most decision-relevant claims, each with an inline citation.
- **Evidence and analysis**: supporting context, comparisons, tradeoffs, and uncertainty.
- **Recommendation or implications**: only when the evidence supports one; explain the reasoning.
- **Risks and unknowns**
- **Sources**: a numbered bibliography with title, publisher or author, date, URL, and access date when useful.

Use inline citations such as `[1]` that map unambiguously to the source list. Cite the original source whenever possible. Never fabricate citations, URLs, quotations, statistics, or source metadata. If browsing or source access is unavailable, say so and provide a research plan rather than pretending the brief is sourced.

## Quality checks

Before returning the brief, verify that:

- Material factual claims have citations.
- Sources actually support the claims they are attached to.
- The source list is complete and links are usable.
- Recommendations are distinguished from evidence.
- The brief answers the question directly and stays within the requested scope.
