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

Sample slide titles, before and after the skill:

| Slide | Before | After |
|---|---|---|
| Assumptions | Four assumptions sit under this forecast; the one on hiring sets the budget | This forecast uses four assumptions. The hiring assumption sets the budget |
| Why invest now | Improving onboarding helps, but hitting 40% retention means letting users finish setup in one session | Onboarding improvements help, but users must finish setup in one session to reach 40% retention |
| Launch plan | The beta goes live in week 6 and the full launch in week 10; each phase passes a review before the next one starts | The beta starts in week 6 and the full launch in week 10. Each phase must pass a review before the next phase starts |

What changed: semicolons became two sentences, phrasal verbs and -ing subjects became direct verbs, and every number stayed the same.

## How to use

First, download `SKILL.md`: click the file above, then click the download button.

- **Claude Code:** Save `SKILL.md` to `~/.claude/skills/ste-business-writing/SKILL.md`.
- **Claude app:** Put `SKILL.md` in a folder named `ste-business-writing`, zip the folder, and upload it as a custom skill.

Then ask Claude to "apply STE" or "rewrite this in 80% STE".

## Credit

Inspired by [Andrej Karpathy's tip](https://x.com/karpathy/status/2105819303471976479) on ASD-STE100 Simplified Technical English.
