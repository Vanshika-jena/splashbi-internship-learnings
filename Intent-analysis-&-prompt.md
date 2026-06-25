#Intent analysis and Prompt Engineering
## What is Intent Analysis in NL-to-SQL
When a user asks a question in plain english, the system needs to figure out *what kind* of question it is before generating SQL. 
This is intent analyis: Classifying the user's query so the right logic, prompt, and response format can be applied. W
Without intent routing, every query gets treated the same way. With it, the system can handle fundamentally different types of questions - each needing a different approach.

---

### Drill down
**What it is:** When a user sees a result and wants to go deeper into a specific part of it. Example - "Show me sales by region" followed by "break down of west region further."
**Why it needs its own prompt:** The system needs to understand that this is a *continuation with deeper granularity* - not a fresh query. It needs contect from the previous result to know what to drill into.
**What I did:** Gave the prompting logic for drill activation

---

### RCA — Root Cause Analysis
**What it is:** When a user asks *why* something happened rather 
than *what* happened. For example — "why did sales drop in Q3?" 
rather than "show me Q3 sales."

**Why it needs its own prompt:** This is the hardest intent. The 
AI needs to shift from data retrieval to analytical reasoning — 
identifying contributing factors, not just fetching numbers. The 
SQL and the response structure are both different.

**What I did:** RCA was a bit different as it was more analytical reasoning that data retrieval. I wrote the rca schema file and the rca intent for it too

---

### Continuation Analysis
**What it is:** When a user asks a follow-up question that builds 
directly on the previous one. For example — "now show me the same 
data for last year" after a current year query.

**Why it needs its own prompt:** The system needs to carry forward 
context from the previous exchange — same filters, same dimensions 
— while applying the new modification the user asked for.

**What I did:** Made the prompt which made sure that to is_continuation happened

---

## What I Learned About Prompt Engineering

**Iteration is everything**
No prompt works perfectly on the first try. Each of these features 
went through multiple versions before the output was consistent.

**Intent clarity drives output quality**
The more precisely the prompt defines what kind of response is 
expected, the more reliably the model produces it. Vague prompts 
produce vague outputs.

**Context dependency is the hardest problem**
Drill down and continuation both depend on what came before. 
Managing that context — what to pass forward, what to drop — is 
where most of the prompting complexity lives.

**Small wording changes produce big output differences**
[One specific example of a wording change you made and how it 
changed the output — even roughly]

## Broader Observation

Working across four different intents showed me that NL-to-SQL 
isn't one problem — it's a family of problems. Each intent type 
has its own failure modes, its own prompt structure, and its own 
definition of a "correct" output.

That's what makes building these systems hard, and what makes 
evaluation of LLM outputs genuinely difficult — there's rarely 
one right answer.
