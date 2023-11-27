
> For the non-cartesian case see at *[[distributive monoidal category]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition 

+-- {: .num_defn}
###### Definition

A [[category]] $C$  with [[finite products]] $(-)\times(-)$ and [[finite coproducts]] $(-) + (-)$ is called (finitary) **distributive** if for any $X,Y,Z\in C$ the canonical [[distributivity]] morphism
$$ X\times Y + X\times Z \longrightarrow X\times (Y+Z)$$
is an [[isomorphism]].  The canonical morphism is the unique morphism such that $X\times Y \to X\times (Y+Z)$ is $X\times i$, where $i\colon Y\to Y +Z$ is the coproduct injection, and dually for $X\times Z \to X\times (Y+Z)$.

Equivalently, a category $C$ with finite products and coproducts is distributive if for any $X \in C$, the functor $X \times -$ [[preserved limit|preserves finite coproducts]].

=--

+-- {: .num_remark}
###### Remark

This notion is part of a hierarchy of [[distributivity for monoidal structures]], and generalizes to [[distributive monoidal categories]] and [[rig categories]].  A [[linearly distributive category]] is _not_ distributive in this sense.

=--

This axiom on binary coproducts easily implies the analogous $n$-ary result for $n\gt 2$.  In fact it also implies the analogous 0-ary statement that the projection
$$ X\times 0 \to 0$$
is an isomorphism for any $X$ (see Proposition \ref{nullary} below).  Moreover, for a category with finite products and coproducts to be distributive, it actually suffices for there to be *any* [[natural transformation|natural]] family of isomorphisms $X\times Y + X\times Z \cong X\times (Y+Z)$, not necessarily the canonical ones ([Lack](#Lack)).

A category $C$ with finite products and all small coproducts is **infinitary distributive** if the statement applies to all small coproducts.  One can also consider $\kappa$-distributivity for a [[cardinal number]] $\kappa$, meaning the statement applies to coproducts of cardinality $\lt\kappa$.

Any [[extensive category]] with finite products is distributive, but the converse is not true.

## Properties 

+-- {: .num_prop #monic} 
###### Proposition 
In a category with products and coproducts, if products distribute over binary coproducts, then [[coproduct]] [[coprojections]] are [[monomorphism|monic]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $i_B: B \to B + C$ be a coproduct coprojection, and suppose given maps $f, g: A \to B$ such that $i_B f = i_B g$. We observe that the coprojection 

$$i: A \times B \to A \times B + A \times C$$ 

is monic because it has a [[retraction]] $(1_{A \times B}, \phi): A \times B + A \times C \to A \times B$. (All we need here is the existence of a map $\phi: A \times C \to A \times B$, for example the composite $A \times C \stackrel{\pi_A}{\to} A \stackrel{\langle 1_A, f \rangle}{\to} A \times B$.)  

The composite of the coprojection $i$ with the canonical isomorphism $A \times B + A \times C \cong A \times (B + C)$, namely $1_A \times i_B: A \times B \to A \times (B + C)$, is therefore also monic. Given that $\langle 1_A, i_B f \rangle = \langle 1_A, i_B g \rangle: A \to A \times (B + C)$, we conclude 

$$(1_A \times i_B)\langle 1_A, f \rangle = \langle 1_A, i_B f \rangle = \langle 1_A, i_B g \rangle = (1_A \times i_B)\langle 1, g \rangle,$$ 

whence $\langle 1_A, f\rangle = \langle 1_A, g\rangle: A \to A \times B$ since $1_A \times i_B$ is monic. It follows that $f = g$, as was to be shown. 
=-- 

+-- {: .num_prop #nullary} 
###### Proposition 
If products distribute over binary coproducts, then products distribute over nullary coproducts (i.e., the projection $X \times 0 \to 0$ is an isomorphism for all objects $X$). 
=-- 

+-- {: .proof} 
###### Proof 
We show that $X \times 0$ is initial. Clearly $\hom(X \times 0, Y)$ is inhabited by $X \times 0 \to 0 \to Y$ for any object $Y$. On the other hand, since the two coprojections $0 \to 0 + 0$ coincide, the same holds for the two coprojections $X \times 0 \to (X \times 0) + (X \times 0)$, by applying the distributivity isomorphism $X \times (0 + 0) \cong (X \times 0) + (X \times 0)$. This is enough to show that any two maps $X \times 0 \to Y$ coincide, since given maps $f, g : X \times 0 \to Y$, we have $f = [f, g] \circ i_1 = [f, g] \circ i_2 = g$.
=-- 

+-- {: .num_prop} 
###### Proposition  
In a distributive category, the [[initial object]] is [[strict initial object|strict]]. 
=-- 

+-- {: .proof} 
###### Proof 
Given an arrow $f: A \to 0$, we have that $\pi_A: A \times 0 \to A$ is a retraction of $\langle 1, f \rangle: A \to A \times 0$, so that $A$ is a retract of $A \times 0 \cong 0$. But retracts of initial objects are initial. 
=-- 

## Examples
 {#Examples}

Every [[bicartesian closed category]] is distributive since in that case the cartesian product $X \times -$ is a [[left adjoint]] and then the distributivity requirement is an instance of the [[adjoints preserve (co-)limits|preservation of colimits by left adjoints]].
For example,

* the category [[Set]] of [[sets]], 

* any [[topos]].

But closedness is far from necessary, for example

* the category [[Top]] of [[topological spaces]] with respect to forming [[product topological spaces]] and [[disjoint union topological spaces]];

is a distributive category.

These categories have in common that they are [[extensive category|extensive]]. An example[^Freyd] of a distributive category that is not extensive is given by

* the category of [[rectangular bands]] which has objects [[semigroup|semigroups]] $X$ satisfying $x x = x$ for all $x\in X$ and $x y x=x$ for all $x,y\in X$.

Since for [[poset|posets]] viewed as categories, finite products and coproducts are given by [[meets]] and [[joins]] we find:

* A [[poset]] viewed as a category is distributive iff it is a [[distributive lattice]]. Accordingly, non distributive lattices provide instances of categories with finite products and coproducts that do not distribute over each other.

A further non-example:

* The category $Pfn$ of sets and [[partial functions|partial functions]] has finite coproducts and products. The former given by [[disjoint unions]] as in [[Set]] and the latter by $(X\times Y)+X+Y$ (where $\times,+$ indicate the usual product and coproduct in $Set$) with projections $\pi_1,\pi_2$ given on the domains of definition $(X\times Y)+X$ (resp. $(X\times Y)+Y$) by $\pi_1((x,y))=x$ and $\pi_1(x)=x$ (resp. $\pi_2((x,y))=y$ and $\pi_2(y)=y$). Since the [[initial object]] $\empty$ is not [[strict initial object|strict]], $Pfn$ is not distributive.


[^Freyd]: Pointed out by [[Peter Freyd]] in [this discussion](https://www.mta.ca/~cat-dist/catlist/1999/extensive).

## Free distributive categories

\begin{proposition}

* The free distributive category on a category $\mathcal{C}$ with finite products is given by the finite [[free coproduct completion]]: $FinCoprod(\mathcal{C})$. That is, $FinCoprod(\mathcal{C})$ is distributive, and induces a bijection between distributive functors $FinCoprod(\mathcal{C})\to \mathcal{D}$ and product preserving functors 
$\mathcal{C}\to \mathcal{D}$, natural in distributive categories $\mathcal{D}$.

* The free distributive category on a category $\mathcal{C}$ is the finite [[free coproduct completion]] of the finite [[free product completion]]: $FinCoprod(FinProd(\mathcal{C}))$. That is, $FinCoprod(FinProd(\mathcal{C}))$ is distributive, and induces a bijection between distributive functors $FinCoprod(FinProd(\mathcal{C}))\to \mathcal{D}$ and functors 
$\mathcal{C}\to \mathcal{D}$, natural in distributive categories $\mathcal{D}$. 

\end{proposition}
This is noted in [Cockett 1993, p. 280, also Corollary 5.9](#Cockett93), where [[Bob Walters]] and [[Shu-Hao Sun]] are named as advocates of this method. (However, note that Cockett does not insist on an initial object.)

In particular, then, the free distributive category, which is the free distributive category on the empty category, is the [[category of finite sets]], up to equivalence.

## Related concepts

* [[distributive law]]

* [[distributivity for monoidal structures]]

  * [[distributive monoidal category]]

  * [[bipermutative category]]

  * [[linearly distributive category]]

  * [[rig category]]

* [[extensive category]]

* [[distributive lattice]]

* [[objective number theory]]

* [[completely distributive category]]

* [[totally distributive category]]



## References 

* {#CarboniLackWalters93} [[Aurelio Carboni]], [[Stephen Lack]], [[Bob Walters|R. F. C. Walters]], _Introduction to extensive and distributive categories_, JPAA **84** (1993) pp. 145-158 &lbrack;<a href="https://doi.org/10.1016/0022-4049(93)90035-R">doi:10.1016/0022-4049(93)90035-R</a>&rbrack;

* {#Cockett93} [[Robin Cockett]], *Introduction to distributive categories*, Mathematical Structures in Computer Science **3** (2009) 277-307 &lbrack;<a href="https://doi.org/10.1017/S0960129500000232">doi:10.101/S0960129500000232</a>&rbrack;

* {#Lack} [[Stephen Lack]], *Non-canonical isomorphisms*, Journal of Pure and Applied Algebra **216** 3 (2012) 593-597  &lbrack;[arXiv:0912.2126](http://arxiv.org/abs/0912.2126), [doi:10.1016/j.jpaa.2011.07.012](https://doi.org/10.1016/j.jpaa.2011.07.012)&rbrack;

See also

* {#catlistdiscussion}[Freyd, Lack, Lawvere et al: CATLIST discussion on extensive categories 1996](https://www.mta.ca/~cat-dist/catlist/1999/extensive)

* Wikipedia, *[Distributive category](https://en.wikipedia.org/wiki/Distributive_category)*

For more see at *[[distributive monoidal category]]*.


[[!redirects distributive categories]] 
[[!redirects distributive coproduct]]
[[!redirects distributive coproducts]]
