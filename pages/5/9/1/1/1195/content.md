Minimal logic, introduced by I. Johansson in 1936, is [[intuitionistic logic]] without the _ex falso quodlibet_ rule $\bot \vdash A$.  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for classical logic and restricting to sequents $\Gamma\vdash\Delta$ where $\Delta$ must contain _exactly one_ formula.

Because it is not the case here that
anything follows from a contradiction, minimal logic is a
[[paraconsistent logic]].

Models of minimal logic are cartesian closed categories, optionally
with finite $n$-ary coproducts for $n\gt 1$.  Under the [Curry-Howard
correspondence](http://en.wikipedia.org/wiki/Curry-Howard_correspondence) minimal logic corresponds to [simply-typed lambda
calculus](http://en.wikipedia.org/wiki/Simply-typed_lambda_calculus), which is roughly speaking another way of saying that both are forms of the [[internal logic]] of [[cartesian closed category|cartesian closed]] categories.

+--{: .query}
Finn, I\'m unsure of what exactly is supposed to be 'minimal logic'.  Does [this unreadable reference](http://projecteuclid.org/DPubS?verb=Display&version=1.0&service=UI&handle=euclid.ndjfl/1093870451&page=record) match your understanding?  To wit: two connectives ($\Rightarrow$ and $\bot$, with $\neg{p}$ defined as $p \Rightarrow \bot$), two axiom schemes ($p \Rightarrow q \Rightarrow p$ and $(p \Rightarrow q \Rightarrow r) \Rightarrow (p \Rightarrow q) \Rightarrow p \Rightarrow r$) and modus ponens.  Note in particular no characterisation of $\bot$ whatsoever (which strikes me as a little too minimal).

I think that I thought that minimal logic did not have $\neg$ or $\bot$ at all; that seems like a more reasonable amount of minimality to me.  Also, it seems that your first paragraph fits the above reference better, while your last fits better the version with no negation at all.  But I may be missing something.  ---[[Toby Bartels]]

[[Mike Shulman|Mike]]: I've definitely seen "minimal logic" used to mean logic that has $\bot$ and $\neg$ but no rule $\bot\vdash A$.

_Toby_:  Possibly I was just thinking of the wrong thing when I created the links here; it doesn\'t seem so interesting anymore.  (^_^)  Well, no point changing it now.

_Finn_: I too have seen minimal logic presented using $\neg$ and $\bot$.  I don't have my van Heijenoort with me, but I think Hilbert gave a definition of such a system in the early 1920s.  Johansson was the first to call it 'minimal logic', although I can't remember whether he included negation or $\bot$.

I think the two approaches, with and without $\bot$, are equivalent anyway, in the absence of _ex falso quodlibet_, because '$\bot$', if it's included, is just another proposition.  The only reason I would include it is for continuity with presentations of classical or intuitionistic logic.  Then the difference between them seems to be in how they handle $\bot$.

(That said, I would take the sequent-calculus presentations to be canonical, because they make it more obvious that the differences are structural, rather than logical.  But I don't know how to draw inference rules on the wiki.)

_Toby_:  Actually, I find the sequent-structure distinction between intuitionistic and classical (and presumably minimal) logics rather arbitrary.  After all, there are sequents with exactly one formula on the right that are valid classically but not intuitionistically or valid intuitionistically but not minimally; it\'s just that Gentzen chose the axiomatic ones to avoid those.

Actually, as I like dependent type theory, I tend to always think of logical judgements as having arbitrary left-hand sides but always a single item on the right.  Of course, dependent type theory does lend itself particularly well to intuitionistic logic, so perhaps that\'s unfair.  Maybe I ought to get more into the spirit of the sequent calculus to understand why the differences between these three logics *should* be understood as structural.

Mike has some inference rules [[michaelshulman:2-internal logic|here]].

_Finn_:  Thanks for the link.  I'll have a go at typesetting some inference rules at some point.

I don't think the distinction between different kinds of sequent is arbitrary at all -- it seems to me to be fundamental.  Of course, a sequent like $\vdash P\vee\neg P$ has exactly one formula on the right, but in proving it you need to pass through $\vdash P,\neg P$.  You need the same sequent to prove the double negation law too, so I like to think of these axioms as really being artefacts of the extra structural freedom of classical logic.

I don't understand you when you say 'Gentzen chose the axiomatic \[sequents\] to avoid \[well-formed but invalid sequents\]'.  The axiom sequents are just those that have the same formula $P$ both on the left and on the right -- are you thinking of derived ones like $P\wedge Q\vdash P$?  They are not essential.  It may be a matter of taste, but I certainly find sequent calculus to be far more elegant than natural deduction, precisely because it draws a very clear distinction between logical rules and structural rules.

If you're interested, my TCD technical report is all about the Curry--Howard correspondence for classical logic, and it includes (what I hope is) a fairly intuitive explanation of sequent calculus and associated term notations for minimal and classical logic.  It's available [here](https://www.cs.tcd.ie/publications/tech-reports/reports.08/TCD-CS-2008-55.pdf).

_Toby_:  Thanks, that looks interesting.  As for Gentzen\'s choice and the arbitrariness, you must have seen that LK can be presented in slightly different forms and that the little choices here make a big difference when you restrict to sequents with so many formulas on a given side.

For example, is the rule for disjunction on the left
$$\frac{\Gamma, A \vdash \Delta \qquad \Sigma, B \vdash \Pi}
{\Gamma, \Sigma, A \vee B \vdash \Delta, \Pi}$$
as on [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Sequent_calculus) or
$$\frac{\Gamma, A \vdash \Delta \qquad \Gamma, B \vdash \Delta}
{\Gamma, A \vee B \vdash \Delta}$$
as in your report?
By Wikipedia\'s version, there aren\'t enough such intuitionistic sequents (and so their definition of $LJ$ needs an exception to fix this) and no such minimal sequents, while your version allows them.  On the other hand, if you include corresponding rules for $\bot$ (which are surely required for elegance), then Wikipedia would have
$$\frac{}
{\bot \vdash}$$
which is (correctly) an intuitionistic but not minimal sequent, while you would have
$$\frac{}
{\Gamma, \bot \vdash \Delta}$$
which could be a minimal sequent even though you wouldn\'t want it.

Anyway, I\'ll read your report more closely than is needed just to see how you write LK.  (^_^)

_Finn_:  What you're talking about here is the distinction between 'multiplicative' rules (Wikipedia) and 'additive' ones (me (and Gentzen :)), as in linear logic.  In the presence of contraction and weakening on _both_ sides these are equivalent, of course, but the restriction on intuitionistic and minimal sequents is 'really' about restricting these structural rules on the right -- only one weakening for LJ, none for (what I call) LM and no right contraction for either.

You're right that the multiplicative versions don't work well for these subsystems of LK -- but I think the choice is far from arbitrary, as linear logic shows.  That is, the choice of additive versus multiplicative inference rules seems to be intimately related to the structural aspects of the logic.

As for $\Gamma,\bot\vdash\Delta$ as an axiom, that just isn't included in minimal logic.  (By the way, your point above was well taken, that it would seem better to leave $\bot$ out of minimal logic entirely, but I think most people like having $\neg$ in their logics, even if it's just $\to$ in disguise)
=--