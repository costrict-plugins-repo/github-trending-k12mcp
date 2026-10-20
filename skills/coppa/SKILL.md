---
description: Analyze COPPA applicability for products where children under 13 may be users. Use when the user asks about COPPA requirements, verifiable parental consent, child-directed products, or age gating for K-12 applications.
---

Use the k12mcp MCP tool `k12_analyze_coppa_applicability` to analyze COPPA requirements for "$ARGUMENTS".

If the user did not provide enough context, ask them:
- What age range are the users? (e.g. K-5, middle school, all K-12)
- Can students under 13 access the product directly, or only through teacher accounts?
- Does the product collect any personal information from users? (name, email, device ID, photos, location, etc.)
- Is the product directed at children, or is it a general-audience tool used in schools?
- Does the school operator provide consent on behalf of parents, or do parents consent individually?

Call the tool with the information gathered, then present the response in plain language:
- State clearly whether COPPA applies and under what conditions
- Describe any consent mechanism requirements (verifiable parental consent vs. school operator exception)
- List operational and contractual requirements
- Surface the `disclaimer` prominently
- Note the `freshness_metadata.staleness_status`
