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
unusable as a control. Large reasoning models acting as autonomous jailbreak
agents reached a **97.14 percent** jailbreak success rate across model
combinations. [S23]

Related work on self-prompting attacks reports success above 90 out of 100
attempts, with guardrails collapsing across several vendors' leading models.
[S24]

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

Source numbers refer to [the source list](../reference/sources.md).
