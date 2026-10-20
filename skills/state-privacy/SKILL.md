---
description: Look up state student privacy laws for one or more U.S. states. Use when the user asks about state-level student data privacy requirements, which states have additional laws beyond FERPA, or what a specific state requires for edtech vendors.
---

Use the k12mcp MCP tool `k12_get_state_privacy_laws` to retrieve state privacy law requirements for "$ARGUMENTS".

If the user did not specify states or product context, ask them:
- Which states are you selling into or targeting? (You can specify multiple)
- What type of product: SIS, LMS, assessment, tutoring, communication tool, or other?
- Are you a for-profit vendor or a nonprofit/open-source provider?

Call the tool with the states and product category, then present the response in plain language:
- For each state: summarize the applicable statutes and key vendor obligations
- Highlight states with requirements that go beyond federal FERPA (e.g. California SOPIPA, New York Ed Law 2-d, Colorado SB23-008)
- Flag any states where a signed DPA is required before any data sharing, even for free products
- Surface the `disclaimer` prominently
- Note the `freshness_metadata.staleness_status` for each state -- laws change frequently
