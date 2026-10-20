# k12mcp Claude Code Plugin

K-12 compliance and integration guidance for developers, inside Claude Code.

This plugin connects Claude Code to the [k12mcp](https://k12mcp.vercel.app) MCP server, giving you structured answers about FERPA, COPPA, state privacy laws, DPA requirements, SIS integrations, rostering protocols, and procurement pathways -- without leaving your editor.

---

## Installation

### From this repo (before official marketplace listing)

```
/plugin marketplace add crafty184/k12mcp-plugin
/plugin install k12mcp@k12mcp-plugin
```

Claude Code will prompt you for your API key when you enable the plugin.

**Get a free API key at [k12mcp.vercel.app](https://k12mcp.vercel.app)** -- no credit card required. You get 10 credits on signup.

---

## Skills

| Skill | What it does | Credits |
|-------|-------------|---------|
| `/k12mcp:ferpa` | FERPA obligation analysis for data fields and workflows | 10 |
| `/k12mcp:coppa` | COPPA applicability analysis for products with under-13 users | 10 |
| `/k12mcp:state-privacy` | State student privacy law requirements by state | 20 |
| `/k12mcp:dpa` | DPA clause readiness check against district requirements | 20 |
| `/k12mcp:scan-codebase` | Scan field/route names for K-12 PII exposure | Free |
| `/k12mcp:sis-info` | SIS platform details, API support, district adoption | 10 |
| `/k12mcp:rostering` | Rostering protocol recommendations by product type | 25 |
| `/k12mcp:procurement` | Procurement pathway guidance by district size and product type | 25 |

---

## Agent

`/agents` includes a **compliance-review** agent that runs a full multi-step review:

1. Gathers product context (data fields, user ages, target states, product type)
2. Runs FERPA, COPPA, state privacy, and DPA checks in sequence
3. Scans your data model for PII exposure
4. Delivers a structured summary: what is covered, gaps to close, recommended next steps

Use this before starting district procurement conversations.

---

## Example usage

```
/k12mcp:ferpa Does storing student assignment scores alongside user IDs require FERPA safeguards?
```

```
/k12mcp:coppa My app lets students ages 10-13 log in with school SSO. What COPPA mechanisms are required?
```

```
/k12mcp:scan-codebase student_id, assignment_score, teacher_name, parent_email, address, device_id
```

```
/k12mcp:state-privacy California, Texas, New York -- what do I need beyond FERPA?
```

---

## Credit costs

Signup gives you 10 free credits (1 FERPA or COPPA check). Paid plans:

| Plan | Credits/month | Price |
|------|--------------|-------|
| Starter | 50 | See k12mcp.vercel.app |
| Growth | 100 | See k12mcp.vercel.app |
| Pro | 300 | See k12mcp.vercel.app |
| Top-up | 20 (one-time) | $5 |

`k12_scan_codebase` is always free.

---

## Important note

All responses include a legal disclaimer. This tool provides educational information only and does not constitute legal advice. State privacy laws change frequently. Verify all compliance requirements with qualified legal counsel before shipping your product.

Knowledge files are reviewed every 180 days. Each response includes `freshness_metadata` with a `staleness_status` field.

---

## Links

- Portal and signup: [k12mcp.vercel.app](https://k12mcp.vercel.app)
- Server repo: [github.com/crafty184/k12mcp](https://github.com/crafty184/k12mcp)
- Issues: [github.com/crafty184/k12mcp-plugin/issues](https://github.com/crafty184/k12mcp-plugin/issues)
