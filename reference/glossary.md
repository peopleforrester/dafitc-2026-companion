# Glossary

The session moved between training vocabulary, acquisition vocabulary and AI
vocabulary. This is every term it used that is not obvious from context.

---

## Training and qualification

**AFSC.** Air Force Specialty Code. The identifier for a career field. Each one
has its own CFETP.

**CFETP.** Career Field Education and Training Plan. The Air Force's training
master document for a career field, containing the Specialty Training Standard
and the proficiency codes for every task. See the [code
key](proficiency-code-key.md).

**STS.** Specialty Training Standard. The task list inside a CFETP.

**JQS.** Job Qualification Standard. What a CFETP becomes once it is placed in
an individual's AF Form 623 training record and used to certify tasks.

**AF Form 623.** On-the-Job Training Record. The individual record where a
trainer and a certifier initial each qualified task.

**UGT.** Upgrade Training. The path to a 3-, 5-, 7- or 9-skill level.

**Go/no-go.** The qualification standard for on-the-job training. "Go" means
the person can perform the task without assistance to local standards for
accuracy, timeliness and correct procedures.

**Core task.** A task a supervisor identifies as required for a duty position.

**Capstone.** A piece of real work in the learner's own environment, with their
own tools, measured against the workflow's existing measures. The proof of a
context-specific outcome.

**DCWF.** DoD Cyber Workforce Framework. The work-role catalog underneath DoDM
8140.03, which now includes data and AI roles.

---

## Doctrine, policy and assurance

**TTP.** Tactics, techniques and procedures. The documented way a unit actually
performs a task, as distinct from general doctrine.

**AFDN.** Air Force Doctrine Note. AFDN 25-1 is the AI one.

**cATO.** Continuous Authorization to Operate. Continuous, infrastructure
enforced monitoring in place of a periodic paper review. Originated in the Air
Force in 2018.

**SWFT.** Software Fast Track. The 2025 DoD CIO initiative replacing the paper
authorization package with automated machine-readable evidence.

**ATO.** Authorization to Operate. The decision that a system may run.

**AO.** Authorizing Official. The person who makes that decision and carries the
risk.

**CUI.** Controlled Unclassified Information.

**DISTRIBUTION A.** Approved for public release, distribution unlimited.

**NSPM.** National Security Presidential Memorandum. NSPM-11 is the June 2026 AI
one.

**DAF.** Department of the Air Force, meaning both the Air Force and the Space
Force.

**DoW.** Department of War. The department renamed from Department of Defense,
so older `defense.gov` links now redirect to `war.gov`.

---

## AI terms as this session used them

**Agent.** A system that decides which tools to call and in what order, rather
than only producing text.

**Agentic.** Describing a system with that property. Often used loosely; ask
what a specific product means by it.

**Autonomy.** How independently a system acts without being asked each time.

**Agency.** How far a system's writes reach. Separate from autonomy, and
conflating the two is how organisations end up at level 5 by accident. See
[levels of autonomy](../instruments/levels-of-autonomy.md).

**Human in the loop.** A person approves each action before it runs.

**Human on the loop.** A person monitors and can intervene, but the system runs
continuously without per-action approval.

**Human out of the loop.** The system acts and the change stands without a
person confirming it.

**Guardrail.** A constraint on what a system may do. The question that matters
is where it is enforced. A constraint stated in a system prompt is a request. A
constraint enforced in infrastructure is a guardrail. See
[enforcement](../instruments/enforcement.md).

**Prompt injection.** Content that reaches a model and is treated as
instruction rather than data. Number one on the OWASP list for LLM applications.

**Jailbreak.** Getting a model to produce output its own guardrails were meant
to prevent.

**Retrieval.** Fetching source material for a model to answer from. **Role-aware
retrieval** filters that material by who is asking, at the moment of retrieval.

**Grounding.** Answering from supplied material rather than from training, with
the source citable.

**Hallucination**, or confabulation in NIST's vocabulary. Output that is fluent
and wrong. Mitigable to a large degree with grounding, retrieval and
verification. Not eliminable by asking a model to be careful.

**RAG.** Retrieval-augmented generation. Grounding, implemented.

**MCP.** Model Context Protocol. A standard way for a model to call tools.

**Deterministic.** The same input gives the same result every time. Models are
not. Rules outside them can be, which is the whole enforcement argument.

**RMF.** Risk Management Framework. NIST AI 100-1 for AI specifically.

**AI-MAP.** AI Maturity Appraisal and Roadmap. Organisational rather than
individual assessment. See the [AI Adoption Maturity
Model](official-documents.md#organisational-maturity).

---

<sub>Reference · [All contents](../README.md) · Next: [Sources](sources.md)</sub>
