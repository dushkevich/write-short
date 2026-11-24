# Whole-message examples

Three invented messages, before and after. Use them to see how the rules work together.

## 1. Status update

**Before**
> Great news! I've successfully completed the implementation of the new upload pipeline. Basically, after performing a thorough investigation of the various issues we were encountering, it turned out that the root cause was related to the rate limiting on the TikTok API side, so I went ahead and implemented an exponential backoff mechanism with jitter, which should significantly improve reliability going forward. I also made some minor refactors to the config handling. Let me know if you have any questions!

**After**
> Uploads to TikTok work again. I ran 5 test uploads, and all 5 went through.
>
> **What was wrong:** TikTok only lets us upload a few times a minute. When we went over that, it refused, and our code gave up.
> **The fix:** now, when TikTok refuses, the code waits a bit and tries again, waiting longer each time.
>
> I also tidied the settings file. Nothing changes for you.

What changed: the result moved to line 1 (rule 2). "Successfully", "great", "significantly" became "5 of 5" (rule 5). "Rate limiting", "exponential backoff with jitter" became what happens (rules 7, 14). "Some minor refactors" became what it means for the reader (rule 1).

## 2. A question

**Before**
> Quick question: should we go with a VPS running Docker Compose or a managed serverless platform, given the cold-start latency and egress cost tradeoffs?

**After**
> Where should the shop's website run? Both options cost about the same at your traffic, so the choice is about who fixes it when it breaks.
>
> **Your own rented server, $6 a month:** pages always load fast. If it breaks at night, the site stays down until someone fixes it.
> **A hosting service, free at your traffic:** it fixes itself. The first visit after a quiet hour loads about 2 seconds slower.
>
> My pick: **the hosting service**, so nobody has to watch the site at night. Server or hosting service?

What changed: the situation comes before the choice. Each option says what happens if you pick it, not how it works inside (rule 16). "Cold start" and "egress" became what the reader would notice (rule 7). A recommendation is included.

## 3. Saying back a decision before acting

**The reader wrote**
> don't delete the old photos. move them to the archive drive, and only delete the duplicates

**Before** (acting at once)
> Got it, cleaning up the old photos now.

**After** (rule 3)
> Here's what I understood:
> - Move the old photos to the archive drive.
> - Delete only exact duplicates.
> - Delete nothing else.
>
> One thing to check: by "old" I mean everything taken before 2024. Is that right? I'll start once you say yes.

What changed: "cleaning up" squeezed "move, and delete only duplicates" into a phrase that could mean "delete". Saying it back catches that before anything is lost, and it brings up the one unclear word.
