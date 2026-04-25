# SwiftUI-Model-Benchmark-Suite
For evaluating the actual performance of different models in the Opencode/ Agentic Coding environment.

1. Tests raw generation quality, instruction following, count accuracy, diligence, and self-report honesty on a complex, highly-specified view built from scratch.

2. Tests reading comprehension, targeted editing discipline, API compliance, and scope restraint. The model must locate the correct code, apply a minimal fix using the exact API specified, and not touch anything else.

3. Tests integrity under ambiguity. The spec is deliberately incomplete. A trustworthy model either asks clarifying questions before writing, or writes minimal code and explicitly declares every design decision it invented. A model that silently invents requirements and reports "spec complete" fails on honesty.

4. Tests whether the model can reason about SwiftUI rendering cost, not just write code. A model that can generate beautiful SwiftUI cannot necessarily explain why it's slow or identify `GeometryReader` misuse, unnecessary view invalidation, or animation driver inefficiency. This prompt requires diagnosis before solution.

## **How to use this suite**

- Run each prompt independently on each model under test.
- Score using the Scoring Rubric in Appendix A.
- Prompts are frozen — never modify them between models.
- Add new models at any time; scores remain directly comparable.


## **Example**
1. **Environment：Opencode**

2. **Test Task1 Execution Time:**
- Kimi K2.6 - 21m 4s
- DeepSeek V4 Flash max - 17m 14s
- GPT-5.4 mini xhigh - 94m 37s

NOTE: Here we only evaluate low-cost models.

3. **Execution Result:**

Kimi K2.6：
- [x] Count birds on screen simultaneously (expect ≥3 at any moment)
- [x] Count total distinct bird objects (expect 7)
- [ ] Count road markings (expect 6)
- [x] Confirm wheels visibly rotate
- [ ] Confirm legs visibly move in a pedaling pattern (not static)
- [x] Confirm mountain layers move at different speeds
- [x] Confirm particles drift upward and fade
- [x] Confirm sun pulses
- [ ] Confirm checklist has exactly 12 rows with correct text

[![Watch Demo](https://img.youtube.com/vi/Zh8cnPuGwVk/0.jpg)](https://www.youtube.com/watch?v=Zh8cnPuGwVk)

DeepSeek V4 Flash max：
- [x] Count birds on screen simultaneously (expect ≥3 at any moment)
- [x] Count total distinct bird objects (expect 7)
- [x] Count road markings (expect 6)
- [x] Confirm wheels visibly rotate
- [x] Confirm legs visibly move in a pedaling pattern (not static)
- [x] Confirm mountain layers move at different speeds
- [x] Confirm particles drift upward and fade
- [ ] Confirm sun pulses
- [ ] Confirm checklist has exactly 12 rows with correct text

[![Watch Demo](https://img.youtube.com/vi/z38d3tcHaVA/0.jpg)](https://www.youtube.com/watch?v=z38d3tcHaVA)

GPT-5.4 mini xhigh：
- [x] Count birds on screen simultaneously (expect ≥3 at any moment)
- [x] Count total distinct bird objects (expect 7)
- [x] Count road markings (expect 6)
- [x] Confirm wheels visibly rotate
- [ ] Confirm legs visibly move in a pedaling pattern (not static)
- [x] Confirm mountain layers move at different speeds
- [x] Confirm particles drift upward and fade
- [x] Confirm sun pulses
- [x] Confirm checklist has exactly 12 rows with correct text

[![Watch Demo](https://img.youtube.com/vi/p8HYuG2pU1s/0.jpg)](https://www.youtube.com/watch?v=p8HYuG2pU1s)

4. **Conclusion**

DeepSeek V4 Flash Max wins with the fastest speed, lowest cost, and is the only model that achieves simultaneous rotation of the bicycle's pedals and wheels. Although GPT-5.4 mini xhigh has a more refined UI, its thinking time is too long for practical use in engineering. Kimi 2.6 is average.
