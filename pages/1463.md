
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The ultrafilter theorem
* tic
{: toc}

## Idea

In [[classical mathematics]], the ultrafilter theorem is a theorem about ultrafilters, proved as a standard application of [[Zorn's lemma]].  In the [[foundations]] of mathematics, however, it is interesting to consider which results are implied by it or equivalent to it (very few imply it without being equivalent, other than those that imply the full axiom of choice itself).


## Statement and proof

+-- {: .un_theorem}
###### Ultrafilter theorem

Given a [[set]] $X$, every proper [[filter]] on $X$ may be extended to an [[ultrafilter]] (that is, a [[maximal element|maximal]] [[proper filter]]) on $X$.
=--

+-- {: .proof}
###### Standard proof

Given a proper filter $F$ on $X$, consider the [[partial order|poset]] of proper filters that refine (contain) $F$, ordered by inclusion (reverse refinement).  Of course, $F$ is in this poset.  Given a chain $\mathcal{C}$ of proper filters that refine $F$, the [[union]] $F \cup \bigcup \mathcal{C}$ is a proper filter that refines $F$ and is an upper bound of $\mathcal{C}$.  By [[Zorn's lemma]], there is a proper filter maximal among those that refines $F$, which is therefore maximal among all proper filters.
=--

Although this proof uses Zorn's lemma, the statement itself is weaker.  In particular, it is weaker than the [[axiom of choice]] (even assuming the principle of [[excluded middle]]).


## Strength and weakness as a "choice principle" 

Although the ultrafilter theorem is weaker than the axiom of choice, it can be used to prove quite a few results that are traditionally proved using [[Zorn's lemma]] (or some other thing equivalent to the axiom of choice). For example, it can be used to prove 

* the [[Hahn–Banach theorem]] (which in turn implies existence of Lebesgue non-measurable sets), 

* the [[Banach-Tarski paradox|Banach–Tarski paradox]], 

* the [[prime ideal theorem]] for [[rigs]], [[rings]], and [[Boolean algebras]], 

* that every [[formally real field]] can be [[total order|totally ordered]], 

* existence and uniqueness of [[algebraic closures]] (see [[splitting field]]), 

* existence of non-trivial [[ultraproducts]], 

* the [[compactness theorem]] and completeness theorem for [[first-order logic]] (see below) 

as a partial list. An enlightening discussion of the things one might expect to be able to prove using the ultrafilter theorem is given [here at MO](http://mathoverflow.net/questions/202458/how-do-i-apply-the-boolean-prime-ideal-theorem). 

However, in other respects, the ultrafilter theorem is very weak as a "choice principle". For example, it is too weak to prove the axiom of [[countable choice]] (so for example, it cannot prove that a countable union of countable sets is countable), a fact exhibited in Cohen's first model for the failure of the axiom of choice (where even countable choice fails but the ultrafilter theorem holds). It therefore cannot prove the [[axiom of dependent choice]] either. 

It can prove *some* traditional applications of [[dependent choice]]. For example, it can be used to [[linear order|linearly order]] any set. From there it can be used to prove that a countable union of nonempty finite sets is countable, which in turn can be used to establish the weak K&#246;nig lemma; see [here](/nlab/show/compactness+theorem#totalorder). 

In [[constructive mathematics]], the ultrafilter principle also implies [[De Morgan's law]], which means that the poset of [[truth values]] $\Omega$ is a [[De Morgan Heyting algebra]]. Any [[topos]] with an internal ultrafilter principle is thus a [[De Morgan topos]]. 

## Other formulations

Here are several statements equivalent (internal to an arbitrary [[topos]]) to the ultrafilter theorem.

The first three are, if you work through the definitions, almost direct rephrasings of the theorem above:

*  Every [[net]] has a universal subnet.  (We must define 'subnet' and 'universal net' properly to make this work, at which point the equivalence is immediate.)

*  The Boolean prime ideal theorem: every proper [[ideal]] in a [[Boolean ring]] is contained in a [[prime ideal]].  (Stronger formulations of the Boolean prime ideal theorem also follow.)

*  The [[Stone representation theorem]]: every [[Boolean algebra]] is a subalgebra of some [[function algebra]] $2^X$ into the [[initial object|initial]] Boolean algebra.  (Stronger formulations of the Stone representation theorem also follow.)

These basic results in [[logic]] are equivalent to the ultrafilter theorem:

*  Consistency: if a set $\Sigma$ of formulas in propositional [[classical logic]] is syntactically consistent (proves no contradiction), then it is semantically consistent (has a model).  (The converse is immediate; stronger formulations of the consistency theorem, including for predicate logic, also follow.)

*  Compactness: if every finite subset of $\Sigma$ has a model, then so does $\Sigma$.  (The converse is immediate; stronger formulations of the compactness theorem, including for predicate logic, also follow.)

Various characterisations of [[compact spaces]] are equivalent to the ultrafilter theorem:

*  Given a set $S$, the space $2^S$ (in the product topology) is compact.  (This can be seen as a very weak form of the Tychonoff theorem below.)

*  More generally, if every ultrafilter on a [[convergence space]] $X$ is convergent, then $X$ is compact.  (The converse is immediate.)

*  A [[uniform space]] is compact if it is [[complete space|complete]] and [[totally bounded space|totally bounded]] (i.e. it is [[Bishop-compact]]).  (The converse is immediate.)

These classical results in analysis are equivalent to the ultrafilter theorem in a [[Boolean topos]] with [[natural numbers object]]:

*  The [[Tychonoff theorem]] for [[Hausdorff spaces]]: any product of compact Hausdorff spaces is compact; equivalently, any product of compact Hausdorff spatial [[locales]] is spatial.  (If we drop the Hausdorff condition, then the result is equivalent to the full [[axiom of choice]].)

*  [[Stone–Čech compactification]]: the [[compact Hausdorff spaces]] form a [[reflective subcategory]] of [[Top]].  (The classical result that they form a reflective subcategory of the category $T_{3\frac{1}{2}}$ of completely regular Hausdorff spaces is enough; the classical result that the reflection is a dense embedding on $T_{3\frac{1}{2}}$ also follows.)

*  [[Banach–Alaoglu theorem]]: the closed unit ball of the double dual of a [[Banach space]] is weak* compact.  (The result for *separable* spaces does not require the ultrafilter theorem.)


## Failures

Of course, since the ultrafilter theorem is independent of [[ZF]], there are models in which it fails.  More strongly, however, there are apparently models of ZF in which *every ultrafilter (on every set) is principal*.  See [this MO answer](http://mathoverflow.net/questions/76495/existence-of-non-principal-ultrafilters-on-sets/76499#76499).


## References

Various equivalences with the ultrafilter theorem are stated and proved (in <b>ZF</b>) in

* Eric Schechter; [[HAF|Handbook of Analysis and its Foundations]].

See a summary (in GIF!): [page 1](http://www.math.vanderbilt.edu/~schectex/ccc/excerpts/equivuf1.gif) and [page 2](http://www.math.vanderbilt.edu/~schectex/ccc/excerpts/equivuf2.gif).

It\'s possible that I\'ve made some mistakes above in deciding which of these use excluded middle or the existence of a natural numbers object.  (I very much doubt that any of them use replacement.)

For the ultrafilter principle in constructive mathematics: 

* John Bell, "Boolean Algebras and Distributive  Lattices Treated Constructively", _Mathematical Logic  Quarterly  45_, 1999. [pdf](publish.uwo.ca/~jbell/BOOLCON.pdf)


[[!redirects ultrafilter principle]]
[[!redirects ultrafilter theorem]]
[[!redirects ultrafilter lemma]]
