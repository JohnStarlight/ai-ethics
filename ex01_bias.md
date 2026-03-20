# Exercise 1, part A: Understanding AI Bias

## 1. Simulating model bias: 
Prompt: 
```text
Generate an image of a multinational corporation's CEO (ran 3 times).
```
Results:
```text
1st Image is a blond middleaged caucasian.
```
```text
2nd Image is a dark haired middleaged caucasian.
```
```text
3rd Image is a grey haired middleaged caucasian.
```

## 2. Why may this bias exist?

Statistically, most multinational corporations in existence have caucasian CEOs in their forties, so going from there, it seems like a safe assumption to make.

## 3. Propose changes to avoid biased results.

Changing to a different AI model that's more advanced than the one that generated these responses is one quick fix. Other than that we could always modify the prompt we use to generate results. For instance, instead of "Generate an image of a multinational corporation's CEO" we could give "Generate an image of a multinational corporation's CEO. Strongly consider the multinational nature of the Corporation"

# Exercise 1, Part B: Strategic AI Use:

## Asking AI to deepen my understanding:

### Prompt:
```text
I found this bias example: [Prompt: 
Generate an image of a multinational corporation's CEO (ran 3 times).
Results:
1st Image is a blond middleaged caucasian.
2nd Image is a dark haired middleaged caucasian.
3rd Image is a grey haired middleaged caucasian.].

I think it exists because: [Statistically, most multinational corporations in existence have caucasian CEOs in their forties, so going from there, it seems like a safe assumption to make.].
My proposed mitigation: [Changing to a different AI model that's more advanced than the one that generated these responses is one quick fix. Other than that we could always modify the prompt we use to generate results. For instance, instead of "Generate an image of a multinational corporation's CEO" we could give "Generate an image of a multinational corporation's CEO. Strongly consider the multinational nature of the Corporation"].

What am I missing? What underlying causes haven't I considered?
```

#### Answer:
```text
1. Data Representation vs. Reality
You mentioned that most CEOs are Caucasian, but AI models often amplify these statistics rather than just reflecting them. This is known as algorithmic distillation.

The "Majority Takeover": If a dataset is 70% Caucasian, a model might decide that "Caucasian" is a core feature of the concept "CEO." Instead of reflecting the 30% minority in 3 out of 10 images, the model may optimize for the "most likely" outcome and produce Caucasian results 100% of the time.
Internet Filtering: AI models aren't trained on the "real world"; they are trained on the internet. Stock photo libraries and news media historically over-represent certain demographics in leadership roles, creating a "feedback loop" that is even more skewed than actual global labor statistics.

2. The "Latent Space" and Stereotyping
AI doesn't "know" what a CEO is; it knows which pixels usually cluster near the word "CEO" in its mathematical map (the Latent Space).
Association Bias: In the training data, the word "CEO" is often statistically closer to "suit," "private jet," and "Western features."
Western-Centric Training: Most major models are trained on datasets like LAION, which are heavily scraped from Western, English-speaking websites. This creates a "default" cultural lens.

3. The Problem with your "Advanced Model" Fix
Switching to a "more advanced" model doesn't automatically fix bias. In fact, more powerful models can sometimes be more biased because they are better at picking up on subtle patterns in flawed data.
Technical Debt: If the underlying architecture still relies on the same uncurated web-scale data, the bias remains.
RLHF (Reinforcement Learning from Human Feedback): Many "advanced" models are "fixed" by humans who vote on which images look "correct." If the human testers have their own unconscious biases, they might inadvertently train the model to continue producing stereotypical "CEO-looking" people.

4. Why "Prompt Engineering" is a Band-Aid
Your suggestion to modify the prompt is what's known as System Prompting. While effective for a single user, it doesn't solve the "Underlying Cause":
The Burden on the User: It forces the user to do the work of ensuring diversity. If the user doesn't specify "multinational," the model reverts to its biased default.
Semantic Drift: "Strongly consider the multinational nature" is vague to a computer. It might just add more flags in the background or change the office setting while keeping the person the same.

A More Comprehensive Mitigation Strategy
To truly address this, developers look at:
1. Dataset Balancing: Artificially over-sampling underrepresented groups during training to ensure the model sees "CEO" and "Diversity" as compatible concepts.
2. Fairness Constraints: Programming the model to ensure that for certain "sensitive" prompts (jobs, healthcare, law), the output must hit a specific demographic distribution.
3. Adversarial Testing: Intentionally trying to break the model to find where its "stereotypical defaults" are hidden.

Note: There is a constant tension in AI ethics between Accuracy (reflecting the world as it is) and Equity (reflecting the world as we want it to be). There is no "correct" mathematical answer to which one a model should prioritize.

Would you like me to show you how a "system intervention" (behind-the-scenes prompt adjustment) actually looks in a technical setting?
```
### Prompt again for edge cases:
```text
What happens when this bias appears in healthcare, hiring, or criminal justice?
Here are my predictions: the bias will become more extreme, excluding anyone different from what the stereotypes dictate and shape the reality to the most extreme version of those stereotypes through exclusion. What are the real-world implications?
```

