---
name: discovery-sandler-questions
description: >
  This skill should be used when preparing customized Sandler Pain Funnel questions for
  an enterprise discovery call. It retrieves the ordered Sandler Pain Funnel question
  framework from Notion and rewrites each question using specific details from company and
  prospect research inputs. Questions must follow the Notion document order exactly and must
  reference concrete research details — generic, uncustomized questions are a hard rejection.
---

# Sandler Question Customization

Retrieve the Sandler Pain Funnel framework from Notion and customize each question for a
specific prospect.

## Inputs

- **Company Snapshot** — output from the `discovery-company-research` skill
- **Prospect Profile** — output from the `discovery-prospect-research` skill, including
  any gatekeeper or sparse-profile flags

## Workflow

**Step 1 — Retrieve the Sandler Pain Funnel framework from Notion**

Use the Notion connector (Notion MCP) to:
1. Search Notion for "Sandler Pain Funnel"
2. Open and read the full Sandler Pain Funnel document
3. Extract all questions in their documented order — do not reorder

**Critical:** If the Notion document is unavailable or cannot be retrieved, stop immediately
and report:

> ⚠️ Cannot proceed — the Notion MCP is required to retrieve the Sandler Pain Funnel
> framework. Please verify your Notion connection is active and that the Sandler Pain Funnel
> document exists in your workspace. Re-run this skill once the connection is confirmed.

Do not attempt to reconstruct the framework from memory. The Notion document is the
authoritative source.

**Step 2 — Review research flags before customizing**

Before writing any questions, check the Prospect Profile for:
- **⚠️ Gatekeeper flag** → Adapt all questions to surface interest that motivates an
  introduction to the right decision-maker. Frame questions around what this person cares
  about, and lead toward "Is there someone else at [Company] I should connect with?"
- **⚠️ Sparse profile flag** → Customize from company context alone for prospect-specific
  questions. Note limited personalization inline where it applies.

**Step 3 — Customize each question**

For each question in the Sandler Pain Funnel (in the exact order from the Notion document):

1. Read the generic question
2. Rewrite it to incorporate specific details from the Company Snapshot and/or Prospect
   Profile — their specific digital channels, content situation, industry, role, or known
   pain points
3. The rewritten question must be substantively different from the generic template:
   - Not acceptable: "How do you manage your content at [Company]?"
   - Acceptable: "You're running a website, mobile app, and digital signage network — how
     does your team manage publishing updates across all three of those channels today?"

4. For gatekeeper prospects, each question should angle toward surfacing enough pain or
   interest that the contact wants to bring in the right stakeholder.

**Step 4 — Produce the Customized Questions**

Output in this format:

---

**Sandler Pain Funnel Questions — Customized for [Name] at [Company]**

**[Stage name from Notion document]**

1. [Customized question — specific to this company and contact]
   *(If sparse personalization: Note: based on company context — limited prospect-specific data)*

2. [Next customized question]

[Continue through all stages and questions in Notion document order]

---

## Guidelines

- Follow the Notion document question order exactly — no reordering or omissions
- Every question must reference specific research details — company name alone as a
  substitution is not sufficient
- If a question genuinely cannot be personalized (no relevant research data), customize
  from the company's industry context and note it inline
- If Notion MCP is unavailable, stop — do not reconstruct the framework from memory
- If both research inputs are thin, customize from available data and flag per-question
  where personalization was limited
