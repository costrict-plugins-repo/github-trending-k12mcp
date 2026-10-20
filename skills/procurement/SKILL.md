---
description: Get K-12 procurement pathway guidance for edtech vendors. Use when the user asks how to sell to schools or districts, what the procurement process looks like, how long it takes, what approvals are needed, or how district size affects the buying process.
---

Use the k12mcp MCP tool `k12_get_procurement_pathway` to get procurement pathway guidance for "$ARGUMENTS".

If the user did not provide enough context, ask them:
- What type of product are you selling? (SaaS, hardware, curriculum, assessment, etc.)
- What is your target buyer: individual teacher, school principal, district administrator, or school board?
- What district size are you targeting? (large urban 10k+ students, mid-size 2-10k, small rural under 2k)
- What is your price point and licensing model? (per seat, per school, district-wide, freemium)
- Are you already on any state or cooperative purchasing contracts? (e.g. TIPS, AEPA, Sourcewell)

Call the tool with the product and target context, then present the response in plain language:
- Describe the typical procurement stages: pilot, DPA review, budget approval, board approval (if applicable)
- Estimate timeline by district size and deal value
- Flag requirements that must be met before a district can sign: DPA, security review, equity review, curriculum alignment
- Note cooperative purchasing contracts that can accelerate the process
- Surface the `disclaimer` and `freshness_metadata.staleness_status`
