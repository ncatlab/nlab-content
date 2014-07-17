
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Banach algebras
* table of contents
{: toc}

## Definitions

An associative unital Banach algebra is [[monoid object]] in the [[closed monoidal category]] of [[Banach spaces]] (with [[short linear operators]] as [[morphisms]], and the usual [[internal hom]], or equivalently the [[projective tensor product]]).  However, Banach algebras are not usually assumed to be unital, making them [[semigroup]] objects (or even [[magma]] objects if not assumed to be associative).

Explicitly, this means a [[Banach space]] $A$ equipped with a [[bilinear map|bilinear]] _multiplication_ map
$$ m\colon A \times A \to A ,$$
which again is usually taken to be [[associativity|associative]] (and may even be unital), such that
$$ {\|a \cdot b\|} \leq {\|a\|} \cdot {\|b\|} ,$$
where $a \cdot b$ (or just $a b$) means $m(a, b)$.

In the unital case, we should also require ${\|1\|} \leq 1$, although some authors leave this out.  Other authors require ${\|1\|} = 1$, which is too strong, since it rules out the [[trivial ring|trivial algebra]].  (However, ${\|1\|} = 1$ follows from ${\|1\|} \leq 1$ and the existence of any element $a \ne 0$).  One can of course always formally adjoin a unit $e$ with ${\|e\|} = 1$, forming the Banach algebra $A \oplus \langle{e}\rangle$ (using the $l^1$-[[l-1-direct sum|direct sum]]).

The explicit description in terms of $m$ is of course earlier; but the abstract description as an internal monoid makes clear the most natural definition of [[Banach coalgebra]]: a [[comonoid]] in the same monoidal category.

+-- {: .query}
YC: An earlier version of this entry said that "the correct" definition of Banach coalgebra is as a comonoid in the usual monoidal category of Banach spaces and [[short linear operators]]. I would prefer that this be amended, with similar wording as what I've chosen, since experience has shown that the most fruitful candidates for "Banach spaces with coalgebraic structure" are NOT comonoids in this sense. One should instead only require a comultiplication which takes values in something like the injective tensor product, or if you are working with Cstar objects, in something like the spatial tensor product. Does anyone object to my rewording?
=--

## Examples

* A standard associative example is $L^1(\mathbb{R})$ with [[Lebesgue measure]], where the multiplication is taken to be [[convolution]]. (This lacks a unit for the multiplication, since there is no $L^1$ function $e$ that represents the [[Dirac functional]] $f \mapsto f(0)$, via
$$ f(0) = \int_{-\infty}^{\infty} e(x) f(x) \,\mathrm{d}x ,$$ 
on [[continuous functions]] $f\colon X \to \mathbb{C}$.) One can generalize this example in straightforward fashion, replacing $\mathbb{R}$ by any [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological group]] $G$, and Lebesgue measure by a [[Haar measure]] on $G$; the algebra is unital if and only if $G$ is [[discrete space|discrete]].

* For *any* [[measure space]] $X$, $L^{\infty}(X)$ is a [[commutative ring|commutative]] unital associative Banach algebra (in fact a unital $C^*$-[[C-star-algebra|algebra]], in fact a [[von Neumann algebra]] if $X$ is [[localizable measure space|localizable]]) with respect to pointwise multiplication.

* If $A$ is a Banach space, the [[internal hom]] $hom(A, A)$ is a unital Banach algebra (by [[general abstract nonsense]]).

* Any $C^*$-[[C-star algebra|algebra]] (and thus every [[von Neumann algebra]]) is in particular a Banach algebra.

* The [[normed division algebras]] are (possibly nonassociative) Banach [[division algebras]] over $\mathbb{R}$.

