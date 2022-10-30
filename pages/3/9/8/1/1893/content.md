
> There is also a notion of [[special lambda-ring]]. But in most cases by ''$\lambda$-ring'' is meant ''special $\lambda$-ring''.


# $\Lambda$-rings
* table of contents
{: toc}



## Idea

A _$\lambda$-ring_ is a [[commutative ring]] which is in addition equipped with operations that behave as the operations of forming [[exterior powers]] (of [[vector spaces]]/[[representations]]) in a [[representation ring]]. The name derives from the common symbol $\Lambda^n$ for the $n$th [[exterior power]].

### Motivation from representation theory

Typically one can form [[direct sums]] of [[representations]] of some [[algebra|algebraic]] [[structure]].  The [[decategorification]] to [[isomorphism classes]] of such [[representations]] then  inherits the structure of a [[commutative monoid]]. But nobody likes commutative monoids: we all have an urge to subtract.  So, we throw in formal negatives and get an [[abelian group]] --- the _[[Grothendieck group]]_.

In many situations, we can also take [[tensor product|tensor products]] of representations.  Then the Grothendieck group becomes something better than an abelian group.  It becomes a [[ring]]: the [[representation ring]]. 
Moreover, in many situations we can also take [[exterior power|exterior]] and [[symmetric power|symmetric]] powers of representations;  indeed, we can often apply any [[Young diagram]] to a representation and get a new representation. Then the [[representation ring]] becomes something better than a ring: it becomes a _$\lambda$-ring_.

More generally, the [[Grothendieck group]] of a [[monoidal category|monoidal]] [[abelian category]] is always a ring, called a [[Grothendieck ring]].   If we start with a [[braided monoidal category|braided monoidal]] abelian category, this ring is commutative.   But if we start with a [[symmetric monoidal category|symmetric monoidal]] abelian category, we get a $\lambda$-ring.   

So, $\lambda$-rings are all about getting the most for your money when you [[decategorify|decategorify]] a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] --- for example the category of [[representations]] of a [[group]], or the category of [[vector bundle|vector bundles]] on a [[topological space]].


Unsurprisingly, the [[Grothendieck group]] of the free symmetric monoidal abelian category on one generator is the free $\lambda$-ring on one generator.  This category is very important in representation theory.  Objects in this category are called [[Schur functor|Schur functors]], because for obvious reasons they act as functors on _any_ symmetric monoidal abelian category.  The irreducible objects in this category are called 'Young diagrams'.  Elements of the free $\lambda$-ring on one generator are called [[symmetric function|symmetric functions]].


### In terms of universal algebra

A *$\lambda$-ring* $L$ is a [[P-ring]] presented by the [[polynomial ring]] $Symm=\mathbb{Z}[h_1,h_1\dots]$ in countably many indeterminates over the [[integer|integers]] or, equivalently, $Symm$ is the ring of [[symmetric function|symmetric functions]] in countably many [[variables]]. This means that (the underlying set valued functor of) $L$ is a [[copresheaf]] presented by $Symm$ such that

1. $L:\CRing \to CRing$ defines an endofunctor on the category of commutative rings.

2. $L$ gives rise to a [[comonad]] on $C Ring$.

A $\lambda$-ring is hence a commutative ring equipped with a [[co-action]] of this comonad. As always is the case with [[monad|monads]] and comonads this definition can be formulated in terms of an [[adjunction]].



## Definition
 
### The "orthodox" definition

+-- {: .num_defn}
###### Definition

A _$\lambda$-structure_ on a [[commutative ring|commutative unital ring]] $R$ is defined to be a sequence of maps $\lambda^n$ for $n\ge 0$ satisfying

1. $\lambda^0(r)=1$ for all $r\in R$

2. $\lambda^1=id$

3. $\lambda^n(1)=0$, for $n\gt 1$

4. $\lambda^n(r+s)=\sum_{k=0}^n \lambda^k(r)\lambda^{n-k}(s)$, for all $r,s\in R$

5. $\lambda^n(r s)=P_n(\lambda^1(r),\dots,\lambda^n(r),\lambda^1(s),\dots,\lambda^n(s))$ for all $r,s\in R$

