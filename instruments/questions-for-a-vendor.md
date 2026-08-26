# Questions for a vendor

For anyone evaluating an AI capability or a training contract. Every question
here has a wrong answer that should end the conversation.

Print it. Take it into the meeting.

---

## On training and competency

**1. Show me how you measure competency, not completion.**

Wrong answer: a graduation rate, hours viewed, or enrollments. Those tell you
training occurred. They do not tell you performance improved.

What you want: the same person, measured against the same instrument before and
after, with the change reported.

**2. Whose standard do you assess against?**

Wrong answer: theirs.

What you want: yours. Your [proficiency codes](../reference/proficiency-code-key.md),
your task list, your evaluator.

**3. Can a learner do a capstone in their own environment, with their own
tools?**

Wrong answer: a generic sandbox, or a demo environment that looks nothing like
your systems.

If a vendor cannot give you a simulated, or real, in-your-environment
experience, they do not understand that seat time will not help you. This is the
single fastest disqualifier on the page.

**4. What dashboard do I get?**

You are owed one. What each person is trained in. What they are good at. What
they know. What they do not know.

**5. Who defines success on the outcome metric?**

Wrong answer: the training provider.

Outcome metrics use the existing measures of the workflow itself. If the vendor
defines the measure, they are grading their own work.

---

## On the AI capability itself

**6. Where is the guardrail enforced?**

Wrong answer: in the system prompt, in the model's instructions, or "the model
is trained not to do that".

What you want: enforcement in infrastructure, evaluated before the model's output
is acted on. A constraint the model can choose to ignore is a request, not a
control. See [enforcement](enforcement.md).

**7. When your agent calls a tool on my behalf, whose authority does it run
with?**

Wrong answer: a service account, or the application's own credentials.

What you want: the requester's authority and scope. If a user asks for something
they are not cleared for, the answer must be no, because the request runs as
them.

**8. Is retrieval filtered by role, at retrieval time?**

Wrong answer: filtering after retrieval, or redacting the answer.

When documents become vectors they lose their source permissions. Material a
person was never cleared to see must never enter their context in the first
place.

**9. Is sensitive content removed before ingestion or after retrieval?**

Before. If the model can see it, it can surface it.

**10. Show me the log an authorizing official would read.**

Every tool call, the identity it ran as, the decision, and the rule that produced
it. If there is no such log, there is no governance claim to make.

**11. What does your system do that you cannot verify?**

An honest vendor has an answer. Enforcement is not accuracy, and a vendor who
claims their guardrails make the output correct is confusing two different
things.

---

## On the commercial arrangement

**12. Who owns the data rights to model outputs, and is that settled at award?**

GAO found federal programs that could not use their own model outputs because
this was never negotiated. Settle it before the build, not at the end.

**13. What happens to my corpus?**

Where it is stored, who can reach it, what it is used for, and what happens when
the contract ends.

**14. What is your evidence, and is it yours?**

Vendor telemetry is fine as long as it is labelled as vendor telemetry. A vendor
citing their own numbers as neutral industry fact is telling you something about
how they handle evidence generally.

---

## The one that matters most

**15. Which single workflow should we start with, and why that one?**

A vendor who answers "all of them", or who answers without asking about your
workflows, has not understood the problem.

Run their answer through [the gate](the-gate.md). If their proposed beachhead
fails two of the seven, they picked it for their convenience rather than your
outcome.
