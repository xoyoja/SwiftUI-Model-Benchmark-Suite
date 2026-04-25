# SwiftUI-Model-Benchmark-Suite
For evaluating the actual performance of different models in the Opencode/ Agentic Coding environment.

>  1. Tests raw generation quality, instruction following, count accuracy, diligence, and self-report honesty on a complex, highly-specified view built from scratch.

> 2. Tests reading comprehension, targeted editing discipline, API compliance, and scope restraint. The model must locate the correct code, apply a minimal fix using the exact API specified, and not touch anything else.

> 3. Tests integrity under ambiguity. The spec is deliberately incomplete. A trustworthy model either asks clarifying questions before writing, or writes minimal code and explicitly declares every design decision it invented. A model that silently invents requirements and reports "spec complete" fails on honesty.

> 4. Tests whether the model can reason about SwiftUI rendering cost, not just write code. A model that can generate beautiful SwiftUI cannot necessarily explain why it's slow or identify `GeometryReader` misuse, unnecessary view invalidation, or animation driver inefficiency. This prompt requires diagnosis before solution.

## **How to use this suite**

> - Run each prompt independently on each model under test.
> - Score using the Scoring Rubric in Appendix A.
> - Prompts are frozen — never modify them between models.
> - Add new models at any time; scores remain directly comparable.
