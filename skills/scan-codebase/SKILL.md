---
description: Scan field names, route names, or data model identifiers for potential K-12 PII exposure. Free tool, no credits required. Use when the user wants to check whether their data model or API surface may collect or expose student or staff personally identifiable information.
---

Use the k12mcp MCP tool `k12_scan_codebase` to scan "$ARGUMENTS" for potential K-12 PII exposure.

This tool is free and does not consume credits.

If the user did not provide field names or identifiers, ask them to provide:
- A list of database field names, API parameter names, or route paths from their codebase
- (Optional) Their product type and target user age range for more specific analysis

Call the tool with the identifiers provided, then present the response in plain language:
- List each field flagged as potentially sensitive and explain why
- Categorize by risk level: FERPA-covered, COPPA-relevant, or general PII
- Note any fields that suggest logging or analytics pipelines that may inadvertently capture PII
- Recommend which fields should be reviewed with legal counsel before launch
- This tool is informational only -- surface the `disclaimer` prominently
