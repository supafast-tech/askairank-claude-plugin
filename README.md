# AskAiRank plugin for Claude Code and Cowork

AskAiRank checks every day how ChatGPT, Claude, Perplexity, Gemini and other AI engines answer the questions your buyers ask, and whether they name your brand. This plugin connects Claude to your AskAiRank account so you can read those results, manage prompts and brand settings, run checks and audits, and get recommendations, all in conversation.

## What's inside

- **MCP server** `askairank` at `https://mcp.askairank.com/mcp` (remote, OAuth sign-in).
- **Skills**
  - `setup`: connect your account and check that it works.
  - `visibility-report`: visibility per engine, trend, mentions and cited sources.
  - `competitor-check`: who the engines recommend instead of you, and a head-to-head comparison.
  - `track-prompt`: add a buyer question to track and check it right away.

## Tools

**Read:** `get_account`, `list_brands`, `get_visibility_summary`, `list_mentions`, `list_competitors`, `compare_with_competitor`, `list_prompts`, `list_citation_sources`, `get_recommendations`, `generate_report`, `get_notification_settings`.

**Manage prompts:** `add_prompt`, `update_prompt`, `pause_prompt`, `resume_prompt`, `remove_prompt` (needs `confirm: true`).

**Manage brand:** `update_brand` (name, domain, locale, AI-visibility profile), `update_notification_settings` (alert email, Telegram, severity).

**Run checks:** `run_visibility_check` asks the AI engines one tracked question now; `run_site_audit` scans a site's AI-readiness (robots rules, llms.txt, structured data and more). Both use a manual check or scan from your plan.

Nothing can be deleted for good, your account and brand can't be deleted, billing and plan changes aren't exposed, and passwords, email and team members stay out of reach.

## Requirements

An AskAiRank account (https://askairank.com). You can create one during sign-in; tracking works during the three-day trial and on any paid plan. Add your brand once at https://app.askairank.com.

## Install

```
/plugin marketplace add supafast-tech/askairank-claude-plugin
/plugin install askairank@askairank-claude-plugin
```

Then run `/mcp`, pick **askairank**, choose **Authenticate** and sign in.

Claude on the web or desktop without the plugin: Settings, Connectors, Add custom connector, and paste `https://mcp.askairank.com/mcp`. Full guide: https://askairank.com/claude

## Privacy

The plugin sends the requests Claude makes to AskAiRank and nothing else. AskAiRank does not receive your conversation. Access is granted with OAuth and can be revoked at any time in AskAiRank, Account, Connected apps. Privacy policy: https://askairank.com/privacy. Terms: https://askairank.com/terms.

## Support

contact@askairank.com

## Author

SupafastTech (SupafastTech LLC). MIT licence.
