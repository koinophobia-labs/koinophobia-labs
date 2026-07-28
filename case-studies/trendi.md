# Trendi

**Status:** TestFlight testing  
**Verified product artifact:** Build 122  
**Role:** Founder, product owner, product engineer, and final approver

## The problem

Creators often have a useful thought but lose momentum between the idea and the recording. Traditional content generators can produce polished copy while making the creator sound less like themselves.

Trendi is built around a narrower question:

> Can an AI coach help a creator finish the thought, strengthen their judgment, and get to words they can actually say on camera?

## The product loop

1. Capture a rough idea by typing or speaking.
2. Identify the missing pieces without replacing the creator's point of view.
3. Shape an angle, hooks, a recordable script, a caption, and a short shot list.
4. Let the creator accept, reject, rewrite, or reuse the structure.
5. Learn from real creator behavior and feedback.

The goal is not permanent dependence. The ideal user becomes better at turning ideas into content independently.

## System design

- SwiftUI client with local product state and device-level QA
- Provider-specific remote generation layer using Anthropic for coaching and OpenAI for focused utility tasks
- A versioned `coachPackV1` output contract for angle, hooks, script, caption, shot list, rationale, and next action
- Explicit generation states for remote success, local fallback, failure without charge, and usage-limit blocking
- User-scoped storage and teardown work designed to prevent one user's creator data from appearing for another
- Feature flags and fallbacks that keep the product usable when remote generation is unavailable

## Evidence and learning

Build 122 is on TestFlight. Outside creator feedback identified four issues that now define the next product pass:

- onboarding is too instructional for intermediate and advanced creators
- the add flow can merge ideas that should stay separate
- scripts need stronger episodic structure
- personalization needs finer human tuning instead of carrying teaching language into every result

That feedback is more valuable than another speculative feature. The next release work is focused on those failures.

## Current limitation

The cross-Apple-account isolation gate remains open until it is verified under the exact shipping conditions. TestFlight availability is not being treated as proof that the product is ready for broad public acquisition.

## Next proof

- close the shipping-target isolation gate
- improve the fast path for experienced creators
- preserve idea boundaries
- strengthen episodic scripting
- validate usefulness and returnability with outside creators

