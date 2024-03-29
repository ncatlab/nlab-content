
# $JBW$-algebras in quantum mechanics
* table of contents
{: toc}

## Idea

It can be nice to describe the [[kinematics]] of a [[quantum system]] using a [[JBW-algebra]].  (Then some extra structure is needed for [[dynamics]]; see [below] (#dynamics).)


## Motivation

$JBW$-algebras are arrived at by the confluence of several lines of motivation.

To begin with, the algebraic approach to quantum mechanics (which is also the basis of [[AQFT]]) is a common generalization of [[classical mechanics]] using [[phase spaces]] (or even [[Poisson manifolds]] or even [[Poisson algebras]]) and [[quantum mechanics]] using [[Hilbert spaces]].  In this approach, we have an [[algebra of observables]], of which special cases are the [[commutative algebra]] underlying a Poisson algebra (or its [[complexification]]) and the [[algebra of operators]] on a Hilbert space.  This also allows one to apply [[superselection rules]] at a fundamental level by restricting to a [[subalgebra]].

More particularly, one may restrict to _bounded_ observables, that is those for which there is a largest possible absolute value that could be observed.  There is a philosophical reason for this, that no measuring device in reality is unbounded; but it also makes the algebra more tractable, and an arbitrary observable $O$ can still be described by a [[sequence]] of bounded observables with increasing cut-offs.

At this point, it\'s natural to expect the algebra of observables to be a [[Banach space]] (and so, being an algebra, some kind of [[Banach algebra]]), with the [[norm]] giving this largest possible absolute value.  In fact, [[complex number|complex]] $C^*$-[[C*-algebra|algebras]] are usually used; both the algebra of bounded [[continuous functions]] on a Poisson manifold (or indeed any [[local compactum]]) and the algebra of [[bounded operators]] on a Hilbert space are $C^*$-algebras.

Then we may further refine from $C^*$-algebras to $W^*$-[[W*-algebra|algebras]].  This actually amounts to generalizing the notion of observable.  Whereas a typical commutative $C^*$-algebra is an algebra of [[continuous functions]], a typical commutative $W^*$-algebra is an algebra of [[measurable functions]].  This is necessary if we want to include [[characteristic functions]], reflecting an observation of whether the system is in some [[measurable subset]] of phase space.  (If it is on the boundary, then we won\'t be able to tell; this is reflected in that the $W^*$-algebra of functions identifies functions that are [[almost equality|equal almost everywhere]].)  The [[functional calculus]] of $W^*$-algebras also allows for [[composition]] of an observable with a measurable function on its [[spectrum]], allowing us to (for example) turn continuous observables into less-precise discrete ones.  Of course, the algebra of bounded operators on a Hilbert space is also a $W^*$-algebra.  Finally, the algebra of observables that respect a class of superselection rules will also typically form a $W^*$-algebra.

There is, however, an objection to all of these algebras of observables, which is that they have many elements that are not observable.  Only the [[self-adjoint elements]] of these algebras are considered to be observable.  (Even if we allow for complex-valued observables, only the [[normal element]]s can be observables.)  By themselves, the self-adjoint operators form a [[Jordan algebra]].  Instead of recovering the classical case when the algebra of operators is [[commutative algebra|commutative]], we recover it when the Jordan algebra of self-adjoint operators is [[associative algebra|associative]] (and specifically we get the classical algebra of real-valued observables immediately).  Thus, the algebra of observables is a Jordan algebra, even if it is viewed as embedded within a larger algebra.

The analytic structure on a Jordan algebra that makes it the algebra of self-adjoint elements in a $W^*$-algebra is captured in the definition of a [[JW-algebra]] (Jordan $W$-algebra, which may be read as a Jordan $W^*$-algebra with trivial [[involution]]) or [[JBW-algebra]] (Jordan--Banach $W$-algebra, which allows exceptional cases such as the [[Albert algebra]]).  This is a loss of [[extra structure|structure]] from the full $W^*$-algebra; in fact, a complex $W^*$-algebra can be recovered from a $JBW$-algebra by giving it an additional compatible [[Lie algebra]] structure, making it into a [[JLBW-algebra]], which (as explained there) is equivalent to a complex $W^*$-algebra.  However, the $JBW$-algebra already identifies what the observables and states are, so it is a sufficient place to start from.


## Description

>This is hastily copied from elsewhere and minimally edited. More work should be done to spell this out.

We have:

* a [[Banach space]] $A$ whose elements are thought of as (bounded, real-valued) [[observables]];
* a [[Banach space]] $A_*$, some of whose norm-$1$ elements (those to be identified later as 'positive') are thought of ([[normal state|normal]], [[mixed state|mixed]]) [[states]];
* with $A$ expressed as the [[dual Banach space|dual]] of $A_*$;
* with a commutative (but [[nonassociative algebra|nonassociative]]) multiplication operation on $A$;
* with the resulting nonassociative [[Banach algebra]] $A$ satisfying a few technical conditions:
  * [[power-associative algebra|power-associativity]]: all ways of parenthesizing $x^n$, for $x$ an element of $A$ and $n$ a [[natural number]], are equal;
  * positivity: ${\|x^2\|} \leq {\|x^2 + y^2\|}$; and
  * the [[B-identity]]: ${\|x^2\|} = {\|x\|^2}$.

In particular, the positivity allows us to define a [[partial order]] on $A$ according to which an element of $A$ is (weakly) _positive_ if it is a limit of sums of squares, and then an element $\psi$ of $A_*$ is _positive_ (and hence a _normal state_ if it has norm $1$) if every positive element $x$ of $A$ takes $\psi$ to a nonnegative real number.

If the multiplication on $A$ happens to be [[associative algebra|associative]], then there exists a [[measure space]] $X$ such that $A_*$ is the [[Lebesgue space]] $L^1(X)$ and $A$ is $L^\infty(X)$.  It is always possible to take $X$ to be [[localizable measure space|localizable]], in which case the [[Radon–Nikodym theorem]] applies and we can identify $L^1(X)$ with the space of [[absolutely continuous measures]] on $X$.  At this point, the measure on $X$ is irrelevant except for its specification of [[full set|full]] (or [[null set|null]]) subsets, so we may treat $X$ as simply a [[localizable measurable space]] (which includes this data).  Then the choice of $X$ is actually [[the|essentially unique]].

In this way, the associative case reduces to [[probability theory]].  We have a measurable space $X$, an observable is an [[essentially bounded function]], and a state is a [[probability measure]].  It is true that we only have localizable spaces, but these are the only ones that satisfy the nice theorems (such as Radon--Nikodym, aforementioned) anyway.  (Similarly, the observables are defined only up to [[almost equality]], and the normal states must be [[absolutely continuous measures]].)

In the general (nonassociative) case, we still think of the elements of $A$ (the observables) as essentially bounded functions, but now on a sort of [[noncommutative geometry|noncommutative]] (or rather nonassociative) space, and we may still think of the elements of $A_*$ (the states) as probability measures on that space.  (This is particularly appropriate in the [[Bayesian interpretation of quantum mechanics]].)  Because $A$ is a Jordan algebra instead of an associative algebra, *all* of its elements may be thought of as observables, but this is more of a convenience than an essential feature.

We might also want to consider generalized (non-normal) [[state on an operator algebra|states]], that is norm-$1$ [[positive operator|positive]] [[linear functionals]] on $A$.  (Every state in $A_*$ may be so interpreted, using the natural map $A_* \to (A_*)^{**} = A^*$).  One may go further and consider [[quasistate]]s on $A$, if any exist (besides the states themselves).

In particular, if $A$ is the space of [[bounded operators|bounded]] [[self-adjoint operators]] on some [[Hilbert space]] $H$, then $A_*$ is the space of [[trace-class operator|trace-class]] self-adjoint operators on $H$.  Then a normal state is a [[density matrix]], and the pure states (those that cannot be written as nontrivial [[convex combinations]] of other states) are those of the form ${|\psi\rangle \langle\psi|}$ for $\psi$ a unit vector in $H$.


## Dynamics {#dynamics}

We can add [[dynamics]] by giving the $JBW$-algebra the structure of a [[pointed object|pointed]] [[JLBW-algebra]], that is by defining a kind of [[commutator]] (the 'L') and identifying one of the operators in the algebra as the [[Hamiltonian]] (the 'pointed').  This is mathematically equivalent to a [[complex numbers|complex]] $W^*$-[[W*-algebra|algebra]] equipped with a [[self-adjoint element]].


## Related concepts

* [[interpretation of quantum mechanics]]

* [[finite quantum mechanics in terms of dagger-compact categories]]

* [[AQFT]]


[[!redirects JBW-algebras in quantum mechanics]]
[[!redirects JBW-algebras in quantum physics]]
[[!redirects JBW-algebraic approach to quantum mechanics]]
[[!redirects JBW-algebraic approach to quantum physics]][[!redirects JBW-algebraic quantum mechanics]]
[[!redirects JBW-algebraic quantum physics]]
