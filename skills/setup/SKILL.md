---
name: setup
description: Connect Claude to an AskAiRank account and confirm the connection works. Use when the user installs the AskAiRank plugin, asks how to sign in, or an AskAiRank tool fails with an authentication error.
---

# Set up AskAiRank

The plugin ships a remote MCP server at `https://mcp.askairank.com/mcp`. It signs in with OAuth, so there is no API key to paste.

1. Run `/mcp`, select **askairank** and choose **Authenticate**. A browser tab opens on app.askairank.com.
2. Sign in with an AskAiRank email and password or with Google. A new account starts on a three-day trial.
3. On the consent screen, check what Claude will be able to do and click **Allow**. Return to Claude.
4. Call `get_account` and tell the user which email and plan they are connected with.
5. Call `list_brands`. If there are no brands, explain that a brand is added once in the AskAiRank app at https://app.askairank.com, and that results appear after its first daily check.

If a tool says the account has no access, the trial has ended and there is no plan. Say so plainly and don't push an upgrade.

To disconnect: AskAiRank, Account, Connected apps, Disconnect. Or remove the server in `/mcp`.

Help: contact@askairank.com.
