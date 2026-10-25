# AI Coding Interview: Candidate Prep

Your side of the interview: what is graded, how to pace it, and what to say.
Distilled from Hello Interview's [AI-enabled coding guide](https://www.hellointerview.com/learn/ai-coding/overview/introduction) and from my own rounds (Finout, Cyera).

## What is graded

1. **Problem solving:** you break the problem down and work in the right order before opening the chat.
2. **Control over the AI:** you direct it and decide the architecture; it does not decide for you.
3. **Verification:** you run code after every meaningful change, read what you keep, and test before moving on.
4. **Communication:** the interviewer sees your prompts but not your thinking, so you say it.

"We'll ask you about any line you keep." (Finout)
"We care about how you reason, not how much you finish." (Finout)

## Before the day

Ask the recruiter:

- Structured (CoderPad or HackerRank, their AI) or open-ended (my editor, my AI, screen share)?
- Starter code or from scratch? How many phases?
- Any AI-tool restrictions, or a practice environment?
- Is AI-generated planning fine, or should I design by hand?
- If they are vague: "What should I have set up on my machine?"

Prepare:

- Structured: spend 30 minutes in the platform's practice pad, and practice with a weak model, since interview assistants often feel worse than the ones you use day to day.
- Open-ended: big terminal font, clean editor, assistant set to short answers, this skill loaded.
- Record one practice run while narrating, then watch it for long silences and over-narration.

## Kickoff prompt (open-ended)

> This is a live interview and the interviewer is watching. Use the ai-coding-interview skill. Be concise. Grill me before planning.

## Pacing

| Phase | Budget |
| --- | --- |
| Orient: read entry points, data model, tests; run the tests | 5-10 min |
| Plan: 3-5 ordered steps, said out loud | about 10 seconds to state |
| Structured rounds: bug fix, then feature, then scale | pace so phase 1 does not eat the clock |
| Write it yourself | anything you can type in under a minute |
| Fighting one generation | 2 min max: one sharper reprompt, then type it |
| Narration | one statement every 30-60 seconds |

## The loop

**Intent, prompt, review aloud, move on.**

- Before: "I'm going to ask it to add the split calculation to `previewSplit`, using the existing row type."
- After: "This matches, except it throws where the codebase returns error objects, so I'll reprompt."
- While waiting: explain the approach, or read the code for the next step and sketch test cases.
- When thinking: "Let me think about this for a second."
- When stuck: ask the interviewer. It counts as collaboration.
- When pivoting: name the problem with the current approach, the new approach, and why it fixes it.
- Avoid: silent typing, staring at a spinner, deleting code without saying why.

## Prompting

- Translate the problem through your own plan. Avoid pasting the raw statement.
- Use the codebase's names: class, method, data structure, return type.
- Delegate volume (boilerplate, tests, known algorithms) and keep judgment (data structures, edge cases, schema).
- Ask for concise code: minimal comments, no new abstractions.
- Commit or checkpoint at green points in open-ended formats, so you can roll back instead of patching layered errors.

## Red flags to catch in AI output

- **Correctness shortcuts:** `any`, casts, a swallowed `try/catch`, deleted or weakened tests, hardcoded values.
- **Over-design:** base classes, strategy patterns, or config where an `if` or a constant does the job.
- **Textbook answers** that ignore existing helpers or the problem's twist.
- **Spirals:** "let's restructure" or "start over" when the model is stuck.

## Lessons from my own rounds

- **Ask about the domain first.** At Finout, guessing how already-tagged rows should be treated in the preview cost two rounds. One question would have settled it.
- **Build less than you can.** 180 lines plus 150 test lines in ten minutes was defensible but heavy. Every extra line is a question you might get.
- **Constants over config.** Anything configurable needs a reason you can say in one sentence.
- **Match the spec's example exactly**, show it running next to the example, and name any deviation.
- **Say "all recs" to move fast,** and override by number where you disagree.

## Testing checklist

Happy path, empty or zero, single element, boundaries, duplicates, invalid input, scale.
Agree on the cases with the interviewer before implementing when building from scratch.
Run the full suite before optimizing, and again after each change.
