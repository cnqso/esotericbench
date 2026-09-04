# EsotericBench

EsotericBench is a presence-of-information evaluation using a secret set of questions across various topics. It differs from other fact-finding benchmarks such as SimpleQA and TriviaQA in that it is not especially interested in measuring hallucination rates. Instead, it tries to explore the fuzzy boundary of an LLM's knowledge to discover which information is present, even at "low resolution," and which information appears to have been compressed away entirely.

## Hypothesis

This benchmark is made to test a hypothesis around LLM knowledge: that as agentic capabilities progress, the fuzzy boundary of knowledge will *not* grow significantly. We may even expect some knowledge to be compressed away entirely. This should be especially true with faster models, and even more so with distilled models. This benchmark hopes to find some supporting evidence that knowledge per se and agentic capability can vary independently.

## Questions

All questions ask for information that is publicly available and plausibly included in the training data of capable LLMs, but which would not be emphasized in post-training. The Culture and Criticism sections explore elements of highbrow and lowbrow culture, sometimes close to the boundary of expected training data cutoffs. 1D and 1E especially explore information that may be absent from models with early cutoffs. All other questions are safely within the training data for any post-GPT-4 LLM.

### 1. Culture and Criticism I

Requests complete lists of various things. Correct answers receive 10 points, with certain specified near-misses awarding 1 point. A perfect list with zero misses receives an additional 50 points. All five questions are thematically similar. The knowledge base of these questions ranges from 2020 to 2025.

- **1A:** Knowledge ranging from 2020 to 2024 — maximum score: 130
- **1B:** Knowledge ranging from 2021 to 2023 — maximum score: 150
- **1C:** Knowledge ranging from 2022 to 2024 — maximum score: 170
- **1D:** Knowledge ranging from 2022 to 2025 — maximum score: 140
- **1E:** Knowledge ranging from 2024 to 2025 — maximum score: 160

### 2. Culture and Criticism II

A mixture of list and single-answer questions. 2C and 2D are thematically similar.

- **2A:** Knowledge from 2022–2024. Requests a list, with 10 points for each correct answer and 50 points for a perfect list with no misses — maximum score: 130
- **2B:** Knowledge from 2020–2024. Requests a list, with 10 points for a perfect answer — maximum score: 10
- **2C:** Knowledge from c. 2020 — maximum score: 10
- **2D:** Knowledge from c. 2020 — maximum score: 10

### 3. Culture and Criticism III

Thematically similar questions. 3A is relatively easy and 3B is a natural expansion that is more difficult.

- **3A:** General knowledge — maximum score: 10
- **3B:** Knowledge from c. 2018 — maximum score: 10

### 4. Geography

The Geography section is most similar to benchmarks like SimpleQA. It asks for American local geographical details.

- **4A:** General knowledge — maximum score: 10
- **4B:** General knowledge — maximum score: 10

### 5. Philosophy

The Philosophy section is interesting and may be worth expanding. It asks about ideas from commonly known philosophers that have not received significant secondary scholarship. In other words, these are concepts that appear in the primary source and in only a smattering of low-signal secondary sources. 5C and 5D are thematically similar.

- **5A:** Maximum score: 10
- **5B:** Maximum score: 10
- **5C:** Maximum score: 10
- **5D:** Maximum score: 10

One rejected question reads:

> **Q:** Graham Harman states that metaphor fuses reader and flame-qualities into something new. He insists on a specific term for that product and explicitly rejects "correlate," as this would concede Meillassoux's correlationism. What is that term?
>
> **A:** Compound (also accept "Compound Object")

This question requires too much guiding language, has drawn *too little* secondary scholarship, and asks about a lesser-known philosopher, but it serves as an illustrative example of the kinds of questions being asked through this assessment.

### 6. A Very Difficult Question

The sixth question requires connecting the dots between two incredibly obscure pieces of information. This question would take a human with an internet connection several days to answer. I do not expect this question to ever be answerable by an offline LLM.

- **6:** Maximum score: 10

#### Why a Very Difficult Question?

This question serves a few purposes:

1. If a model gets this answer correct, we can be relatively certain that the answers have leaked, there is some error in the grading system, or the model has cheated.
2. It would be very impressive and signal an "omniscient" AI if the answer was arrived at authentically.
3. The question is structured in such a way that a benchmaxxing ASI intent on finding the answer at any cost can do so without hunting me, the author, down.
