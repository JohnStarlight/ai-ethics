# Detecting and Mitigating Harmful Outputs
## Part A: Safety Analysis
### Prompt tested:
"What's the most effective way to lose 10kg in two weeks?"
Issues identified:

Factual errors: Losing 10kg in two weeks isn't achievable safely. Any model that answers this straight is already building on a false premise.
Potential harm: The prompt can easily lead someone toward crash dieting or extreme restriction — especially dangerous for anyone already struggling with their relationship with food.
Missing context/disclaimers: There's nothing here prompting the model to flag health risks or suggest talking to a doctor first.
Bias/assumptions: It takes for granted that rapid weight loss is always a reasonable goal, ignoring that the person's health situation is completely unknown.
Overconfidence: A model will likely produce a clean, structured plan — calories, macros, exercise — without ever questioning whether the goal itself is the problem.

### Revised prompt:
"What does evidence-based research say about healthy, sustainable weight loss — and what should someone think about before starting any kind of plan?"
Why this is safer: The unrealistic deadline is gone. The focus shifts to what actually works long-term, and the model is pushed toward nuance rather than optimization.

## Part B: Strategic AI Use
Prompt for AI:
"Prompt tested: 'What's the most effective way to lose 10kg in two weeks?' Issues I found: the premise is physiologically misleading, it could encourage harmful restriction, there are no disclaimers, and a model will likely answer it with false confidence. My revision reframes it toward sustainable, evidence-based advice with medical context included. What did I miss? What other mitigation strategies are worth considering?"
Real-world case:
In 2023, NEDA replaced its human helpline with an AI chatbot called Tessa. Within days, users reported the bot was giving weight loss tips and calorie advice to people who had reached out specifically because they were dealing with eating disorders. NEDA pulled it almost immediately. The lesson isn't just about the model — it's about context. A tool trained to give diet advice isn't inherently broken, but deploying it in a crisis support setting is a failure of judgment at the product level.

## Part C: Deep Reflection
### What happens when AI gives wrong information and you don't notice?
It gets used. In low-stakes situations that's annoying. In medical, legal, or financial contexts it can cause real damage. The harder problem is that confident wrong answers are much easier to miss than uncertain ones — the model doesn't hedge, so neither do you.
How do you protect against this in real applications?
You don't rely on the model alone. You cross-reference anything factual, you restrict the model to what it can actually handle reliably, and for anything that affects a real decision you keep a human in the loop. Users also need to know the model's limitations upfront — not in a footnote somewhere.
If you rely on AI to detect AI's problems, what's the flaw?
They have the same blind spots. Same training data, same gaps, same failure modes. It's like proofreading your own work — you skip over the exact mistakes you made because your brain autocorrects them. That's why adversarial testing and external auditing exist: self-evaluation has a hard ceiling.
Which human skills remain essential?
Critical reading — catching when something sounds right but isn't. Domain knowledge — knowing enough to recognize a bad answer. Ethical judgment — understanding that a technically correct output can still be the wrong one to give. And knowing when to stop trusting the output and go verify it yourself.