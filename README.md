# reflect

A Claude Code skill for self-analysis and personal pattern recognition. Acts as a rigorous analytical partner — not a therapist, but a structured mirror that helps you examine your own behaviors, emotional patterns, and recurring dynamics with clinical precision.

## What It Does

- Tracks behavioral and emotional patterns across sessions using persistent local notes
- Applies therapeutic frameworks (CBT, attachment theory, IFS, somatic/polyvagal, and more) without announcing them
- Searches current research before making any clinical claim — sources cited inline
- Produces structured clinical observations you can share with a human therapist
- Imports and summarizes chat history from other AI conversations
- Remembers your preferred language and terminology already explained

## Installation

1. Copy the `reflect/` folder into your Claude Code skills directory:

   ```
   ~/.claude/skills/reflect/
   ```

2. Create your notes files:

   ```
   ~/Documents/Notes/reflect-notes.md
   ~/Documents/Notes/reflect-quick-ref.md
   ```

   These will be populated automatically after your first session.

## Usage

Invoke the skill in any Claude Code session:

```
/reflect
```

Or with context already stated:

```
/reflect — I had a difficult conversation with my manager today
```

### First Session

On first use, the skill will ask your preferred language, then open with: *"What's going on?"*

### Importing History From Another AI

If you've had relevant sessions elsewhere, type something like:

> "I want to import my chat history from another conversation"

The skill will give you a prompt to paste at the end of that conversation. Paste the output back and your notes will be updated automatically.

### Ending a Session

When you're done, signal it explicitly — say something like "我们今天到这里" or "let's wrap up". This tells the skill to do its closing work:

1. **Synthesize** — distills the session's key themes and turning points into a concise narrative
2. **Name patterns** — surfaces recurring dynamics that showed up, adding to or refining the running pattern log
3. **Suggest a between-session observation** — gives you one concrete thing to notice or track before the next session
4. **Update both notes files** — writes the session record to `reflect-notes.md` and refreshes `reflect-quick-ref.md` so the next session picks up exactly where you left off
5. **Run an evolution check** — compares this session against prior entries to flag any shifts, regressions, or emerging themes in your longer arc

If you just close the conversation without signaling, the session won't be properly saved and this synthesis work won't happen.

## Notes Files

| File | Purpose |
| --- | --- |
| `reflect-quick-ref.md` | Fast-scan reference loaded at every session start — known patterns, active hypotheses, terminology log, last session summary |
| `reflect-notes.md` | Full longitudinal record — timestamped session entries with clinical observations, verbatim quotes, and evolution notes |

Both files are rebuilt/updated at the end of every session. They accumulate into a detailed psychological portrait over time.

## Privacy

All your data stays local. The notes files live on your own machine — nothing is sent to any server beyond the standard Claude API call you're already making. No conversation content is stored or logged by this skill.

This means your psychological portrait is genuinely yours: portable, deletable, and never used to train anything. If privacy is a concern, you can also point the notes paths to an encrypted folder or a location of your choosing.

## Philosophy

You are the agent. The skill provides the framework, the challenge, and the mirror — not the insight. Expect to be pushed back on when your reasoning doesn't hold.
