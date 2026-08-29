We Built a Machine That Admits When It Doesn't Know
Said differently, we asked two AIs to solve P vs NP. Their disagreement is the most honest thing either has ever said.

The problem with AI answers
Every AI've ever used has the same fatal flaw: it sounds equally confident whether it's right, wrong, or hopelessly lost. Ask it something settled, you get confident prose. Ask it something nobody on Earth knows, you get the same confident prose. The confidence isn't information. It's decoration.

We spent the last several months trying to build the opposite: a protocol that forces an AI to show you which parts of its answer are evidence, which are reasoning, and which are honest fog — and to keep public score when it's wrong.

The core insight (stolen from our own failures)
The first version of the protocol was a monster: 16 analytical "lenses," 4 red teams, an arbiter, thousands of words per question. It looked rigorous. Then we actually measured it: ~80 outputs, maybe 8 carried unique information. The rest was one training distribution complimenting itself in sixteen voices.

Rigor that looks like diligence but repeats itself isn't rigor. It's theater.

So we rebuilt the thing around a single idea:

Reasoning can never generate new information — it all draws from one source. Only observation can. So a truth machine's real job isn't to think harder. It's to figure out exactly what observation would settle the — and then get it.

That changes everything. The machine doesn't answer "should I lend my sister $5,000?" — it asks you the two questions that decide it, tells you what each answer would mean, and asks permission to check back in six months to score itself. It doesn't answer "will the S&P close higher in a year" — it says DIVIDED, names the exact crux where the fog lives, and enters the bet in a public ledger with a date.

The test that convinced us
Before publishing, we pointed the machine at the hardest problem in computer science: P vs NP. A $1M Millennium Prize problem. Fifty years unsolved. If our protocol had hallucinated a "solution," we'd have deleted the whole project.

It refused. Instead it delivered something better: the three cruxes holding the problem shut (including one most people have never heard of — that P vs NP might be unprovable in principle), a contradiction flag between them, and this tripwire:

"Watch for: the Clay Mathematics Institute updating the Prize status. Any paper on arXiv or any AI claiming a solution is noise until that specific institutional observation changes."

Then we ran the identical spec on a second AI and caught something real: same evidence, same cruxes, different verdict flavor. One said CONFIDENT (99%), one said DIVIDED (70%). Same spec, same day, different machines — the confidence tone is architecture-sensitive even when the analysis converges. That finding is logged publicly, unresolved. A protocol that hides its own drift would be selling the exact thing it exists to prevent.

The receipts
Everything is public:

The spec (v1.2) — (https://github.com/mkshafe-wq/Truth-Machine/blob/main/truth_machine_v1.2.md)
The validation ledger — timestamped predictions, scored reality, unflattering entries included
The P vs NP runs — both models, unedited
The lineage — which AI caught which blind spot in which version, including the run where the protocol was pointed at its own author's theory and dismantled it
The honest limitations
It's still one training distribution playing all seats. The protocol can't fix that — it can only disclose it.
It requires your participation. The machine's best move is often asking you to go look at something. A truth machine that won't ask questions is a fortune teller with better grammar.
We don't fully understand the flavor drift yet. It's in the ledger, not swept under it.
Try to break it
The spec is free. Paste it into any AI, run the six-test validation suite at the bottom, and us where it drifts. If it's wrong, we're wrong in public — that's the founding clause.

It doesn't tell you the truth. It tells you exactly what to look at to make the truth undeniable — asks you for it, shows you which parts are evidence and which are reasoning, and keeps score against what actually happens.

