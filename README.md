# Recruiting Skills

AI-powered skills for Claude Code that help recruiters source, evaluate, and engage candidates. Designed for non-technical HR and talent acquisition professionals.

## What's Included

| Skill | What It Does |
|-------|-------------|
| **Job Requirement Analysis** | Walks you through a structured 18-dimension analysis of a role before you start sourcing |
| **ICP Builder** | Turns a job description into a weighted scoring rubric (must-have / important / nice-to-have) |
| **Job Seller** | Identifies what's exciting about a role, rewrites boring job ads, generates outreach hooks |
| **Sourcing Strategy Generator** | Creates Boolean search strings, Google X-ray searches, and a full channel checklist |
| **Candidate Screener** | Scores candidates against your rubric with evidence, ranks batches, writes hiring manager briefings |
| **Outreach Writer** | Writes personalized LinkedIn, email, and X messages with A/B variants and follow-up sequences |

Plus: a **pipeline tracker template** and **playbooks** for capturing what worked per role type.

## Installation

**Step 1: Download this repo**

Click **Code -> Download ZIP** on GitHub, then unzip it. Or clone it:

```
git clone https://github.com/michaljuhas/recruiting-skills.git
```

**Step 2: Choose an install option**

If you are on Mac and do not see `.claude` in Finder, that is expected because dot-folders are hidden. Use Terminal for copy commands.

**Option A - Project install (Claude Code / project-scoped)**

Copy the `.claude` folder into your recruiting project:

```
cp -r recruiting-skills/.claude /path/to/your-recruiting-project/
```

**Option B - Claude home install (basic Claude Chat / global)**

Copy the `.claude` folder into your Claude home so it works in plain Claude Chat without extra project subfolders:

```
cp -r recruiting-skills/.claude ~/.claude
```

Then restart Claude or start a new conversation so skills are reloaded.

The `.claude` folder includes everything:
- **Skills** — the 6 AI-powered recruiting tools
- **Playbooks** — per-role strategy memory (edit these as you learn what works)
- **Templates** — pipeline tracker

## Quick Start

Once installed, just talk to Claude naturally:

1. **"Here's a job description, analyze the requirements"** — triggers Job Requirement Analysis
2. **"Build me a scoring rubric for this role"** — triggers ICP Builder
3. **"Make this job ad more appealing"** — triggers Job Seller
4. **"Where should I find candidates for this role?"** — triggers Sourcing Strategy Generator
5. **"Score this candidate against our rubric: [paste profile]"** — triggers Candidate Screener
6. **"Write outreach for this candidate"** — triggers Outreach Writer

## Customization

Each skill learns from YOUR past work. The more examples you add, the better the output matches your style.

### `my-examples/` — Your Past Work

Every skill has a `my-examples/` folder. Drop in files that show your preferred style:

| Skill Folder | What to Add |
|-------------|-------------|
| `.claude/skills/candidate-icp-builder/my-examples/` | Past ICPs or scoring rubrics you liked |
| `.claude/skills/job-seller/my-examples/` | Job ads that attracted great candidates |
| `.claude/skills/sourcing-strategy-generator/my-examples/` | Search strings and community lists that worked |
| `.claude/skills/candidate-screener/my-examples/` | Past candidate evaluations and hiring manager briefings |
| `.claude/skills/outreach-writer/my-examples/` | Your best outreach emails, InMails, and follow-ups |

Each folder ships with a Software Project Manager example so you can see the expected format.

**Outreach tone**: Save your preferred writing style in `.claude/skills/outreach-writer/my-examples/tone.md` (e.g., "casual and direct, always lead with the candidate's work, keep messages under 100 words").

### `playbooks/` — What Worked Per Role Type

After hiring for a role, capture what worked in a playbook file:

```
.claude/playbooks/software-project-manager.md
.claude/playbooks/frontend-engineer.md
.claude/playbooks/data-scientist.md
```

Each playbook has three sections: **What Worked** (best channels, outreach approaches), **What Didn't Work** (channels to avoid), and **Notes** (tips for next time). See `.claude/playbooks/example-software-project-manager.md` for the format.

All skills read from `playbooks/` automatically — they'll prioritize proven channels and avoid ones that failed.

### `resources/` — Guides and Mind Maps

The `job-requirement-analysis/`, `job-seller/`, and `sourcing-strategy-generator/` skills have `resources/` folders where you can upload PDF guides, mind maps, or reference materials. Claude will read and reference them.

## Recommended Workflow

The skills work best when chained together:

```
Job Requirement Analysis → ICP Builder → Job Seller → Sourcing Strategy → Candidate Screener → Outreach Writer
```

But you can use any skill independently. Paste a JD and get an ICP. Paste a profile and get a quick assessment. Ask for outreach and get messages ready to send.

## File Structure

```
├── .claude/                   # Copy this entire folder to install
│   ├── skills/                # The 6 AI-powered recruiting tools
│   │   ├── job-requirement-analysis/
│   │   ├── candidate-icp-builder/
│   │   ├── job-seller/
│   │   ├── sourcing-strategy-generator/
│   │   ├── candidate-screener/
│   │   └── outreach-writer/
│   ├── playbooks/             # Per-role strategy memory
│   └── templates/             # Pipeline tracker template
└── examples/                  # Sample JD and workflow walkthrough
```

## Examples

- `examples/example-jd.md` — A sample Software Project Manager JD you can paste to test any skill
- `examples/example-workflow.md` — A walkthrough showing ICP → Screen → Outreach chained together

## Support

This project was created by **Michal Juhas**, an AI advisor helping teams get more productive with AI.

For implementation support, workshops, and community:
- Join the community at [aiwithmichal.com](https://aiwithmichal.com?ref=GitHub&utm_source=github&utm_medium=readme&utm_campaign=recruiting-skills)
- Get individual or group support to set up AI-powered recruiting workflows
- Attend workshops to learn how to get the most out of AI in your daily work

## Contact

- Personal website: [michaljuhas.com](https://michaljuhas.com)
- Connect on LinkedIn: [linkedin.com/in/michaljuhas](https://www.linkedin.com/in/michaljuhas/)

## License

MIT

Enjoy.