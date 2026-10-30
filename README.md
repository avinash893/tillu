# Tillu

Tillu is an intelligent Discord assistant built for community and gaming servers. It uses Google Gemini for conversational AI and comes with built-in server memory, customizable autonomous rules, and a situational meme engine designed not to sound repetitive.

## Key Features

### Situational Meme Engine
- Context-aware banter: Memes trigger naturally in conversation rather than on every single reply.
- Extensive library: Contains a curated collection of over 1,000 trending, classic Bollywood, Desi, and gaming references.
- Anti-repetition: Tracks recently used references so jokes stay fresh.

### Server Memory (#tillu-memory)
- Learns community inside jokes, lore, and member facts.
- Vision support to parse and remember uploaded image memes and screenshots.

### Custom Autonomous Rules (#tillu-updates)
- Server admins can teach Tillu specific behavior triggers in plain English (for example: "When someone asks about rules, tell them to check #announcements").
- Rules are saved persistently and applied directly to conversational reasoning.

### Dynamic Personality Styles
- Switch between distinct styles: Sarcastic & Witty, Short & Punchy, Roast Mode, or Helpful & Friendly.

### Deduplicated Self-Audit Engine
- Runs automated checks on recent queries and error logs every 4.8 hours.
- Generates new robustness rules only when actual task errors happen, preventing repetitive audit reports.

### Multi-Server Setup
- Automatically sets up dedicated channels on server join.
- Built-in per-user cooldowns to prevent spam and rate limits.

## Project Architecture

- `config.py`: Environment configuration, tokens, paths, and Discord intents.
- `meme_engine.py`: Indexed meme repository, emotion tagging, and cooldown logic.
- `memory_manager.py`: Persistent storage for guild lore, user facts, and meme history.
- `rule_manager.py`: Custom rule storage and prompt injection.
- `self_reflection.py`: Autonomous audit loop with duplicate-prevention filters.
- `ai_engine.py`: Gemini client, personality prompt builder, and image handling.
- `bot.py`: Discord gateway event handlers, slash commands, and message listeners.