* The only Banach division algebra over $\mathbb{C}$ is $\mathbb{C}$ itself, by the [[Gel'fand–Mazur theorem]].

* A $JB$-[[JB-algebra|algebra]] (or more generally a [[Jordan–Banach algebra]]) is a nonassociative (but commutative) kind of Banach algebra.  (The commutative associative Banach algebras also count as Jordan--Banach algebras.)


### An example of a 'nonunital' Banach algebra that has an identity element
Let $C_n$ be a cyclic group of order $n\geq 2$ and look at the Banach algebra (in the "strict" sense of a monoid object in $Ban$) that is obtained by equipping the Banach space $\ell^1(C_n)$ with the natural convolution product: $\delta_x * \delta_y = \delta_{x+y}$. There is a "short" homomorphism from $\ell^1(C_n)$ into the ground field which is just the unique linear extension of the group homomorphism $C_n \to \{1\}$ (by the free property of the $\ell^1$-functor) and we let $J$ be the kernel of this homomorphism. ($J$ is the so-called "augmentation ideal".) Now $J$ is a semigroup object in $Ban$ and as an algebra it has an identity element $p$, but a calculation/hindsight shows that $\delta_e-p$ must be the constant function $C_n \to \{1/n\}$, so that $p$ has norm $(1-1/n)+(n-1)/n = 2-2/n$.

## Arens products
If $A$ is a Banach algebra, its bidual $A^{**}$ has two naturally induced Banach algebra structures on it: these are the so-called Arens products on the second dual. These correspond to the left and right [[tensorial strength]]s for the bidual monad on the category of Banach spaces (whether with [[short linear operators]] as [[morphisms]], or all bounded linear operators). In different language, the two Arens multiplications arise from natural transformations 

$$\alpha_{A B}: A^{\ast\ast} \otimes B^{\ast\ast} \to (A \otimes B)^{\ast\ast}$$ 

$$\,$$ 

$$\beta_{A B}: A^{\ast\ast} \otimes B^{\ast\ast} \to (A \otimes B)^{\ast\ast}$$ 

described at [[monoidal monad]]; putting $A = B$ and post-composing with $m^{\ast\ast}: (A \otimes A)^{\ast\ast} \to A^{\ast\ast}$ produces the two Arens products. They are named for Richard Arens, who has a 1955 paper which studies this construction in a more general setting . One can see Arens's "phyla" -- with hindsight and Whig history -- as a precursor of symmetric closed monoidal categories.

[Link to talk by F. E. J. Linton on Arens products](http://tlvp.net/~fej.math.wes/CMS-June2010/Arens01.htm)


#### Arens regularity
Algebras where the two Arens products coincide are said to be Arens regular: since $B(H)$, the algebra of bounded linear operators on a Hilbert space $H$, has this property, so do all its closed subalgebras, in particular all $C^*$-[[C-star algebra|algebra]]s.
In contrast, if $G$ is an infinite locally compact group, a result of N. J. Young shows that $L^1(G)$ is not Arens regular. Consequently, it is not isomorphic as a topological algebra to any closed subalgebra of $B(H)$. Note that this consequence is significantly deeper than the observation that the norm on $L^1(G)$ does not satisfy the C-star identity with respect to the usual involution on $L^1(G)$. See also comments on [this MO question](http://mathoverflow.net/questions/134074/banach-algebra-counterexample).

In general, a Banach algebra $A$ is Arens regular if and only if, for each $\mu\in A^*$, the orbit maps $a\mapsto a\cdot\mu$ and $a\mapsto \mu\cdot a$ are [[weakly compact]] as linear maps $A\to A^*$. (Going from memory here, this result is due to J. S. Pym.) By using known results for factorization of [[weakly compact]] maps, it follows that if $A$ is Arens regular, one can construct a [[reflexive Banach space]] $E$ and an injective homomorphism of topological algebras $A\to B(E)$ which has closed range; this appears to have first been done explicitly by S. Kaijser.
+-- {: .query}
I suspect that here I mean something like a strict monomorphism in the category of monoid objects in TVS, but I am not sure of the details.
=--
However, this is not a characterization of Arens regularity; Young also observed that for any locally compact group $G$ one may build a reflexive Banach space $E$ and construct an injective homomorphism of topological algebras $L^1(G)\to B(E)$ which has closed range.

## Related concepts

* [[Banach module]]

[[!include analytic geometry ingredients -- table]]

## References

* Zbigniew Semadeni, _Banach spaces of continuous functions_, vol. I, [gBooks](http://books.google.com/books/about/Banach_spaces_of_continuous_functions.html?id=vCDvAAAAMAAJ)

* N. Landsman, _Mathematical topics between classical and quantum mechanics_, Springer

* Walter Rudin, _Functional analysis_

* Richard V. Kadison, John R. Ringrose, _Fundamentals of the theory of operator algebras_

* F. F. Bonsall, J. Duncan, _Complete normed algebras_


* T. W. Palmer, _Banach Algebras and the General Theory of \* -Algebras_

Discussion in the context of ([[global analytic geometry]]) [[analytic geometry]] is in the following articles.

Lecture notes on the concept of the [[spectrum (geometry)]] of a Banach ring include

* Sarah  Brodsky, _Non-archimedean geometry_ ([pdf](http://math.berkeley.edu/~sstich/MAT_274/Math_274_3_Feb_2012.pdf))

A more [[topos theory|topos-theoretic]] perspective:


* {#BassatKremnitzer13} [[Oren Ben-Bassat]], [[Kobi Kremnizer]], section 6.5 of _Non-Archimedean analytic geometry as relative algebraic geometry_ ([arXiv:1312.0338](http://arxiv.org/abs/1312.0338))
category: analysis


[[!redirects Banach algebra]]
[[!redirects Banach algebras]]

