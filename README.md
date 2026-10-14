# Call Copilot

A live copilot for calls. Your phone listens to the call, works out which voice is you and which is them, and puts an answer to each question on the screen about two seconds after they stop talking. Follow-up questions get a new card on top.

- **Interview mode:** answers written in first person, ready to say out loud, built only from your background.
- **Meeting mode:** what to say, plus facts, code or concepts they ask for, and any action they give you.

## Why it is a web page, not Claude Code

- The Claude app and Claude Code work turn by turn. Neither can keep the mic open and follow a call continuously.
- So the agent is one web page (`index.html`) that runs in your phone's browser.
- **Deepgram** is the ears: live speech to text that labels each speaker.
- **Claude** is the brain: it reads the running transcript and writes the answer.

## One-time setup (about 10 minutes)

1. **Deepgram key:** sign up at console.deepgram.com (comes with free starting credit), then API Keys, Create key.
2. **Anthropic key:** console.anthropic.com, add a little credit under Billing, then API Keys, Create key.
3. **Open the page on your phone** at its https link. In Safari: Share, Add to Home Screen, so it opens like an app. (The mic only works over https, so the file has to be hosted, not opened from Files.)
4. **Settings (gear icon):** paste both keys, your name, and your background (CV, projects, stories).

## Before every call

- Settings, **This call:** company, role, job description or agenda. Add tricky words (names, tech terms) so they are spelt right.
- **Laptop audio on speakers, not headphones.** The phone has to hear them.
- Phone flat on the desk near the laptop, screen on, page open.
- Tap **Start** and say "testing, testing". The banner confirms it has your voice.

## During the call

- The newest answer card sits on top. Older ones fold below; tap to open.
- **Answer now:** answers the last thing they said, if it missed it.
- **Type:** ask privately, e.g. "shorter", "give me a number for that".
- **Swap:** if ME and THEM are the wrong way round. You can also tap a ME / THEM label in the transcript (tap "Live transcript" to open it).
- **Pause** stops listening. After the call: Settings, **Copy notes** saves the transcript and every answer.

## Good to know

- Keys and your background stay in this phone's browser only. Call audio goes to Deepgram; the transcript goes to Anthropic.
- Phones cut the mic when you lock the screen or switch apps. The page keeps the screen awake while listening.
- Brain: Haiku is fastest, Sonnet is the default balance, Opus is deepest but slower.
- Both services charge by usage. Check current pricing on each console.
- **Watch a demo** on the home screen runs a scripted interview with no keys, so you can see the flow first.

## Files

- `index.html`: the whole agent, one file
- `README.md`: this guide
