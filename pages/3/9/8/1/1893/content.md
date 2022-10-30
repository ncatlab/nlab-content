## Disambiguation

There is also a notion of [[special lambda-ring]]. But in most cases by ''$\lambda$-ring'' is meant ''special $\lambda$-ring''.

##Idea##

A *$\lambda$-ring* $L$ is a [[P-ring]] presented by the [[polynomial ring]] $Symm=\mathbb{Z}[h_1,h_1\dots]$ in countably many indeterminates over the [[integer|integers]] or, equivalently, $Symm$ is the ring of [[symmetric function|symmetric functions]] in countably many variables. This means that (the underlying set valued functor of) $L$ is a [[copresheaf]] presented by $Symm$ such that

1. $L:\CRing \to CRing$ defines an endofunctor on the category of commutative rings.

1. $L$ gives rise to a [[comonad]] on $C Ring$.

A $\lambda$-ring is hence a commutative ring equipped with a [[co-action]] of this comonad. As always is the case with [[monad|monads]] and comonads this definition can be formulated in terms of an [[adjunction]].

## Motivation from algebra

In many situations, we can take [[direct sum|direct sums]] of [[representation|representations]] of some algebraic gadget.  So, decategorifying, the set of isomorphism classes of representations becomes a [[commutative monoid]]. But nobody likes commutative monoids: we all have an urge to subtract.  So, we throw in formal negatives and get an [[abelian group]] --- the so-called [[Grothendieck group]].

In many situations, we can also take [[tensor product|tensor products]] of representations.  Then our Grothendieck group becomes something better than an abelian group.  It becomes a [[ring]]: the [[representation ring]]. But, we're not done!  In many situations we can also take [[exterior power|exterior]] and [[symmetric power|symmetric]] powers of representations.  Indeed, we can often apply any [[Young diagram]] to a representation and get a new representation! Then our representation ring becomes something better than a ring.  It becomes a $\lambda$-ring!

More generally, the [[Grothendieck group]] of a [[monoidal category|monoidal]] [[abelian category]] is always a ring,
called a [[Grothendieck ring]].   If we start with a [[braided monoidal category|braided monoidal]] abelian category, this ring is commutative.   But if we start with a [[symmetric monoidal category|symmetric monoidal]] abelian category, we get a $\lambda$-ring!   

So, $\lambda$-rings are all about getting the most for your money when you decategorify a symmetric monoidal abelian category --- for example the category of [[representations]] of a group, or the category of [[vector bundle|vector bundles]] on a space.


Unsurprisingly, the [[Grothendieck group]] of the free symmetric monoidal abelian category on one generator is the free $\lambda$-ring on one generator.  This category is very important in representation theory.  Object in this category are called [[Schur functor|Schur functors]], because for obvious reasons they act as functors on _any_ symmetric monoidal abelian category.  The irreducible objects in this category are called 'Young diagrams'.  Elements of the free $\lambda$-ring on one generator are called [[symmetric function|symmetric functions]].

## Definition
 
### The "orthodox" view on $\lambda$-rings

+-- {: .num_defn}
###### Definition
A $\lambda$-structure on a commutative unital ring $R$ is defined to be a sequence of maps $\lambda^n$ for $n\ge 0$ satisfying


1. $\lambda^0(r)=1$ for all $r\in R$

1. $\lambda^1=id$

1. $\lambda^n(1)=0$, for $n\gt 1$

1. $\lambda^n(r+s)=\sum_{k=0}^n \lambda^k(r)\lambda^{n-k}(s)$, for all $r,s\in R$

1. $\lambda^n(r s)=P_n(\lambda^1(r),\dots,\lambda^n(r),\lambda^1(s),\dots,\lambda^n(s))$ for all $r,s\in R$

1. $\lambda^m(\lambda^n(r)):=P_{m,n}(\lambda^1(r),\dots,\lambda^{m n}(r))$, for all $r\in R$

where $P_n$and $P_{m,n}$ are certain (see the reference for their calculation) [[universal polynomial|universal polynomials]] with integer coefficients. $R$ is in this case called a *$\lambda$-ring*. Note that the $\lambda^n$ are not required to be morphisms of rings.

A morphism of $\lambda$-structures is defined to be a morphism of rings commuting with all $\lambda^n$ maps.

There exists a $\lambda$-ring structure on the ring $1+ R[ [t] ]$ of power series with constant term $1$ where

