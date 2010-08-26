# Decidable propositions
* table of contents
{: toc}

## Idea

A [[proposition]] is decidable if we know whether it is [[true]] or [[false]].  This has (at least) two interpretations, called below 'formal' and 'informal'; however, these adjectives are rarely used and must be guessed from the context.


## In logic

In [[logic]], a proposition $p$ in a given [[theory]] (or in a given [[context]] of a given theory) is __formally decidable__ if their is a proof in that theory (or in that context) of $p$ or a proof of $\neg{p}$.  Of course, this only makes sense if the logic of the theory includes [[negation]].

Any statement that can be proved or refuted is decidable, and one might hope for a consistent [[foundation of mathematics]] in which every statement is decidable.  However, G&#246;del\'s [[incompleteness theorem]] dashes these hopes; any consistent theory strong enough to model [[arithmetic]] (actually a rather weak form of arithmetic) must contain undecidable statements.

For example, the [[continuum hypothesis]] is undecidable in [[ZFC]].


## In constructive mathematics

In [[constructive mathematics]], a proposition $p$ is __informally decidable__ if the [[law of excluded middle]] applies to $p$; that is, if $p \vee \neg{p}$ holds.  Of course, in [[classical mathematics]], every statement is decidable in this sense.  Even in constructive mathematics, no statement is undecidable; that is, $\neg{p \vee \neg{p}}$ is always false; however, this is not enough to make $p \vee \neg{p}$ true.

For example, consider the [[Riemann hypothesis]].  This may be expressed as $\forall x, P(x) \vee \neg{P(x)}$ for $P$ some [[predicate]] on [[natural numbers]].  For each $x$, the statement $P(x)$ is decidable (that is, $\forall x, P(x) \vee \neg{P(x)}$ holds), and indeed one can in principle work out which with pencil and paper.  However, the Riemann hypothesis itself has not yet been proved (constructively) to be decidable.

A [[set]] $A$ has __[[decidable equality]]__ if every [[equality|equation]] between elements of $A$ (every proposition $x = y$ for $x, y$ in $A$) is decidable.  A [[subset]] $B$ of a set $C$ is a __[[decidable subset]]__ if every statement of membership in $B$ (every proposition $x \in B$ for $x$ in $A$) is decidable.


## Relation between these

In many foundations of constructive mathematics, the [[disjunction property]] holds (in the global context).  That is, if $p \vee q$ can be proved, then either $p$ can be proved or $q$ can be proved.  By G&#246;del\'s incompleteness theorem, any consistent foundation of classical arithmetic cannot have this property, but some consistent foundations of intuitionistic arithemtic (such as [[Heyting arithmetic]]) do.

In any consistent logic with the disjunction property, a proposition is formally decidable if and only if it can be proved to be informally decidable.  (Note that the claim that $p$ is formally decidable is a statement in the metalanguage, while the claim that $p$ is informally decidable is a statement in the object language.)


[[!redirects decidable proposition]]
[[!redirects decidable propositions]]
