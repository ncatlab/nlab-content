
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Paraconsistent logic
* table of contents
{: toc}

## Overview

A **paraconsistent logic** is a [[logic]] in which it can happen that a [[contradiction]] is true, in the sense that both $A$ and $\neg A$ hold for some [[proposition]] $A$, without the logic becoming *trivial* in the sense that *all* propositions are true.  Put differently, a paraconsistent logic is one in which the schema _ex contradictione quodlibet_:
$$A,\, \neg{A} \;\vdash\; B $$
(for all formulas $A$ and $B$) does not hold.  Logics which are not paraconsistent are sometimes said to be **explosive**: a single contradiction explodes the entire system into triviality.

Two related schemata are _ex falso quodlibet_:
$$\bot\; \vdash\; B$$
and the _[[law of non-contradiction]]_
$$A,\, \neg{A} \;\vdash\; \bot. $$
Either of these may hold in a paraconsistent logic, but of course (assuming transitivity of entailment) not both.

Another pair of schemata which cannot both hold in a paraconsistent logic are _additivity_
$$ A \;\vdash\; A \vee B $$
and the _disjunctive syllogism_:
$$ \neg A ,\, A \vee B \;\vdash\; B. $$
The fact that the two of these together imply _ex contradictione quodlibet_ is known the _Lewis independent argument_.

## Examples

Here we survey some paraconsistent logics.  In-depth development of particular paraconsistent logics should be done on separate individual pages.

