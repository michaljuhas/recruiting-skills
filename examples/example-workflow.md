# Example Workflow: ICP → Screen → Outreach

This walkthrough shows how to chain three skills together for a complete sourcing workflow. The role is a Software Project Manager at a B2B marketplace startup.

---

## Step 1: Build the ICP

**What you say to Claude:**

> Here's a job description for a Software Project Manager. Build me a scoring rubric.
>
> [paste the JD from example-jd.md]

**What Claude produces:**

A scoring rubric table like this:

| # | Criterion | Tier | Weight | How to Evaluate |
|---|-----------|------|--------|-----------------|
| 1 | Project delivery track record | Must-have | 3 | Look for 3+ completed software projects with measurable outcomes |
| 2 | Stakeholder management | Must-have | 3 | Evidence of managing competing priorities across business and engineering |
| 3 | Agile/Scrum experience | Must-have | 3 | Has run sprints, retros, planning. Look for CSM or Agile Coach experience |
| 4 | SDLC understanding | Must-have | 3 | Can speak to CI/CD, code reviews. Doesn't need to code |
| 5 | Cross-functional leadership | Important | 2 | Has led teams with devs, QA, design, product. Team sizes 8+ |
| 6 | SaaS/B2B experience | Important | 2 | Worked at SaaS or B2B company |
| 7 | Budget management | Important | 2 | Has managed project budgets or team allocation |
| 8 | Risk management | Important | 2 | Examples of identifying and mitigating project risks |
| 9 | PM certification | Nice-to-have | 1 | PMP, Prince2, or CSM listed |
| 10 | E-commerce/marketplace | Nice-to-have | 1 | Worked on marketplace or e-commerce products |
| 11 | Remote team management | Nice-to-have | 1 | Managed distributed or cross-timezone teams |
| 12 | Migration experience | Nice-to-have | 1 | Part of monolith-to-microservices or major scaling |

**Claude then asks:** "Does this rubric look right? Should I adjust any tiers or weights?"

**You respond:** "Looks good, but move 'SaaS/B2B experience' to must-have — we really need someone who understands our space."

Claude adjusts and confirms. The rubric is now locked in for scoring.

---

## Step 2: Screen a Candidate

**What you say to Claude:**

> Score this candidate against our rubric:
>
> Jana Novakova — Senior Project Manager at TechFlow Solutions (SaaS, 200 employees), Prague. 7 years in project management, 4 in tech. MSc Business Informatics from Czech Technical University. Led delivery of a payment integration platform used by 500+ merchants. Reduced sprint cycle time by 25% through process improvements. Certified Scrum Master. Skills: Agile, Scrum, Jira, Confluence, stakeholder management, risk management.

**What Claude produces:**

### Candidate Profile
- **Name**: Jana Novakova
- **Current Title**: Senior Project Manager
- **Company**: TechFlow Solutions (SaaS)
- **Location**: Prague
- **YoE**: 7 years (4 in tech)
- **Key Skills**: Agile/Scrum, Jira, Stakeholder Management, Risk Management

### Scoring

| # | Criterion | Weight | Score | Evidence |
|---|-----------|--------|-------|----------|
| 1 | Project delivery | 3 | 3 | Payment platform for 500+ merchants |
| 2 | Stakeholder mgmt | 3 | 2 | Mentioned but no C-suite evidence |
| 3 | Agile/Scrum | 3 | 3 | CSM certified, 25% cycle time reduction |
| 4 | SDLC understanding | 3 | 2 | Business Informatics degree, CI/CD awareness |
| 5 | SaaS/B2B (now must-have) | 3 | 3 | 4 years in B2B SaaS |
| 6 | Cross-functional leadership | 2 | 3 | Led team of 10 |
| 7 | Budget management | 2 | 1 | No specific evidence |
| 8 | Risk management | 2 | 2 | Listed as skill, no specific examples |
| 9 | PM certification | 1 | 0 | CSM only, no PMP/Prince2 |
| 10 | E-commerce/marketplace | 1 | 2 | Payment platform is adjacent |
| 11 | Remote team mgmt | 1 | 1 | Hybrid but no cross-timezone |
| 12 | Migration experience | 1 | 0 | NOT FOUND |

**Score: 58/78 = 74% — Worth considering**

### Hiring Manager Briefing
> Jana is a solid fit with strong B2B SaaS delivery experience and proven Agile expertise. Her payment platform work is directly relevant to our marketplace context. Main gaps: no evidence of C-suite stakeholder management or budget ownership. Recommend exploring both in the interview, along with how she'd approach the microservices migration challenge.

---

## Step 3: Write Outreach

**What you say to Claude:**

> Write outreach for Jana Novakova based on her profile and our role.

**What Claude produces:**

### LinkedIn Connection Request — Version A
> Hi Jana — your delivery of the payment platform at TechFlow for 500+ merchants caught my eye. Would love to connect about a PM role at a B2B marketplace.

### LinkedIn InMail — Version A
> Hi Jana — your work shipping the payment platform at TechFlow stood out.
>
> We're building a B2B marketplace (15K+ businesses, Series A) and looking for a Senior PM to lead a 12-person team. The challenge: microservices migration while shipping 3 major features this quarter.
>
> Given your SaaS delivery track record, I think this could be a strong fit. 15 minutes for a quick chat?

### Follow-up (5-7 days later)
> Hi Jana — circling back. One thing I didn't mention: the team has almost zero turnover over 2 years, and the engineering leads are sharp and collaborative. Happy to share more if you're curious.

---

## Key Takeaways

1. **Start with the ICP** — it makes everything downstream better. Scoring without a rubric is just guessing.
2. **Validate the rubric** — the recruiter adjusting "SaaS/B2B" to must-have changed the scoring meaningfully.
3. **Outreach references real details** — Jana's specific projects and achievements, not generic flattery.
4. **The workflow is additive** — each step builds on the previous one. You can stop at any point and still have useful output.
