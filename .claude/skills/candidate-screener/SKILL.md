---
name: candidate-screener
description: >-
  Scores candidates against an ICP rubric with evidence-based evaluation. Handles
  single profiles and batch screening with ranked comparison tables. Use when
  the user pastes a candidate profile (LinkedIn text, resume, GitHub), multiple
  profiles, or asks to evaluate/compare/rank candidates.
---

# Candidate Screener

## Quick Start

Paste a candidate profile (LinkedIn text, resume content, or notes) and this skill will extract structured data, score against your ICP, and generate a hiring manager briefing.

For multiple candidates, separate them with `---`.

## Before You Begin

1. **Check `my-examples/`** for past evaluations or briefings. Match the format, tone, and depth the recruiter prefers.
2. **Check `../playbooks/`** for a matching role playbook. If found, weight screening signals that historically predicted good hires.
3. **Check conversation context** for an ICP/scoring rubric. If none exists, ask: "I don't see a scoring rubric in our conversation. Would you like to provide a JD so I can build one first, or should I do a general assessment without scoring?"

## Single Candidate Evaluation

### Step 1: Extract Structured Profile

```markdown
## Candidate Profile
- **Name**: [extracted or "NOT FOUND"]
- **Current Title**: [...]
- **Current Company**: [...]
- **Location**: [...]
- **Years of Experience**: [estimated from career history]
- **Education**: [...]
- **Key Skills**: [top 5-8 skills from profile]
- **Notable Achievements**: [2-3 standout items]
- **Online Presence**: [URLs if found]
```

**Never invent details.** If a field is not in the provided data, write **"NOT FOUND"**.

### Step 2: Score Against ICP Rubric

For each criterion in the rubric:

```markdown
| # | Criterion | Weight | Score (0-3) | Evidence |
|---|-----------|--------|-------------|----------|
| 1 | [criterion] | 3 | [0-3] | [Quote or specific evidence from profile, or "NOT FOUND"] |
```

**Scoring guide:**
- **3**: Strong evidence, clearly meets/exceeds the criterion
- **2**: Moderate evidence, likely meets the criterion
- **1**: Weak evidence, partially meets or unclear
- **0**: No evidence found, or evidence of not meeting the criterion

**Total weighted score** = sum of (weight × score) for all criteria
**Fit percentage** = total weighted score / maximum possible score × 100

### Step 3: Flag Signals

**Red Flags** (if any):
- Job hopping without career progression
- Skill mismatches vs stated experience level
- Gaps that could indicate issues (but note: gaps have many legitimate explanations)

**Standout Signals** (if any):
- Achievements that exceed expectations for the level
- Unique background that adds unexpected value
- Evidence of leadership, initiative, or impact beyond the role

### Step 4: Hiring Manager Briefing

Write a 3-5 sentence summary covering:
1. Overall fit assessment (strong/moderate/weak) with the key reason
2. Top 1-2 strengths relevant to this role
3. Key gap or risk (if any)
4. Suggested interview focus area

## Batch Screening (Multiple Candidates)

When the user provides multiple profiles (separated by `---` or clearly delineated):

1. Score each candidate silently using the single-candidate process
2. Output a ranked comparison table:

```markdown
| Rank | Name | Current Title | Score | Fit % | Top Strengths | Key Gaps | Recommendation |
|------|------|---------------|-------|-------|---------------|----------|----------------|
| 1 | [name] | [title] | [score] | [%] | [1-2 items] | [1 item] | Pursue |
| 2 | [name] | [title] | [score] | [%] | [1-2 items] | [1 item] | Pursue |
| 3 | [name] | [title] | [score] | [%] | [1-2 items] | [1 item] | Maybe |
```

**Recommendation categories:**
- **Pursue**: Score 70%+ and no critical gaps in must-haves
- **Maybe**: Score 50-70% or has addressable gaps worth discussing
- **Pass**: Score below 50% or critical must-have gaps

3. Below the table, provide:
   - 2-3 sentence summary of the top candidates
   - Any patterns observed (e.g., "All candidates lack cloud experience — consider relaxing this criterion or sourcing differently")
   - Who to prioritize for outreach and why

## Rules

- **Never hallucinate.** Only use information provided. If something is unclear, say so.
- **Transparent scoring.** Every score must have a one-line evidence reference.
- **Copy-paste ready.** All output should be in fenced markdown blocks.
- **Suggest next steps.** After screening, suggest: "Ready to write outreach? Use the **Outreach Writer** skill."
