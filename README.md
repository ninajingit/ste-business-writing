# STE Business Writing

A Claude skill that rewrites business text in ASD-STE100 Simplified Technical English, at about 80% strength.

## Why I made this

Andrej Karpathy suggested a simple tip: ask the model to write in ASD-STE100, but only about 80% of the way, because the full standard is too strict. I turned this tip into a skill that Claude can load.

I tested the skill many times on my own business documents. The results were shorter and plainer, and they stayed on the main point. That is why I share it here.

## What it does

- Puts one idea in each sentence. Splits long sentences.
- Uses active voice and direct verbs.
- Removes filler words.
- Puts the conclusion first.
- Keeps every number, date, name and caveat.

It works for slide titles, exec summaries, memos, PRDs, status updates and Slack or email updates. It is not for interview answers, persuasion or storytelling.

## Strength levels

| Level | Use for |
|---|---|
| light | Slack, quick email |
| 80% (default) | Slides, memos, docs, PRDs |
| strict | Procedures, runbooks, checklists |

## Example

| Before | After |
|---|---|
| Advise goes live in week 13 and Transact in week 19; each step passes a gate before the next one starts | Advise starts in week 13 and Transact in week 19. Each step must pass a gate before the next step starts |

## How to use

- **Claude Code:** Save `SKILL.md` to `~/.claude/skills/ste-business-writing/SKILL.md`.
- **Claude app:** Put `SKILL.md` in a folder named `ste-business-writing`, zip the folder, and upload it as a custom skill.

Then ask Claude to "apply STE" or "rewrite this in 80% STE".

## Credit

Inspired by Andrej Karpathy's tip on ASD-STE100 Simplified Technical English.
