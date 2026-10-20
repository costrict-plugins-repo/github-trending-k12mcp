---
description: Get rostering protocol recommendations for K-12 edtech products. Use when the user asks about Clever, Classlink, OneRoster, LTI, or how to handle student roster sync with schools and districts.
---

Use the k12mcp MCP tool `k12_get_rostering_options` to get rostering guidance for "$ARGUMENTS".

If the user did not provide enough context, ask them:
- What type of product are you building? (LMS, assessment, tutoring, productivity tool, etc.)
- What is your target district size? (large urban, suburban, small rural, or all sizes)
- Do you already support any rostering protocols?
- Do you need SSO/identity in addition to roster data?

Call the tool with the product type and district context, then present the response in plain language:
- Recommend which rostering protocol(s) to prioritize first (Clever vs. Classlink vs. OneRoster vs. LTI)
- Explain the tradeoffs: district adoption rates, implementation complexity, data depth, and SSO bundling
- Note which protocols are preferred by large urban districts vs. smaller districts
- Flag any certification or partnership requirements (e.g. Clever certification)
- Surface the `disclaimer` and `freshness_metadata.staleness_status`
