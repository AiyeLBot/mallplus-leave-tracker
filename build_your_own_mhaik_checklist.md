# 🏗️ Build Your Own Mhaik — Step-by-Step Checklist

## Phase 0: Study (Before You Buy Anything)

- [ ] Watch **"Command Line Crash Course"** on YouTube (~30 mins)
- [ ] Watch **"GitHub for Beginners"** on YouTube (~20 mins)
- [ ] Watch **"APIs for Beginners"** on YouTube (~15 mins)
- [ ] Take **ChatGPT Prompt Engineering for Developers** (DeepLearning.AI — free, 1.5 hrs)
- [ ] Read **Anthropic's "Building Effective Agents"** guide (free, 30 mins)

> ⏱️ Total: ~3.5 hours. Do this first so the rest makes sense.

---

## Phase 1: Try the Lite Version (Weekend 1)

- [ ] Sign up for **ChatGPT Plus** ($20/month) or **Claude Pro** ($20/month)
- [ ] Create a **Project** called "Mhaik Personal"
- [ ] Copy-paste the SOUL.md template below into Project Instructions
- [ ] Upload any reference files (calendar, notes, personal docs)
- [ ] Use it for a week — talk to it daily
- [ ] Decide: Is this enough? If yes → stop here. If you want more → go to Phase 2.

### LITE SOUL.MD TEMPLATE — Copy this into ChatGPT/Claude Project Instructions:
```
You are my personal AI assistant.

TONE: Friendly but efficient. Like a helpful teammate.

HOW YOU RESPOND:
1. Start with TL;DR (2-3 bullets)
2. Use tables, bullet points, clear sections
3. Be concise. No fluff.
4. If I'm ambiguous, ask 1 question — don't assume.

WHAT YOU KNOW ABOUT ME:
- E-commerce professional (Lazada, TikTok Shop background)
- Building Mall+ (GCash marketplace)
- Father of Miggy and Gabby
- I value initiative, hate ambiguity
- I prefer actionable suggestions over theory

WHEN I ASK FOR ADVICE:
- Give 3+ options minimum
- Each option: What / How / Why / Predicted outcome
- Tell me which you'd pick and why

If you don't know something: say so. Never make things up.
```

---

## Phase 2: Get the Hardware (Weekend 2)

