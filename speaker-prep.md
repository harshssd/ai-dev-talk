# Speaker Preparation Document
## "How I Ship 10x Faster: AI-Powered Software Development in 2026"
### 45-Minute Talk by Harsha (HyperFocused Engineer)

---

## 1. PRE-TALK CHECKLIST (30 minutes before)

- [ ] **tmux session running with Agent Teams live**
  - Start 45 minutes before talk begins
  - Command: `tmux new-session -s main -d -x 200 -y 50`
  - Spawn 3 teams in parallel panes (Feature A / Feature B / Bug C)
  - Keep at least one in "explore" mode so it's visibly working during talk
  - Screenshot for slide 21 ready to display

- [ ] **Laptop on stage**
  - Connected to projector (test HDMI/USB-C)
  - Brightness at 100%
  - Do NOT disturb OFF
  - Battery 100% (or plugged in)
  - Catppuccin Mocha terminal theme active
  - Font size: 16-18pt (readable from back of room)

- [ ] **Slides loaded and tested**
  - Deck open in presentation mode (not edit mode)
  - Presenter notes visible on your screen only
  - Test every transition and video/screenshot embed
  - Advance slides with keyboard (spacebar) not clicker — clicker is backup only

- [ ] **Water bottle stage left**
  - Room temperature, not ice cold (won't disrupt throat)
  - Keep in pocket or cup holder offstage

- [ ] **Wireless clicker tested**
  - Batteries fresh (replace day-of, not the morning-before)
  - Has backup USB receiver in pocket
  - Tested on all slides — some projectors are picky about range

- [ ] **Demo script open in editor**
  - Fallback prompts for Claude Code if things go wrong (see section 5)
  - Not visible to audience
  - Keep terminal window small so you can see slides + terminal simultaneously

- [ ] **Backup slides printed (3 copies)**
  - Slide numbers in corner (speaker reference)
  - Keep in podium or back pocket
  - Only for if projector dies mid-talk

- [ ] **Voice warm-up (5 minutes)**
  - Hum scale from low to high: do-re-mi-fa-sol-la-ti-do
  - Say opening line 3x slowly, 3x at normal pace
  - Drink water

- [ ] **Mic test**
  - Wireless lapel mic: clipped to shirt collar (not tie — it muffles)
  - Walk across stage, speak in normal voice
  - Check volume level from back of room
  - If handheld, test grip and angle

- [ ] **Time check with organizers**
  - When does talk start? (set phone alarm for 5 minutes before)
  - How much time for Q&A after? (adjust "The Close" accordingly)
  - Where are the 5-minute, 1-minute warnings? (watch for hand signals from stage manager)

- [ ] **Tech support contact on speed dial**
  - Have organizer's number in phone
  - Projector password reset ready
  - WiFi password written down (for fallback demo)

---

## 2. TIMING GUIDE (45 minutes total)

### Minute-by-Minute Breakdown with Visual Markers

**Total time: 45:00**
**Buffer built in: 5 minutes (for applause, laughs, questions)**

```
┌─ TIME ─┬─────────────────────────────┬────────────┬─ PACING ─────────────┐
│ 0:00   │ HOOK: Title Slide           │ 3:00       │ ENERGY: High (intro) │
│ 3:00   │ ACT 1: Learning             │ 7:00       │ PACE: Medium-fast    │
│ 10:00  │ ACT 2: Planning             │ 10:00      │ PACE: Deliberate     │
│ 20:00  │ ACT 3: Building             │ 10:00      │ ENERGY: Peak         │
│ 30:00  │ ACT 4: Review & Ship        │ 7:00       │ PACE: Accelerate     │
│ 37:00  │ ACT 5: Oncall              │ 5:00       │ ENERGY: Lower        │
│ 42:00  │ CLOSE: The Playbook         │ 3:00       │ ENERGY: Lift (exit)  │
│ 45:00  │ [END]                       │            │ [APPLAUSE]           │
└────────┴─────────────────────────────┴────────────┴──────────────────────┘
```

### Scene-by-Scene Timing (with signals)

**0:00-0:20 | HOOK: Title Slide + Opening Line**
- Slide 1 already projected (audience sees it as you walk on)
- Stand center stage, make eye contact
- Deliver opening line with confidence: "Six months ago, I was mass-applying to jobs..."
- PACING: Slow. Pause after each sentence. Let it sink in.
- SIGNAL: If running over, speed up after 0:15

**0:20-0:40 | The Reveal (tmux screenshot)**
- Transition to Slide 3: "This is running right now."
- Point to live Agent Teams visualization
- Let that image speak for 10 seconds of silence
- PACING: Slow. This is the WOW moment.

**0:40-3:00 | Why This Matters + Agenda**
- Deliver: "By the end of this talk, you'll have a complete playbook..."
- Slide 4: Show the 5 acts as a timeline
- Walk through each act title (Learning, Planning, Building, Review, Oncall)
- PACING: Medium. Build momentum into Act 1.
- SIGNAL: If running late, cut this to 1:30 — skip detailed agenda walk, just show slide

**3:00-5:00 | ACT 1 Setup: "How I Learn a New Stack"**
- Slide 5: Act divider (dark screen with "ACT 1: LEARN")
- Transition: "Let me show you a real example from today."
- Slide 6: "The Old Way" — YouTube, docs, trial/error
- PACING: Relatable, slightly self-deprecating (sell the pain point)
- EMOTION: Frustration with the old way

**5:00-6:00 | gstack Discovery Story**
- Slide 7: "The New Way"
- Tell the story: "Someone mentions gstack. Instead of 2 hours..."
- Slide 8: Terminal screenshot of gstack install
- PACING: Fast. Show the contrast to "old way"
- EMOTION: Relief, competence

**6:00-7:15 | Act 1 Beats (Beat 1-3)**
- Slide 8-9: Show actual output of install process
- Walk through the three beats:
  - Beat 1 (Discovery): AI explores, asks clarifying questions
  - Beat 2 (Setup): Detects conflicts, suggests prefix mode, installs Bun
  - Beat 3 (Expertise): 5 minutes in, you have 36 new commands mapped
- PACING: Narrative. This is a story, not a feature list.
- SIGNAL: If running behind, compress beats 1-2 into single slide (2 min)

**7:15-10:00 | Act 1 Key Takeaway + Optional Demo**
- Slide 9: "Before/After" comparison (time investment)
- Deliver key takeaway: "Stop learning tools in isolation..."
- Optional LIVE DEMO (2 min): If confident with pacing, show 60-sec Claude Code session where you ask it to set up a tool
  - Pre-load this in a terminal window
  - Risk: If slow, SKIP demo. Just show screenshot instead (Slide 8)
- PACING: If doing demo, slow down. If showing screenshot, normal pace.
- ENERGY: Building momentum into Act 2

---

**10:00-10:30 | ACT 2 Setup: "From Idea to Architecture"**
- Slide 10: Act divider
- Transition: "Now let's zoom out. You have an idea. Where do you start?"
- Slide 11: Cortis — the real example
- PACING: Shift from fast to deliberate. This is the thinking section.
- EMOTION: Excitement about the idea, but also doubt

**10:30-12:00 | The Problem (Cortis Context)**
- Slide 11: "The Idea: Real-time meeting intelligence"
- Deliver Beat 1: "I had an idea. Cool idea. But where do you even start?"
- Slide 12: Visual of the problem (meeting attendees, context needed)
- PACING: Slower. Let them sit with the ambiguity.
- EMOTION: Vulnerability (not knowing where to start is OK)

**12:00-14:30 | Office Hours & Forcing Questions**
- Slide 12: The 6 forcing questions (displayed with clear formatting)
- Walk through each question, pause after each:
  1. Who is this for and why do they care?
  2. What's the smallest version that proves the thesis?
  3. What's your unfair advantage?
  4. What kills this?
  5. How do you know it's working?
  6. What do you do first?
- Slide 13: Diagram showing how office hours narrowed the idea
- PACING: Deliberate. Pause after each question so it lands.
- EMOTION: Clarity emerging from structure

**14:30-16:00 | Autoplan Pipeline**
- Slide 13: Diagram of CEO → Design → Eng → DX chain
- Explain: "Then I ran `/autoplan`. This chains four reviews automatically."
- Walk through each review lane
- Slide 14: Screenshot of actual plan output
- PACING: Medium-fast. Show the throughput of parallel reviews.
- EMOTION: Wow, it does all that in one command?

**16:00-17:30 | Interactive Planning in Claude Code**
- Slide 15: "Key Insight: AI doesn't replace judgment. It structures it."
- Tell story: "I was in plan mode — Claude proposed, I refined, we iterated."
- Slide 14: Show plan structure (Context, Steps, Files Modified, Verification)
- PACING: Normal. This is the "aha" moment.

**17:30-20:00 | Plan-to-Tasks & Act 2 Wrap**
- Slide 16: `/plan-tasks` breaks plan into parallelizable work items
- Show example task card (inputs, outputs, acceptance criteria)
- Deliver Act 2 key takeaway: "Planning is where AI gives you the biggest leverage..."
- PACING: Slow for key takeaway. This is the thesis of Act 2.
- SIGNAL: If running behind, compress to just Slides 13-15 (5 min) and summarize beats

---

**20:00-20:30 | ACT 3 Setup: "Parallel Agents: Your AI Team"**
- Slide 16: Act divider (large, dark)
- Transition: "Now we get to the fun part. Implementation."
- Slide 17: Title card — "Parallel Agents: Your AI Engineering Team"
- PACING: Energy shift. Get faster. This is peak delivery.
- EMOTION: Excitement

**20:30-22:30 | Multiple Approaches Diagram**
- Slide 17-18: The three approaches (tmux panes, Agent Teams, Conductor)
- Walk through each approach (don't deep-dive, just show the concept)
  - Approach 1: Multiple tmux panes (what I use today)
  - Approach 2: Agent Teams (experimental, what I'm exploring)
  - Approach 3: Conductor (external tool option)
- PACING: Fast. This is showing range of options.
- EMOTION: Technical enthusiasm

**22:30-24:00 | Agent Teams Live Moment**
- Slide 19: Real screenshot of 3 panes in tmux with Claude Code running
- Point at the screen: "Right now, while I'm talking, my team is doing this..."
- Don't try to explain what each pane is doing in detail — just show it's alive
- PACING: Pause and let them stare at the screenshot (8 seconds of silence)
- SIGNAL: This is your WOW moment #2. Stay quiet and let it sink.

**24:00-26:30 | The Permission Spectrum**
- Slide 20: SPEED ←→ SAFETY diagram with four modes:
  - bypassPermissions (autonomous) for side projects
  - acceptEdits (auto-edit) for active dev
  - default (ask me) for production
  - plan-only (read-only) for oncall
- Walk through each, explain when you'd use it
- Slide 20: Risk matrix (feature branch = high autonomy, hotfix = human review)
- PACING: Moderate. This is nuanced — don't rush.
- EMOTION: Pragmatism (not all work is equal, different work needs different trust)

**26:30-30:00 | Act 3 Key Takeaway**
- Deliver: "You are the CEO of an AI engineering team..."
- Slide 21: Visual of CEO delegating
- Explain: Your job isn't to write every line, it's to set constraints and review output
- PACING: Slow. This is a philosophy statement, not a feature.
- SIGNAL: If running behind (past 26:30), compress permission spectrum (1 min) and jump to takeaway

---

**30:00-30:30 | ACT 4 Setup: "Review & Ship"**
- Slide 22: Act divider
- Transition: "Code is ready. Now what?"
- Slide 23: "The Review Pipeline"
- PACING: Building toward ship. Maintain energy.

**30:30-32:00 | Code Review Specialists**
- Slide 23: Diagram of parallel specialist agents (Security, Perf, Testing, Maintainability, Red Team)
- Walk through `/gstack-review`:
  - Spawns parallel specialists, each gets fresh context
  - Findings deduplicated and ranked by confidence
- Explain: "Each specialist sees the code independently"
- PACING: Fast. Show the parallelism.
- EMOTION: Thoroughness (you get better coverage than most teams)

**32:00-33:30 | QA & Ship**
- Slide 24: Chromium browser automation screenshot (real browser clicking through app)
- Explain `/gstack-qa`: "Not synthetic. Real browser. Finds visual bugs."
- Slide 25: The ship command flow (tests → changelog → version → PR)
- Explain `/gstack-ship`: "One command. Everything flows."
- PACING: Accelerate. Show momentum.

**33:30-35:00 | Guardrails**
- Slide 26: Four guardrail commands (careful, freeze, guard, cso)
- Walk through each briefly:
  - `/gstack-careful` — warns before destructive commands
  - `/gstack-freeze` — locks edits to one directory
  - `/gstack-guard` — both combined
  - `/gstack-cso` — full security audit (OWASP + STRIDE)
- Slide 27: "Speed without safety is just chaos."
- PACING: Slow for the guardrails section. This is about responsibility.
- EMOTION: Maturity (real engineering is about tradeoffs)

**35:00-37:00 | Act 4 Key Takeaway & Transition to Act 5**
- Slide 27: Key insight — "AI review isn't replacing human review. It's making human review worth doing."
- Explain: By the time code reaches you, obvious issues are fixed
- PACING: Normal. Smooth transition into Act 5.

---

**37:00-37:30 | ACT 5 Setup: "3 AM Pages"**
- Slide 28: Act divider
- Transition: "Not all work is planned. What about emergencies?"
- Slide 29: "3 AM Page and the AI That Has Your Back"
- PACING: Tone shift. This is real, stressful, relatable.
- EMOTION: Empathy (everyone knows what 3 AM is like)

**37:30-39:00 | The Old Way vs New Way**
- Slide 29: The scenario — "It's 3 AM. PagerDuty fires. Error you've never seen."
- Old way: Grep, dashboards, code you haven't touched in months
- New way: `/gstack-investigate` (show what it does)
  - Reads error, traces code path
  - Checks git blame
  - Proposes root cause with evidence
  - Suggests fix with rollback plan
- Slide 30: Output of investigate command
- PACING: Sympathetic but fast. Show relief.
- EMOTION: Relief (someone has your back)

**39:00-40:30 | Safety Net & Human in the Loop**
- Explain: For oncall, you WANT human in the loop
- Use `default` permission mode: Claude proposes, you approve each step
- Slide 31: Permission diagram focused on oncall (human in the loop)
- Explain: "At 3 AM, I want to understand what's happening."
- But Claude has already done context-gathering (read 50 files, correlate, narrow to 3 lines)
- PACING: Slower. You want them to trust the system but verify it.
- EMOTION: Confidence + responsibility

**40:30-42:00 | Post-Incident & Closing Act 5**
- Slide 32: `/gstack-retro` generates retrospective
- Timeline, root cause, action items, prevention measures
- What used to take 1 hour now takes 5 minutes of review
- Slide 33: Key insight — "Replace context-gathering, not judgment."
- PACING: Normal. Build toward close.

---

**42:00-44:00 | THE CLOSE: "The Playbook"**
- Slide 34: Act divider — "THE PLAYBOOK"
- Transition: "Here's what I want you to take away..."
- PACING: Build energy. Final lift.
- EMOTION: Inspiration

- Deliver meta-lesson: "The competitive advantage isn't AI itself. The advantage is having a SYSTEM."
- Slide 35: The 30-Minute Challenge (on screen)
  - Minute 0-5: Install Claude Code
  - Minute 5-10: Install gstack
  - Minute 10-15: Open your hardest current project
  - Minute 15-25: Run /office-hours on your biggest open question
  - Minute 25-30: Run /review on your latest PR
- PACING: Moderate. Walk them through each step.
- EMOTION: Empowerment (they can do this today)

**44:00-44:45 | Final Line**
- Deliver final line with conviction: "I maintain six products solo. Not because I'm a 10x engineer. Because I have a 10x workflow. And now you do too."
- Slide 36: Logo/link slide (Claude Code, gstack, Agent Teams)
- Slide 37: Final slide — "I have a 10x workflow. Now you do too." + QR code to slides
- PACING: Slow. Let the final line hang.
- HOLD SILENCE for 3 seconds after final line
- WAIT for applause before leaving stage

**44:45-45:00 | Applause & Transition to Q&A**
- Acknowledge applause (nod, smile)
- Step back to podium for Q&A if prepared to do so
- If not, say: "Thanks! Happy to chat in the hallway" and leave stage

---

### Pacing Rules of Thumb

- **SLOW DOWN if:** Sharing a story beat, delivering a key takeaway, showing a wow moment (Agent Teams), delivering the closing line
- **SPEED UP if:** Running behind schedule, showing code details, listing features, or explaining technical setup
- **PAUSE for:** Laughter, reactions, "aha" moments, reading time for on-screen text (5 seconds minimum)
- **WATCH for stage manager signals:**
  - 5-minute warning: wrap up Act 4 or early Act 5
  - 1-minute warning: jump straight to closing line
  - Time's up signal: STOP immediately, deliver closing line in condensed form

---

## 3. TRANSITION PHRASES (word-for-word)

Use these exact phrases to move between sections. They feel natural, maintain flow, and signal a shift in the audience's attention.

### HOOK → ACT 1
"Let me show you exactly what that looks like. And I'll start with the beginning of this workflow — how I actually learn new tools so fast."

### ACT 1 → ACT 2
"OK, so you can learn a new stack in 30 minutes. But once you've learned it, the real question is — what are you going to build? And that's where planning comes in."

### ACT 2 → ACT 3
"You've got your plan. Your task breakdown. Now the real work starts. But here's the thing — you don't do it alone. You build a team."

### ACT 3 → ACT 4
"So you've got your agents working on features. Code is being written. The natural question is — how do you make sure that code is actually good? How do you review it?"

### ACT 4 → ACT 5
"All of this assumes you're working during normal business hours. But software doesn't only break during business hours. And that's when the rules change."

### ACT 5 → CLOSE
"So we've covered the full cycle — learning, planning, building, reviewing, and handling emergencies. But I don't want this to feel theoretical. Let me give you something concrete you can do in the next 30 minutes."

### CLOSE → Q&A
"That's the talk. Questions before I hand it back to [organizer name]?"

---

## 4. KEY STORIES & BEATS (One Thing to Remember)

For each act, the core emotional beat and the ONE sentence the audience must remember.

### ACT 1: LEARNING
**Emotional Beat:** Frustration → Relief
- **Story:** gstack discovery. Someone mentions it. Instead of YouTube tutorials + docs + Stack Overflow + trial/error (2 hours), you have one conversation with Claude and you have 36 new commands installed, configured, and understood (15 minutes).
- **Real Anecdote:** "I actually did this yesterday. I'd never heard of gstack before. Ten minutes later, I had the entire skill pack mapped and ready to use."
- **One Thing to Remember:** "Stop learning tools in isolation. Let AI explore, install, configure, and teach you — all in one flow. Your job is to ask the right questions."

### ACT 2: PLANNING
**Emotional Beat:** Ambiguity → Clarity → Confidence
- **Story:** Cortis (meeting intelligence) — you have the idea, but you don't know where to start. Run `/office-hours` (6 forcing questions), then `/autoplan` (CEO review, design review, eng review, DX review in parallel). In 20 minutes, you have a complete architecture plan.
- **Real Anecdote:** "The design review told me I was thinking about this wrong. I was trying to build a full understanding system. The review pushed back and said — no, focus on professionals with 5+ external meetings per week. That one constraint changed everything."
- **Other Anecdotes from Portfolio:**
  - System Design Arcade: Tested with 92 unit tests to validate architecture before building UI
  - Broadside: Cross-platform planning revealed that sharing logic between iOS and Android saved 3 days of duplicate work
- **One Thing to Remember:** "Planning is where AI gives you the biggest leverage. Not because it plans better than you — but because it forces you through a complete framework in minutes instead of days."

### ACT 3: BUILDING
**Emotional Beat:** Overwhelm → Empowerment
- **Story:** Agent Teams running in tmux. Three sessions in parallel (Feature A, Feature B, Bug C) working independently. Each has its own Claude Code agent, its own context, its own git worktree. They coordinate via slack-like messaging. While you're on stage, they're working.
- **Real Anecdote:** "Earlier today, I spun up three agents. The lead spawned explore agents to assess each project's state. Then I assigned them specific tasks. One went to work on Cortis (meeting intelligence). One on Broadside (social media posting). One on System Design Arcade test coverage. No hand-holding. No waiting for me to give step-by-step instructions. They just worked."
- **Permission Model:** Different work needs different trust levels
  - Side projects (Tossup) → `bypassPermissions` (full autonomy)
  - Active development (Cortis new feature) → `acceptEdits` (auto-apply changes)
  - Production hotfix → `default` (ask me first)
  - Oncall debugging → `plan-only` (show me the plan, I'll execute)
- **One Thing to Remember:** "You are the CEO of an AI engineering team. Your job isn't to write every line — it's to set the right constraints, assign the right tasks, and review the output."

### ACT 4: REVIEW & SHIP
**Emotional Beat:** Doubt → Conviction
- **Story:** Code review that actually works. Instead of one human reading code and guessing about security, performance, testing, you get five parallel specialist agents.
  - Security reviewer (OWASP top 10)
  - Performance reviewer (N+1 queries, memory leaks)
  - Testing reviewer (coverage gaps, flaky tests)
  - Maintainability reviewer (tech debt, abstractions)
  - Red team (tries to break your code)
- **Real Anecdote:** "System Design Arcade shipped with 92 tests. That's not because I'm obsessive (okay, maybe I am). It's because the testing reviewer kept finding gaps in the test plan. Every review iteration, it caught something I would have missed. By ship time, the code was bulletproof."
- **Ship Pipeline:**
  - `/gstack-review` → parallel specialist reviews
  - `/gstack-qa` → real browser automation (not synthetic tests)
  - `/gstack-ship` → tests, changelog, version bump, PR
  - `/gstack-cso` → full security audit if production
- **One Thing to Remember:** "Speed without safety is just chaos. The right guardrails let you go FASTER because you're not anxious about breaking things."

### ACT 5: ONCALL
**Emotional Beat:** Stress → Control → Trust
- **Story:** 3 AM page. Error you've never seen. Old way: grep, dashboards, code archaeology, hope. New way: `/gstack-investigate` reads the error, traces the code path, checks git blame, narrows to root cause, proposes fix with rollback.
- **Real Anecdote:** "I maintain Koo (baby tracking app). One night, it went down. Supabase auth was failing. I ran investigate. Claude read 30 files, found the breaking change was in my last deploy (forgot to set an env var), proposed the fix, and I verified it in 3 minutes instead of 45 minutes of context-gathering."
- **Human-in-the-Loop:** For oncall, you WANT the human in the loop. Use `default` permission mode. Claude proposes each step, you approve. At 3 AM, you need to understand what's happening, not just delegate.
- **Post-Incident:** `/gstack-retro` generates the full retrospective (timeline, root cause, action items, prevention). What used to take 1 hour of writing takes 5 minutes of review.
- **One Thing to Remember:** "AI doesn't replace your oncall judgment. It replaces the 45 minutes of context-gathering so you can make the right call in 5 minutes instead of 50."

---

## 5. DEMO RUNBOOK

### Live Demo Strategy

**DECISION POINT (at 7:15 in timing guide):**
If you are on pace or ahead of time AND you are confident in your internet connection, run the optional gstack install demo. If you are behind schedule or nervous about connection, SKIP and show the screenshot instead.

### Optional Live Demo: Installing a New Tool (60 seconds, 7:15-8:15)

**Setup (before talk):**
- Have a fresh Claude Code session open in a terminal window (not visible to audience until you transition)
- Keep this terminal window in the corner of your screen, hidden behind slides
- When ready to demo, use keyboard shortcut (Cmd+Tab or similar) to bring terminal forward
- Pre-type the command you'll use (or have it in your clipboard ready to paste)

**The Demo Flow:**
1. **Slide 7 is showing**: "The New Way"
2. Say: "Let me show you this in real time. I'm going to ask Claude to help me set up a tool I've never used before."
3. **Switch to terminal** (Cmd+Tab)
4. **Show the prompt you're about to type:** "Watch this..."
5. **Type the question** (or paste if pre-copied):
   ```
   Can you help me install [tool name] and show me what it does?
   For example: Can you help me install prettier and explain its key commands?
   ```
6. **Wait for Claude's response** (it will output in stream)
7. **Talk through what it's doing:** "Claude is exploring the tool, reading the docs, checking my system for dependencies..."
8. **Show key output:** When Claude finishes, highlight:
   - What it discovered
   - What it installed
   - What configuration changes it made
9. **Make the point:** "Fifteen minutes of YouTube and Stack Overflow, compressed into one conversation."
10. **Switch back to slides** and continue

**Fallback if Demo Fails (Recommended):**
- If Claude Code takes >30 seconds to respond, ABORT
- Say: "Let me show you what this output looks like..." and jump to Slide 8 (screenshot of actual gstack install)
- Never wait more than 60 seconds on stage for a tool to respond — it kills momentum

**Fallback Commands (Pre-Tested):**
- If gstack install demo doesn't work, ask Claude something simpler:
  - "What are the top 5 things I should know about tmux plugins?"
  - "Can you explain what Catppuccin theme is and why I'd use it?"
- These will respond faster and still demonstrate AI exploration in real time

---

### Live Demo: Agent Teams (Optional, 23:30-24:30)

**Setup (before talk):**
- Have the actual tmux session running in the background (started 45 minutes before talk)
- Agents should be actively working (not stalled waiting for input)
- Have a screenshot of the Agent Teams session as Slide 19 backup if live session fails

**The Demo Flow:**
1. **Slide 19 is showing**: The live tmux screenshot
2. Say: "This isn't a recording. This is happening right now."
3. **PAUSE for 8 seconds and let them stare**
4. Point at the terminal and walk through what each pane is doing:
   - Pane 1: Feature A (code changes visible, progress shown)
   - Pane 2: Feature B (exploring files, asking questions)
   - Pane 3: Bug C (error logs, proposing fix)
5. Say: "Three parallel conversations. Three different projects. No hand-holding from me. They're reading the codebase, understanding the context, and moving forward."
6. **Do NOT try to explain details of what they're doing in depth** — just show it's alive and working
7. Move to next slide

**Fallback if Session Stalls:**
- Agents sometimes wait for input or get stuck
- If this happens, just say: "The agents are thinking through this one..." and move to next slide
- Show the screenshot as a static visualization instead
- Don't try to "fix it" on stage

---

### No Live Demos: All-Screenshot Strategy (Safer)

If you decide not to do live demos (totally fine — many excellent talks don't):
- Slides 8, 19, 21, 30 are your demo replacements
- They show REAL output from real sessions, not mockups
- Talk through them like you would a live demo ("Here's what this output looks like...")
- You save 3+ minutes of potential technical issues
- Audiences don't know the difference between live and screenshot

---

## 6. ENERGY & PACING NOTES

### Where to Slow Down (Emphasis Points)

1. **0:40 | The Reveal (Agent Teams tmux)**
   - Slow to a halt
   - Let the image speak
   - Pause for 8-10 seconds of pure silence
   - This is WOW moment #1

2. **5:00-6:00 | gstack Story (Act 1)**
   - Slow down on the contrast
   - "Instead of 2 hours of YouTube and tutorials... [PAUSE] ...you have one conversation."
   - Let that sink in

3. **10:30-12:00 | Cortis Problem Statement (Act 2)**
   - Shift from fast to deliberate
   - "You have an idea. [PAUSE] It's cool. [PAUSE] But where do you even start?"
   - Vulnerability moment

4. **14:00-14:30 | Office Hours Forcing Questions**
   - One question at a time
   - Pause after each question so the audience sits with it
   - Don't rush through the 6 questions

5. **16:00 | Key Insight (Act 2)**
   - Slide 15: "AI doesn't replace judgment. It structures it."
   - Say this line slowly
   - Pause before and after

6. **24:00-26:30 | Permission Spectrum (Act 3)**
   - Slow down on the permission model
   - Show the thinking: "Not all work is equal. Different work needs different trust."
   - Walk through 4 modes deliberately

7. **26:30 | You Are the CEO**
   - Slow down
   - "Your job isn't to write every line."
   - Pause for emphasis

8. **33:00 | Speed Without Safety**
   - Key insight slide
   - Deliver slowly
   - "Speed without safety is just chaos."

9. **42:00-44:45 | The Close (Final 3 Minutes)**
   - Everything slows down
   - Deliver the final line with maximum gravitas
   - "I maintain six products solo. Not because I'm a 10x engineer. Because I have a 10x workflow. And now you do too."
   - HOLD SILENCE for 3 seconds after this line

---

### Where to Speed Up (Building Momentum)

1. **3:00-5:00 | Act 1 Setup**
   - Move fast through the "old way" contrast
   - Show the pain point quickly, move to solution
   - Momentum builder for Act 1

2. **6:00-7:00 | gstack Install Walkthrough**
   - Show features quickly
   - Build excitement about what 36 commands can do
   - "Instant expertise"

3. **20:30-22:00 | Multiple Approaches (Act 3)**
   - Zoom through the three approaches
   - Don't deep-dive into each
   - Show range of options quickly

4. **22:30-24:00 | Agent Teams Running**
   - After the pause on the screenshot, move quickly to explain what's happening
   - "Three parallel conversations..."
   - Maintain energy momentum

5. **30:30-35:00 | Code Review & Ship Pipeline**
   - Fast-forward through the spec review details
   - Build momentum toward ship
   - "Review → QA → Ship → Guardrails"

---

### Energy Curve (How to Manage Your Presence)

```
                    ENERGY LEVEL

                        ^
                        |
                   Act 3 PEAK
                   (24:00)
                        |
                    Act 1     Act 2
                  (energetic) (thinking)
                   |              |
               ----+-----+--------+--------+----
               HOOK   ACT1   ACT2   ACT3   ACT4
               High   High   Med    PEAK   High
                0:00   3:00  10:00  20:00  30:00

                        Act 5   CLOSE
                        (calm)  (lift)
                        |         |
               --------+-----+----+--
              (37:00) (42:00) (44:45)
              Med     Low→High  High

```

### Energy Tips

- **Opening (0:00-0:40):** Stand tall, make eye contact, speak with confidence. This sets the tone.
- **Act 1 (3:00-10:00):** High energy. You're telling a relatable story. Lean in.
- **Act 2 (10:00-20:00):** Drop the energy slightly. You're asking them to think. Slower cadence, deliberate pacing. You might pace side to side (not too much pacing, just enough to show thoughtfulness).
- **Act 3 (20:00-30:00):** Peak energy. This is the exciting part. Stand center stage. Use hand gestures. Let your voice rise slightly. Show enthusiasm about parallel agents.
- **Act 4 (30:00-37:00):** Maintain high energy. You're explaining something technical but important. Show conviction in the safety argument.
- **Act 5 (37:00-42:00):** Drop energy again. This is relatable, real, urgent. You're talking about 3 AM. Lower voice slightly. Show empathy.
- **Close (42:00-45:00):** Build energy back up. You're inspiring them. Final line is delivered with maximum conviction. Then STOP and let applause come.

---

### Pacing Adjustments (How to Stay on Time)

**If you're ahead of schedule (at 20:00, you're on pace for 40:00 finish):**
- Add depth to Act 4 review details
- Spend more time explaining the permission spectrum
- Take longer pauses after key insights
- You have 5 minutes of buffer

**If you're behind schedule (at 20:00, you're on pace for 50:00 finish):**
- Skip the optional live demo (use screenshot instead)
- Compress Act 2 beats (cover 1 and 3, skip 2)
- Reduce Act 3 permission spectrum detail (just do 2 modes instead of 4)
- Shorten Act 5 (focus on investigate, skip retro details)
- Move straight to closing line if you hit 42:00

**Stage Manager Signals:**
- Watch for a hand signal from stage manager
- 5-minute warning: finish Act 5 early and go straight to close
- 1-minute warning: JUMP to final line and close immediately
- When you see "time's up" signal, STOP and deliver this condensed final line:
  ```
  "I maintain six products solo because I have a 10x workflow. Now you do too. Let's chat about this in the hallway."
  ```

---

## 7. EXPANDED Q&A PREP

### 15+ Likely Questions with Detailed Answers

**Organize by category: Cost/Tooling, Code Quality, Security, Team Adoption, Skeptics**

---

### COST & TOOLING (Expected objections about price)

**Q1: "How much does this actually cost?"**

A (Friendly): "About $100/month total. Claude Pro is $20/month. If you're doing heavy usage, Claude Max is $100/month. gstack is free (MIT license). Supabase is free tier up to reasonable scale. Expo is free. tmux is free. So your biggest cost is the Claude subscription, and you get $200+ back in time savings weekly."

A (Expanded): "I spend about $100/month on Claude (usually the Max plan for the extended context). That's $1,200/year. I save 20+ hours per week on maintenance and shipping, which at an average dev salary of $150k/year, that's $58,000 of time savings per year. ROI is clear."

A (If Skeptical): "I get it — another subscription. But think about it this way: you're already spending money on tools (GitHub, Vercel, database hosting, monitoring). This one is the highest leverage investment I make. It directly reduces the number of hours I work."

---

**Q2: "What if Claude goes down or changes their pricing?"**

A (Honest): "It's a real risk. I stay plugged into the community and watch announcements. If Claude pricing becomes untenable, there are alternatives (GPT-4, Gemini, open-source models). The workflow itself isn't Claude-specific — it's about having an AI agent in your loop. The tools are tools."

A (Reassurance): "That said, I think Claude's pricing is sustainable because of the value it delivers. $20/month for a tool that saves 20 hours/week of my time? That's a bargain. Anthropic knows this, and they have incentive to keep it affordable."

---

**Q3: "Do I need to learn tmux and all these config files?"**

A (Honest): "No. tmux is useful for managing parallel sessions, but it's not required. You can run multiple Claude Code sessions in separate terminal windows. The config files (Catppuccin, TPM) are nice-to-haves. The core workflow works with vanilla terminal + Claude Code."

A (Practical): "If you're just starting, install Claude Code and gstack first. Use them for a month. Once you're comfortable, then optimize your terminal environment. One thing at a time."

---

**Q4: "What about using other tools like Cursor or Windsurf?"**

A (Honest): "I use Claude Code specifically because I like the workflow and the context window (1M tokens). Cursor and Windsurf are great tools. They have different models and different feature sets. The important thing is: you should use whatever tool lets you work fastest. This talk uses Claude, but the principles apply to any AI coding agent."

A (Specificity): "Claude Code's strength is the Agent Teams experimental feature and the extended context. Those matter for my workflow. Your mileage may vary."

---

### CODE QUALITY (Will AI code be bad?)

**Q5: "Won't AI-generated code be lower quality? How do you avoid technical debt?"**

A (Direct): "Counter-intuitive answer: the code quality is higher than before. Because of the review pipeline. Before, I'd ship code that passed my smell test. Now, every PR goes through five parallel specialist reviews (security, performance, testing, maintainability, red team). Coverage is better. Edge cases are caught before they're live."

A (Real Example): "System Design Arcade has 92 unit tests. That's not despite using AI — that's because of it. The testing reviewer kept finding gaps. I would have shipped with maybe 30 tests. Now it has 3x coverage, and it's more maintainable as a result."

A (Nuance): "That said, I still write and understand every line of code. AI writes the implementation, but I write the architecture and tests. I review every PR before it ships. The guardrails are there."

---

**Q6: "How do you avoid becoming dependent on AI?"**

A (Reframe): "This is like asking if using an IDE makes you dependent on autocomplete. No — it makes you faster. I could write code in vim without any helper. But why would I? I still understand every line. AI handles the mechanical parts (boilerplate, test generation, code review checklists). The architecture, the product decisions, the judgment — that's still me."

A (Practice): "I actually make a point to understand what Claude is doing. When it generates code, I read it. When it proposes a refactor, I verify the logic before shipping. I'm not blindly trusting."

A (Evidence): "I can deploy and oncall on any of these six products because I understand them deeply. If I didn't understand the code, I couldn't debug production issues. I can."

---

**Q7: "What if an AI agent writes vulnerable code?"**

A (Direct): "That's exactly what the security reviewer is for. `/gstack-review` spawns a dedicated security specialist that checks OWASP top 10, STRIDE modeling, common vulnerabilities. For critical code, I also run `/gstack-cso` which does a full security audit."

A (Real Example): "Early on, I had an agent suggest an SQL query that was vulnerable to injection. The security reviewer caught it immediately. That's the system working as intended."

A (Human Check): "At the end of the day, I'm still shipping code. I own it. If something is wrong, it's my responsibility. The AI tools just raise the bar for what 'good' looks like."

---

**Q8: "How do you handle code reviews when you have six products?"**

A (Workflow): "The `/gstack-review` pipeline runs automatically. By the time I'm looking at a PR, the obvious issues are already fixed or flagged. My review is higher-level: does this solve the right problem? Does it fit the architecture? Are there any edge cases the specialist reviews missed?"

A (Scale): "Honestly, this is why I can maintain six products solo. With just human review, I couldn't. With parallel specialist reviews, it's manageable."

---

### SECURITY (Privacy & data concerns)

**Q9: "What about sending my proprietary code to Anthropic's servers?"**

A (Direct): "Valid concern. Here's what happens: when you use Claude Code with the API, your code context is sent to Anthropic's servers (they need to see it to give you answers). Anthropic has a strict privacy policy — they don't train on API usage by default."

A (Options): "If you need even stronger guarantees, Claude Code has a `--bare` flag that limits what gets sent to Anthropic. You can also use a local inference model (open-source Claude alternative) if you have the compute."

A (Real): "For my public projects (GitHub public repos), this isn't a concern. For proprietary code at my previous job (AWS, DoorDash), I would have been more careful. Choose the permission level that matches your risk tolerance."

---

**Q10: "Can AI agents accidentally expose secrets in my code?"**

A (Yes, then mitigation): "Yes, it's possible. That's why you should: (a) never paste secrets into Claude, (b) use environment variables for all secrets, (c) don't ask AI to 'complete' code that has secrets visible, (d) run secrets scanning as part of your review pipeline."

A (gstack): "gstack has a built-in secret detection as part of the security review. It flags things that look like API keys, credentials, PII. Not perfect, but a good safety net."

A (Process): "The real mitigation is process. Don't ask AI to work with secrets directly. Have a human handle secrets. Everything else can be AI-assisted."

---

### TEAM ADOPTION (How to use this at work?)

**Q11: "Can you use this in a team environment?"**

A (Yes): "Absolutely. gstack has a team mode. When you run `./setup --team`, every developer on the team gets access to the same 36 skills. All the `/gstack-*` commands work the same. The workflow scales."

A (More): "Agent Teams can coordinate across a shared codebase using git worktrees. Multiple developers can have multiple AI agents working on different features in the same repo without stepping on each other."

A (Practice): "At a team level, I'd recommend: (a) agree on which commands are auto-execute (autonomy) and which require human review (safety), (b) use shared git worktrees to avoid conflicts, (c) have a review checklist that all PRs go through (human + AI)."

---

**Q12: "How would you pitch this to a skeptical manager?"**

A (Business): "Frame it as shipping velocity + code quality. 'We can build 2x faster and have better test coverage. That means shipping value faster and fewer production issues. Here's the cost: $20/dev/month. Here's the return: 10+ hours/dev/week saved.'"

A (Proof): "Start with a small team. Give them Claude Code + gstack for 1 month. Measure: lines of code shipped, bugs found in production, time-to-ship. If the metrics improve (they will), the business case sells itself."

A (Reframe): "Some managers worry about quality. Flip it: 'This tool lets us do MORE code review, not less. Every PR gets 5 specialist reviews. That's better quality assurance than we have now.'"

---

**Q13: "What about hiring and training junior engineers?"**

A (Honest): "This is a trade-off. If your goal is to develop junior engineers' deep expertise, they need to struggle sometimes. AI assistance can short-circuit that learning. So I'd be thoughtful about how much autonomy to give a junior."

A (Different): "That said, AI is amazing for onboarding. A junior can run `/office-hours` and `/autoplan` to understand the system architecture in 30 minutes instead of 3 days. They can run `/review` to learn what good code looks like from the specialist reviews. It's a different kind of learning."

A (Recommendation): "For a junior: start with read-only permission modes (plan-only). Let them propose changes, see the AI review, and learn from it. Gradually increase autonomy as they prove understanding."

---

### SKEPTICS (Hostile or doubting questions)

**Q14: "Isn't this just hype? Will AI actually save me time?"**

A (Evidence): "Fair question. My evidence: I maintain 6 products solo and shipped 2 new ones in the last 6 months. That's not possible without force-multipliers. The time savings are real."

A (Specific): "Concrete examples: what used to take me 2 hours (learning a new tool) now takes 15 minutes. What used to take 1 hour (code review) now takes 20 minutes (my job is to verify the specialist review, not do it myself). What used to take 3 days (architecture planning) now takes 1 day."

A (Skepticism Check): "That said, if you try this and don't see time savings in your specific context, that's fair. This workflow isn't magic — it's a system. It works if the work you do fits the system."

---

**Q15: "What happens when AI gets smarter? Won't your workflow become obsolete?"**

A (Reframe): "Actually, the opposite. As AI gets smarter, the workflow compounds. Better planning tools → better architecture. Better code review → fewer bugs. Better agents → more parallelism."

A (Future): "In 3-5 years, AI agents will be good enough to handle oncall without human oversight. Today, I'm human-in-the-loop. Tomorrow, I might just set the policy and let AI enforce it. The tools evolve, but the system remains."

A (Opportunity): "Instead of worrying about obsolescence, think about this: what if you started building this system today? In 3 years, you'd be so far ahead that the improvements would just be icing."

---

**Q16: "Isn't this just code generation? We tried that before and it was a mess."**

A (Distinction): "This is NOT Copilot-style autocomplete. It's not 'suggest the next line of code.' It's structured workflow. Plan → Build → Review → Ship. Each step has guardrails and human oversight. It's orchestration, not just generation."

A (Proof): "Show them the actual output (Slides 14, 23, 30, 32). These aren't random AI suggestions. They're structured reviews, detailed plans, and actionable findings. The difference is night-and-day from 'write a function that does X.'"

A (Maturity): "Copilot was early-stage. The tooling is much better now. Structured workflows, permission modes, specialist agents, context management — these are designed to avoid the mess of raw code generation."

---

### BONUS QUESTIONS (Less likely but good to prep)

**Q17: "What's the learning curve? How long before I'm productive?"**

A: "Honest answer: 2-3 days to be useful, 1-2 weeks to be fluent. Day 1: install Claude Code and gstack, try `/office-hours` on your biggest problem. Day 2: run `/review` on an existing PR, see the feedback quality. Day 3: set up Agent Teams if you want parallel sessions. By week 2, you're using it daily and seeing returns."

---

**Q18: "What's your biggest regret about this workflow?"**

A: "I wish I'd started earlier. I spent years coding alone when I could have been using AI as a thought partner. Also, I underestimated how much the permission model matters — spent the first month with too much autonomy and had to reel it in."

---

**Q19: "How do you stay updated with rapid changes in AI tooling?"**

A: "I follow Anthropic announcements, check the gstack changelog weekly, and have a dedicated time (Friday afternoon) where I experiment with new features. Most weeks there's nothing new worth adopting. Some weeks (like Agent Teams launch), there is. Having a learning cadence matters."

---

### Q&A Delivery Tips

- **Restate the question** before answering (shows you listened, gives you thinking time)
- **Answer in 30-60 seconds** — if you're going longer, cut it short with "happy to chat about this after"
- **Admit uncertainty** when appropriate ("That's a good question, I haven't run into that yet...")
- **Redirect if needed** ("That's more of an Anthropic roadmap question, but the current tooling does X...")
- **Have a watching mechanism** — if someone asks something technical and you're short on time, say "great question, let's grab coffee after and dig into this"

---

## 8. AUDIENCE-SPECIFIC ANGLES

### How to Adjust the Talk for Different Audiences

#### For Startup Developers
**Adjust emphasis:**
- Lead with the 30-minute challenge (they love speed)
- Focus on Act 3 (building fast) and Act 4 (shipping without QA team)
- Highlight: cost ($100/month), time savings (20 hrs/week), ability to ship 6 products solo
- Downplay: enterprise guardrails, team coordination

**Key line to emphasize:**
"Your competitive advantage as a startup is shipping 10x faster than the incumbents. This workflow is how you do it."

**Question to watch for:**
"Can we use this with our existing CI/CD pipeline?" — Answer with Act 4 details about gstack-ship and integrations.

---

#### For Enterprise Engineers
**Adjust emphasis:**
- Lead with Act 2 (planning at scale) and Act 4 (review pipeline)
- Focus on code quality, security reviews, compliance
- Highlight: parallel specialist reviews, guardrails (careful, freeze, cso), human-in-the-loop
- Downplay: shipping 6 products solo, moving fast as the primary goal

**Key line to emphasize:**
"Speed without safety is just chaos. The right guardrails let you go faster because you're not anxious about breaking things."

**Question to watch for:**
"How does this work with our security review process?" — Answer by positioning /gstack-cso and /gstack-review as pre-human-review, raising the bar for what reaches your security team.

---

#### For Engineering Managers
**Adjust emphasis:**
- Lead with Act 1 (learning faster) and Act 5 (oncall experience)
- Focus on team adoption (Q12 in Q&A), developer satisfaction, retention
- Highlight: junior engineer onboarding, less 3 AM pages, predictable shipping
- Downplay: personal productivity hacks

**Key line to emphasize:**
"You are the CEO of an AI engineering team. Your job isn't to write every line — it's to set the right constraints, assign the right tasks, and review the output."

**Specific angle:**
"If you implement this at your company: (a) developers ship 2-3x faster, (b) code quality goes up due to specialist reviews, (c) oncall gets easier (human judgment, AI context gathering). That's retention and happiness."

---

#### For Students / Early Career
**Adjust emphasis:**
- Lead with Act 1 (learning) and Act 2 (planning)
- Focus on learning velocity and building projects quickly
- Highlight: free tools (gstack, tmux, Expo), how AI accelerates learning
- Downplay: production guardrails, complex permission modes

**Key line to emphasize:**
"Stop learning tools in isolation. Let AI explore, install, configure, and teach you — all in one flow. Your job is to ask the right questions."

**Specific angle:**
"You can now learn a new stack in 30 minutes, not 2 weeks. That means you can explore more technologies, build more projects, and find what you love faster."

**Caution:**
Students might think this is "AI doing the work for them." Correct that misconception: "AI is a learning partner, not a replacement. You still need to understand the code, architecture, and design. This just compresses the mechanical parts."

---

#### For CTOs / Technical Leaders
**Adjust emphasis:**
- Lead with Act 2 (planning for scale) and entire delivery pipeline
- Focus on: consistency across teams, knowledge transfer, reducing key-person risk
- Highlight: team mode for gstack, Agent Teams coordination, guardrails
- Downplay: personal workflows, solo shipping

**Key line to emphasize:**
"If your best engineer is doing things that only they understand, you're at risk. This workflow makes the workflow repeatable and teachable."

**Specific angle:**
"Implement this across your engineering team: everyone uses the same skills (/gstack-*), everyone follows the same review pipeline, everyone benefits from specialist reviews. It raises your baseline quality and reduces hero culture."

---

## 9. COMMON PITFALLS (What Can Go Wrong in Tech Talks)

### Pitfall 1: Live Demo Fails
**What happens:** Claude Code times out, API call fails, terminal freezes, projector doesn't show output clearly.

**Prevention:**
- Have a screenshot of the same demo as Slide 8/19/30 backup
- Practice the demo on stage equipment before talk (different projector, different WiFi)
- Set a 30-second timeout in your head — if it's not responding by then, abort to screenshot

**If it happens (Recover):**
- Say: "Let me show you what this output looks like" and click to the screenshot slide
- Don't dwell on it. "Sometimes internet is slow. Here's the actual result from when I did this earlier..."
- Move on. Audiences are forgiving.

---

### Pitfall 2: Timing Runs Long
**What happens:** You're at 30:00 but only 20 minutes have passed. You're on pace to go 60+ minutes.

**Prevention:**
- Rehearse full talk with a timer (ask a friend to time you)
- Know which sections can be compressed (Act 1, Act 5)
- Practice skipping the optional live demo

**If it happens (Recover):**
- Watch for the 5-minute signal from stage manager
- If you get it early, compress Act 5 (jump the intro, go straight to investigate story)
- If you get "1 minute," jump straight to final line
- Don't try to squeeze everything in — finish strong, not rushed

---

### Pitfall 3: Audience Looks Confused (Lost on Technical Details)
**What happens:** You mention gstack-cso or STRIDE modeling and see blank stares.

**Prevention:**
- Remember: not everyone knows these tools. Don't assume baseline knowledge.
- When introducing a tool/concept, define it once: "gstack is a pack of 36 AI skills written by Garry Tan..."

**If it happens (Recover):**
- Pause and say: "That's `/gstack-cso` — a comprehensive security check. You don't need to memorize the command names. The point is: specialist reviews are running in parallel."
- Adjust jargon for that audience level and move on
- After talk, detailed questions can be answered in hallway

---

### Pitfall 4: Someone Asks a Hostile Question
**What happens:** "This is just hype" or "AI-generated code is always garbage" or "You're just making this up."

**Prevention:**
- Expect this. Skepticism is good. Have your Q&A answers ready.
- Reframe as curiosity, not hostility

**If it happens (Recover):**
- Don't get defensive
- Restate the question: "So you're asking whether the time savings are real, or whether it's just marketing?"
- Answer directly with evidence (actual numbers, portfolio examples)
- End with: "Fair point. If this doesn't work for you, that's OK. But it's working for me and my users who benefit from faster shipping."
- Move to next question

---

### Pitfall 5: You Blank on a Story or Stat
**What happens:** You forget the exact number ("It takes 3 hours or 2 hours? I forget...") or you can't remember the Cortis story.

**Prevention:**
- Write key numbers on your notes (time savings, lines of code, number of tests)
- Have anecdotes written out in shorthand on note cards

**If it happens (Recover):**
- Say: "I want to make sure I get the stat right..." and pause
- If it's not critical, move on: "The exact number doesn't matter — the point is it's significantly faster"
- If it's critical, admit it: "I'm blanking on the exact percentage, but let's say 10x faster to be conservative" and move on
- Audiences don't mind small mental lapses — they happen to everyone

---

### Pitfall 6: Projector/Audio Fails
**What happens:** Projector goes down, mic cuts out, slides won't advance, screen goes black.

**Prevention:**
- Test all equipment 1 hour before talk
- Have a backup mic (handheld in pocket)
- Have slides on a USB stick AND on your laptop AND projected
- Know how to advance slides with keyboard (spacebar or arrow keys), not just clicker

**If it happens (Recover):**
- Don't panic. Pause. Alert stage tech.
- Keep talking. Your voice is the talk, the slides are supporting material
- "While they fix that, let me tell you about gstack..." (keep delivering content)
- If projector is down for >2 minutes, ask organizer: do we continue with audio-only or wait?
- You can deliver 90% of this talk with just your voice. Let slides be the icing.

---

### Pitfall 7: You Run Out of Energy
**What happens:** By Act 5, your voice is tired, you're speaking monotone, energy is dragging.

**Prevention:**
- Warm up voice before talk (hum scale, say opening line)
- Drink water between acts (have bottle stage left)
- Take strategic pauses to reset breathing
- Move around stage (don't stand in one spot for entire 45 minutes)

**If it happens (Recover):**
- Pause and take a sip of water
- Shift your position on stage (move stage left, then stage right)
- Deliberately lower your voice for Act 5 (it's supposed to be lower energy anyway)
- On closing act, lift energy back up for final punch

---

### Pitfall 8: Someone Asks "Can I use this on Windows?"
**What happens:** You're macOS-centric in the talk. Windows user asks about compatibility.

**Prevention:**
- Mention compatibility in opening: "I use macOS, but the tools work on Linux and Windows too"
- Have a quick answer about WSL or Git Bash

**If it happens (Recover):**
- "Great question. Claude Code works on Windows. gstack works on Windows. tmux is less common on Windows, but you can use it via WSL. The workflow is the same, the setup might vary slightly."
- Don't deep-dive into Windows setup on stage — "happy to help after the talk"

---

### Pitfall 9: You Mispronounce a Name or Tool
**What happens:** You say "Supabase" wrong or butcher "Garry Tan."

**Prevention:**
- Practice tool names and names out loud before talk
- Supabase = "SOUP-uh-base" (not "Super-base")
- Garry = "GARY" (not "GARR-ee")

**If it happens (Recover):**
- Keep going. Most people won't notice. If someone corrects you, say "thanks, I'll remember that next time" and move on.

---

### Pitfall 10: Slides Show Wrong Content
**What happens:** A screenshot of code is cut off, a demo output is too small to read from the back, a diagram is blurry.

**Prevention:**
- Test every slide on the actual projector
- Font size >16pt for any code/text
- Use high-resolution screenshots (not tiny zoomed-out views)
- Color contrast: dark text on light, light text on dark (not medium gray on medium blue)

**If it happens (Recover):**
- If slide is important, describe it: "This slide shows the agent teams tmux session. Three panes, each running Claude Code in parallel..."
- If slide is decoration, skip it
- Move forward. Don't spend talk time trying to fix slide readability.

---

## 10. 30-SECOND, 2-MINUTE, AND 5-MINUTE VERSIONS

### Elevator Pitch (30 seconds)
Use this when you meet someone who asks "What was your talk about?"

"I ship 10x faster by using AI as an engineering team instead of just coding alone. I have a system: Claude Code for planning and building, gstack for structured workflows, Agent Teams for parallel development, specialist AI code reviews. In 30 minutes, you can set this up on your own projects. It's not theory — I maintain 6 products solo using this workflow."

**Delivery:** Confident, conversational, no slides needed. 1-2 minutes if they want details.

---

### Networking Version (2 minutes)
Use this when someone says "Tell me more about your talk" and has 2 minutes before the next session.

"Here's the workflow: You have an idea. Run `/office-hours` — a forcing function that challenges your assumptions. Then `/autoplan` — which does architecture review, design review, and engineering review in parallel, giving you a complete plan in 15 minutes.

Then you build. I use Claude Code + gstack (36 AI skills). For parallel work, I use Agent Teams — multiple Claude Code sessions running simultaneously across different features. Each agent gets its own context window, its own git worktree.

Then review. `/gstack-review` spawns five parallel specialists: security, performance, testing, maintainability, and red team. By the time you're looking at the PR, the obvious issues are fixed.

The whole thing compounds. You're faster at planning, faster at building, faster at reviewing. That's how one engineer maintains six products."

**Delivery:** Clear, story-driven, use hand gestures to show the flow.

---

### Extended Pitch (5 minutes)
Use this when someone wants the real details and has grabbed you for coffee.

"I built six products simultaneously as a solo founder: Cortis (meeting intelligence), Broadside (social media scheduler), System Design Arcade (learning platform), Koo (baby tracker), Tossup (cricket auction), Zeroshot (Python game).

The secret isn't that I work harder. It's that I stopped coding alone.

Here's the system:

**Learning:** Used to spend 2 hours learning a new tool (YouTube, Stack Overflow, trial/error). Now: 15 minutes. I ask Claude to explore the tool, read the docs, install it, configure it, teach me. Instant expertise.

**Planning:** I run `/office-hours` — six forcing questions that validate the idea. Then `/autoplan` chains four reviews in parallel (CEO, Design, Eng, DX). In 20 minutes, I have a complete architecture. That's where AI gives maximum leverage.

**Building:** Multiple Claude Code sessions in parallel. Feature A, Feature B, Bug C all happening simultaneously. I'm the CEO — I assign work, review output. Not writing every line.

**Reviewing:** The `/gstack-review` command spawns five specialist agents that review code simultaneously. Security, performance, testing, maintainability, red team. Each specialist gets fresh context. When I review the PR, the easy issues are already fixed.

**Shipping:** `/gstack-ship` runs tests, generates changelog, bumps version, opens PR. One command.

**Oncall:** 3 AM page? `/gstack-investigate` reads the error, traces code, checks git blame, proposes fix with rollback. I approve, not execute blind.

The competitive advantage isn't AI — everyone has access to Claude. It's having a *system* that compounds. Better planning → better architecture. Better review → fewer bugs. Better tools → faster iteration.

I maintain six products solo not because I'm a 10x engineer. Because I have a 10x workflow. Now you do too."

**Delivery:** Conversational, no slides needed. Watch for questions — if they ask something, go deep on that topic. Otherwise, finish with: "You can set this up in 30 minutes. Start with Claude Code and gstack, then experiment with Agent Teams if you want parallel sessions. Happy to send you the resources after."

---

## 11. FINAL REMINDERS (Print These Out)

- [ ] **Arrive 45 minutes early.** Start tmux agents 45 min before talk. Test slides 30 min before. Warm up voice 5 min before.

- [ ] **The opening line is critical.** "Six months ago, I was mass-applying to jobs. Today, I ship more code in a week than most teams ship in a month — across six different products."

- [ ] **WOW moment #1 (0:40):** Agent Teams screenshot. Pause. Silence. Let it speak.

- [ ] **WOW moment #2 (23:30):** Live Agent Teams tmux. Point. Pause. "This is happening right now."

- [ ] **The final line (44:45):** Deliver with conviction. Pause after. "I maintain six products solo. Not because I'm a 10x engineer. Because I have a 10x workflow. And now you do too."

- [ ] **Watch pacing.** If you're behind, skip the optional live demo. If you're ahead, add depth to Act 4 permission spectrum.

- [ ] **If something fails:** Recover with confidence. "Let me show you the actual result" (switch to screenshot). Keep delivering. The talk is good even if the demo breaks.

- [ ] **Q&A:** Restate the question, answer in 30-60 seconds, admit uncertainty when appropriate, redirect if needed.

- [ ] **After the talk:** Be ready for 5-10 minute hallway questions. Have your 30-sec and 2-min versions ready.

- [ ] **Photos:** If organizers want speaker photos, have a few slides ready to pose in front of (Slide 3 with Agent Teams, or final slide with closing line).

---

## QUICK REFERENCE: Time Anchors

```
0:00 ─ HOOK (3 min) ─────────── Opening + Agenda
3:00 ─ ACT 1 (7 min) ─────────── Learning new tools
10:00 ─ ACT 2 (10 min) ────────── Planning (Cortis story)
20:00 ─ ACT 3 (10 min) ────────── Building (Agent Teams)
30:00 ─ ACT 4 (7 min) ─────────── Review & Ship
37:00 ─ ACT 5 (5 min) ─────────── Oncall
42:00 ─ CLOSE (3 min) ────────── Final line + Applause
45:00 ─ [END] ──────────────────
```

**If ahead of schedule:** Add to Act 2 or Act 4 details.
**If behind schedule:** Skip Act 1 live demo, compress Act 5, jump to final line at 42:00.

---

**Good luck. You've got this. Ship it.**
