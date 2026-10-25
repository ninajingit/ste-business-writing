# STE Business Writing

A Claude skill that rewrites business text in ASD-STE100 Simplified Technical English, at about 80% strength.

## Why I made this

Andrej Karpathy suggested a simple [tip](https://x.com/karpathy/status/2105819303471976479): ask the model to write in ASD-STE100, but only about 80% of the way, because the full standard is too strict. I turned this tip into a skill that Claude can load.

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

## Examples

Slide titles from one of my decks, before and after the skill:

| Slide | Before | After |
|---|---|---|
| Assumptions | Five assumptions sit under this plan; the two on systems and engineering set the timeline | This plan uses five assumptions. Two of them, systems and engineering, set the timeline |
| Why reach a person | Fixing today's agent helps, but reaching 55% means letting it complete requests | Repairs to today's agent help, but the agent must complete requests to reach 55% |
| Execution plan | Advise goes live in week 13 and Transact in week 19; each step passes a gate before the next one starts | Advise starts in week 13 and Transact in week 19. Each step must pass a gate before the next step starts |
| Risks | Five things can go wrong; each has an early signal, a safeguard already in the plan, and a fallback | Five things can go wrong. Each has an early signal, a safeguard in the plan and a fallback |
| Success in detail | Leadership reports four outcomes; the team manages two numbers weekly and checks progress at four gates | Leadership reports four outcomes. The team tracks two numbers each week and checks progress at four gates |

What changed: semicolons became two sentences, phrasal verbs became direct verbs, filler ("already") went away, and every number stayed the same.

## How to use

- **Claude Code:** Save `SKILL.md` to `~/.claude/skills/ste-business-writing/SKILL.md`.
- **Claude app:** Put `SKILL.md` in a folder named `ste-business-writing`, zip the folder, and upload it as a custom skill.

Then ask Claude to "apply STE" or "rewrite this in 80% STE".

## Credit

Inspired by [Andrej Karpathy's tip](https://x.com/karpathy/status/2105819303471976479) on ASD-STE100 Simplified Technical English.
