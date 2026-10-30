# 🤖 Tillu — Intelligent Discord AI Assistant

**Tillu** is an autonomous, multi-tenant Discord AI assistant powered by Google Gemini and tailored for gaming and community servers. Featuring dynamic personality controls, a 1,000+ meme engine with situational pacing, real-time memory learning, and autonomous self-evolution.

---

## 🚀 Core Features

### 1. 🎭 1,000+ Situational Meme Engine
- **Context-Aware Pacing**: Only triggers memes when appropriate (~20% of casual banter) to avoid repetitive spam.
- **Vast Knowledgebase**: 1,000+ indexed Desi, Bollywood, and gaming meme dialogues and cultural references.
- **Anti-Repetition Tracking**: Cooldown prevents using the same meme twice in a row.

### 2. 🧠 Living Server Memory (`#tillu-memory`)
- **Community Lore**: Remembers inside jokes, user facts, and custom server lore.
- **Vision AI Support**: Inspects uploaded meme images, captures context, and integrates them into memory.

### 3. 📜 Autonomous Behavior Rules (`#tillu-updates`)
- **Natural Language Custom Rules**: Admins can set behavior triggers on the fly (e.g., *"If someone asks X, answer Y"*).
- **Instant Enforcement**: Rules are injected directly into Tillu's reasoning loop.

### 4. 🎛️ Dynamic Personality Modes
- **Sarcastic & Witty**: Humorous, clever comebacks and gaming banter.
- **Short & Punchy**: Rapid, one-line answers.
- **Roast Mode**: Playful, savage banter for community channels.
- **Helpful & Friendly**: Professional, polite, and detailed explanations.

### 5. 🔬 Deduplicated Self-Evolution Engine
- **5x Daily Self-Audits**: Reviews recent interactions, error rates, and intent accuracy every 4.8 hours.
- **Smart Deduplication**: Only generates new robustness rules when actual failures occur, preventing repetitive reports.

### 6. 🛡️ Safe & Scalable Multi-Tenant Architecture
- **Anti-Spam Cooldown**: Built-in rate limiting per user to protect against API quota limits.
- **Zero-Friction Setup**: One-click category (`📁 TILLU`) and channel auto-provisioning upon server join.

---

## 📂 Architecture & File Roadmap

| File | Purpose |
| :--- | :--- |
| `config.py` | Central configuration, environment variables, paths, and bot intents |
| `meme_engine.py` | 1,000+ indexed meme bank with emotion tagging and anti-repeat logic |
| `memory_manager.py` | Per-server lore, user facts, and meme memory bank |
| `rule_manager.py` | Dynamic natural language rule persistence and injection |
| `self_reflection.py` | 5x daily autonomous self-auditor with deduplication fix |
| `ai_engine.py` | Gemini AI caller, dual-tone system prompt builder, and vision processor |
| `bot.py` | Discord client events, commands (`/ask`, `/setup`, `/settings`), and message listeners |
