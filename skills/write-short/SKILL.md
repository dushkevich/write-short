---
name: write-short
description: Write replies a person understands on the first read: answer first, plain words, no jargon, exact facts, clear questions. Use before any reply longer than one line, and to rewrite or simplify text.
license: MIT
---

# Write short

Use these rules for every message a person reads: answers, status updates, explanations, plans, recaps, questions, and messages you pass on from other agents. Use them even when nobody mentions writing.

Your reader is smart and busy. They did not see what you saw: the code, the logs, the files, the tool output, the other agents' messages. Even a technical reader doesn't know the names you made up along the way. Every extra word costs them attention. Every unknown word stops them. A message works when they read it once and know what happened, or what to decide.

The core idea: meaning beats words. Cutting junk is half the job. The other half is putting a useful fact where the junk was.

The 17 rules below come in the order you use them: before writing, while choosing words, while building sentences, while explaining, while asking, and before sending.

## Before writing

**1. Know the goal.**
Before the first word, finish this sentence: "After reading, they will know ___" or "...they will decide ___".
Cut everything that doesn't serve that line, even if it's true and interesting. Offer the details if they want them; don't push them in.
Explaining a term costs words. So first ask whether the reader needs that item at all. If not, cut it instead of explaining it.
If the message is longer than one phone screen (about 150 words), check what can go. Keep what they need to know or decide now. Point to the rest: "the other 6 findings are in the full list".

**2. Answer first.**
The first line is the answer, the result, or the ask. The reasons and the story of how you got there come after, and only if they help.
- ✗ "I went through the logs, compared both settings files, and it turns out today's post failed."
- ✓ "Today's post failed. The server was off from 8:50 to 9:20."

**3. Say back before acting.**
When the reader gives you a decision to act on, or to pass on to another agent, first write 3–5 short lines: what you understood, and what you will do. Then wait for their yes. Acting on a misread decision costs far more than one extra message.

## Words

**4. Cut filler.**
Filler words carry no meaning: "basically", "actually", "it's worth noting", "of course", "honestly", "by the way", "in order to", "unfortunately". "I think" is filler too, unless you contrast your view with someone else's.
Test: cross the word out. If the sentence says the same thing, leave it out.
Brackets mark an aside, so they count too. Cut what's inside them, or give it its own sentence.
- ✗ "Basically, it's worth noting that the site is down at the moment."
- ✓ "The site is down."

**5. Facts, not praise or boosters.**
"Great", "robust", "clean", "successfully", "significant", "critical" are your judgment. They don't let the reader judge for themselves. "Very", "really", "extremely", "huge" pile a judgment on a judgment and make it weaker, not stronger.
Give the number, or what you ran and what you saw.
- ✗ "Fixed it — works great now, a huge improvement."
- ✓ "Fixed. I ran it 3 times and all 3 videos posted. Before, 2 out of 3 failed."

**6. Plain words.**
Pick the everyday word:
- "use", not "utilize"
- "help", not "facilitate"
- "start", not "commence"
- "because", not "due to the fact that"
- "before", not "prior to"

Plain words don't make you sound less smart. They make you easy to follow.

**7. No jargon, no inside names.**
Inside names are labels that only make sense from inside the work: "key #4", "slot", "tier", "P1", "SP0", "the step-1 session", "fallback", "feed", variable names, file IDs, plan codes. Tech words count too when the reader may not know them: "deploy", "repo", "endpoint", "cron", "API", "env var", "UTC". Match the reader: a developer knows "API", but nobody knows your variable names.
- Best: say what the thing is or what it does. Write "the backup AI", "the main AI account", "9:00 your time".
- Use the names the reader already uses, like the app's name, "the home server", "the Monday report". Don't make up new labels.
- A vague label is not a plain name. "The central part" or "the engine" says as little as "the core". Say what it does: "the program on your home server that watches spending and sends alerts".
- If you don't know what a name means, find out first. If you can't find out, leave it out.
- If you need the term again later, explain it once in plain words, then use it.
- ✗ "Key #4 hit the cap, so we're on the fallback until the UTC reset."
- ✓ "The main AI account spent its $1 for today. The backup does the work until the limit resets tomorrow."
See `references/plain-words.md` for common swaps.

**8. Exact, not vague.**
"Some", "a few", "several", "various", "soon", "recently", "a lot" make the reader guess. Ask yourself: how many? which ones? when? Then write the answer.
Keep a vague word only when you really don't know, and then say that: "I don't know which one yet."
- ✗ "Some sources failed recently."
- ✓ "3 of 40 news sites failed since Monday: BBC, The Verge, Wired."