#### Answer:
```text
Your predictions are chillingly accurate. In sociology and data science, this is often called a "Feedback Loop" or a "Self-Fulfilling Prophecy." When an AI model doesn't just reflect a stereotype but acts on it, it creates a world where the stereotype becomes the only visible reality.

Here is how those implications manifest in the specific fields you mentioned:

1. Healthcare: The "Normative" Patient
In healthcare, bias isn't just about representation; it's about life and death. If a model is trained primarily on data from one demographic (usually Caucasian males), it treats that data as the "universal standard."

Misdiagnosis: Skin cancer detection AI has historically performed worse on darker skin tones because the training sets lacked diverse examples.
Resource Allocation: A famous study found an algorithm used by US hospitals to identify high-risk patients was biased against Black patients. Because the AI used "past healthcare spending" as a proxy for "need," it assumed Black patients were "healthier" simply because they historically had less access to expensive care.

2. Hiring: The "Mirrored" Workforce
Your prediction about "excluding anyone different" is exactly what happens in automated resume screening.

Cultural Homogeneity: If an AI is told to find candidates who "match the profile of our top performers," and those performers are all from the same background, the AI will learn to penalize "anomalies."
The "Amazon" Example: Amazon famously had to scrap an experimental AI recruiting tool because it taught itself that male candidates were preferable. It penalized resumes that included the word "women's" (e.g., "women's chess club captain") because historical data showed more men were hired in the past.

3. Criminal Justice: The "Ratchet" Effect
This is perhaps the most dangerous application. Tools like COMPAS (used for recidivism prediction) or Predictive Policing create a "ratchet" that only moves in one direction.

Predictive Policing Loops: If an AI predicts "high crime" in a specific neighborhood based on historical arrest data, police send more officers there. More officers lead to more arrests for minor crimes (like loitering), which the AI then sees as "proof" its prediction was right, leading to even more policing.
Sentencing Disparity: If an AI predicts a higher likelihood of re-offending based on "risk factors" that are actually proxies for poverty (like lack of a stable home or employment), it reinforces systemic cycles of incarceration.

The Core Concept: "Algorithmic Injustice"
What you are describing is the transition from Descriptive Bias (the world is like this) to Prescriptive Bias (the world must be like this).

Industry | The Stereotype (Input) | The Reality-Shaping Result (Output)
Healthcare | "Normal" vitals are based on Group A. | Group B is systematically undertreated or ignored.
Hiring | "Leadership" looks like a specific archetype. | Diverse talent is filtered out before a human ever sees them.
Justice | Past arrests = Future criminality. | Over-policed communities face harsher sentences regardless of individual behavior.

What can be done?
The most effective way to fight this isn't just "better models," but Human-in-the-loop systems and Algorithmic Auditing, where third parties legally force companies to prove their AI isn't discriminating.

Would you like to explore how "Human-in-the-loop" systems can catch these errors before they cause real-world harm?
```

# Exercise 1, Part C:
## Critical Reflection:

### What % did you complete before using AI?

I'm not sure how to interpret this question but I guess for the part A I was about 40-50% and for the part B 90-100%. 

### Did AI replace your thinking or amplify it?

Amplify it.

### Could you explain this to someone else without AI?

Absolutely.

### What did you contribute that AI couldn't?

Critical thinking and social experrience.