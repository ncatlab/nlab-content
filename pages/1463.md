In classical mathematics, the ultrafilter theorem is a theorem about ultrafilters, proved as a standard application of [[Zorn's lemma]].  In the [[foundations]] of mathematics, however, it is interesting to consider which results are implied by it or equivalent to it (very few imply it without being equivalent).

## Statement and proof

+-- {: .un_theorem}
###### Ultrafilter theorem

Given a [[set]] $X$, every proper [[filter]] on $X$ may be extended to an [[ultrafilter]] (that is, a maximal proper filter) on $X$.
=--

+-- {: .proof}
###### Standard proof

Given a proper filter $F$ on $X$, if $F$ is not maximal, then there is some [[subset]] $A$ of $X$ such that $A \cap B$ is [[inhabited set|inhabited]] whenever $B \in F$ but $A \notin F$; so extend $F$ to $F' = F \cup \{A\}$ to get another proper filter.  Given a chain of proper filters on $X$, their [[union]] is a proper filter.  Now apply Zorn\'s lemma.
=--

As is typical with applications of Zorn\'s lemma, the second step requires the principle of [[excluded middle]].  As such, the validity of this proof is equivalent to the [[axiom of choice]].  However, the statement itself is weaker than the axiom of choice.

## Other formulations

Here are several statements equivalent (internal to an arbitrary [[topos]]) to the ultrafilter theorem.

The first three are, if you work through the definitions, almost direct rephrasings of the theorem above:
*  Every [[net]] has a universal subnet.  (We must define 'subnet' and 'universal net' properly to make this work, at which point the equivalence is immediate.)
*  The Boolean prime ideal theorem: every proper [[ideal]] in a [[Boolean ring]] is contained in a [[prime ideal]].  (Stronger formulations of the Boolean prime ideal theorem also follow.)
*  The Stone representation theorem: every [[Boolean algebra]] is a subalgebra of some (classical) [[power set]] $2^X$.  (Stronger formulationss of the Stone representation theorem also follow.)

These basic results in [[logic]] are equivalent to the ultrafilter theorem:
*  Consistency: if a set $\Sigma$ of formulas in propositional [[classical logic]] is syntactically consistent (proves no contradiction), then it is semantically consistent (has a model).  (The converse is immediate; stronger formulations of the consistency theorem, including for predicate logic, also follow.)
*  Compactness: if every finite subset of $\Sigma$ has a model, then so does $\Sigma$.  (The converse is immediate; stronger formulations of the compactness theorem, including for predicate logic, also follow.)

Various characterisations of [[compact space]]s are equivalent to the ultrafilter theorem:
*  Given a set $S$, the space $2^S$ (in the product topology) is compact.  (This can be seen as a very weak form of the Tychonov theorem below.)
*  More generally, if every ultrafilter on a [[convergence space]] $X$ is convergent, then $X$ is compact.
*  A [[uniform space]] is compact if it is complete and totally bounded.  (The converse is immediate.)

These classical results in analysis are equivalent to the ultrafilter theorem in a [[Boolean topos]] with [[natural numbers object]]:
*  The Tychonov theorem for Hausdorff spaces: any product of compact Hausdorff spaces is compact; equivalently, any product of compact Hausdorff spatial [[locale]]s is spatial.  (If we drop the Hausdorff condition, then the result is equivalent to the full [[axiom of choice]].)
*  Stone--Cech compactification: the compact Hausdorff spaces are a [[reflective subcategory]] of [[Top]].  (The classical result that they form a reflective subcategory of the category $T_3$ of completely regular Hausdorff spaces is enough; the classical result that the reflection is a dense embedding on $T_3$ also follows.)
*  Banach--Alaoglu theorem: the closed unit ball of the double dual of a [[Banach space]] is weak* compact.  (The result for *separable* spaces does not require the ultrafilter theorem.)

## References

Various equivalences with the ultrafilter theorem are stated and proved (in <b>ZF</b>) in

* Eric Schechter; Handbook of Analysis and its Foundations.

See a summary (in GIF!): [page 1](http://www.math.vanderbilt.edu/~schectex/ccc/excerpts/equivuf1.gif) and [page 2](http://www.math.vanderbilt.edu/~schectex/ccc/excerpts/equivuf2.gif).

It\'s possible that I\'ve made some mistakes above in deciding which of these use excluded middle or the existence of a natural numbers object.  (I very much doubt that any of them use replacement.)