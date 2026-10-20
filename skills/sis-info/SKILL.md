---
description: Get integration details for K-12 Student Information Systems (SIS). Use when the user asks about PowerSchool, Infinite Campus, Skyward, Tyler SIS, Aeries, or other SIS platforms -- their API support, data formats, district adoption, and integration considerations.
---

Use the k12mcp MCP tool `k12_get_sis_info` to retrieve information about "$ARGUMENTS".

If the user did not specify a SIS platform, ask them:
- Which SIS platform(s) are you trying to integrate with? (PowerSchool, Infinite Campus, Skyward, Tyler SIS, Aeries, Frontline, etc.)
- What data do you need from the SIS? (roster, attendance, grades, demographics, schedule)
- Are you targeting a specific district, or building a general integration?
- Do you need real-time sync or batch/nightly imports?

Call the tool with the platform name(s) and context, then present the response in plain language:
- Summarize API availability, supported protocols (REST, SOAP, SIF, OneRoster), and authentication methods
- Note district adoption rates and which regions or district sizes favor each SIS
- Flag known integration challenges or data access limitations
- Recommend which SIS to prioritize first if building for broad K-12 adoption
- Surface the `disclaimer` and `freshness_metadata.staleness_status`
