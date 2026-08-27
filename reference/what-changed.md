# What changed, and what to stop repeating

Things that were true recently and are not any more, plus two claims in wide
circulation that do not survive checking. Each was verified while building this
repository.

If you are carrying slides, a policy reference or a talking point from the last
eighteen months, check it against this page.

---

## Retired or replaced

**NIPRGPT was sunset on 31 December 2025.** GenAI.mil launched 9 December 2025.
Any material naming NIPRGPT as the Department of the Air Force generative AI
platform is out of date.

**AFI 36-2201, Air Force Training Program, is rescinded.** The governing
authority is now **DAFMAN 36-2689, Training Program**, which covers the
proficiency codes, core-task identification, on-the-job training and the AF Form
623 record. Copies of the 2010 AFI still circulate on unofficial mirrors and
still appear in search results.

**The department renamed to Department of War.** Older `defense.gov` addresses
now redirect to `war.gov`. Check any DoD citation you are carrying forward.

**The November 2023 DoD Data, Analytics and AI Adoption Strategy was displaced**
by the Artificial Intelligence Strategy for the Department of War, 9 January
2026.

**DAFI 36-2670, Total Force Development, has been hollowed out** by interim
changes. Training moved to DAFMAN 36-2689, enlisted developmental education to
DAFI 36-2685, voluntary education to DAFI 36-2681. Cite the children rather than
the parent.

---

## Changing now

**Some career fields are migrating off the numeric proficiency scale.** A
behavioural-statement coding system using P for performance, K for knowledge and
pk is replacing the 1-2-3-4 and A-B-C-D key in some CFETPs. Anything anchored on
the numeric key, including [the code key here](proficiency-code-key.md), should
say which generation it assumes. Check your own CFETP.

---

## Two claims that do not survive checking

### The ordering bot that did someone's homework

**It did not happen.** The viral claim was that a fast-food customer-service
assistant was tricked into debugging Python instead of taking an order. An
internal investigation found no evidence, the circulating screenshots and videos
are believed fraudulent, and the company does not have an AI customer assistant
in its app. A near-identical version at another chain was confirmed Photoshopped
by that company.

[Fast Company, 24 April 2026](https://www.fastcompany.com/91532091/mcdonalds-ai-bot-didnt-go-rogue)

**This affects the deck in this repository.** The speaker notes on slide 25 tell
that story as a real example. The deck is published as it was delivered rather
than quietly corrected, so the correction lives here instead. If you reuse those
notes, cut that passage and use S23 or S24.

The vulnerability class is real. That story is not evidence of it. For real
evidence use [S23 or S24](sources.md).

The documented ordering-bot failure people are sometimes thinking of is a
drive-thru voice system gamed into accepting an absurd order, which is a
denial-of-service by input rather than a capability leak. Different failure mode.

### The 95 percent of AI pilots that deliver nothing

The figure comes from MIT Project NANDA's *The GenAI Divide*. Two things about
it.

**The report was withdrawn.** Its original address served the PDF until 18 August
2025, then 404, and now redirects elsewhere. Only an archived copy is citable.

**The authors hedged it themselves**, verbatim: "These figures are directionally
accurate based on individual interviews rather than official company reporting."
The sample was 52 structured interviews. It is not peer reviewed.

The failure *mode* the report describes, generic tools bolted onto workflows
nobody redesigned, is well supported and worth citing. The headline number is a
directional estimate and should not be presented as a measurement.

---

## Precision on figures worth quoting

**The 97.14 percent jailbreak rate** is the union across all attacker and target
model combinations in that study, not a rate any single model achieved.
Per-attacker success ranged from 90 percent down to under 13 percent. [S23]

**The "more than 90 out of 100 attempts"** figure counts attack *attempts* in
which at least one unsafe output appeared among ten responses. It is not a
per-response rate, and two reasoning models from one vendor resisted that
specific attack. [S24]

**BCG's 10/20/70 is effort allocation, not budget.** Several secondary write-ups
render it as budget. BCG's own sentence says efforts.

**GenAI.mil user counts are an official self-report, not an audited figure.**
Say "nearly 1.7 million" rather than rounding, and date it.

---

<sub>Reference · [All contents](../README.md) · Next: [Glossary](glossary.md)</sub>
