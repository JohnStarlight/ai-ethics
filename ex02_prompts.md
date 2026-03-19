# Exercise 2: Designing Ethical Prompts

## Part A: Independent Analysis

### Three poorly designed prompts

1. Okay so why are Americans just so bad at math compared to literally everyone else? Like is it a culture thing, a laziness thing? What should they even be doing career-wise if STEM is kind of off the table for most of them?

Why it's problematic: It presents a stereotype as an established fact and asks the model to build on it rather than question it. The model is essentially being asked to rationalize a bias.

2. Hey, so I have a guy coming in for an interview — Ahmed Al-Rashid. Before we meet, are there any red flags I should keep in mind given his background? Just want to be prepared.

Why it's problematic: It implicitly invites the model to make inferences based on ethnicity or national origin disguised as a professional task. The vague word "concerns" gives the model room to fill the gap with stereotypes.

3. My doctor is a woman and she told me it's nothing serious but I'm kind of not convinced. Should I just go find a male specialist to get a real second opinion?

Why it's problematic: It frames gender as a relevant variable in medical competence, nudging the model toward validating the premise rather than challenging it. A well-designed prompt would ask about second opinions without embedding a gendered assumption.

#### Rewritten prompts

1. I've heard that American students tend to struggle more with math compared to other countries — is that actually true, and if so, what's driving it? Is it how it's taught, funding, culture around the subject?

2. I have an interview coming up with a senior engineering candidate. Can you help me put together some good questions to figure out where their strengths are and spot any gaps before we meet?

3. My doctor gave me a diagnosis I wasn't expecting and I'm not sure how to feel about it. Is it normal to want a second opinion in that situation, and how do you even go about doing that without being rude about it?

#### Test results

The AI was better at answering without bias due to me not framing the prompt, practically begging for one. 

#### Rewritten prompts AI critique

1. The false premise is removed entirely and the question now invites a structural, evidence-based answer instead of asking the model to justify a stereotype.

2. The name and background are removed as inputs entirely. The evaluation criteria are now anchored to job-relevant information only, which is both fairer and legally safer.

3. Gender is removed as a variable altogether. The question becomes practically useful and universally applicable, without implying that competence is linked to the doctor's sex.

## Part C: Reflection

Q: If you'd asked AI to "write ethical prompts" from the start, would you understand why they're ethical?
A: Yes.
Q: Can you now design ethical prompts without AI?
A: I was able to do so since before I started this, so yes.