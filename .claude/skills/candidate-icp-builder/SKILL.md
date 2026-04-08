---
name: candidate-icp-builder
description: >-
  Builds structured Ideal Candidate Profiles with weighted scoring rubrics from
  job descriptions or requirement analyses. Extracts must-haves, important, and
  nice-to-have criteria with weights (3/2/1). Use when the user pastes a job
  description, says "I need to hire", or wants to create a scoring rubric.
---

# Ideal Candidate Profile Builder

## Quick Start

Paste a job description or requirement analysis, and this skill will build a structured ICP with a scoring rubric you can use to evaluate candidates.

## Before You Begin

1. **Check `my-examples/`** for past ICPs. If found, match the style, structure, and level of detail the recruiter prefers.
2. **Check `../playbooks/`** for a playbook matching this role type. If found, incorporate proven screening signals and evaluation criteria. Tell the user: "I found a playbook for [role type] — incorporating what historically worked."

## Process

### Step 1: Extract Role Context
From the JD or requirement analysis, identify:
- Job title, department, reporting line
- Seniority level
- Location / remote policy
- Compensation signals (if stated)
- Team context and project nature

### Step 2: Categorize Requirements into Three Tiers

| Tier | Weight | Definition |
|------|--------|------------|
| **Must-have** | 3 | Hard requirements. Dealbreakers if missing. |
| **Important** | 2 | Strongly preferred. Candidates without these are weaker but not disqualified. |
| **Nice-to-have** | 1 | Bonus qualifications. Differentiate between otherwise equal candidates. |

Parse every requirement from the JD into one of these tiers. Include:
- Technical skills and tools
- Experience and background
- Certifications
- Soft skills and competences
- Industry/domain knowledge
- Cultural and personality signals

### Step 3: Build the Scoring Rubric

Output a table in this format:

```markdown
| # | Criterion | Tier | Weight | How to Evaluate |
|---|-----------|------|--------|-----------------|
| 1 | [Skill/requirement] | Must-have | 3 | [What evidence to look for] |
| 2 | [Skill/requirement] | Important | 2 | [What evidence to look for] |
| 3 | [Skill/requirement] | Nice-to-have | 1 | [What evidence to look for] |
```

The "How to Evaluate" column is critical — it tells the recruiter what to look for on a profile or in a conversation. Be specific: "Look for 5+ years in project management roles at tech companies" not just "Experience."

### Step 4: Validate with the Recruiter

**Always ask before proceeding:**

> "Here's the scoring rubric I've built. Before we use it to evaluate candidates:
> 1. Are the tiers correct? Should any criterion move up or down?
> 2. Are the weights right? Should any must-have actually be nice-to-have (or vice versa)?
> 3. Is anything missing that you'd want to score on?
>
> Adjust as needed — this rubric drives all candidate scoring."

**Do NOT auto-score candidates without the recruiter confirming the rubric first.**

### Step 5: Calculate Scoring Summary

After confirmation, provide:
- Total number of criteria per tier
- Maximum possible score: sum of (weight × 3) for all criteria
- Scoring guide: how to interpret total scores (e.g., "Above 80% = strong fit, 60-80% = worth considering, below 60% = likely not a match")

## Output Format

Present everything in a single copy-paste-ready fenced markdown block.

## What's Next

After the ICP is confirmed, suggest:
- "Ready to evaluate a candidate? Use the **Candidate Screener** skill."
- "Want to improve the job posting? Use the **Job Seller** skill."
- "Need to find candidates? Use the **Sourcing Strategy Generator** skill."
