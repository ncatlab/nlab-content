
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Idempotents
* table of contents
{: toc}

## Idea

The notion of an _idempotent_ [[morphism]] in a [[category]] generalizes the notion of _[[projector]]_ in the context of [[linear algebra]]: it is an [[endomorphism]] $e \colon X \to X$ of some [[object]] $X$ that "squares to itself" in that the [[composition]] of $e$ with itself is again $e$:

$$
  e \circ e = e
  \,.
$$

Accordingly, given any idempotent $e \colon X \to X$ it is of interest to ask what [[subobject]] $A \stackrel{i}{\hookrightarrow} X$ of $X$ it is the projector onto, in that there is a [[projection]] $X \stackrel{p}{\to} A$ such that the idempotent is the composite of this projection followed by including $A$ back into $X$:

$$
  e \colon X \stackrel{p}{\to} A \stackrel{i}{\hookrightarrow} X
  \,.
$$

As opposed to the case of linear algebra, in general such a factorization into a projection onto a subobject $A$ need not actually exists for an idempotent $e$ in a generic category. If it exists, one says that $e$ is a _[[split idempotent]]_. 

Accordingly, one is interested in those categories for which every idempotent is split. These are called _[[idempotent complete categories]]_ or _[[Cauchy complete categories]]_. If a category is not yet idempotent complete it can be completed to one that is: its _[[Karoubi envelope]]_ or _[[Cauchy completion]]_.


## Definition

An [[endomorphism]] $e\colon B \to B$ in a [[category]] is an **idempotent** if the [[composition]] with itself equals itself 

$$
  e \circ  e = e
  \,.
$$

A **splitting** of an idempotent $e$ consists of morphisms $s\colon A \to B$ and $r\colon B \to A$ such that $r \circ s = 1_A$ and $s \circ r = e$.  In this case $A$ is a [[retract]] of $B$, and we call $e$ a [[split idempotent]].

Of course, we can simply consider the __idempotent elements__ of any [[monoid]].


## Properties

### The algebra of idempotents

Given an [[abelian monoid]] $R$, the idempotent elements form a [[submonoid]] $Idem(R)$.

Given a [[commutative ring]] $R$, the idempotent elements of $R$ form a [[Boolean algebra]] $Idem(R)$ with these operations:

*  $\top \coloneqq 1$,
*  $P \wedge Q \coloneqq P Q$,
*  $\bot \coloneqq 0$,
*  $P \vee Q \coloneqq P - P Q + Q$,
*  $\neg{P} \coloneqq 1 - P$.

This is important in [[measure theory]]; if $R$ is the ring $L^\infty(X,\mathcal{M},\mathcal{N})$ of [[essentially bounded function|essentially bounded]] [[real number|real]]-valued [[measurable functions]] on some [[measurable space]] $(X,\mathcal{M})$ modulo an ideal $\mathcal{N}$ of [[null sets]], then $Idem(R)$ is the Boolean algebra of [[characteristic functions]] of [[measurable sets]] modulo null sets, which is [[isomorphic]] to the Boolean algebra $\mathcal{M}/\mathcal{N}$ of measurable sets modulo null sets itself.

If $R$ is a commutative $*$-[[star-ring|ring]], then we may restrict to the [[self-adjoint element|self-adjoint]] idempotent elements to get the Boolean algebra $Proj(R)$.  In measure theory, if $R$ is the [[complex number|complex]]-valued version of $L^\infty(X,\mathcal{M},\mathcal{N})$, then $Proj(R)$ will still reconstruct $\mathcal{M}/\mathcal{N}$.  In [[operator algebra]] theory, the self-adjoint idempotent elements of an operator algebra are called [[projection operator]]s, which is the origin of the notation $Proj$.  (Sometimes one requires projection operators to be _proper_: to have norm $1$; the only projection operator that is not proper is $0$.)

The projection operators of a commutative $W^\star$-[[W-star-algebra|algebra]] give the link between operator algebra theory and measure theory; in fact, the [[categories]] of commutative $W^\star$-algebras and of [[localisable measurable spaces]] (or [[measurable locales]]) are [[dual equivalence|dual]], and $W^\star$-algebra theory in general may be thought of as noncommutative measure theory.  In noncommutative measure theory, the projection operators are still important, but they no longer form a Boolean algebra.


### The universal idempotent-split completion

Given a [[category]] $\mathcal{C}$ one may ask for the [[universal construction|universal]] category obtained from $\mathcal{C}$ subject to the constraint that all idempotents are turned into [[split idempotents]]. This is called the _[[Karoubi envelope]]_  of $\mathcal{C}$. More generally, in [[enriched category theory]] it is called the _[[Cauchy completion]]_ of $\mathcal{C}$.


## Related concepts

* [[retract]], [[section]]

* [[Cauchy complete category]]

* [[idempotent complete (infinity,1)-category]]

* [[idempotent semiring]]

## References

* [[Saunders MacLane]], §I.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


Formalization in [[homotopy type theory]]:

* {#Shulman14} [[Mike Shulman]], _[Splitting idempotents](http://homotopytypetheory.org/2014/12/08/splitting-idempotents/)_ 

[[!redirects idempotent]]
[[!redirects idempotents]]
[[!redirects idempotent element]]
[[!redirects idempotent elements]]
[[!redirects idempotent operator]]
[[!redirects idempotent operators]]
[[!redirects idempotent morphism]]
[[!redirects idempotent morphisms]]