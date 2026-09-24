---
name: visibility-report
description: Build a short AI visibility report for a brand tracked in AskAiRank: visibility per engine, trend, the answers that mentioned the brand and the sources those engines cited. Use when the user asks how visible their brand is in ChatGPT, Claude, Perplexity or Gemini, or wants a weekly or monthly AI search summary.
---

# AI visibility report

1. If the user has more than one brand, call `list_brands` and ask which one, unless it is obvious from the request.
2. Call `get_visibility_summary` with the requested period (7, 14, 30 or 90 days; default 30).
3. Call `list_mentions` for the same period with `limit` 10.
4. Write the report:
   - one line with overall visibility and the number of checks;
   - a small table: engine, visibility %, mention rate %, average position;
   - the two or three strongest and weakest engines, in plain words;
   - up to five mentions: question, engine, position, a short quote;
   - the domains cited most often in those mentions, since they are the pages AI engines trust for this topic.
5. End with at most three concrete next steps drawn from the data (for example: an engine that never mentions the brand, a cited domain where the brand is absent).

Terms: visibility is the share of checks where the brand appears in the top 10 of the answer; mention rate is the share where it is named at all. Don't invent numbers that the tools didn't return.
