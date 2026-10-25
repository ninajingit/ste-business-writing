---
name: "ste-business-writing"
description: "Rewrite or write business text (slide titles, memos, docs, PRDs, emails) in ASD-STE100 style at about 80% compliance: short sentences, one idea each, direct verbs, nothing lost."
---

# STE Business Writing (ASD-STE100, 80% mode)

Based on Andrej Karpathy's tip (Oct 2026): ask the model to write in ASD-STE100 Simplified Technical English, but only about 80% of the way, because the full standard is too strict. This skill defines which 80% to keep for business writing.

## When to use
- The user asks to apply "STE", "Karpathy style", "80% STE", or to make text clearer or easier to scan.
- Informational business text: slide titles, exec summaries, memos, PRDs, status updates, runbooks, Slack or email updates.

## When NOT to use
- Interview answers.
- Outreach, persuasion, storytelling, or personal essays. STE makes these sound flat.
- If unsure, ask the user.

## Strength levels (default: 80%)
- light: Slack, quick email. Split long sentences, remove filler. Keep natural tone.
- 80%: slides, memos, docs, PRDs. Apply all "Keep" rules below.
- strict: procedures, runbooks, checklists. Add: one instruction per sentence, imperative verb first, max 20 words.

## Keep (the 80%)
1. One idea per sentence. Replace semicolons with a period. The first sentence must carry the main point alone.
2. Sentence length: max 25 words for descriptions, max 20 for instructions.
3. Active voice. Name who does the action.
4. Direct, simple verbs. Replace phrasal verbs and soft causatives with one clear verb: "goes live" -> "starts", "sit under" -> "uses", "letting it complete" -> "must complete".
5. Specific verbs over vague ones: "manages" -> "tracks" when tracking is the real action.
6. One term per concept. Do not rotate synonyms (agent / bot / assistant). Pick one and keep it.
7. Remove filler words and adverbs that add no fact: "already", "really", "it's important to note", "Great question".
8. Prefer noun or finite-verb subjects over -ing subjects: "Fixing the agent helps" -> "Repairs to the agent help".
9. Answer first. Put the conclusion or decision in the first sentence.

## Relax (the 20%)
- Ignore the STE approved-word dictionary. Keep domain terms (checkout, CVR, settlement, RTGS, LLM eval, gate) as-is.
- Allow common business words even if STE bans them.
- Keep a natural rhythm for titles; they do not need to be full instructions.

## Never lose
- Numbers, dates, percentages, week numbers, names, identifiers.
- Conditions, caveats, and hedges ("if", "about", "may").
- Meaning. If a rewrite changes a claim, keep the original.

## Korean text
STE is English-only. For Korean, apply the same spirit:
- 한 문장에 한 정보만 담기. 긴 문장은 마침표로 나누기.
- 명사구 대신 동사로 끝나는 문장 쓰기 ("검토 진행 예정" -> "검토할 예정이다").
- 주어를 밝히고 능동문으로 쓰기.
- 같은 대상은 같은 용어로 부르기.
- 결론을 첫 문장에 두기 (두괄식).

## Process (rewrite mode)
1. Confirm strength level if unclear; otherwise use 80%.
2. Rewrite each sentence or title against the Keep rules.
3. Self-check: word count per sentence, no semicolons, active voice, one term per concept, every number and caveat still present.
4. Leave text unchanged if it already passes. Do not rewrite for the sake of change.
5. Never use em dashes.

## Output format
- For slides or many short items: a table with columns Item | Before | After.
- Then 2 to 3 bullets on the common patterns changed.
- State that numbers and meaning are unchanged, or flag anything that changed.
- Offer to revert any single item.

## Reference example (slide deck titles)
| Slide | Before | After |
|---|---|---|
| Assumptions | Four assumptions sit under this forecast; the one on hiring sets the budget | This forecast uses four assumptions. The hiring assumption sets the budget |
| Why invest now | Improving onboarding helps, but hitting 40% retention means letting users finish setup in one session | Onboarding improvements help, but users must finish setup in one session to reach 40% retention |
| Launch plan | The beta goes live in week 6 and the full launch in week 10; each phase passes a review before the next one starts | The beta starts in week 6 and the full launch in week 10. Each phase must pass a review before the next phase starts |
| Risks | Three things can go wrong; each has an early signal, a fix already in the plan, and a fallback | Three things can go wrong. Each has an early signal, a fix in the plan and a fallback |
| Metrics | Leadership reports three outcomes; the team manages one number weekly and checks progress at two reviews | Leadership reports three outcomes. The team tracks one number each week and checks progress at two reviews |

Patterns shown: semicolon split into two sentences, phrasal verbs replaced by direct verbs, filler ("already") removed, -ing subject replaced, numbers unchanged.
