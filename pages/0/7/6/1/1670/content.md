
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


# Moore closures
* table of contents
{: toc}

## Idea

The concept of _Moore closure_ is a very general idea of what it can mean for a [[set]] to be _closed_ under some condition.  It includes, as special cases, the operation of [[closed subspace|closure]] in a [[topological space]], many examples of generation of structures from [[base|bases]] and even [[subbase|subbases]], and generating [[subalgebras]] from subsets of an algebra.

Secretly, it is the same thing as the collection of subsets preserved by some [[monad]] on a [[power set]] (the subset of "[[modal types]]"). In fact it is a special case of the notion of [[closure operator]] or [[modality]] in [[logic]]/[[type theory]], namely the special case where the ambient [[category]]/[[hyperdoctrine]] is the [[topos]] [[Set]].


## Definitions

We give two equivalent definitions. The first one

* [In terms of closure condition](#InTermsOfClosureCondition)

gives the explicit condition for a [[subset]] of a [[power set]] to qualify as a Moore closure, the second

* [In terms of closure operators](#InTermsOfClosureOperators)

characterizes Moore closures as the collections of [[modal types]] of suitable [[closure operators]]. More abstractly, this characterizes Moore closures

* [In terms of monads](#InTermsOfMonads)

on the [[subobject lattice]] of the given set.

### In terms of closure condition
 {#InTermsOfClosureCondition}

+-- {: .num_defn}
###### Definition

Let $X$ be a [[set]], and let $\mathcal{C} \subset \mathcal{P}X$ be a collection of [[subsets]] of $X$.  Then $\mathcal{C}$ is a __Moore collection__ if every [[intersection]] of members of $\mathcal{C}$ belongs to $\mathcal{C}$. 

That is, given a family $(A_i)_i$ of sets in $X$,
$$ \forall i,\; A_i \in \mathcal{C} \;\Rightarrow\; \bigcap_i A_i \in \mathcal{C} .$$

=--

+-- {: .num_defn}
###### Definition

Given any collection $\mathcal{B}$ whatsoever of subsets of $X$, the Moore collection __generated__ by $\mathcal{B}$ is the collection of all intersections of members of $\mathcal{B}$. 

=--

+-- {: .num_remark}
###### Remark

This is indeed a Moore collection, and it equals $\mathcal{B}$ if and only if $\mathcal{B}$ is a Moore collection.

=--

### In terms of closure operators
 {#InTermsOfClosureOperators}

+-- {: .num_defn #ClosureOperator}
###### Definition

Again let $X$ be a set, and now let $Cl$ be an operation on subsets of $X$.  Then $Cl$ is a __closure operation__ if $Cl$ is isotone, extensive, and idempotent.  That is,

1.  $ A \subseteq B \;\Rightarrow\; Cl(A) \subseteq Cl(B) $,
1.  $ A \subseteq Cl(A) $, and
1.  $ Cl(Cl(A)) \subseteq Cl(A) $ (the reverse inclusion follows from the previous two properties).

=--

+-- {: .num_prop}
###### Proposition

If $Cl$ is a closure operation, then let $\mathcal{C}$ be the collection of sets that equal their own closures (the "[[modal types]]" or "[[local objects]]").  Then $\mathcal{C}$ is a Moore collection.

Conversely, if $\mathcal{C}$ is a Moore collection, then let $Cl(A)$ be the intersection of all closed sets that contain $A$.  Then $Cl$ is a closure operator.

Furthermore, the two maps above, from closure operators to Moore collections and vice versa, are inverses.
=--


### In terms of monads
 {#InTermsOfMonads}

Moore closures on $X$ are precisely [[monads]] on  the [[subobject lattice]] $\mathcal{P}X$.  The property (1) of a closure operator, def. \ref{ClosureOperator}, corresponds to the action of the monad on morphisms, while (2,3) are the [[unit of an adjunction|unit]] and multiplication of the monad.  (The rest of the requirements of a monad are trivial in a [[poset]], since they state the equality of various morphisms with common source and target.)



## Examples
 {#Examples}

The [[closed subsets]] in a [[topological space]] form a Moore collection; here the closure of a set $A$ is its closure in the usual sense.  In fact, a topological space can be *defined* as a set equipped with a Moore closure with either of these additional properties (which are equivalent):

*  $Cl(\empty) = \empty$ and $Cl(A \cup B) = Cl(A) \cup Cl(B)$.
*  $\empty$ is closed, and so is $A \cup B$ if $A$ and $B$ are closed.

(However, these properties may fail in [[constructive mathematics]]; in fact, a topology cannot be constructively recovered from its closure operation.)

The first pair of properties is equivalent to the following weaker ones given that $A \subseteq Cl(A)$:

* $Cl(\empty) \subseteq \empty$ and $Cl(A \cup B) \subseteq Cl(A) \cup Cl(B)$.

The closure operator of a topological space with underlying set $X$, and thus in classical mathematics, a topology on a set $X$, can thus be described as an [[monoidal monad | oplax monoidal monad]] on the [[join semilattice]] $\mathcal{P}X$ considered as a cocartesian monoidal category.  

Notice that a preclosure in a [[pretopological space]], is not a closure in the above sense, even though some authors do call this 'closure'.


Here are some algebraic examples:

*  The [[subgroup]]s of a [[group]] $G$ form a Moore collection; the closure of a subset $B$ of $G$ is the subgroup generated by $B$.

*  The subrings of a [[ring]] $R$ form a Moore collection; the closure of a subset $B$ of $R$ is the subring generated by $B$.

*  The subspaces of a [[vector space]] $V$ form a Moore collection; the closure of a subset $B$ of $V$ is the subspace spanned by $B$.

*  OK, you get the idea.  This applies to any [[algebraic theory]]. For a [[Lawvere theory|finitary algebraic theory]], the lattice of closed elements is an [[algebraic lattice]]. 

But also:

*  The [[normal subgroup]]s of $G$ form a Moore collection; the closure of $B$ is the normal subgroup generated by $B$.

*  The [[ideal]]s of a ring $R$ form a Moore collection; the closure of $B$ is the ideal generated by $B$.

*  The (topologically) closed subspaces of a [[Hilbert space]] $H$ form a Moore collection; the closure of $B$ is the closed subspace generated by $B$.

*  And many further examples.

Here are some examples on [[power set]]s:

*  The topologies on $X$ form a Moore collection on $\mathcal{P}X$; the closure of a subset $\mathcal{B}$ of $\mathcal{P}X$ is the topology generated by $\mathcal{B}$ as a [[subbase]].

*  The [[filter]]s on $X$ form a Moore collection on $\mathcal{P}X$; the closure of $\mathcal{B}$ is the filter generated by $\mathcal{B}$ as a [[subbase]].  (The *proper* filters on $X$ do *not* form a Moore collection; not every $\mathcal{B}$ generates a proper filter.)

*  The $\sigma$-[[sigma-algebra|algebras]] on $X$ form a Moore collection on $\mathcal{P}X$; the closure of $\mathcal{B}$ is the $\sigma$-algebra generated by $\mathcal{B}$.  (This is the 'abstract nonsense' way to generate a $\sigma$-algebra; else you have to do transfinite induction on countable [[ordinal number|ordinals]].)

*  And so on.

Topping off these, the Moore collections on $X$ form a Moore collection on $\mathcal{P}X$; the closure of $\mathcal{B}$ is the Moore collection generated by $\mathcal{B}$ as described in the definitions.

See also at _[[matroid]]_.


## Generalisations

The definition of Moore collection really makes sense in any [[inflattice]]; even better, the definition of closure operator makes sense in any [[partial order|poset]].  This context is the generic meaning of [[closure operator]]; here are some examples:

*  Instead of $\mathcal{P}X$, work in the [[opposite category|opposite poset]] $\mathcal{P}^{op}X$.  Then the open sets in a [[topological space]] $X$ form a Moore collection whose closure operator is the usual interior operation.  Now we can define a topological space as a set equipped with a Moore closure operator on $\mathcal{P}^{op}X$ that preserves [[join]]s (which here are [[intersection]]s); this definition is even valid constructively.

*  Let $f \dashv g$ be a [[Galois connection]] between [[partial order|posets]] $A$ and $B$.  Call an element of $A$ _normal_ if $g(f(a)) \leq a$ (the reverse is always true).  Then $g \circ f$ is a closure operator.  This generalises the case of the normal subgroups of $G$ when $G$ is the [[Galois group]] of an extension of [[field]]s.

Since Galois connections are simply [[adjunction]]s between posets, the concept of Moore closure cries out for [[categorification]].  And in fact, the answer is well known in category theory: it is a [[monad]].

## Related concepts

* [[matroid]]

* [[modal operator]], [[modality]]

* [[modal logic]], [[modal type theory]], [[modal homotopy type theory]]


## References

*  Erich Schechter, Section 4.1-4.12 in: *[[Handbook of Analysis and its Foundations]]*

See also:

* Wikipedia, _[Closure operator](http://en.wikipedia.org/wiki/Closure_operator)_

* B. Venkateswarlu, R. Vasu Babu
, Getnet Alemu, _Morphisms on Closure Spaces and Moore Spaces_ [pdf](https://www.ijpam.eu/contents/2014-91-2/6/6.pdf)


[[!redirects Moore closure]]
[[!redirects Moore closures]]
[[!redirects Moore clsoure]]
[[!redirects Moore collection]]
[[!redirects Moore collections]]