6. $\lambda^m(\lambda^n(r)):=P_{m,n}(\lambda^1(r),\dots,\lambda^{m n}(r))$, for all $r\in R$

where $P_n$and $P_{m,n}$ are certain (see the reference for their calculation) [[universal polynomial|universal polynomials]] with integer coefficients. $R$ is in this case called a *$\lambda$-ring*. Note that the $\lambda^n$ are not required to be morphisms of rings.

A [[homomorphism]] of $\lambda$-structures is defined to be a [[homomorphism]] of [[rings]] commuting with all $\lambda^n$ maps.

=--

+-- {: .num_example}
###### Example

There exists a $\lambda$-ring structure on the ring $1+ R[ [t] ]$ of 
[[power series]] with constant term $1$ where

a) addition on $1+R[ [t] ]$ is defined to be multiplication of power series

b) multiplication is defined by

$$(1+\sum_{n=1}^\infty r_n t^n)(1+\sum_{n=1}^\infty s_n t^n):=1+\sum_{n=1}^\infty P_n(r_1,\dots,r_n,s_1,\dots,s_n)t^n$$

c) the $\lambda$-operations are defined by

$$\lambda^n (1+\sum_{m=1}^\infty r_m t^m)=1+\sum_{m=1}^\infty P_{m,n}(r_1,\dots,r_{mn})t^m$$

=--

