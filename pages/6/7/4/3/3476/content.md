
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# W-types
* toc
{: toc}

## Idea

A *W-type* is a [[set]] or [[type]] which is defined [[induction|inductively]] in a [[well-founded relation|well-founded]] way.  In most [[set theory|set theories]], W-types can be proven to exist, but in [[predicative mathematics]] or [[type theory]], where this is not the case, they are often assumed explicitly to exist.

The elements of a W-type can be considered to be "rooted well-founded trees" with a certain branching type; different W-types are distinguished by their branching signatures.  A branching signature is represented essentially by a [[family of sets]] $\{A_b\}_{b\in B}$ which can be interpreted as requiring that each *node* of the tree is labeled with an element of the set $B$, and that if a node is labeled by $b$ then it has exactly ${|A_b|}$ outgoing edges, each labeled by an element of $A_b$.  From a more computational point of view, the W-type can be viewed as a data type, where $B$ indexes the set of *constructors* and $A_b$ is the *arity* of the constructor $b$.

If the trees are not required to be well-founded, we obtain instead a [[coinduction|coinductively]] defined type, called a "co-W-type" or an [[M-type]].

## Examples

The most basic W-type is the [[natural numbers]].  Here there are two constructors:
* $0$ of arity zero, and
* $S$ of arity one.
Therefore, zero is a natural number, any natural number has a successor, and all natural numbers are generated in this way.

Similarly, if $X$ is any set, then the W-type $L X$ of lists of elements of $X$ has $|X|+1$ constructors:
* $nil$ of arity zero, and
* $cons(x,-)$ of arity one, for each $x\in X$.
Therefore, $nil$ is a list, $cons(x,\ell)$ is a list for any list $\ell$ and $x\in X$, and all lists are generated in this way.


## Definition

Actually, there are two slightly different formulations of W-types.

### W-types in categories

This version of W-types is the most natural for mathematicians used to thinking in terms of set theory or category theory.  Here we describe a W-type as the [[initial algebra|initial]] algebra for an endofunctor.  The family $\{A_b\}_{b\in B}$ can be thought of as a map $f\colon A\to B$ in some category $C$ (the fiber over $b\in B$ being $A_b$), and the endofunctor in question is the composite
$$ C \overset{A^*}{\to} C/A \overset{\Pi_f}{\to} C/B \overset{\Sigma_B}{\to} C. $$
Such a composite is called a [[polynomial endofunctor]].  Here $A^*$ is the [[pullback]] functor (a.k.a. $A\times -$), $\Pi_f$ is a [[dependent product]], and $\Sigma_B$ is a [[dependent sum]] (a.k.a. the [[forgetful functor]] from $C/B$ to $C$).  This definition makes sense in any [[locally cartesian closed category]], although the W-type (the initial algebra) may or may not exist in any given such category.

This definition is most useful when the category $C$ is not just locally cartesian closed but is a [[Π-pretopos]], since often we want to use at least coproducts in constructing $A$ and $B$.  For example, a [[natural numbers object]] is a W-type specified by one of the coproduct inclusions $1\to 1+1$, and the [[list object]] $L X$ is a W-types specified by $X\to X+1$.  More generally, endofunctors that look like [[polynomial]]s in the traditional sense:
$$ F(Y) = A_n \times Y^{\times n}  + \dots + A_1 \times Y  + A_0 $$
can be constructed as polynomial endofunctors in the above sense in any $\Pi$-pretopos.  A $\Pi$-pretopos in which all W-types exist is called a *$\Pi$-$W$-pretopos*.

In a [[topos]] with a [[natural numbers object]], W-types for any polynomial endofunctor can be constructed as certain sets of well-founded trees; thus every topos with a NNO is a $\Pi$-$W$-pretopos.  This applies in particular in the topos [[Set]] (unless one is a [[predicative mathematics|predicativist]], in which case $Set$ is not a topos and W-types in it must be postulated explicitly).

W-types can also be generalized to initial algebras for *dependent* polynomial functors, which are given by composites
$$ C/D \overset{p^*}{\to} C/A \overset{\Pi_f}{\to} C/B \overset{\Sigma_q}{\to} C/D $$
for some morphisms
$$ D \overset{p}{\leftarrow} A \overset{f}{\to} B \overset{q}{\to} D. $$
Note that we do not necessarily have $q f = p$, so this is not just simply a polynomial endofunctor of $C/D$ considered as a lccc in its own right.


### W-types in type theory

In [[type theory]], W-types are introduced by giving explicit constructors and destructors, a.k.a. introduction and elimination rules.  If the type theory is *extensional*, i.e. [[identity type|identities]] have unique proofs and (dependent) function types are extensional ($f=g$ if and only if $f(x)=g(x)$ for all $x$), then this is more or less equivalent to the categorical version given above.  The type theories that are the [[internal logic]] of familiar kinds of categories are all extensional in this sense.

The main distinction from the naive categorical theory above is that the map $f$ must be assumed to be a [[display map]], i.e. to exhibit $A$ as a [[dependent type]] over $B$, in order that the dependent product $\Pi_f$ be defined.  In the case of dependent polynomial functors, $q$ must also be a display map in order to define $\Sigma_q$.  (Actually, using adjointness, one can still define the W-type even if $q$ is not a display map, but its properties are not as good.  This extra generality is important, however; for example, [[identity type]]s arise as this more general kind of W-type.)

+--{: .query}
[[Mike Shulman]]: Is the term "W-type" still used in this generality?  Or are they just called "inductive types"?
=--

However, in the absence of extensionality (i.e. in *intensional* type theory), W-types cannot be proven to be initial algebras for the corresponding polynomial endofunctor.  In particular, the constructors cannot be proven to be injective.  This applies already for the natural numbers: in ordinary Martin-Lof type theory the successor function on natural numbers cannot be proven to be injective.

## Related concepts

[[!include notions of type]]

## References

* [[Ieke Moerdijk]] and Palmgren, "Wellfounded trees in categories"

*  [[Benno van den Berg]],  [[Ieke Moerdijk]] (2008-09-25); _$W$-types in sheaves_; [vdBM_Wtypes.ps/pdf](http://www.phil.cmu.edu/projects/ast/Papers/)

[[!redirects W-types]]

