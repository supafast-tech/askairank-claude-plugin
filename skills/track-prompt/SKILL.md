---
name: track-prompt
description: Add a new buyer question for AskAiRank to track and optionally check it right away across AI engines. Use when the user wants to monitor a new query, keyword or question in ChatGPT, Claude, Perplexity or Gemini answers.
---

# Track a new question

1. Rephrase the user's idea into the question a buyer would type into an AI assistant, 6 to 140 characters, without the brand name (for example "best invoicing tool for freelancers").
2. Call `add_prompt` with that text (and `brand_id` if the account has several brands). Report whether it is tracked or saved as paused because the plan's tracked limit is full.
3. Ask before running a check now: `run_visibility_check` sends the question to every engine on the user's plan, takes up to a minute and uses one of the plan's manual checks. Scheduled daily checks run anyway.
4. If the user agrees, call `run_visibility_check` with the prompt id and list, per engine, whether the brand was named and in what position.