a) addition on $1+R[ [t] ]$ is defined to be multiplication of power series

b) multiplication is defined by

$$(1+\sum_{n=1}^\infty r_n t^n)(1+\sum_{n=1}^\infty s_n t^n):=1+\sum_{n=1}^\infty P_n(r_1,\dots,r_n,s_1,\dots,s_n)t^n$$

c) the $\lambda$-operations are defined by

$$\lambda^n (1+\sum_{m=1}^\infty r_m t^m)=1+\sum_{m=1}^\infty P_{m,n}(r_1,\dots,r_{mn})t^m$$

([Hopkins](#Hopkins))
=--

+-- {: .num_remark}
###### Remark
Let $\Lambda$ denote the ring of [[symmetric function|symmetric functions]], let $R$ be a $\lambda$-ring.

Then for every $x\in R$ there is a unique morphism of $\lambda$-rings

$$\Phi_x:\Lambda\to R$$

sending $e_1\mapsto x$, $e_n\mapsto \lambda^n(x)$, $p_n\mapsto\psi^n(x)$ where $e_n$ denotes the $n$-th [[elementary symmetric function]] and $\psi^n$ denotes the $n$-th [[Adams operation]] (explained in the reference).

Equivalently this result asserts that $\Lambda$ is the free $\lambda$-ring in the single variable $e_1$.

([Hopkins](#Hopkins))
=--

+-- {: .proof}
###### Proof
We define $\Phi_x(e_1)=x$, then the assumption on $\Phi_x$ to be a morphism of $\lambda$-rings yields $\Phi_x(e_n)=\Phi_x(\lambda^n(e_1))=\lambda^n(x)$.
=--

+-- {: .num_remark}
###### Remark and Theorem
([Hazewinkel](#Hazewinkel) 1.11, 16.1)
a) The endofunctor of the category of commutative rings
$$\Lambda:\begin{cases}C Ring \to C Ring\\A\mapsto 1 + A [ [t] ]\end{cases}$$
sending a commutative ring to the set of power series with constant term $1$ is representable by the polynomial ring $Symm \coloneqq \mathbb{Z}[h_1, h_2,\dots]$ in an infinity of indeterminates over the integers.

b) There is an adjunction $(forget\, \lambda\dashv \Lambda)$ where $forget\,\lambda: \lambda Ring\to CRing$ is the forgetful functor assigning to a $\lambda$-ring its underlying commutative ring.

The left inverse $\g_{S,A}$ of the natural isomorphism $q_{S,A}:hom(forget\,\lambda,A)\to hom(S,\Lambda(A))$ is given by the [[ghost component]] $s_1$.
=--

An instructive introduction to the "orthodox"- and preparation for the "heterodox" view (described below) on $\lambda$-rings is Hazewinkel's survey article on Witt vectors, ([Hazewinkel](#Hazewinkel)). There is also a [[Hazewinkel, Witt vectors|reading guide]] to that article.


## The "heterodox" view on $\lambda$-rings

There is a second, "heterodox" way to approach $\lambda$-rings with a strong connection to [[arithmetic]] used by James Borger in his paper [$\Lambda$-rings and the field with one element](http://arxiv.org/abs/0906.3146).  Quoting the abstract:

>The theory of $\Lambda$-rings, in the sense of Grothendieck's Riemann--Roch theory, is an enrichment of the theory of commutative rings. In the same way, we can enrich usual [[algebraic geometry]] over the ring $\mathbf{Z}$ of integers to produce $\Lambda$-algebraic geometry. We show that $\Lambda$-algebraic geometry is in a precise sense an algebraic geometry over a deeper base than $\mathbf{Z}$ and that it has many properties predicted for algebraic geometry over the mythical [[field with one element]]. Moreover, it does this is a way that is both formally robust and closely related to active areas in arithmetic algebraic geometry.

Let $p$ be a prime number. Recall that for any commutative ring $R$  the [[Frobenius morphism]] is defined by $F_R:x\mapsto x^p$.

+-- {: .num_defn}
###### Defiition
Let $A$ be a commutative ring or a [[lambda ring]].
A morphism $Fl:A\to A$ is called a *Frobenis lift* if the restriction $Fl \,|_{A/pA}$ of $Fl$ to the quotient ring is the Frobenius morphism $F_{A/pA}$.
=--

+-- {: .num_example}
###### Example
The $p$-th [[Adams operation]] $\psi_p$ is a Frobenius lift. Moreover given any two prime numbers then their Adams operations commute with each other.
=--

The following two theorems are crucial for the "heterodox" point of view. We will see later that in fact we do not need the torsion-freeness assumption.

+-- {: .num_theorem}
###### Theorem
(Wilkerson's theorem)
Let $A$ be an additively torsion-free commutative ring. Let $\{\psi_p\}$ be a commuting family of Frobenius lifts.

Then there is a unique $\lambda$-ring structure on $A$ whose Adams operations are the given Frobenius lifts $\{\psi_p\}$.
=--

+-- {: .num_theorem}
###### Theorem
A ring morphism $f$ between two $\lambda$-rings is a morphism of $\lambda$-rings (i.e. commuting with the $\lambda$-operations) iff  $f$ commutes with the [[Adams operations]].
=--

+-- {: .num_cor}
###### Corollary
There is an equivalence between the category of torsion-free $\lambda$-rings and the category of torsion-free commutative rings.
=--

Now we will argue that these statements hold for arbitrary commutative rings.

+-- {: .num_remark}
###### Remark
a)  The category $\lambda Ring$ of $\lambda$-rings is [[monadic]] and [[comonadic]] over the category of $C Ring$ of commutative rings.

b)  The category $\lambda Ring_{\neg tor}$ of $\lambda$-rings is [[monadic]] and [[comonadic]] over the category of $C Ring_{\neg tor}$ of commutative rings.
=--

+-- {: .num_prop}
###### Proposition

Let $\i:C Ring_{\neg tor}\hookrightarrow C Ring$ be the inclusion. Let $W^\prime$ denote this comonad on $C Ring_{\neg tor}$. Then

a) $W \coloneqq Lan_i i\circ W^\prime \colon C Ring\to CRing$ is a comonad.

b) The category of coalgebras of $W$ is equivalent to the category of $\lambda$-rings.

c) $W$ is the [[big-Witt-vectors functor]].
=--

+-- {: .num_remark}
###### Remark
The "heterodox" generalizes to arbitrary [[Dedekind domain|Dedekind domains]] with finite residue field.

 For instance over $F_p[x]$ (instead of $\mathbb{Z}$), we would look at families of $\psi$-operators indexed by the irreducible monic polynomials $f(x)$, and each $\psi_{f(x)}$ would have to be congruent to the $q$-th power map modulo $f(x)$, where $q$ is the size of $F_p[x]/(f(x))$.
=--


## Related concepts

* [[Grothendieck group]]

* [[p-divisible group|p-divisible groups]].

* [[field with one element]]

* [[blueprint|blueprints]], [[blueprint|blue scheme]]


## References

* John Baez, [comment](http://golem.ph.utexas.edu/category/2007/12/this_weeks_finds_in_mathematic_19.html#c013821).

* Hazewinkel, formal groups and applications

* [[Hazewinkel, Witt vectors]], [pdf](http://arxiv.org/abs/0804.3888).{#Hazewinkel}

* John R. Hopkins, universal polynomials in lambda rings and the K-theory of the infinite loop space tmf, thesis, [pdf](http://dspace.mit.edu/bitstream/handle/1721.1/34544/71011847.pdf?sequence=1){#Hopkins}

* Donald Knutson, $\lambda$-Rings and the Representation Theory of the Symmetric Group, Lecture Notes in Mathematics, Vol. 308, Springer, Berlin, 1973.

* [concretenonsense blog](http://concretenonsense.wordpress.com/2009/07/23/lambda-rings)
* Donald Yau, [LAMBDA-RINGS] (http://www.worldscibooks.com/mathematics/7664.html), World Scientific, 2010.

school/conference in Leiden: Frobenius lifts and lambda rings 5-10. October 2009 featuring 

* Pierre Cartier: Lambda-rings and Witt vectors


* Lars Hesselholt: The de Rham-Witt complex

* Alexandru Buium: Arithmetic differential equations

* James Borger: Lambda-algebraic geometry 

[conference site](http://www.lorentzcenter.nl/lc/web/2009/342/info.php3?wsid=342)

[participants](http://www.lorentzcenter.nl/lc/web/2009/342/participants.php3?wsid=342)




[[!redirects lambda-ring]]
[[!redirects ∞-ring]]
[[!redirects ∞-ring]]
[[!redirects Lambda-rings]]
[[!redirects lambda-rings]]
[[!redirects ∞-rings]]
[[!redirects ∞-rings]]
[[!redirects lambda ring]]