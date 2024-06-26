
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Continuous posets
* table of contents
{: toc}

## Definitions

Let $P$ be a [[poset]] with [[directed joins]].


### Elementary definition

+-- {: .un_defn}
###### Definition
For $a, b \in P$, we say that $a$ is **way below** $b$ and write $a \ll b$ if whenever $S \subseteq P$ is a [[directed subset]] and $b \leq \bigvee S$ (where $\bigvee S$ denotes the [[join]] of $S$), then there exists $s \in S$ with $a \leq s$.
=--

+-- {: .un_defn}
###### Definition
We say that $P$ is **continuous** if for every $a\in P$, the subset
$$ \Downarrow (a) \coloneqq \{ b \in P | b \ll a \} $$
is directed and has join $a$.
=--

If $P$ also has finite joins, hence is a [[suplattice]], then $\Downarrow(a)$ is automatically directed, so the condition reduces to $\bigvee (\Downarrow(a)) = a$; in this case $P$ is called a **continuous lattice**.


### Adjoint characterization

Let $Idl(P)$ denote the poset of [[ideals]] in $P$, i.e. subsets that are downward-closed and upwards-directed.

+-- {: .un_prop}
###### Proposition

A poset $P$ has directed joins if and only if the [[principal-ideal]] map $\downarrow : P \to Idl(P)$, defined by
$$ \downarrow(a) \coloneqq \{ b \in P | b \leq a \} ,$$
has a [[left adjoint]], which must be $\bigvee$.
=--

+-- {: .un_theorem}
###### Theorem
A poset $P$ with directed joins is continuous if and only if $\bigvee: Idl(P) \to P$ has its own left adjoint, which must be $\Downarrow$.
=--

This characterization generalizes directly to the notion of [[continuous category]].


## Morphisms

Since a continuous poset must have directed joins, the obvious [[morphisms]] in a [[category]] whose [[objects]] are continuous posets would be the [[Scott-continuous functions]], that is those that preserve directed joins.  (These always preserve the order; that is, they are [[monotone functions]].)

Between continuous lattices, we may use the same morphisms; or we may more generally use those Scott-continuous functions that preserve the [[semilattice]] structure of finitary [[joins]], in other words, the [[suplattice]] morphisms that preserve all joins.  However, because a suplattice is a [[complete lattice]], another common choice is to use the Scott-continuous functions that are also [[inflattice]] morphisms, that is those that also preserve all [[meets]].  Another choice might be the complete-lattice morphisms, those that preserve all meets and all joins.


## Properties

* Continuous lattices are those [[complete lattices]] for which taking [[suprema]] of directed subsets commutes with taking [[infima]] of arbitrary subsets. 

* The [[forgetful functor]] $U$ from the category of continuous lattices to the [[category of sets]] is [[monadic functor|monadic]] if we use Scott-continuous inflattice morphisms. Here the left adjoint of $U$ takes a set $X$ to the lattice of [[filters]] on $X$ (that is filters in the [[power set]] Boolean algebra $P X$). For more, see [[filter monad]]. 

* The category of continuous lattices is [[cartesian closed category|cartesian closed]] if we use all Scott-continuous functions.  This category was used by [[Dana Scott]] to construct models of the untyped [[lambda calculus]]. 

* Every continuous lattice is a [[Baire lattice]].

## Examples

* In [Freyd08](#Freyd08) in [[constructive mathematics]] an [[interval coalgebra]] is a [[continuous poset]] and the [[unit interval]] is the terminal interval coalgebra. 

* A [[locale]] is called [[locally compact locale|locally compact]] just when the corresponding [[frame]] is a continuous lattice. This is equivalently to being an [[exponentiable object|exponentiable]] in the [[category of locales]]. A [[continuous map]] between such locales is [[proper map|proper]] iff its [[direct image]] function (which is always an [[inflattice]] morphism) is [[Scott topology|Scott-continuous]].

* As a consequence the [[category of open subsets|lattice of open subsets]] of a topological space is a continuous lattice if and only if the [[sobrification]] of the topological space is [[locally compact]] (i.e. every point of the sobrification has a [[neighborhood base]] made of compact subsets).

## Related pages

* [[continuous category]]
* [[locally compact locale]]

* Continuous posets can be generalized to [[continuous algebras]] for any [[lax-idempotent 2-monad]].

## References

* Rudolf-E. Hoffmann, _Continuous posets and adjoint sequences_, Semigroup Forum **18** (1979) pp. 173-188. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN001253433))

 * Karl H. Hofmann, _A note on Baire spaces and continuous lattices_ 1980. Bulletin of the Australian Mathematical Society, 21(2), pp. 265-279. 

See section 30 of

* {#Freyd08} [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects continuous poset]]
[[!redirects continuous posets]]
[[!redirects continuous lattice]]
[[!redirects continuous lattices]]

[[!redirects way-below relation]]
[[!redirects way below relation]]
[[!redirects way-below containment]]
[[!redirects way below containment]]
[[!redirects way-below]]
[[!redirects way below]]
