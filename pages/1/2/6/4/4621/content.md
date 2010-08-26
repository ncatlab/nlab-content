# Decidable propositions
* table of contents
{: toc}

## Idea

A [[proposition]] is decidable if we know whether it is [[true]] or [[false]].  This has (at least) two interpretations, which we will call 'internal' and 'external'; however, these adjectives are rarely used and must be guessed from the context.


## Externally decidable propositions in logic

In [[logic]], a proposition $p$ in a given [[theory]] (or in a given [[context]] of a given theory) is __externally decidable__ if there is in that theory (or in that context) a proof of $p$ or a refutation of $p$ (a proof of $\neg{p}$).  Of course, this only makes sense if the logic of the theory includes an operation of [[negation]].

Any statement that can be proved or refuted is decidable, and one might hope for a consistent [[foundation of mathematics]] in which every statement is decidable.  However, G&#246;del\'s [[incompleteness theorem]] dashes these hopes; any [[consistent theory]] strong enough to model [[arithmetic]] (actually a rather weak form of arithmetic) must contain undecidable statements.

For example, the [[continuum hypothesis]] is undecidable in [[ZFC]], assuming that $ZFC$ is consistent at all.


## Internally decidable propositions in constructive mathematics

In [[constructive mathematics]], a proposition $p$ is __internally decidable__ if the [[law of excluded middle]] applies to $p$; that is, if $p \vee \neg{p}$ holds.  Of course, in [[classical mathematics]], every statement is decidable in this sense.  Even in constructive mathematics, some statements are decidable and no statement is undecidable; that is, $\neg{p \vee \neg{p}}$ is always false, but this is not enough to guarantee that $p \vee \neg{p}$ is true.

For example, consider the [[Riemann hypothesis]] (or any of the many unsolved $\Pi_1$-[[Pi-1-proposition|propositions]] in [[number theory]]).  This may be expressed as $\forall x, P(x) \vee \neg{P(x)}$ for $P$ some [[predicate]] on [[natural numbers]].  For each $x$, the statement $P(x)$ is decidable (that is, $\forall x, P(x) \vee \neg{P(x)}$ holds), and indeed one can in principle work out which with pencil and paper.  However, the Riemann hypothesis itself has not yet been proved (constructively) to be decidable.

A [[set]] $A$ has __[[decidable equality]]__ if every [[equality|equation]] between elements of $A$ (every proposition $x = y$ for $x, y$ in $A$) is decidable.  A [[subset]] $B$ of a set $C$ is a __[[decidable subset]]__ if every statement of membership in $B$ (every proposition $x \in B$ for $x$ in $A$) is decidable.


## Relation between these

In many foundations of constructive mathematics, the [[disjunction property]] holds (in the global context).  That is, if $p \vee q$ can be proved, then either $p$ can be proved or $q$ can be proved.  By G&#246;del\'s incompleteness theorem, no consistent foundation of classical arithmetic can have this property, but some consistent foundations of intuitionistic arithmetic (such as [[Heyting arithmetic]]) do.

In any consistent logic with the disjunction property, a proposition is externally decidable if and only if it can be proved to be internally decidable.  (Note that the claim that $p$ is externally decidable is a statement in the metalanguage, while the claim that $p$ is internally decidable is a statement in the object language.)


## Categorial interpretation

The [[internal logic]] of any [[Heyting category]] $C$ is a [[type theory]] in [[first-order logic|first-order]] [[intuitionistic logic]]; conversely, any such theory $T$ has a [[category of contexts]] which is a Heyting category.

Under this correspondence, the [[contexts]] of $T$ correspond to the [[objects]] of $C$, and the [[propositions]] in a given context correspond to the [[subobjects]] of that object.  Then a proposition in a context $X$ is externally decidable if and only if it is, as a subobject of $X$, either $X$ itself (corresponding to being provable) or the [[initial object]] (corresponding to being refutable).  And a proposition in the context $X$ is internally decidable if and only if, when thought of as a subobject $A$ of $X$, the [[union]] of $A$ and $\neg{A}$ is $X$.

The [[slice category]] $C/X$ is [[two-valued category|two-valued]] if and only if the context $X$ is consistent and every proposition in that context is externally decidable.  $C$ is a [[Boolean category]] if and only if every proposition in every context is internally decidable.
+-- {: .query}
This makes me think that we should define $p$ to be externally decidable iff $p$ is provable whenever it is not refutable, which in a constructive metalogic is weaker than the definition above.  But then we lose the relationship with the disjunction property.  I guess that we need intuitionistic, classical, and paraconsistent forms of external decidability, just as for two-valuedness.
=--


[[!redirects decidable proposition]]
[[!redirects decidable propositions]]
