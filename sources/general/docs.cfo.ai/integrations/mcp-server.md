# Source: https://docs.cfo.ai/integrations/mcp-server

cfo.ai runs its own MCP server at `https://api.cfo.ai/mcp`. Any AI client that supports remote MCP servers can connect, including Claude Code and Codex. The connection lets an external agent use the same workspace tools Ari uses. Those tools can inspect your Model and, when authorized, change live Pages, Scenarios, Variables, Dimensions, and formulas. You, Ari, and the external agent share the same Model. Work created through the connection remains visible in your cfo.ai workspace, where you can inspect the assumptions, edit the result, or continue the work with Ari. Setup below covers Claude Code and Codex.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#before-you-start)

Before you start

You need a cfo.ai account with access to the intended workspace. If you do not have one yet, sign up at [app.cfo.ai](https://app.cfo.ai) and complete the required account setup first.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#claude-code)

Claude Code

1

Add the MCP server

Open a terminal and add cfo.ai as an MCP server:

```
claude mcp add --transport http cfoai https://api.cfo.ai/mcp
```

2

Start Claude Code

```
claude
```

3

Open the MCP menu

Type `/mcp` and look for `cfoai` in the list of servers.

4

Authenticate

Select `cfoai`, then choose **Authenticate**. A browser window opens. Make sure you’re logged into your cfo.ai account before approving the connection.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#codex)

Codex

1

Add the MCP server

Open a terminal and add cfo.ai as an MCP server:

```
codex mcp add cfoai --url https://api.cfo.ai/mcp
```

2

Authenticate

```
codex mcp login cfoai
```

A browser window opens. Make sure you’re logged into your cfo.ai account before approving the connection.

3

Verify

Start Codex with `codex`, then type `/mcp` to confirm `cfoai` is connected.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#other-mcp-clients)

Other MCP clients

Any harness that supports remote MCP servers can connect. Add `https://api.cfo.ai/mcp` as a custom connector or MCP server in your agent’s settings, then sign in with your cfo.ai account when the browser prompt appears.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#choose-the-correct-workspace)

Choose the correct workspace

If your account belongs to one workspace, the connection can use it automatically. If your account belongs to several workspaces, ask the agent to call `list_orgs`, select the correct workspace by its ID or slug, and pass that value as `org_id` on each later tool call. Writes apply to the selected live workspace. Use a Scenario when you want an external agent to work on an alternative plan without changing Main.

## 

[​](https://docs.cfo.ai/integrations/mcp-server#agent-instructions)

Agent instructions

Rather have your agent do this? Copy this prompt into it. Your agent will walk you through everything, from sign-up to a working connection, and tell you when it needs you:

```
Set up cfo.ai for me. Fetch https://docs.cfo.ai/agent-instructions.md and follow the instructions there. If I don't have a cfo.ai account yet, walk me through creating one first, then connect the cfo.ai MCP server to this harness and verify it's working.
```

If you are an AI agent reading this page: fetch `https://docs.cfo.ai/agent-instructions.md` and follow it. Once authenticated, your agent can call the available cfo.ai tools directly. If authentication fails, check that you are signed in to the correct cfo.ai account and have access to the intended workspace.

Ctrl+I