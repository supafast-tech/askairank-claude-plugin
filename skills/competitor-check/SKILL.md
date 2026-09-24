---
name: competitor-check
description: Find which competitors AI engines recommend for a brand's market and compare the brand with one of them engine by engine, using AskAiRank data. Use when the user asks who ChatGPT or Perplexity recommends instead of them, or how they stack up against a named competitor.
---

# Competitors in AI answers

1. Call `list_competitors` (default 30 days, `limit` 10). Present them ranked by visibility with share of voice, and say where the user's own brand ranks.
2. If the user named a competitor, or after listing asks for one, call `compare_with_competitor` with that name. Use the exact name from `list_competitors` when possible.
3. Summarise: overall metrics side by side, then the engines where the user leads and where they trail.
4. If a competitor wins on specific engines, call `list_mentions` filtered by that engine to show the questions where the brand was named, so the user sees which answers they already appear in.

Keep it factual. If the competitor is not in the results for the period, say so and suggest a longer period (90 days).
