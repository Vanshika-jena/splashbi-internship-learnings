A personal knowledge repository documenting everything I understood, built, and observed during my internship at SplashBI(June 2026), this happened after my first year of BTech.
This repo contains no confiedential code or proprietary information. 

## What is splashBI?
SplashBI is an analytucs platform enhanced by AI capabililites, offering conversational insights. and advanced analytics.

## what i worked on
**Pivot table feature**
Extened SplashAI's existing chart response system. When a user asks 
a query and the AI responds with a chart, there was already a feature 
showing the SQL behind it. I added a new feature — if the user asks 
for a pivot table, the AI now generates one from that same query. 
Built through prompt engineering.

**Schema Analysis & Fixes**  
Analyzed schema files across four enterprise modules — Workforce, 
General Ledger, Recruitment, and Receivables — identifying structural 
issues affecting SQL generation quality. Delivered fixes across 
categories like naming inconsistencies, missing relationships, and 
incorrect mappings.

**RAG System Exposure**  
Observed and studied SplashBI's production RAG pipeline powering 
SplashAI — understanding how retrieval and generation work together 
in a real NL-to-SQL product.

**Cross-team Knowledge Transfers**  
Participated in KTs with every major team — AI Engineering, Backend, 
Frontend, DBA, QA, CloudOps, and DevOps — to understand how each 
role contributes to a production AI product.


## Technologies & Concepts

| Area | Stack |
|------|-------|
| AI/ML | RAG, NL-to-SQL, Prompt Engineering, LLMs, Schema Design |
| Languages | Python, SQL |
| Frontend | React, Angular |
| Backend | Java |
| Databases | Oracle, MySQL, PostgreSQL |
| QA | Playwright, LoadRunner |
| DevOps | Git, Jenkins |
| Cloud | CloudOps (infrastructure & deployment) |

---

## Repo Structure
/learnings

rag-systems.md         — RAG concepts and what I saw in production

nl-to-sql.md           — How NL-to-SQL works and schema design

schema-design.md       — Schema files, issues found, fixes made

pivot-table-feature.md — The feature I built, end to end

/reflections

sdlc-observations.md   — How real product teams work together

week-by-week.md        — Brief notes from each week

---

## Why I Made This

I joined SplashBI after my 1st year with basic Python knowledge and 
no real sense of how AI products are built in production. 5 weeks 
later I had seen a live RAG system, shipped a feature, analyzed 
enterprise schemas across four business domains, and sat in rooms 
with engineers across every team in a software company.

This repo exists so I don't forget what I learned — and so I can 
build on it properly going into 2nd year.

---

## What's Next

Building the technical depth to match the context I gained here —
starting with a RAG Q&A system and an agentic NL-to-SQL project, 
both from scratch.

*Vanshika | CS Undergrad, KIIT University | 2nd Year*

