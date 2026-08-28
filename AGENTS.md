# Piggy Banker documentation guide

This repository publishes the Piggy Banker documentation site with Mintlify.

## Source of truth

Use current product direction first, then the canonical application repository and its contracts. Do not derive Piggy Banker behavior from competitor documentation or generated research archives.

## Product language

- The firm workspace manages clients, shared Templates / Playbooks, billing, and firm operations.
- Client navigation is exactly Overview, Context, Pages, Agents, and Connections, in that order.
- Metrics management belongs inside Pages; Metrics is not a separate destination.
- Context contains Company, Money, and Strategy facts. It is not canonical finance data.
- Connections and source data remain distinct from Context.
- Lil Piggy is a client-scoped side companion, not a primary destination.
- The client portal is a separate authenticated shell.

## Accuracy boundaries

- Label material availability as available now, coming soon, implemented-dark, or planned.
- Do not present Pages, unified Page Templates / Playbooks, solo billing, or public MCP/WebMCP as shipped until verified.
- Do not describe accounting data as real-time without a provider timestamp.
- Do not turn unavailable data into zero.
- Do not imply agents can mutate connected ledgers or bypass approvals.
- Keep proposal, approval, dispatch, and provider delivery as separate states.

## Writing style

- Lead with the user outcome.
- Use active voice and plain finance language.
- Use sentence case for headings.
- Bold actual UI labels only.
- Prefer stable concepts over click-by-click instructions when the UI is still rolling out.
