A paraconsistent logic is one that does not include the
law _ex contradictione quodlibet_, that is, the schema $A,
\neg{A} \vdash B$ for all formulas $A$ and $B$.

Compare _ex falso quodlibet_ $\bot \vdash B$ and the _law of non-contradiction_ $A, \neg{A} \vdash \bot$, which are not quite the same; either may hold in a paraconsistent logic, but of course not both.

# Examples #

In [[minimal logic]], one omits ex falso quodlibet from any of the usual presentations of intuitionistic logic.  The law non-contradiction is valid here.

In the formal dual of intuitionistic logic (which may be presented as a [[sequent calculus]] with the restriction that the left-hand side of any sequent has at most one formula), the law of non-contradiction fails, for the same (or the dual of the) reason that intuitionistic logic does not prove the law of the [[excluded middle]].  Although ex falso quodlibet is still valid (because it is the dual of the intuitionistically valid sequent $A \vdash \top$), ex contradictione quodlibet still does not follow.

In [[relevance logic]], no sequent can be valid unless the hypothesis and conclusion have a variable in common.  Thus, ex contradictione quodlibet is invalid in general, but special cases such as $p, \neg{p} \vdash p$ or $p \wedge q, \neg{p \wedge q} \vdash p \vee r$ are valid.

# Discussion #

Here is some past discussion about which law should define whether a logic is paraconsistent:

+--{: .query}
I made a big change here; I would argue that the failure of $\bot \vdash B$ means that '$\bot$' simply doesn\'t mean $\bot$; but in any case, I\'ve always seen the definition given in terms of negation.  In particular, dual-intuitionistic logic has $\bot \vdash B$ (just as intuitionistic logic has $B \vdash \top$) but is still considered paraconsistent.

[[Finn Lawler|Finn]]: Hmm.  (I presume you meant the ')' to come before 'but is still...'; as it stands that last statement is false.)  The definitions I've seen correspond to what I wrote, but you make a good point -- if we want to think of $LJ^{op}$ as paraconsistent then the definition by means of _ex falso quodlibet_ does seem wrong.  If this is the standard definition, then I certainly won't object -- I'll just avoid relying on philosophers for information about logic in future.

_Toby_:  Yeah, I\'m sure about the standard; our links agree with me too.  (And thanks for catching my parenthesis.)  As for philosophers, they\'re not always as precise as mathematicians; that may be the problem.  Not to mention, there\'s a tendency not to include $\bot$ as a logical constant but instead to simply *define* it as $A \wedge \neg{A}$ (after proving that these are all equivalent, but ignoring the possibility of an empty model), which leads to conflating the two versions.  (In a paraconsistent logic where $A \wedge \neg{A} \equiv B \wedge \neg{B}$ need not hold, one ought to catch the inapplicability of this definition, but maybe not.)

_Finn_: I think you've hit the nail on the head there: *I* think 'ex falso quodlibet' means $\bot\vdash A$ (as you said above, this says that '$\bot$' means $\bot$, the least truth-value), but it seems my sources may have meant $A\wedge\neg A\vdash B$, without saying so.  This is why I never cared much for what's called 'philosophical logic' -- even though I'm a philosophy graduate studying logic (albeit in a computer science department), it was always too fuzzy for my tastes.

Thanks for clearing this up.  Obviously your version should stand.

_Toby_:  You\'re welcome.  But your fancy Latin reminds me that what we have here is technically really the *combination* of the law of non-contradiction (any contradiction is false: $A \wedge \neg{A} \equiv \bot$) and ex falso quodlibet (anything follows from falsehood: $\bot \vdash B$), so I changed the name above.

_Finn_: Right -- I was going to mention that (no, really), but forgot.  Perhaps we should incorporate some of this discussion into the article proper, to help resolve any imprecision in other sources.  I'll do that, if you'd rather not, but not now -- it's way past bedtime here in GMT-land.
=--

# Links #

* [English Wikipedia](http://en.wikipedia.org/wiki/Paraconsistent_logic)
* [Stanford Encyclopedia of Philosophy](http://plato.stanford.edu/entries/logic-paraconsistent/)