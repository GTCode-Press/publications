# What Did the Proof Buy Us?

> Formal verification, AI, and the price of confidence

**Author:** GTCode.com
**Published:** November 11, 2026
**Canonical URL:** https://gtcode.com/articles/what-did-the-proof-buy-us/
**Section:** Articles
**Rights:** All rights reserved. Linking is permitted. Republishing or redistributing our original content requires prior written permission. Attribution alone does not grant permission. [Content-use policy](https://gtcode.com/policies/content-use/).

---

I had 49 proof groups and six checkers. I knew which checks passed and how the proof suite was wired into the build. But I couldn't find a cumulative record of implementation bugs the proofs had exposed, if any.

This was an existing Elixir/OTP ledger system. The verification work had real technical substance. What bothered me was how thoroughly we could account for completed proofs, and how poorly we could account for what we'd learned about the code that actually runs.

A missing findings ledger doesn't mean the work found no bugs. It means we hadn't made that question part of the job. As AI makes proof production easier, I suspect we'll see this problem well beyond one project.

## When proofs earn their keep

For software still being built, the payoff can come early. A proof might expose contradictory requirements or an unsafe state transition while the design is still cheap to change. Maybe that saves a week of debugging. Maybe it gives the developer enough confidence to tackle a difficult change sooner. If it shortens the path to working software, formal verification has done something useful. That doesn't require a spectacular bug-fix commit. Some mistakes never get written.

An existing payment or safety-critical system is a different proposition. There may be failures so costly that narrowing the uncertainty around them is worth a serious investment. But the claim has to survive contact with the real implementation. Proving a tidy model of an OTP process says little about races in the running application if the model omits timeouts, stale task replies, or journal acknowledgments. A bounded search over a few schedules is valuable evidence within its bounds, not a general proof about every schedule on the BEAM.

And if a proof finds no defect, it hasn't made unchanged code safer. It has changed what we can reasonably believe about that code. Perhaps that lets us ship something we were afraid to ship, avoid an unnecessary safeguard, or rule out a failure that would have been disastrous. That's worth money. The question is how much, and what decision the new knowledge changes.

## Big software, small consequences

Here is the category I worry we'll spend a fortune on: large, established systems that are expensive to verify but not especially expensive to fail.

A sprawling back-office application might contain hundreds of thousands of lines of code, use a dozen services, and have more edge cases than anyone wants to count. None of that tells us what happens when it breaks. Maybe operations can restore the last good state within an hour. Maybe the work affected is reversible. Maybe failures are rare and the existing tests already catch most of the costly ones.

Imagine one particular failure would cost $100,000, with an estimated 5% chance of happening in a given year. That's $5,000 in expected annual loss, or about $15,000 over three years before discounting. Even a fictional, perfect intervention that prevented every instance of that failure wouldn't justify a $250,000 verification project on that risk alone.

Those are illustrative numbers, not estimates for any actual software. There may be other serious failures we haven't counted, and the probability estimate could be wrong. Fine: investigate those uncertainties. But don't replace a rough economic argument with the observation that the codebase is large. Complexity tells us verification will be hard. It doesn't tell us the cost will be worth paying.

Sometimes the value comes from faster development, reduced testing, or a safer migration. Put those savings in the calculation if we can support them. And count the full cost: writing and reviewing the specification, checking that the model still matches the code, investigating counterexamples, and repairing proofs when the implementation changes. It's possible to own a beautifully maintained proof suite that has stopped saying much about production.

## Cheap proofs, expensive habits

AI is making specifications, model-checking experiments, and proof sketches cheaper to produce. Used well, that opens doors. It also makes it awfully easy to fill a repository with theorems for no better reason than that we can.

I expect the next twelve months to bring some impressive verification dashboards attached to rather weak business cases. Those teams will be able to report how many proofs passed. The harder questions are which decisions changed, and whether targeted tests plus a few carefully chosen properties would have bought nearly the same assurance for much less.

And generating a proof isn't the same as owning it. Someone must understand the assumptions, distinguish a toy counterexample from a reproducible production defect, and maintain the argument as the code evolves. AI may reduce some of that effort; it doesn't make the responsibility vanish.

A second temptation follows when the work finds no defect: rewrite the implementation so there's something visible to deliver. That's backwards. If verification exposes a genuine bug, fix it and keep the regression. If it reveals a missing requirement, establish that the requirement matters before changing code. If the implementation satisfies the property we cared about, leave it alone. Making unnecessary changes to justify the proof budget only adds another place for bugs to hide.

## Give the next proof a budget

For an established system, I'd start by naming the failures we're afraid of. I'd write down their likely impact, how often we think they might occur, the evidence from tests and incidents, and the specific claim a proof could settle. I'd also be explicit about what the proof *cannot* say about the running system. Then I'd authorize a small, time-boxed investigation, not a promise to verify the whole repository.

At the end of that first tranche, the review should be about evidence and cost. Which counterexamples reproduced in production? Which guarantees now hold, and under what assumptions? Did anything get faster to develop? What did the work cost, including the maintenance we're signing up for? If we cannot make a credible case that the next tranche is worth more than its build and maintenance cost over a stated horizon, stop. Revisit the decision if the system's exposure changes.

Zero defects discovered may be excellent news. I still need to be able to explain why the work was worth buying. If I can't, adding another hundred proofs won't solve that problem.

---

## How to Cite

**BibTeX:**

    @article{gtcodecom2026whatdidproof,
      author  = {{GTCode.com}},
      title   = {What Did the Proof Buy Us?},
      journal = {GTCode.com Articles},
      year    = {2026},
      month   = nov,
      url     = {https://gtcode.com/articles/what-did-the-proof-buy-us/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/articles/what-did-the-proof-buy-us}}
    }

**APA:**
GTCode.com (2026, November 11). What Did the Proof Buy Us?. *GTCode.com Articles*. https://gtcode.com/articles/what-did-the-proof-buy-us/ (Archived at https://github.com/GTCode-Press/publications/tree/main/articles/what-did-the-proof-buy-us)

**Chicago:**
GTCode.com. "What Did the Proof Buy Us?." *GTCode.com Articles*, November 11, 2026. https://gtcode.com/articles/what-did-the-proof-buy-us/. Archived at https://github.com/GTCode-Press/publications/tree/main/articles/what-did-the-proof-buy-us.
