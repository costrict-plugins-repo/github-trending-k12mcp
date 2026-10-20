---
description: Check DPA (Data Processing Agreement) readiness for a K-12 edtech product. Use when the user asks about DPA requirements, data processing agreements, EdSAFE/Student Data Privacy Consortium templates, or what clauses districts typically require.
---

Use the k12mcp MCP tool `k12_check_dpa_readiness` to evaluate DPA clause coverage for "$ARGUMENTS".

If the user did not provide enough context, ask them:
- What type of product: SIS, LMS, assessment, tutoring, communication tool, or other?
- Which states or regions are you targeting?
- Do you already have a DPA template, or are you starting from scratch?
- Have you reviewed the Student Data Privacy Consortium (SDPC) model terms or EdSAFE Alliance addenda?

Call the tool with the product category and target states, then present the response in plain language:
- List required DPA clauses and whether common templates cover them
- Flag state-specific addenda (e.g. California, New York, Texas) that must be attached
- Identify gaps between standard templates and district requirements
- List recommended next steps before initiating district procurement
- Surface the `disclaimer` prominently
- Note the `freshness_metadata.staleness_status`