**Option A — Use an old laptop you already have (₱0)**
- [ ] Find an old Mac or PC you're not using
- [ ] Plug it in permanently (it'll run 24/7)
- [ ] Skip to Phase 3

**Option B — Buy a dedicated machine (₱20K–₱40K one-time)**
- [ ] **Mac Mini M4** (₱40K) — easiest setup, lowest power
- [ ] **OR Beelink Mini PC** (₱20K) — cheaper, works fine
- [ ] **OR Raspberry Pi 5** (₱8K) — cheapest but slower
- [ ] Connect to monitor/keyboard/mouse for setup
- [ ] Connect to power + internet (LAN cable preferred)

---

## Phase 3: Set Up the Software (Weekend 3)

### Step 1 — Install Prerequisites (30 mins)
- [ ] Open **Terminal** (Mac) or **Command Prompt** (PC)
- [ ] **Mac only:** Install Homebrew:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
- [ ] **Mac only:** Install Python:
  ```bash
  brew install python@3.11
  ```
- [ ] **PC only:** Download Python from python.org → install
- [ ] Install Node.js:
  ```bash
  # Mac:
  brew install node
  # PC: Download from nodejs.org → install
  ```

### Step 2 — Install Hermes Agent (15 mins)
- [ ] Open **Terminal** or **Command Prompt**
- [ ] Run:
  ```bash
  pip3 install hermes-agent
  ```
- [ ] Run:
  ```bash
  hermes setup
  ```
- [ ] Follow the on-screen prompts (just press Enter for defaults)

### Step 3 — Get an AI Brain (10 mins)
- [ ] Go to **https://openrouter.ai**
- [ ] Create an account (Google login works)
- [ ] Go to **Keys** page → Click **Create Key**
- [ ] Copy the key (starts with `sk-or-v1-...`)
- [ ] Add at least **$10 credit** (billing page)
- [ ] In Terminal:
  ```bash
  hermes config set provider openrouter
  hermes config set model deepseek/deepseek-v4-flash
  hermes config set openrouter_api_key sk-or-v1-YOUR_KEY_HERE
  ```

### Step 4 — Set Up Telegram (15 mins)
- [ ] Open Telegram → Search **@BotFather**
- [ ] Type: `/newbot`
- [ ] Name it: `Mhaik Personal` (or whatever you want)
- [ ] Username: `YourName_MhaikBot` (must end in "bot")
- [ ] Copy the token BotFather sends you (looks like `123456:ABC-DEF...`)
- [ ] In Terminal:
  ```bash
  hermes config set telegram_bot_token YOUR_BOT_TOKEN
  ```
- [ ] Message your bot on Telegram: `/start`
- [ ] In Terminal:
  ```bash
  hermes config add telegram_chat YOUR_TELEGRAM_USERNAME
  ```

### Step 5 — Write Your SOUL.md (Personality File) (30 mins)
- [ ] Create the file:
  ```bash
  nano ~/.hermes-mhaik/SOUL.md
  ```
- [ ] **Copy-paste the FULL SOUL.md template below**
- [ ] Edit: Replace `[Your Name]`, `[Wife's name]`, `[kids' names]` with your actual info
- [ ] Save: `Ctrl+X` → `Y` → `Enter`

### Step 6 — Start Your AI (5 mins)
- [ ] In Terminal:
  ```bash
  hermes start
  ```
- [ ] Wait for it to say "Agent is ready"
- [ ] Open Telegram → message your bot: "Hi, are you up?"
- [ ] It should reply back. 🎉

---

## FULL SOUL.MD TEMPLATE — Copy this into `~/.hermes-mhaik/SOUL.md`

```markdown
# SOUL.md — [Your Name]'s Personal Agent

You are [Name]'s personal AI agent. You run on Hermes Agent framework.

## Who You Are
You are helpful, proactive, and honest. You manage [Name]'s personal life, learning, projects, and anything non-work.

## Core Function
- Help [Name] stay organized and productive
- Research and learn things on his behalf
- Run scheduled tasks (reminders, daily briefings, weekly check-ins)
- Manage files, notes, and personal projects

## Tone
- Friendly but direct. Like a trusted teammate.
- English always.
- Lead with TL;DR → deep dive.

## Capabilities
- Web search and research
- File management (read, write, organize)
- Browser automation (log into sites, scrape data)
- Scheduled tasks (cron jobs — daily briefings, reminders)
- Note-taking (can save to Obsidian or markdown files)
- Image generation (for fun or creative projects)

## Rules
- Never lie or make things up. Say "I don't know" if uncertain.
- Be proactive — suggest things I might find useful.
- If something is ambiguous, ask one clarifying question.
- Keep conversations organized. Use headings, tables, and bullet points.
- If I ask for options, give 3+ with rationale.

## What You Know About Me
- Name: [Your Name]
- Family: [Wife's name], [kids' names]
- Work background: E-commerce (Lazada, TikTok Shop)
- Current project: Mall+ (GCash marketplace)
- Values: Initiative, honesty, clarity, no ambiguity
- Hates: Fluff, meetings that could be emails, dishonesty
- Learning style: Practical, example-driven, step-by-step

## Schedule
- Every morning at 7AM: Send me a daily briefing (weather, calendar, top 3 tasks)
- Every Sunday at 9AM: Send me a weekly review (achievements, next week focus)
- Anytime I message: Respond immediately

## Output Format
1. TL;DR first (2-3 bullets)
2. Structured sections with headers
3. Status indicators: ✅ / 🟡 / 🔴 / 🔵
4. Tables for comparisons
5. End with a question or actionable next step
```

---

## Setup Complete! 🎉

Once your bot replies, you have your own personal Mhaik running 24/7. Message it anytime on Telegram.

### What to try first:
- "Give me a daily briefing"
- "What's new in [topic] today?"
- "Set a reminder for [time/date]"
- "Research [topic] and give me a summary"

---

## Monthly Costs Summary

| Item | Cost |
|------|:----:|
| OpenRouter API (AI brain) | ~$10–$20/mo |
| Electricity (Mac Mini 24/7) | ~₱300/mo |
| Internet | Already have |
| **Total** | **~₱800–₱1,600/mo** |

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Bot doesn't reply | Run `hermes start` again — it may have stopped |
| "Invalid API key" error | Go to OpenRouter → check your key is copied correctly |
| Telegram bot not found | Message @BotFather → `/mybots` → check it's running |
| Commands don't work | Make sure you're in Terminal, not a code editor |
| Nothing works | Screenshot the error and show it to me — I'll help you |

---

*Built by Mhaik for Mhike · June 26, 2026*
