# 🐉🔥 Dragon War — Voice-Driven Improv Battle Game (Day 10)

**Dragon War** is a high-energy, voice-interactive improv game show built as the final project of the Murf AI 10-Day Voice Agent Challenge.  
The AI acts as the dramatic, witty host of *Improv Battle: Dragon War Edition*, guiding the player through multiple short-form improv scenes and reacting to their performance.

This agent uses:
- 🎤 Real-time microphone input  
- 🎧 Voice output  
- 🧠 Stateful session tracking  
- 🎭 Scenario generation  
- 😂 Dynamic and varied host reactions  

It is designed to feel like a TV show where **you** are the star performer.

---

## 🎯 Core Features

### 🎙️ 1. High-Energy Improv Host Persona
Dragon War speaks like a charismatic game show host:
- Loud, playful, witty  
- Uses hype and humor  
- Provides dynamic reactions  
- Ends each turn with a question to keep the mic open  

Tone inspired by fantasy, competition, and improv comedy.

---

### 🔥 2. Multi-Round Improv Gameplay
Each game session runs **3 rounds**, and each round includes:

1. **Scenario Setup**  
   Dragon War presents a fun, creative prompt:
   - “You are a dragon librarian…”  
   - “You are a time-traveling chef…”  
   - “You are a wizard’s apprentice…”  

2. **Player Performance**  
   The user performs the scenario in character and finishes with **“End scene.”**

3. **Host Reaction**  
   Dragon War replies with:
   - Supportive praise  
   - Neutral analysis  
   - Playful, constructive critique  

   The tone is varied every round to feel realistic.

4. **State Update**  
   The backend stores:
   - Scenario  
   - Player’s performance  
   - Host reaction  

---

### 🧠 3. Session State Management
A simple state object tracks:

```json
{
  "player_name": "Sumanth",
  "current_round": 2,
  "max_rounds": 3,
  "rounds": [
    { "scenario": "...", "player_lines": [...], "host_reaction": "..." }
  ],
  "phase": "awaiting_improv"
}
