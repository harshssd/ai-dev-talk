# How I Ship 10x Faster: AI-Powered Software Development in 2026
## A 45-Minute Talk by Harsha (HyperFocused Engineer)

---

## Speaker Context (for slide design on claude.ai)

**Who I am:** Harsha — Staff-level engineer with experience at AWS, DoorDash, Cruise. Solo founder building multiple products simultaneously. GitHub: hyperfocusedengineer.

**What I actually use daily:**
- **Claude Code** (CLI + desktop) — primary AI coding agent
- **gstack** (Garry Tan's skill pack) — 36 AI slash commands for the full dev lifecycle
- **Agent Teams** — multiple Claude Code sessions working in parallel via tmux
- **Expo SDK 54 / React Native** — mobile apps
- **Supabase / Firebase** — backends
- **Next.js** — web apps

**Active portfolio (built with this workflow):**
- **Cortis** — Real-time meeting intelligence (FastAPI + Supabase + Claude + Pinecone)
- **Broadside** — Cross-platform social media posting (Expo + Cloudflare Workers)
- **System Design Arcade** — Gamified learning platform (Expo + 92 tests)
- **Koo** — Baby tracking app (Expo + Supabase + Gemini AI)
- **Tossup** — Cricket auction platform (Next.js + Supabase)
- **Zeroshot** — Cyberpunk Python learning game (React + Skulpt)

**My setup:**
- macOS, tmux with Catppuccin theme, TPM plugins, vim-style navigation
- Claude Code with Agent Teams (experimental) — team lead + 3 teammates in tmux panes
- gstack installed globally with `gstack-` prefix (36 skills available in every project)
- Permission modes tuned per context: `bypassPermissions` for autonomous work, `acceptEdits` for production code

---

## Talk Structure: The Story Arc

### The Hook (0:00 - 0:03) — 3 minutes

**Title Slide:** "I maintain 6 products solo. Here's how."

**Opening line:** "Six months ago, I was mass-applying to jobs. Today, I ship more code in a week than most teams ship in a month — across six different products. The difference isn't that I work harder. It's that I stopped coding alone."

**The reveal:** Show a screenshot of the tmux Agent Teams session — 3 AI teammates exploring 3 projects simultaneously while you're giving this talk. "This is running right now. While I'm here talking to you, my AI team is reviewing code, merging feature branches, and adding test coverage across three of my projects."

**Why this matters to the audience:** "By the end of this talk, you'll have a complete playbook to do the same thing. Not theory — the exact tools, commands, and workflow I use every day."

---

### Act 1: Learning (0:03 - 0:10) — 7 minutes
#### "How I Learn a New Stack in 30 Minutes"

**The story:** Walk through the REAL example from today — discovering Garry Tan's gstack and going from "what is this?" to fully installed and configured in one conversation.

**Beat 1 — Discovery:**
"Someone mentions a tool. Instead of spending 2 hours reading docs, watching YouTube tutorials, and setting up manually, I do this:"
```
Me: "Can we use Garry Tan's stack everywhere?"
Claude: *explores the repo, reads every config file, maps dependencies, 
        checks for conflicts with my existing setup*
```

**Beat 2 — Intelligent Setup:**
"Claude didn't just install it. It found that gstack's `/ship` and `/retro` commands conflict with my existing custom commands. It suggested `--prefix` mode. It installed Bun (a dependency I didn't have). It updated my global config. One conversation, zero manual steps."

Show the actual output:
```
  linked skills: gstack-autoplan gstack-benchmark gstack-browse 
  gstack-canary gstack-careful gstack-checkpoint gstack-codex...
  gstack ready (claude).
```

**Beat 3 — Instant Expertise:**
"Five minutes after installation, I had a complete guide to using 36 new commands efficiently. Not from docs — from Claude reading every SKILL.md file and synthesizing the workflow."

**Key takeaway for audience:** "Stop learning tools in isolation. Let AI explore, install, configure, and teach you — all in one flow. Your job is to ask the right questions."

**DEMO MOMENT (optional):** Show a 60-second clip of asking Claude to set up a completely new tool and having it work end-to-end.

---

### Act 2: Planning (0:10 - 0:20) — 10 minutes
#### "From Idea to Architecture in One Session"

**The story:** Walk through how Cortis (the meeting intelligence product) was planned.

**Beat 1 — The Problem:**
"I had an idea: real-time meeting intelligence. AI that listens to your meetings, enriches context about participants, and generates follow-ups. Cool idea. But where do you even start?"

**Beat 2 — Office Hours (gstack):**
"gstack has a command called `/office-hours` — modeled after YC office hours. It asks you 6 forcing questions that challenge your assumptions:"
- Who is this for and why do they care?
- What's the smallest version that proves the thesis?
- What's your unfair advantage?
- What kills this?
- How do you know it's working?
- What do you do first?

"It pushed back on my first framing. Made me realize I was building too broad. Narrowed to: professionals who take 5+ external meetings/week."

**Beat 3 — Autoplan Pipeline:**
"Then I ran `/autoplan`. This chains four reviews automatically:"
```
CEO Review    → Is this the right thing to build?
Design Review → Is the UX right?
Eng Review    → Is the architecture sound?
DX Review     → Is the developer experience clean?
```

"Each review uses the output of the previous one. The eng review generated data flow diagrams, identified that I needed Pinecone for vector embeddings, and wrote a test plan."

**Beat 4 — Interactive Planning in Claude Code:**
"The key insight: AI doesn't replace your judgment. It gives you a STRUCTURED framework to apply your judgment faster. I was in plan mode — Claude proposed, I refined, we iterated. The plan file became my source of truth."

Show the plan structure:
```
## Context: Why this change
## Steps: What to do  
## Files Modified: What changes
## Verification: How to test
```

**Beat 5 — Breaking into Tasks:**
"Once the plan was approved, I used `/plan-tasks` to break it into discrete, parallelizable work items. Each task had clear inputs, outputs, and acceptance criteria."

**Key takeaway for audience:** "Planning is where AI gives you the biggest leverage. Not because it plans better than you — but because it forces you through a complete framework in minutes instead of days. You make better decisions because you've considered more angles."

---

### Act 3: Building (0:20 - 0:30) — 10 minutes
#### "Parallel Agents: My AI Engineering Team"

**The story:** Show how Agent Teams work for implementation.

**Beat 1 — Multiple Sessions & Agents:**
"There are several ways to run multiple AI agents in parallel. I'm actively exploring all of them:"

```
Approach 1: Multiple tmux panes, each with its own Claude Code session
┌──────────────┬──────────────┬──────────────┐
│ claude -p    │ claude -p    │ claude -p    │
│ "Feature A"  │ "Feature B"  │ "Fix bug C"  │
│ Project 1    │ Project 2    │ Project 3    │
└──────────────┴──────────────┴──────────────┘

Approach 2: Agent Teams (experimental) — one lead, multiple teammates
┌─────────────────────────────────────────────┐
│ Team Lead → assigns + coordinates           │
├──────────┬──────────┬──────────────────────┤
│Teammate 1│Teammate 2│ Teammate 3            │
│ own ctx  │ own ctx  │ own ctx               │
└──────────┴──────────┴──────────────────────┘

Approach 3: Conductor (conductor.build) — visual dashboard + git worktrees
```

"I'm still exploring Agent Teams — it's experimental but fascinating. The team lead assigns work, teammates get isolated context windows and worktrees, and they can message each other. It's like managing a remote engineering team, except the standup takes 0 seconds."

**Beat 2 — What I've Tried So Far:**
"Earlier today, I spun up an agent team to work on three of my projects simultaneously. The lead spawned 3 explore agents to assess each project's state before assigning tasks. It's early days, but the direction is clear — we're moving from 'AI pair programmer' to 'AI engineering team.'"

**Beat 3 — The Permission Spectrum:**
"This is where it gets nuanced. Not everything should be autonomous."

```
SPEED ←──────────────────────────→ SAFETY

bypassPermissions    acceptEdits    default    plan-only
   (autonomous)      (auto-edit)   (ask me)   (read-only)
   
   Side projects     Active dev    Production   Oncall
   Feature branches  New features  Hotfixes     Debugging
```

"I match the permission level to the risk. Side project feature branch? Full autonomy. Production hotfix? Human in the loop."

**LIVE DEMO MOMENT:** If possible, show the tmux session with agents working. Even seeing them read files and make decisions is impressive to an audience.

**Key takeaway for audience:** "You are the CEO of an AI engineering team. Your job isn't to write every line — it's to set the right constraints, assign the right tasks, and review the output."

---

### Act 4: Review & Ship (0:30 - 0:37) — 7 minutes
#### "The Review Pipeline That Catches What Tests Miss"

**The story:** Show the review → QA → ship pipeline.

**Beat 1 — Code Review (Not What You Think):**
"`/gstack-review` doesn't just lint your code. It spawns parallel specialist agents:"
- Security reviewer (OWASP top 10)
- Performance reviewer (N+1 queries, memory leaks)
- Testing reviewer (coverage gaps, flaky tests)
- Maintainability reviewer (tech debt, abstractions)
- Red team (tries to break your code)

"Each specialist gets fresh context — no bias from the others. Findings are deduplicated and ranked by confidence."

**Beat 2 — QA with Real Eyes:**
"`/gstack-qa` opens a real Chromium browser and clicks through your app. Not a synthetic test — actual browser automation that finds visual bugs, broken flows, accessibility issues."

**Beat 3 — Ship:**
"`/gstack-ship` is the final gate: runs tests, creates changelog, bumps version, opens PR. One command."

**Beat 4 — The Guardrails:**
"For production apps, I add safety layers:"
- `/gstack-careful` — warns before destructive commands
- `/gstack-freeze` — locks edits to one directory
- `/gstack-guard` — both combined
- `/gstack-cso` — full security audit (OWASP + STRIDE)

"Speed without safety is just chaos. The right guardrails let you go FASTER because you're not anxious about breaking things."

**Key takeaway for audience:** "AI review isn't replacing human review. It's making human review worth doing — by the time code reaches you, the obvious issues are already fixed."

---

### Act 5: Oncall Buddy (0:37 - 0:42) — 5 minutes
#### "3 AM Pages and the AI That Has Your Back"

**The story:** How AI changes the oncall experience.

**Beat 1 — The Scenario:**
"It's 3 AM. PagerDuty fires. You're groggy, looking at an error you've never seen. The old way: grep through logs, check dashboards, read code you haven't touched in months, hope you don't make it worse."

**Beat 2 — The New Way:**
```
/gstack-investigate
```
"One command. It systematically:"
- Reads the error and traces the code path
- Checks git blame for recent changes
- Auto-freezes to the affected module (so you don't accidentally break something else)
- Proposes a root cause with evidence
- Suggests a fix with rollback plan

**Beat 3 — The Safety Net:**
"For oncall, I WANT the human in the loop. I use `default` permission mode — Claude proposes, I approve each step. At 3 AM, I want to understand what's happening, not just throw code at it."

"But Claude has already done the hard part: reading 50 files, correlating the error with recent deploys, and narrowing it to 3 lines of code. My job is just to verify and approve."

**Beat 4 — Post-Incident:**
"`/gstack-retro` generates the retrospective. Timeline, root cause, action items, prevention measures. What used to take an hour of writing takes 5 minutes of review."

**Key takeaway for audience:** "AI doesn't replace your oncall judgment. It replaces the 45 minutes of context-gathering so you can make the right call in 5 minutes instead of 50."

---

### The Close (0:42 - 0:45) — 3 minutes
#### "The Playbook — Your Next 30 Minutes"

**The meta-lesson:**
"Here's what I want you to take away: the competitive advantage isn't AI itself. Everyone has access to Claude, GPT, Gemini. The advantage is having a SYSTEM — a repeatable workflow that compounds."

**The 30-minute challenge (give the audience a concrete next step):**

```
Minute 0-5:   Install Claude Code (brew install claude-code or npm)
Minute 5-10:  Install gstack (git clone + ./setup)
Minute 10-15: Open your hardest current project
Minute 15-25: Run /office-hours on your biggest open question
Minute 25-30: Run /review on your latest PR
```

"In 30 minutes, you'll have experienced the entire spectrum — from strategic thinking to tactical code review. And you'll never go back to coding alone."

**Final line:** "I maintain six products solo. Not because I'm a 10x engineer. Because I have a 10x workflow. And now you do too."

---

## Slide Deck Outline (for claude.ai)

### Slide Design Notes
- **Theme:** Dark mode, terminal aesthetic (matches the tools being discussed)
- **Font:** Monospace for code, clean sans-serif for text
- **Color palette:** Catppuccin Mocha (matches my actual terminal theme)
- **Screenshots:** Use REAL screenshots from my setup, not mockups
- **No bullet-point walls** — one idea per slide, heavy use of terminal screenshots and diagrams

### Slide List

1. **Title:** "I maintain 6 products solo. Here's how." + name + socials
2. **The Portfolio:** Grid of 6 app screenshots/logos
3. **The Secret:** Screenshot of tmux with 3 agent teammates running
4. **Agenda:** The 5 acts as a visual timeline
5. **ACT 1: LEARN** — section divider
6. **The Old Way:** YouTube tutorial → docs → Stack Overflow → trial and error → 2 hours
7. **The New Way:** One conversation → installed, configured, documented → 15 minutes
8. **Demo: gstack install** — terminal screenshot showing the full flow
9. **Before/After:** Side-by-side of learning a new tool old vs new
10. **ACT 2: PLAN** — section divider
11. **The Idea:** Cortis — meeting intelligence (one-liner)
12. **Office Hours:** The 6 forcing questions
13. **Autoplan Pipeline:** CEO → Design → Eng → DX diagram
14. **The Plan File:** Screenshot of an actual plan output
15. **Key Insight:** "AI doesn't replace judgment. It structures it."
16. **ACT 3: BUILD** — section divider
17. **The Terminal:** 3 approaches diagram — tmux panes, Agent Teams, Conductor
18. **Multiple Sessions:** How to run independent Claude sessions in parallel
19. **Agent Teams (Exploring):** Team lead + teammates — what works, what's rough
20. **The Permission Spectrum:** Speed ↔ Safety slider diagram — different modes of autonomy
21. **Live Screenshot:** Real tmux session with agents exploring projects
22. **Key Insight:** "You are the CEO of an AI engineering team."
22. **ACT 4: REVIEW & SHIP** — section divider
23. **Review Army:** Parallel specialist agents diagram
24. **QA with Real Eyes:** Chromium browser automation screenshot
25. **The Ship Command:** One command → tests, changelog, version, PR
26. **Guardrails:** careful, freeze, guard, cso — when to use each
27. **Key Insight:** "Speed without safety is just chaos."
28. **ACT 5: ONCALL** — section divider
29. **3 AM Page:** The scenario
30. **Investigate:** What it does automatically
31. **The Safety Net:** Why human-in-the-loop matters here
32. **Retro:** Automated retrospective
33. **Key Insight:** "Replace context-gathering, not judgment."
34. **THE PLAYBOOK** — section divider
35. **The 30-Minute Challenge:** Step-by-step for the audience
36. **The Stack:** Claude Code + gstack + tmux + Agent Teams (logos/links)
37. **Resources:** Links to everything mentioned
38. **Final Slide:** "I have a 10x workflow. Now you do too." + QR code to slides/repo

---

## Q&A Prep — Likely Questions

**Q: How much does this cost?**
A: Claude Pro ($20/mo) or Max ($100/mo for heavy usage). gstack is free (MIT). All other tools are free. I spend about $100/mo total and save 20+ hours/week.

**Q: Doesn't this make you dependent on AI?**
A: I still understand every line of code. AI handles the mechanical parts — boilerplate, exploration, review checklists. The architecture, product decisions, and judgment are still mine. Think of it like using an IDE vs notepad — you're not "dependent" on autocomplete.

**Q: What about code quality?**
A: Higher than before. Every PR goes through parallel specialist reviews (security, performance, testing, maintainability). I have MORE review coverage than most teams, not less.

**Q: What about sensitive/proprietary code?**
A: Claude Code runs locally. Code stays on your machine. API calls send context to Anthropic's servers but they don't train on it (with API usage). For highly sensitive work, you can use the `--bare` flag and limit tool access.

**Q: How do you handle when AI makes mistakes?**
A: That's what the permission spectrum is for. For production code, AI proposes and I approve. The review pipeline catches most issues before they reach me. And `/gstack-careful` prevents destructive commands. The system is designed for safe failure.

**Q: Can this work for a team, not just solo?**
A: Yes. gstack has team mode (`./setup --team`) that gives every developer the same skills. Agent Teams can coordinate across a shared codebase with git worktrees. The workflow scales.

---

## Links & Resources (for final slide / handout)

- **Claude Code:** https://claude.com/claude-code
- **gstack:** https://github.com/garrytan/gstack
- **Conductor:** https://conductor.build
- **Agent Teams Docs:** https://code.claude.com/docs/en/agent-teams
- **tmux Plugin Manager:** https://github.com/tmux-plugins/tpm
- **Catppuccin Theme:** https://github.com/catppuccin/tmux
- **My GitHub:** https://github.com/hyperfocusedengineer

---

## Context for claude.ai (copy this when creating slides)

"I'm Harsha (HyperFocused Engineer). I need you to create a presentation deck from the plan above. Use a dark terminal-aesthetic theme with Catppuccin Mocha colors (base: #1e1e2e, text: #cdd6f4, blue: #89b4fa, green: #a6e3a1, mauve: #cba6f7, peach: #fab387). 

I actually use all of these tools daily — this is not theoretical. I maintain 6 products solo: Cortis (meeting intelligence), Broadside (social media), System Design Arcade (learning), Koo (baby tracking), Tossup (cricket auctions), Zeroshot (Python learning game).

My actual setup: macOS + tmux (Catppuccin Mocha) + Claude Code (Opus 4.6, 1M context) + gstack (36 skills with gstack- prefix) + Agent Teams (experimental, tmux mode). 

The talk is 45 minutes. Make it storytelling, not a feature list. Each act should have a narrative arc with a real example from my projects. Include speaker notes for each slide."
