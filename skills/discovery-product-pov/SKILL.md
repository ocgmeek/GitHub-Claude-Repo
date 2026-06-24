---
name: discovery-product-pov
description: >
  This skill should be used when synthesizing a product point of view for an enterprise
  discovery call with a prospect evaluating headless or AI-powered content management. Given
  company and prospect research outputs, it writes a concise POV section explaining why
  headless or AI content management is relevant to this specific company's content challenges,
  digital channel mix, and strategic goals.
---

# Product POV Synthesis

Write a tailored product point of view for a discovery call, grounded in prospect research.

## Inputs

- **Company Snapshot** — output from the `discovery-company-research` skill
- **Prospect Profile** — output from the `discovery-prospect-research` skill

## Workflow

**Step 1 — Identify the strongest fit signals**

Review the Company Snapshot and identify the 1-2 signals most relevant to headless/AI
content management:

| Signal in Research | POV Hook |
|--------------------|----------|
| Multiple digital channels (website + app + signage) | Deliver content from one source to every channel without duplication |
| Authenticated user experiences | Personalized, governed content at the individual level |
| High content update frequency | Publishing speed and agility across channels |
| Multiple brands, properties, or markets | Content reuse and governance at scale |
| Legacy or described CMS pain | Modernization, developer flexibility, reduced bottlenecks |
| Regulated industry (finance, healthcare, pharma) | Audit trail, compliance, content governance |
| E-commerce with content | Unified commerce and content experience |
| Digital transformation initiative | Foundation for AI-driven content personalization |

If company research is thin, use the company's industry sector as the signal basis and
note that the POV is based on sector patterns.

**Step 2 — Connect to the prospect's role**

Review the Prospect Profile and determine how to frame the POV for this person:
- **Content/Digital Owner** → Frame around operational efficiency and channel control
- **Adjacent Stakeholder (Marketing)** → Frame around campaign agility and audience reach
- **Adjacent Stakeholder (IT)** → Frame around integration, developer velocity, and
  reduced maintenance burden
- **Gatekeeper** → Frame around why this is a conversation worth having with the right
  decision-maker — what business outcome is at stake

**Step 3 — Write the Product POV**

Write a concise POV (150-200 words) with this structure:

---

**Why [Company] and Headless/AI Content Management**

[Opening sentence: acknowledge what you know about their specific content situation —
reference a specific signal from the research, not a generic opener]

[2-3 sentences: explain why headless or AI-powered content management is directly relevant
to their situation. Connect to the specific signals from Step 1. Be direct about the value
without overpromising.]

[Closing sentence: one specific connection to [Prospect Name]'s role and area of
responsibility — or, if they are a gatekeeper, one question this raises that a more senior
stakeholder would want to explore]

---

**Step 4 — Flag if needed**

If the POV is based on industry-level signals rather than company-specific research, add:

> *(Note: limited company-specific research available — POV based on [industry] sector
> patterns. Validate assumptions early in the call.)*

## Guidelines

- Ground every POV in specific research signals — avoid generic statements that could
  apply to any company
- Keep to 150-200 words — this is a prep note, not a pitch
- Create a hypothesis to test in the call, not a claim to defend
- If the contact is a gatekeeper, end with a signal about who else at the company is the
  right conversation and why
- Do not over-customize toward the gatekeeper at the expense of the company's actual
  content situation
