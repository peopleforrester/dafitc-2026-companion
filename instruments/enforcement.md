# Enforcement

How to tell whether an agent is constrained by your infrastructure or by the
model's cooperation.

---

## The distinction

**A prompt-level guardrail is probabilistic.** The same input can produce a
different output. The model *chooses* to comply. It can be jailbroken, and it
drifts with every model change.

**An infrastructure-level guardrail is deterministic.** The same rule gives the
same result every time. The action is blocked before the model decides, and every
attempt is logged.

If the only thing stopping an AI from doing the wrong thing is its own promise in
a system prompt, you do not have a guardrail. **You have a request.**

---

## Why this is not a theoretical concern

Guardrails that a model enforces on itself are bypassable at rates that make them
unusable as a control.

Four reasoning models used as autonomous adversaries against nine widely used
target models produced an **overall jailbreak success rate of 97.14 percent
across all model combinations**. Peer reviewed, Nature Communications, February
2026. [S23]

Say that precisely if you repeat it. It is the union across all attacker and
target pairings, not a rate any single model achieved. Per-attacker success
ranged from 90 percent down to under 13 percent.

Separately, a self-prompting attack elicited unsafe output in **more than 90 out
of 100 attempts against the majority of models tested**, with the authors
reporting that guardrails "tend to collapse" under it. Preprint, not peer
reviewed, and two reasoning models from one vendor resisted this specific
prompt. [S24]

You cannot get a language model to reliably guard a language model, for the same
reason you do not rely on a single person to be their own control. If you want
consistency, the enforcement has to sit somewhere the thing being controlled
cannot reach.

---

## What good looks like

The Department already proved this pattern, on itself.

Continuous authorization started in the Air Force in 2018, on the principle that
continuous, infrastructure-enforced monitoring beats a periodic paper review.
Software Fast Track extended it in 2025 with automated, machine-readable evidence
replacing the paper package. [S5] [S6]

The same logic, one layer over: from authorizing software to governing AI
behavior.

DoD defined trustworthy AI in 2020 as five principles: responsible, equitable,
traceable, reliable, and **governable**. Governable means the system detects
unintended behavior and can disengage on command. [S3] [S4]

Governable in practice means enforced by infrastructure.

---

## What to ask for

- Is the rule evaluated **before** the model's output is acted on, or after?
- Is the decision **logged** in a form an authorizing official can read?
- Does the tool call execute with **the requester's authority and scope**, not
  the application's? An agent acting on your behalf must be bounded by your
  clearance, not by a service account.
- Is retrieval filtered **at retrieval time**, by role? When documents become
  vectors they lose their source permissions, and a system without role-aware
  retrieval will surface material a user was never cleared to see. [S18]
- Is sensitive content removed **before ingestion**, rather than after retrieval?
- Does it map to the risk framework and control catalogue you already operate
  under? [S19]

---

## What it does not do

Enforcement stops unauthorized actions. It does **not** verify that the advice
was correct.

**Enforcement is not accuracy.** Anything that claims otherwise is selling you
something.

---

## If you need to implement this

This page argues the principle and gives you the questions. It does not give you
policies you can apply.

**Agentic Covenants** does: six matrices mapped to the six NIST CSF 2.0
functions, ninety-three cells, with working Kyverno policies, RBAC, Falco rules
and kill-switch runbooks. Free, no dependencies, and its thesis is the same as
this page's, that governance is enforced by infrastructure rather than by prompt.

https://github.com/peopleforrester/agentic-covenants

The CSF 2.0 mapping is the useful part for a federal reader: it lands the
argument in a framework your assessors already use.

Source numbers refer to [the source list](../reference/sources.md).
