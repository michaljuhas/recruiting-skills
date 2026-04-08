---
name: outreach-writer
description: >-
  Writes personalized candidate outreach for LinkedIn (connection request + InMail),
  email, and X DMs. Generates A/B variants and follow-up sequences. Matches the
  recruiter's voice from past examples. Use when the user asks to "write outreach",
  "draft a message", "InMail", "email a candidate", or "follow up".
---

# Outreach Writer

## Quick Start

Share a candidate profile (or reference one from the conversation) and this skill will generate personalized outreach messages across platforms.

## Before You Begin

1. **Check `my-examples/`** for past outreach messages. If found, analyze the recruiter's voice, tone, typical hooks, and message structure. Generate new messages that match their personal style.
2. **Check `my-examples/tone.md`** specifically. If it exists, use it to calibrate voice and style.
3. **Check `../playbooks/`** for a matching role playbook. Use proven outreach approaches and avoid approaches marked as ineffective.
4. **Check conversation context** for job-seller outreach hooks. If available, weave selling points into messages.

**If no tone preference is found**, ask once: "Would you like me to write in a casual, professional, or direct tone? You can save your preferred tone in `my-examples/tone.md` for future use."

## Tone Rules (Always Apply)

These rules are hardcoded — they override any other style guidance:

- **Never use flattery**: No "I'm impressed by your profile", "Your background is amazing", "I was blown away by your experience"
- **Never use vague praise**: Every compliment must reference something specific and concrete
- **Be direct** about why you're reaching out — don't bury the point
- **Don't over-apologize** for reaching out cold — it's your job, own it
- **No corporate buzzwords**: Avoid "synergy", "leverage", "exciting opportunity"
- **Every message must reference at least one specific detail** from the candidate's work, projects, or background

## Output Format — 3 Message Types

### 1. LinkedIn Connection Request Note
- **One sentence only.** Under 300 characters.
- Direct, specific reason to connect. No fluff, no full pitch.
- Example format: "Hi [Name] — saw your [specific project/role detail] and wanted to connect about a [role type] role that might be interesting."

### 2. LinkedIn InMail
- **Salutation and opening merged** into one line (e.g., "Hi Alex — your work on [specific thing] caught my attention.")
- Body is concise — no separate greeting paragraph
- Shorter than email. Get to the point faster.
- Include a clear, low-pressure CTA
- Under 150 words total

### 3. Email
- **Separate subject line** (compelling, not clickbait)
- **Separate salutation line** ("Hi [Name],")
- **Separate opening paragraph** (why you're reaching out + specific candidate reference)
- **Body paragraph** (the opportunity — lead with what's in it for them)
- **CTA paragraph** (low-pressure, specific next step)
- Slightly more formal structure than InMail. Can be a bit longer.
- Under 150 words for body

## Variants and Follow-ups

For each message type, generate:

### A/B Variant
Same message type, different opening hook. Use a different angle:
- **Version A**: Project/work-specific hook (reference their specific work)
- **Version B**: Career growth or challenge hook (what this opportunity offers)

### Follow-up Messages (2 messages)
- **Follow-up 1** (send 5-7 days later): Different angle from initial message. Under 100 words. Don't repeat the first message — add new information or a new hook.
- **Follow-up 2** (send 7-10 days after first follow-up): Short and final. "Closing the loop" tone. Under 50 words. Give them an easy out.

## Angle Options

Use these angles to differentiate messages:
1. **Project impact**: Reference their specific work and connect to the opportunity
2. **Career growth**: What they'll learn, build, or become in this role
3. **Company mission**: Why the company's work matters
4. **Team/culture**: Who they'll work with and why it's special
5. **Technical challenge**: The interesting problem they'd solve

## Message Length Guidelines

| Type | Max Length |
|------|-----------|
| LinkedIn connection note | 1 sentence, <300 chars |
| LinkedIn InMail | <150 words |
| Email body | <150 words |
| Follow-up 1 | <100 words |
| Follow-up 2 | <50 words |

## Output Structure

Present all messages in clearly labeled fenced code blocks so the recruiter can copy-paste directly:

```
## LinkedIn Connection Request — Version A
[message]

## LinkedIn Connection Request — Version B
[message]

## LinkedIn InMail — Version A
[message]

## LinkedIn InMail — Version B
[message]

## Email — Version A
Subject: [subject]
[message]

## Email — Version B
Subject: [subject]
[message]

## Follow-up 1 (send after 5-7 days)
[message]

## Follow-up 2 (send after 7-10 more days)
[message]
```