([Hopkinson](#Hopkinson))

+-- {: .num_prop}
###### Proposition

Let $\Lambda$ denote the ring of [[symmetric function|symmetric functions]], let $R$ be a $\lambda$-ring.

Then for every $x\in R$ there is a unique [[homomorphism]] of $\lambda$-rings

$$\Phi_x:\Lambda\to R$$

sending $e_1\mapsto x$, $e_n\mapsto \lambda^n(x)$, $p_n\mapsto\psi^n(x)$ where $e_n$ denotes the $n$-th [[elementary symmetric function]] and $\psi^n$ denotes the $n$-th [[Adams operation]] (explained in the reference).

Equivalently this result asserts that $\Lambda$ is the [[free construction|free]] $\lambda$-ring in the single variable $e_1$.

=--

This is due to ([Hopkinson](#Hopkinson))


+-- {: .proof}
###### Proof

We define $\Phi_x(e_1)=x$, then the assumption on $\Phi_x$ to be a morphism of $\lambda$-rings yields $\Phi_x(e_n)=\Phi_x(\lambda^n(e_1))=\lambda^n(x)$.

=--

+-- {: .num_theorem}
###### Theorem
([Hazewinkel](#Hazewinkel) 1.11, 16.1)

a) The [[endofunctor]] of the [[category]] of commutative rings
$$\Lambda:\begin{cases}C Ring \to C Ring\\A\mapsto 1 + A [ [t] ]\end{cases}$$
sending a commutative ring to the set of power series with constant term $1$ is representable by the polynomial ring $Symm \coloneqq \mathbb{Z}[h_1, h_2,\dots]$ in an infinity of indeterminates over the integers.

b) There is an [[adjunction]] $(forget\, \lambda\dashv \Lambda)$ where $forget\,\lambda: \lambda Ring\to CRing$ is the forgetful functor assigning to a $\lambda$-ring its underlying commutative ring.

The left inverse $\g_{S,A}$ of the natural isomorphism $q_{S,A}:hom(forget\,\lambda,A)\to hom(S,\Lambda(A))$ is given by the ghost component $s_1$.

(see also ([Borger 08, section 1.8](#Borger08)))

=--

An instructive introduction to the "orthodox"- and preparation for the "heterodox" view (described below) on $\lambda$-rings is Hazewinkel's survey article on [[Witt vectors]], ([Hazewinkel](#Hazewinkel)). There is also a [[Hazewinkel, Witt vectors|reading guide]] to that article.


### The "heterodox" definition
 {#HeterodoxDefinition}

There is a second, "heterodox" way to approach $\lambda$-rings with a strong connection to [[arithmetic]] discussed in detail in ([Borger 08, section 1](#Borger08)). An survey is in ([Borger 09](#Borger09)) where it says in the abstract:


>The theory of $\Lambda$-rings, in the sense of Grothendieck's Riemann--Roch theory, is an enrichment of the theory of commutative rings. In the same way, we can enrich usual [[algebraic geometry]] over the ring $\mathbf{Z}$ of integers to produce $\Lambda$-algebraic geometry. We show that $\Lambda$-algebraic geometry is in a precise sense an algebraic geometry over a deeper base than $\mathbf{Z}$ and that it has many properties predicted for algebraic geometry over the mythical [[field with one element]]. Moreover, it does this in a way that is both formally robust and closely related to active areas in arithmetic algebraic geometry.



First some standard notation:

+-- {: .num_defn #FrobeniusMorphism}
###### Definition

For $p$ a [[prime number]] write $\mathbb{F}_p$ for the [[finite field]] whose underlying [[abelian group]] is the [[cyclic group]] $\mathbb{Z}/p\mathbb{Z}$.

For $A$ an $\mathbb{F}_p$-[[associative algebra|algebra]], then the [[Frobenius endomorphism]] 

$$
  F_p \colon A \longrightarrow A
$$

is that given by taking each element to its $p$th power

$$
  F_p \colon x \mapsto x^p
  \,.
$$

=--


+-- {: .num_defn #LambdaRingByFrobeniusLifts}
###### Definition

For $p$ a [[prime number]], then a _$p$-typical $\Lambda$-ring_ is 

* a [[commutative ring]] $R$ 

* equipped with an [[endomorphism]] $F_A \colon A \to A$

such that under [[tensor product]] with $\mathbb{F}_p$ it becomes the [[Frobenius morphism]], def.\ref{FrobeniusMorphism}:

$$
  \mathbb{F}_p \otimes_{\mathbb{Z}} F_A
  =
  F_p 
  \;
   \colon 
  \;
  \mathbb{F}_p \otimes_{\mathbb{Z}} A
   \longrightarrow  
  \mathbb{F}_p \otimes_{\mathbb{Z}} A
  \,.
$$

A _big $\Lambda$-ring_ is a commutative ring equipped with commuting endomorphisms, one for each prime number $p$, such that each of them makes the ring $p$-typical, respectively, as above.

=--

This is def. 1.7 in ([Borger 08](Borger08)), formulated for the special case of example 1.15 there (which is stated in terms of Witt vectors) and translated to $\Lambda$-rings in view of prop. 1.10 c) (see [the adjunction](#AdjointTriple)) there.


> the following originates from revision 19 but needs attention


+-- {: .num_example}
###### Example
The $p$-th [[Adams operation]] $\psi_p$ is a Frobenius lift. Moreover given any two prime numbers then their [[Adams operations]] commute with each other.
=--

The following two theorems are crucial for the "heterodox" point of view. We will see later that in fact we do not need the torsion-freeness assumption.

+-- {: .num_theorem}
###### Theorem
(Wilkerson's theorem)
Let $A$ be an additively torsion-free commutative ring. Let $\{\psi_p\}$ be a commuting family of Frobenius lifts.

Then there is a unique $\lambda$-ring structure on $A$ whose [[Adams operations]] are the given Frobenius lifts $\{\psi_p\}$.
=--

+-- {: .num_theorem}
###### Theorem
A ring morphism $f$ between two $\lambda$-rings is a morphism of $\lambda$-rings (i.e. commuting with the $\lambda$-operations) iff  $f$ commutes with the [[Adams operations]].
=--

+-- {: .num_cor}
###### Corollary
There is an equivalence between the category of torsion-free $\lambda$-rings and the category of torsion-free commutative rings equipped with commuting Frobenius lifts..
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

## Properties

### Free and co-free $\Lambda$-rings -- Symmetric function and Witt vectors
 {#FreeAndCofreeLambdaRings}


+-- {: .num_prop #AdjointTriple}
###### Proposition

The [[forgetful functor]]
$U \;\colon\; \Lambda Ring \longrightarrow CRing$
from $\Lambda$-rings to [[commutative rings]] has 

* a [[left adjoint]], given by forming the ring $Symm$ of [[symmetric functions]];

* a [[right adjoint]] given by forming the [[ring of Witt vectors]] $W$.

$$
  (Symm \dashv U \dashv W)
  \;\colon\;
  \Lambda Ring
   \stackrel{\overset{Symm}{\leftarrow}}{\stackrel{\overset{U}{\longrightarrow}}{\underset{W}{\leftarrow}}}
  CRing
  \,.
$$

Hence 

* [[rings of Witt vectors]] are the _[[co-free functors|co-free]] Lambda-rings;

* rings of [[symmetric functions]] are the [[free construction|free]] Lambda-rings.

=--

This statement appears in ([Hazewinkel 08, p. 87, p. 97, 98](#Hazewinkel08)). The right adjoint in a more general context is in ([Borger 08, prop. 1.10 (c)](#Borger08)).



+-- {: .num_remark}
###### Remark

On the level of [[toposes]] ([[etale toposes]]) over these [[sites]] of rings, this statement reappears as an [[essential geometric morphism]]
from the [[etale topos]] of [[Spec(Z)]] to that over "[[F1]]"
in [[Borger's absolute geometry]] ([Borger 08](#Borger08), exposition in [Borger 09](#Borger09)).

=--




## Related concepts

* [[Grothendieck group]]

* [[p-divisible group|p-divisible groups]].

* [[field with one element]]

* [[blueprint|blueprints]], [[blueprint|blue scheme]]

* [[Witt vector]]

* [[Borger's absolute geometry]]


## References


* [[Michiel Hazewinkel]], _Formal groups and applications_

* {#Hazewinkel08} [[Michiel Hazewinkel]],  _[[Hazewinkel, Witt vectors|Witt vectors]]_, ([arXiv](http://arxiv.org/abs/0804.3888))
  

* John Baez, [comment](http://golem.ph.utexas.edu/category/2007/12/this_weeks_finds_in_mathematic_19.html#c013821).


* John R. Hopkinson, _Universal polynomials in lambda-rings and the K-theory of the infinite loop space $tmf$_, thesis, [pdf](http://dspace.mit.edu/bitstream/handle/1721.1/34544/71011847.pdf?sequence=1)
  {#Hopkinson}

* Donald Knutson, $\lambda$-Rings and the Representation Theory of the Symmetric Group, Lecture Notes in Mathematics, Vol. 308, Springer, Berlin, 1973.

* [concretenonsense blog](http://concretenonsense.wordpress.com/2009/07/23/lambda-rings)
* Donald Yau, [LAMBDA-RINGS] (http://www.worldscibooks.com/mathematics/7664.html), World Scientific, 2010.

school/conference in Leiden: Frobenius lifts and lambda rings 5-10. October 2009 featuring 

* [[Pierre Cartier]]: Lambda-rings and Witt vectors


* [[Lars Hesselholt]]: The de Rham-Witt complex

* Alexandru Buium: Arithmetic differential equations

* [[James Borger]]: Lambda-algebraic geometry 


[conference site](http://www.lorentzcenter.nl/lc/web/2009/342/info.php3?wsid=342)

[participants](http://www.lorentzcenter.nl/lc/web/2009/342/participants.php3?wsid=342)

Discussion in the context of [[Borger's absolute geometry]] is in

* {#Borger08} [[James Borger]], section 1 of _The basic geometry of Witt vectors, I: The affine case_ ([arXiv:0801.1691](http://arxiv.org/abs/0801.1691))


* {#Borger09} [[James Borger]], _Lambda-rings and the field with one element_ ([arXiv/0906.3146](http://arxiv.org/abs/0906.3146))


[[!redirects Lambda-ring]]
[[!redirects Lambda-rings]]
[[!redirects Lambda ring]]
[[!redirects Lambda rings]]
[[!redirects lambda-ring]]
[[!redirects lambda-rings]]
[[!redirects lambda ring]]
[[!redirects lambda rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]