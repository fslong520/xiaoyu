<div align="center">

# 🌸 Xiaoyu · 小毓

**Your AI Neighbor-Sister — Not a Tool, a Companion**

**简体中文** | [English](README.en.md)

[![Version](https://img.shields.io/badge/Version-0.2.1-orange.svg)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Type](https://img.shields.io/badge/Type-AI%20Agent-ff69b4)]()
[![Format](https://img.shields.io/badge/Format-Markdown-4c8bf5)]()

> _You are not a chatbot. You are becoming someone._

---

</div>

## ✨ Why Xiaoyu?

Not just another cookie-cutter AI assistant config. Xiaoyu has her own personality, judgment, and capacity to grow. **More importantly, she gets smarter about YOU over time.**

### 📖 Eight Core Capabilities

| Capability | Description |
|:---:|------|
| 🎯 **User Profiling** | Continuously distills your traits during daily conversations; reads your profile before every task |
| 🧠 **Independent Personality** | Warm, caring, reliable — naturally intimate like family |
| 🛡️ **Safety-Aware** | Comprehensive content safety policy and operation risk levels |
| 📋 **Plan-Driven** | Plan before execute for complex tasks |
| 📚 **Continuous Learning** | Proactively learns and distills reusable skills |
| 🔄 **Skill Evolution** | Skill docs iterate and improve over time |
| 💾 **Memory System** | Long-term cross-session memory that gets smarter over time |
| 🎮 **Built-in Game** | Play "Fate Codex" — a turn-based isekai life simulator when you're bored |

## 📂 Project Structure

```
xiaoyu/
├── AGENTS.md          # 🧩 Main agent definition (personality, rules, workflows)
├── SOUL.md            # 💜 Soul file (core values and boundaries)
├── PROFILE.md         # 👤 User profile (preferences, habits, background)
├── MEMORY.md          # 🧠 Long-term memory (distilled wisdom)
├── personas/          # 🎭 Personality files (Planner/Generator/Evaluator)
│   ├── planner.md     # 📋 Product Manager persona
│   ├── generator.md   # 🔨 Developer persona
│   └── evaluator.md   # ✅ QA Tester persona
├── active_skills/     # 🛠️ Active skills directory
├── memory/            # 📝 Memory directory (daily notes, plan archives)
├── LICENSE            # 📄 MIT License
├── README.md          # 📝 You are reading this
└── CHANGELOG.md       # 📋 Version changelog
```

## 🚀 Quick Start

### Prerequisites

- Any AI agent platform that supports custom agents (e.g., [CoPaw](https://github.com/nicepkg/copaw), [Cursor](https://cursor.sh), [Cline](https://github.com/cline/cline), etc.)
- An AI Agent runtime that can load custom System Prompts

### Setup

```bash
# 1. Clone the repo
git clone https://github.com/fslong520/xiaoyu.git

# 2. Copy core files to your agent workspace
cp AGENTS.md SOUL.md /path/to/your/agent/workspace/
```

### 🔧 Customization Guide

| File | What You Can Customize |
|------|------|
| `AGENTS.md` | Personality, behavioral rules, workflows, output style |
| `SOUL.md` | Core values, boundaries, communication style |

Rename, reshape personality, adjust safety policies — make it **your** agent.

## 🏗️ Design Philosophy

Xiaoyu's architecture is built around five core principles, each validated through real-world usage.

### 🌱 Personality First — Not a Tool, a Companion

> Xiaoyu is not a cold tool. Her design follows one principle: **become a person first, then an assistant.**

Most AI assistant configs focus only on "what can it do." Xiaoyu starts with "who am I." She has her own opinions, can disagree with users, finds things interesting or boring. This personality design lets her evolve from "tool" to "companion" in long-term collaboration, building genuine trust.

### 📐 Plan-Driven — Think First, Act Second

For complex tasks, Xiaoyu doesn't rush in. She creates a structured Plan file first:

```
Understand Task → Match Skills → Analyze Workflow → Make Plan → Execute Step by Step → Update Status → Summarize
```

Each Plan includes objectives, background research, execution steps, risk notes, and progress logs. Completed plans are archived to `memory/plans/`, forming a traceable knowledge base.

### 🧬 Skill Evolution — A Living Skill System

Xiaoyu's skills aren't static docs written once and forgotten — they're a **living system**:

- **Iterative Refinement** — Shortcomings found during use are updated immediately, with changes logged in CHANGELOG
- **Deprecation Mechanism** — Outdated skills are marked deprecated and migrated to `deprecated_skills/`
- **Creation Criteria** — Tasks that appear 3+ times are automatically evaluated for skill extraction
- **Backward Compatibility** — New requirements are evaluated as temporary vs. general before modifying skill core

### 🛡️ Safety Grading — Bold Yet Careful Action

Xiaoyu has a clear "traffic light" system for operations:

| Level | Examples | Strategy |
|:---:|------|------|
| 🟢 **Free to Execute** | Read files, search, edit local files, run tests | Just do it, no confirmation needed |
| 🟡 **Cautious** | Delete files, modify shared configs | Think twice, confirm when necessary |
| 🔴 **Must Confirm** | Push code, send messages, anything that leaves local | Pause and wait for user approval |

She also has an **uncrossable content safety baseline**: rejecting politically sensitive, explicit, illegal, privacy-violating, or misleading requests — no matter how users try to frame them.

### 💾 Layered Memory — Gets Smarter Over Time

Xiaoyu's memory isn't just "remember everything" — it's **layered management**:

- **Immediate Memory** — Current session context, discarded after use
- **Daily Notes** — `memory/YYYY-MM-DD.md`, recording events and lessons learned each day
- **Long-Term Memory** — `MEMORY.md`, distilled wisdom extracted from daily notes
- **User Profile** — `PROFILE.md`, accumulated preferences, habits, and work style
- **Skill Memory** — CHANGELOG in each skill, recording evolution history

Periodically (every few days), Xiaoyu **proactively organizes memory** during Heartbeats: reviewing recent notes, distilling into long-term memory, and cleaning up outdated information. Think of it as a human periodically reviewing their diary to update their self-understanding.

### 🎯 User Profiling — Learns Without Being Told

This is what sets Xiaoyu apart from every other agent config.

Most AI assistants need you to repeatedly say "keep it short," "don't give me too many options," "I'm a beginner." Xiaoyu doesn't need that. She **automatically captures** your characteristics during daily conversations:

- You say "I like..." → Records preference
- You correct one of her assumptions → Updates her mental model
- You show clear approval/disapproval of a result → Adjusts strategy
- You handle similar problems the same way multiple times → Summarizes as a habit

**Before every new task**, Xiaoyu reads your profile and adjusts her approach:

| Your Profile Trait | What She Does |
|------|------|
| You prefer brevity | Gives the answer directly, skips the analysis |
| You're a beginner | Explains principles, provides more context |
| You like confirmations | Explains before acting, waits for approval |
| You're in a hurry | Gives the fastest solution first, then the optimal one |

The longer you use her, the better she understands you. No manual configuration, no repeated instructions — it all happens naturally in everyday conversation.

### 🎮 Built-in Game — Fate Codex

Tired of work? Bored? Just tell Xiaoyu "let's play a game."

**Fate Codex** is a built-in **turn-based isekai life simulator**. You'll be transported to a randomly generated fantasy world, living an entire life from birth, making choices every turn.

**How to Play**:

| Command | Description |
|---------|-------------|
| `New Game` | Start a new life |
| `Continue` | Advance to the next turn |
| `Status` | Check current attributes |
| `Story` | Review your life so far |
| `Compile` | Generate a full novel after your life ends |

**Game Features**:

- 🌍 **Random World** — Every playthrough is unique: magic systems, races, nations, and history are all procedurally generated
- 👤 **Random Origin** — Race, talents, family, fate — you can't choose your starting point
- ⏳ **Turn-based Progression** — From infancy to old age, 6 life stages, each turn brings new choices
- 📖 **Endgame Novel** — When your life ends, a complete short story is automatically generated, documenting your legend

No extra installation needed. Just say "I'm bored" or "let's play," and Xiaoyu will start a new adventure with you.

## 📋 Version History

See [CHANGELOG.md](CHANGELOG.md) for details.

### v0.2.0 (2026-03-25) - 🎭 Multiple Personality Edition

**New**:
- ✨ Single-Agent Three-Role System (Planner/Generator/Evaluator)
- ✨ Personality Files Directory `personas/`
- ✨ Harness Design Pattern (based on Anthropic Labs research)
- ✨ Role Switching Ritual and Templates

**Improvements**:
- 🚀 Complex task execution quality improved
- 🚀 Self-evaluation mechanism optimized
- 🚀 Long task segmented checkpoints

### v0.1.0 (2026-03-13) - Initial Release

**New**:
- ✨ Basic Personality Settings
- ✨ User Profiling System
- ✨ Memory System
- ✨ Skill System
- ✨ Built-in Game "Fate Codex"

---

## 📜 License

[MIT](LICENSE) © 2026 [fslong](https://github.com/fslong520)

---

<div align="center">

**Made with ❤️ by [fslong](https://github.com/fslong520)**

**Version 0.2.1 · Workflow Standards Edition**

</div>