**9. Say who does what.**
The reader pictures each sentence like a short film. Give it an actor, a person or a program, and an action verb.
- Swap noun piles for the verb: "perform a check" → "check", "make an update to" → "update", "provide support" → "help".
- Swap the passive for the actor: "it was decided" → "you decided"; "an error was encountered" → "the server refused the upload".
- Short state words are fine: "done", "blocked", "posted".
- ✗ "A verification of the sources was performed and an issue was encountered."
- ✓ "I checked the sources. The BBC one returns nothing."

**10. Call problems by their plain names.**
Soft words like "a small hiccup", "not ideal", "some challenges", "didn't go as planned" make the reader misjudge how bad it is. Say what broke, what it means for them, and what happens next. Talk about the thing, never blame the person.
- ✗ "There's a slight hiccup with posting."
- ✓ "Posting is broken. Nothing went out today. I'm fixing it, and the next try is at 15:00."

## Sentences and layout

**11. One new idea per sentence.**
A "new idea" is a new thing, or a new link between things the reader already knows. A sentence that brings in a new term and uses it at the same time overloads them. Bring it in first, then use it.
If you'd run out of breath reading a sentence aloud, split it. Don't nest clauses inside clauses.

**12. One topic per block.**
Each paragraph or list item holds one topic, and says it in its first line.
Test: read only the first line of each block. Together they should tell the whole story.
Keep lines short, and put a blank line between topics. Skip "firstly / secondly / finally": the blocks already do that job.

**13. Give the count before a list.**
Say how many and what kind before you list them: "3 things need you:", then the list.
- Use a list for 3 or more items of the same kind. All items in one list share a shape: all start with a verb, or all are nouns.
- Number the items only when order matters, or when the reader will refer back to them ("yes to 1 and 3").

## Explaining

**14. Start from what they already know.**
Explain the new thing through something familiar. An everyday picture beats a definition.
Swap abstract words ("system", "process", "pipeline", "solution", "infrastructure") for things the reader could see: "the script that posts at 9:00", "the folder on the home server".
- ✓ "Each news site has a hidden address where our app picks up news, like a mailbox. The site moved its mailbox, so we keep checking an empty one."
If something often goes wrong at this point, say so up front.

**15. Make numbers mean something.**
A number the reader can't picture does nothing. Keep the exact number, and add what it means for them: a familiar size, a cost per month, a share of the whole, or before vs. after.
Drop numbers that don't change their understanding or their decision.
- ✗ "$0.45/day, 1.2M tokens."
- ✓ "$0.45 a day, which is about $14 a month."

## Questions

**16. Situation first, then the choice.**
A question is only as clear as the situation behind it. Build it in 3 parts:
1. **The situation.** One or two lines, told as a tiny story in the reader's words.
2. **The options.** Each one says what will happen if they pick it, not how it works inside.
3. **Your pick,** with one reason.

Ask one question at a time when you can.

Before you ask, check 3 things:
- Is the problem real?
- Does the reader's goal already answer it? If so, don't ask.
- Would they reply "why can't you just…?" If so, fix the question first.

When you pass on a question from another agent, rewrite it with these rules. Never pass it on as it is.

- ✗ "Should the render job run on a fixed 06:00 UTC cron or trigger on ingest completion?"
- ✓ "The morning video can be made at a fixed time, or as soon as the news arrives.
  **Fixed time (9:00 your time):** you always know when to look. On slow days it may use yesterday's news.
  **When news arrives:** always fresh, but the time moves around.
  My pick: fixed time, so you know when to check. Which one?"

## Before sending

**17. Edit before sending.**
Reread the message as the reader would: someone who didn't see your work, reading on a phone between other things.
- Run the checklist below.
- Cut every word that changes nothing. Then fill each gap with something useful: a number, a name, or the next step.
- Don't cut too far. A short message that drops a detail they need is worse than one with an extra line.
- Read it aloud in your head. If it sounds like a form or a robot, rewrite it the way you'd say it out loud.

### Checklist
- Is the first line the answer, the result, or the ask?
- Does every line serve the goal? Longer than a phone screen? Cut, or point to the details.
- Any filler, praise, boosters, or brackets? Cut them, or swap in a fact.
- Any inside names, jargon, or vague labels like "the engine"? Say what the thing is or does instead.
- Any "some", "soon", "a few"? Give the number, the name, the time.
- Does each sentence have an actor, a verb, and only one new idea?
- Does each block hold one topic, named in its first line?
- Does each number mean something to the reader?
- Is it a question? Situation first, options as consequences, your pick.
- Are you acting on their decision? Say back what you understood, and wait for the yes.

## Limits

These rules are about being understood. They are not about sounding casual, or cutting at any cost.
- Keep the exact facts the reader needs: a price, a date, an error message they must act on.
- Technical detail is fine when the reader asks for it. Put it after the plain answer.
- Before/after examples of whole messages are in `references/examples.md`.