### Aristotelian syllogistic
 {#AristotelianSyllogistic}

Paraconsistent logic may seem bizarre to a modern mathematician, but the universal adoption of _ex contradictione quodlibet_ is actually quite recent, dating roughly to the invention in the 19th century of what is now called (clearly inappropriately) [[classical logic]].

One of the oldest formalizations of logic is Aristotelian syllogistic, which is not as expressive as modern predicate logic, but could be regarded as paraconsistent.  A syllogistic analogue of _ex contradictione quodlibet_ would be a "syllogism" such as

* All men are mortal.
* Some men are not mortal.
* Therefore, some pigs can fly.

But this is not one of the valid forms of syllogism.

### Minimal logic

In [[minimal logic]], one simply omits _ex falso quodlibet_ from any of the usual presentations of intuitionistic logic.  The law of non-contradiction remains valid.  Minimal logic satisfies the law
$$ A,\, \neg A \;\vdash\; \neg B $$
for any $A$ and $B$.  This is a weaker form of _ex contradictione quodlibet_, which is still strong enough to be undesirable if one wants to do serious things with a paraconsistent logic.

### Dual intuitionistic logic

In a certain sense, _ex contradictione quodlibet_ is "dual" to the law of [[excluded middle]].  The former asserts that $A \wedge \neg A$ is the least truth value (it implies everything else), while the latter asserts that $A\vee \neg A$ is the greatest truth value (namely "true").

In particular, just as [[intuitionistic logic]] is classical logic without LEM (but with ECQ), the _formal dual of intuitionistic logic_ satisfies LEM but not ECQ.  Specifically, here is the law of non-contradiction which fails: _ex falso quodlibet_ is still valid because it is the dual of the intuitionistically valid sequent $A \vdash \top$.

Dual intuitionistic logic may be presented as a [[sequent calculus]] with the restriction that the left-hand side of any sequent has at most one formula.  It can be modeled by the [[closed subsets]] of any topological space, in which $\wedge$ and $\vee$ are intersection and union, and $\neg$ is the closure of the complement.  Thus $A \vee \neg A$ holds because $A \cup \overline{X\setminus A} = X$, but the law of non-contradiction fails because $A\cap \overline{X\setminus A}$ need not be empty (it is one definition of the [[boundary]] of $A$).

### Linear logic

[[linear logic|Linear logic]] is also paraconsistent, although the analysis becomes complicated because connectives such as $\vee$ and $\wedge$, and even $\top$ and $\bot$, bifurcate into positive and negative linear versions.  With the usual definition of linear negation, we have the following.

* _Ex falso quodlibet_ holds for the positive false, $0\vdash B$, essentially by definition.  But it fails for the negative false $\bot$.

* The law of non-contradiction holds for the negative false, $A,\, \neg A \;\vdash\; \bot$.  Since $\neg A$ is equivalent to $A\multimap \bot$, we can regard this as an instance of [[modus ponens]] for the linear implication.  However, LNC fails for the positive false.

* The additivity property holds for the positive disjunction, $A \vdash A\oplus B$, but fails for the negative disjunction $\parr$.

* The disjunctive syllogism holds for the negative disjunction, $\neg A,\, A \parr B \;\vdash\; B$.  Since $\neg A \parr B$ is equivalent to $A\multimap B$, this can also be regarded as an instance of modus ponens for the linear implication.  However, DS fails for the positive disjunction $\oplus$.

Thus, both ways to deduce _ex contradictione quodlibet_ founder precisely on the finer analysis of connectives provided by linearity.  From a linear point of view, one could say that _ex contradictione quodlibet_ arises from a failure to appreciate that $\oplus$ is different from $\parr$, and that $0$ is different from $\bot$.

Note that linear logic does include an alternative negation which *is* explosive, namely $A\multimap 0$.  However, this "negation" does not satisfy some other desirable properties of negation.  For instance, in "classical" linear logic the linear negation $\neg A = A\multimap\bot$ is involutive, $\neg \neg A \dashv\vdash A$, and satisfies [[excluded middle]] for the negative disjunction, $\vdash A \parr \neg A$, but neither of these hold for the explosive negation $A\multimap 0$.

Also worth noting is that _ex contradictione quodlibet_ can alternatively be stated in terms of a conjuction as $A \wedge \neg A \vdash B$.  In linear logic, of course, the meaning of this depends on whether the conjunction $\wedge$ is positive or negative.  The comma separating multiple formulas in a linear sequent is equivalent to a positive conjunction $\otimes$, so in that case the same analysis above applies.  But for the negative conjunction $\&$, even the "explosive" negation is no longer explosive: $A\& (A\multimap 0)$ doesn't entail $0$, since we can only extract $A$ or $A\multimap 0$ but not both.


### Relevance logics

One goal of [[relevance logic]] is to ensure that no sequent can be valid unless the hypothesis and conclusion have a variable in common.  Thus, _ex contradictione quodlibet_ is invalid in general, but special cases such as $p, \neg{p} \vdash p$ or $p \wedge q, \neg{p \wedge q} \vdash p \vee r$ are valid.  Many relevance logics turn out to also be paraconsistent (although this is not a proof).


### Other paraconsistent logics

(There are many other paraconsistent logics one could discuss...)

## Applications

### Paraconsistent set theory

One potential application of paraconsistent logic would be to give a [[set theory]] in which the [[unrestricted comprehension rule]] is valid, but which is nontrivial.  For instance, if $R = \{ x \mid x\notin x \}$ is the set from [[Russell's paradox]], then a paraconsistent logic could admit that both $R\in R$ and $R\notin R$ without trivializing.

It should be noted, however, that not all paraconsistent logics remain nontrivial in the presence of full comprehension.  If the [[contraction rule]] is permitted (as it is in many [[relevance logics]], then it seems hard to avoid [[Curry's paradox]] in the following form.  For any statement $P$, consider the Curry-Russell set $C = \{ x \mid (x\in x) \to P \}$.  Suppose $C\in C$; then by definition of $C$ we have $(C\in C)\to P$, and so (using $C\in C$ again, by contraction) we have $P$.  Therefore, $(C\in C) \to P$.  But then by definition of $C$ we have $C\in C$, and hence by [[modus ponens]] we have $P$.  Note that this argument does not require ECQ.

## See also

* [[dialetheism]]

* [[paraconsistent mathematics]]

* [[square of opposition]]

## Links

* [English Wikipedia](http://en.wikipedia.org/wiki/Paraconsistent_logic)
* [Stanford Encyclopedia of Philosophy](http://plato.stanford.edu/entries/logic-paraconsistent/)

* Slater, B. H. (1995). "Paraconsistent Logics?". Journal of Philosophical Logic. 24 (4): 451–454. doi:10.1007/BF01048355. S2CID 12125719.

* Béziau, Jean-Yves (2000). "What is Paraconsistent Logic?". In D. Batens; et al. (eds.). Frontiers of Paraconsistent Logic. Baldock: Research Studies Press. pp. 95–111. ISBN 0-86380-253-2.

Paraconsistent logics (among other topic related to inconsistency) are covered in the book

* Chris Mortensen, _Inconsistent Mathematics_, Kluwer Mathematics and Its Applications Series, Vol 312 (1995)

[[!redirects dual intuitionistic logic]]