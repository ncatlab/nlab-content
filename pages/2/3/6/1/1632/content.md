
# Banach algebras
* tic
{: toc}

## Definitions

An associative unital Banach algebra is [[monoid object]] in the [[closed monoidal category]] of [[Banach spaces]] (with [[short linear operators]] as [[morphisms]], and the usual [[internal hom]], or equivalently the [[projective tensor product]]).  However, Banach algebras are not usually assumed to be unital, making them [[semigroup]] objects (or even [[magma]] objects if not assumed to be associative).

Explicitly, this means a [[Banach space]] $A$ equipped with a [[bilinear map|bilinear]] _multiplication_ map
$$ m\colon A \times A \to A ,$$
which again is usually taken to be associative (and may even be unital), such that
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
on [[continuous functions]] $f\colon X \to \mathbb{C}$.) One can generalize this example in straightforward fashion, replacing $\mathbb{R}$ by any [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological group]] $G$, and $\mu$ by a [[Haar measure]] on $G$; the algebra is unital if and only if $G$ is [[compact space|compact]].

* For *any* [[measure space]] $X$, $L^{\infty}(X)$ is a [[commutative ring|commutative]] unital associative Banach algebra (in fact a unital $C^*$-[[C-star-algebra|algebra]], in fact a [[von Neumann algebra]] if $X$ is [[localizable measure space|localizable]]) with respect to pointwise multiplication.

* If $A$ is a Banach space, the [[internal hom]] $hom(A, A)$ is a unital Banach algebra (by [[general abstract nonsense]]).

* Any $C^*$-[[C-star algebra|algebra]] (and thus every [[von Neumann algebra]]) is in particular a Banach algebra.

* The [[normed division algebras]] are (possibly nonassociative) Banach [[division algebras]] over $\mathbb{R}$.

* The only Banach division algebra over $\mathbb{C}$ is $\mathbb{C}$ itself, by the [[Gel'fand–Mazur theorem]].

* A $JB$-[[JB-algebra|algebra]] (or more generally a [[Jordan–Banach algebra]]) is a nonassociative (but commutative) kind of Banach algebra.  (The commutative associative Banach algebras also count as Jordan--Banach algebras.)


### Arens products
If $A$ is a Banach algebra, its bidual $A^{**}$ has two naturally induced Banach algebra structures on it: these are the so-called Arens products on the second dual. These correspond to the left and right [[tensorial strength]]s for the bidual monad on the category of Banach spaces (whether with [[short linear operators]] as [[morphisms]], or all bounded linear operators). Algebras where the two Arens products coincide are said to be Arens regular: since $B(H)$, the algebra of bounded linear operators on a Hilbert space $H$, has this property, so do all its closed subalgebras, in particular all $C^*$-[[C-star algebra|algebra]]s.


### An example of a 'nonunital' Banach algebra that has an identity element
Let $C_n$ be a cyclic group of order $n\geq 2$ and look at the Banach algebra (in the "strict" sense of a monoid object in $Ban$) that is obtained by equipping the Banach space $\ell^1(C_n)$ with the natural convolution product: $\delta_x * \delta_y = \delta_{x+y}$. There is a "short" homomorphism from $\ell^1(C_n)$ into the ground field which is just the unique linear extension of the group homomorphism $C_n \to \{1\}$ (by the free property of the $\ell^1$-functor) and we let $J$ be the kernel of this homomorphism. ($J$ is the so-called "augmentation ideal".) Now $J$ is a semigroup object in ${\rm Ban}$ and as an algebra it has an identity element $p$, but a calculation/hindsight shows that $\delta_e-p$ must be the constant function $C_n \to \{1/n\}$, so that $p$ has norm $(1-1/n)+(n-1)/n = 2-2/n$.

## References

* Zbigniew Semadeni, _Banach spaces of continuous functions_, vol. I, [gBooks](http://books.google.com/books/about/Banach_spaces_of_continuous_functions.html?id=vCDvAAAAMAAJ)

* N. Landsman, _Mathematical topics between classical and quantum mechanics_, Springer

* Walter Rudin, _Functional analysis_

* Richard V. Kadison, John R. Ringrose, _Fundamentals of the theory of operator algebras_


category: analysis

[[!redirects Banach algebra]]
[[!redirects Banach algebras]]

[[!redirects Banach ring]]
[[!redirects Banach rings]]
