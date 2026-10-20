---
description: Check FERPA compliance for K-12 data fields or workflows. Use when the user asks about FERPA obligations, student records, directory information, legitimate educational interest, or whether specific data handling requires FERPA safeguards.
---

Use the k12mcp MCP tool `k12_check_ferpa_compliance` to analyze the FERPA implications of "$ARGUMENTS".

If the user did not provide enough context, ask them:
- What data fields does your product collect or process? (e.g. student_id, grades, attendance, behavior records)
- Who are the primary users: teachers, students, parents, or administrators?
- What type of institution: public K-12, private K-12, or higher ed?
- Does your product have a signed contract with the school or district?

Call the tool with the information gathered, then present the response in plain language:
- Summarize whether FERPA applies and why
- List specific obligations and any applicable exceptions (school official, directory information, etc.)
- Surface the `disclaimer` prominently
- Note the `freshness_metadata.staleness_status` so the user knows how current this information is
- Recommend next steps if any obligations are triggered
