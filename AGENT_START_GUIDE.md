# Quickstart Guide: Building AI Agents & Apps from Scratch

Welcome to **AI Engineering from Scratch**! The entire repository has been cloned, the isolated Python environment is configured, and all dependencies are resolving.

---

## 1. Environment & Setup Overview

### Activate the Environment
Always activate the virtual environment in your terminal before running Python lessons:
```bash
source .venv/bin/activate
```
*(Or invoke via `.venv/bin/python` directly)*

### API Keys (`.env`)
When you are ready to connect to real LLM providers (Anthropic, OpenAI, etc.), copy `.env.example` to `.env` and fill in your keys:
```bash
cp .env.example .env
```
Key fields inside `.env`:
- `ANTHROPIC_API_KEY`: For Claude / Computer Use / Tool-calling
- `OPENAI_API_KEY`: For GPT models / Function calling / Embeddings
- `GEMINI_API_KEY`: For Google Gemini models

> **Note:** Many starting lessons (like `Phase 14 Lesson 01`) include **offline mock/scripted loops** so you can learn control flow and mechanics before spending API credits!

---

## 2. Recommended Learning Path for AI Agents & Apps

If your goal is **building AI agents and applications**, follow this focused progression:

```
[Phase 11: LLM Engineering]
   └─ Prompting, Output Parsing, Few-shot CoT, RAG Foundations
           │
           ▼
[Phase 13: Tools & Protocols]
   ├─ Tool Interfaces & Function Calling
   ├─ Model Context Protocol (MCP) (Lessons 06-18, 28-31)
   └─ Agent Skills (Lessons 22-26)
           │
           ▼
[Phase 14: Agent Engineering]  <-- The Core!
   ├─ 01: The Agent Loop (ReAct from scratch)
   ├─ 02-10: Planning, Memory, Self-Reflection & Tool Sandboxes
   ├─ 11-18: Subagents, Session Stores, Production Runtimes
   └─ 31-46: Real-World Workbench, Contracts & Feedback Loops
           │
           ▼
[Phase 16: Multi-Agent & Swarms]
   └─ Orchestrator-Worker, Supervisor, Debate, Shared Memory & A2A
           │
           ▼
[Projects & Capstones]
   ├─ `projects/tiny-coding-agent/`
   ├─ `projects/browser-agent/`
   ├─ `projects/memory-server/`
   └─ `phases/19-capstone-projects/`
```

---

## 3. Immediate Hands-On Commands to Run

### Test 1: Verify the Agent Route Environment
```bash
.venv/bin/python phases/00-setup-and-tooling/01-dev-environment/code/verify.py --route agents
```

### Test 2: Run Your First Agent Loop (ReAct from Scratch)
```bash
.venv/bin/python phases/14-agent-engineering/01-the-agent-loop/code/main.py
```
This runs an agent that reasons, calculates, and reads/writes to a key-value store in a 5-step loop.

### Test 3: Explore MCP (Model Context Protocol)
```bash
.venv/bin/python phases/13-tools-and-protocols/06-mcp-fundamentals/code/main.py
```

### Test 4: Explore LLM Engineering & Prompting
```bash
.venv/bin/python phases/11-llm-engineering/01-prompt-engineering/code/prompt_engineering.py
```

---

## 4. Built-in Agent Skills & Placement Tutor

This repository includes custom Cursor & Agent skills under `skills/`:
- `start-learning`: Placement quiz to assess your level and create a custom study plan in `LEARNING.md`.
- `learn`: Walks through a lesson step-by-step (concept -> math -> code -> quiz).
- `learn-mcp`: Targeted curriculum for mastering Model Context Protocol.
- `learn-agent-skills`: Guide to authoring modular Agent skills.

To test your current level or get a tailored study plan:
```bash
npx skills add rohitg00/ai-engineering-from-scratch
```
or inspect `skills/start-learning/SKILL.md`.
