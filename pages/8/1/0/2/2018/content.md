
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A Noetherian (or often, as below, noetherian) [[ring]] (or [[rng]]) is one where it is possible to do [[induction]] over its ideals, because the ordering of ideals by reverse inclusion is [[well-founded relation|well-founded]]. 

## Definition

### Noetherian rings

Every [[ring]] $R$ has a canonical $R$-$R$-[[bimodule]] structure, with [[left action]] $\alpha_L:R \times R \to R$ and [[right action]] $\alpha_R:R \times R \to R$ defined as the multiplicative binary operation on $R$ and [[biaction]] $\alpha:R \times R \times R \to R$ defined as the ternary product on $R$:
$$\alpha_L(a, b) \coloneqq a \cdot b$$
$$\alpha_R(a, b) \coloneqq a \cdot b$$
$$\alpha(a, b, c) \coloneqq a \cdot b \cdot c$$

Let $\mathrm{TwoSidedIdeals}(R)$ be the [[category of two-sided ideals]] in $R$, whose objects are [[two-sided ideals]] $I$ in $R$, [[subbimodules|sub-$R$-$R$-bimodules]] of $R$ with respect to the canonical bimodule structure on $R$, and whose [[morphisms]] are $R$-$R$-[[bimodule monomorphisms]]. 

An ascending chain of two-sided ideals in $R$ is a [[direct sequence]] of two-sided ideals in $R$, a [[sequence]] of two-sided ideals $A:\mathbb{N} \to \mathrm{TwoSidedIdeals}(R)$ with the following [[dependent sequence]] of $R$-$R$-bimodule monomorphisms: for natural number $n \in \mathbb{N}$, a dependent $R$-$R$-bimodule monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$. 

A [[ring]] $R$ is **Noetherian** if it satisfies the [[ascending chain condition]] on its two-sided ideals: for every ascending chain of two-sided ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the $R$-$R$-bimodule monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$ is an $R$-$R$-[[bimodule isomorphism]]. 

### Left Noetherian rings

Let $\mathrm{LeftIdeals}(R)$ be the category of [[left ideals]] in $R$, whose objects are [[left ideals]] $I$ in $R$, sub-left-$R$-modules of $R$ with respect to the canonical [[left module]] structure $(-)\cdot(-):R \times R \to R$ on $R$, and whose [[morphisms]] are left $R$-module monomorphisms. 

An ascending chain of left ideals in $R$ is a [[direct sequence]] of left ideals in $R$, a [[sequence]] of left ideals $A:\mathbb{N} \to \mathrm{LeftIdeals}(R)$ with the following [[dependent sequence]] of left $R$-module monomorphisms: for natural number $n \in \mathbb{N}$, a dependent left $R$-module monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$. 

A [[ring]] $R$ is **left Noetherian** if it satisfies the [[ascending chain condition]] on its left ideals: for every ascending chain of left ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the left $R$-module monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$ is an left $R$-module isomorphism. 

### Right Noetherian rings

Let $\mathrm{RightIdeals}(R)$ be the category of [[right ideals]] in $R$, whose objects are [[right ideals]] $I$ in $R$, sub-right-$R$-modules of $R$ with respect to the canonical [[right module]] structure $(-)\cdot(-):R \times R \to R$ on $R$, and whose [[morphisms]] are right $R$-module monomorphisms. 

An ascending chain of right ideals in $R$ is a [[direct sequence]] of right ideals in $R$, a [[sequence]] of right ideals $A:\mathbb{N} \to \mathrm{RightIdeals}(R)$ with the following [[dependent sequence]] of right $R$-module monomorphisms: for natural number $n \in \mathbb{N}$, a dependent right $R$-module monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$. 

A [[ring]] $R$ is **right Noetherian** if it satisfies the [[ascending chain condition]] on its right ideals: for every ascending chain of right ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the right $R$-module monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$ is an right $R$-module isomorphism. 

## Examples


+-- {: .num_example #FieldIsNoetherianRing}
###### Example

Every [[field]] is a noetherian ring.

=--


+-- {: .num_example #PIDIsNoetherianRing}
###### Example

Every [[principal ideal domain]] is a noetherian ring.

=--


+-- {: .num_example #PolynomialAlgebraOverNoetherianRingIsNoetherian} 
###### Example

For $R$ a [[Noetherian ring]] (e.g. a [[field]] by example \ref{FieldIsNoetherianRing}) then 

1. the [[polynomial algebra]]  $R[X_1, \cdots, X_n]$

1. the [[formal power series algebra]] $R[ [ X_1, \cdots, X_n ] ]$

over R in a [[finite number]] $n$ of [[coordinates]] are Noetherian.

=--

## Properties 

Spectra of noetherian rings are glued together to define [[noetherian scheme|locally noetherian schemes]]. 

### General

One of the best-known properties is the Hilbert basis theorem. Let $R$ be a (unital) ring. 

+-- {: .num_theorem} 
###### Theorem 
**(Hilbert)** 
If $R$ is left Noetherian, then so is the [[polynomial|polynomial algebra]] $R[x]$. (Similarly if "right" is substituted for "left".) 
=-- 

+-- {: .proof} 
###### Proof 
(We adapt the proof from [Wikipedia](https://en.wikipedia.org/wiki/Hilbert%27s_basis_theorem#First_Proof).) Suppose $I$ is a left ideal of $R[x]$ that is not finitely generated. Using the [[axiom of dependent choice]], there is a [[sequence]] of polynomials $f_n \in I$ such that the left ideals $I_n \coloneqq (f_0, \ldots, f_{n-1})$ form a strictly increasing chain and $f_n \in I \setminus I_n$ is chosen to have degree as small as possible. Putting $d_n \coloneqq \deg(f_n)$, we have $d_0 \leq d_1 \leq \ldots$. Let $a_n$ be the leading coefficient of $f_n$. The left ideal $(a_0, a_1, \ldots)$ of $R$ is finitely generated; say $(a_0, \ldots, a_{k-1})$ generates. Thus we may write 

$$\label{kill} a_k = \sum_{i=0}^{k-1} r_i a_i$$ 

The polynomial $g = \sum_{i=0}^{k-1} r_i x^{d_k - d_i} f_i$ belongs to $I_k$, so $f_k - g$ belongs to $I \setminus I_k$. Also $g$ has degree $d_k$ or less, and therefore so does $f_k - g$. But notice that the coefficient of $x^{d_k}$ in $f_k - g$ is zero, by (eq:kill). So in fact $f_k - g$ has degree less than $d_k$, contradicting how $f_k$ was chosen. 

=-- 

### A homological characterization

+-- {: .num_theorem}
###### Theorem
For a unital ring $R$ the following are equivalent:

1. $R$ is left Noetherian
1. Any small direct sum of injective left $R$-modules is injective.
1. $\operatorname{Ext}^k_R(A, \cdot)$ commutes with small direct sums for any finitely generated $A$.
=--

Direct sums here can be replaced by filtered colimits.

+-- {: .proof} 
###### Proof 
$1 \Rightarrow 2$: assume that $R$ is Noetherian and $I_\alpha$ are injective modules. In order to verify that $I := \bigoplus_\alpha I_\alpha$ is injective it is enough to show that for any ideal $\mathfrak{j}$ any morphism of left modules $f : \mathfrak{j} \to I$ factors through $\mathfrak{j} \to R$. Since $R$ is Notherian, $\mathfrak{j}$ is finitely generated, so the image of $f$ lies in a finite sum $I_{\alpha_1} \oplus \dots \oplus I_{\alpha_n}$. Thus an extension to $R$ exists by the injectivity of each $I_{\alpha_k}$.

$2 \Rightarrow 1$: if $R$ is not left Noetherian then there is a sequence of left ideals $\mathfrak{j}_1 \subsetneq \mathfrak{j}_2 \subsetneq \dots$. Take $\mathfrak{j} := \bigcup_k \mathfrak{j}_k$. The obvious map $j \to \prod_k (\mathfrak{j} / \mathfrak{j}_k)$ factors through $\bigoplus_k (\mathfrak{j} / \mathfrak{j}_k)$, since any element lies in all but finitely many $\mathfrak{j}_k$. Now take any injective $I_k$ with $0 \to \mathfrak{j} / \mathfrak{j}_k \to I_k$. The map $\mathfrak{j} \to \bigoplus_k I_k$ cannot extend to the whole $R$, since otherwise its image would be contained in a sum of finitely many $I_k$. Therefore, $\bigoplus_k I_k$ is not injective.

$2 \Rightarrow 3$: $\operatorname{Ext}^k_R(A, \bigoplus_\alpha X_\alpha)$ can be computed by taking an injective resolution of $\bigoplus_\alpha X_\alpha$. Since direct sums of injective modules are assumed to be injective, we can take a direct sum of injective resolutions of each $X_\alpha$. It remains to note that Hom out of a finitely generated module commutes with arbitrary direct sums.

$3 \Rightarrow 2$: Follows from the fact that $I$ is injective iff $\operatorname{Ext}^1_R(R / \mathfrak{i}, I) = 0$ for any ideal $\mathfrak{i}$.
=--

## Noetherian and Artinian rings

A dual condition is artinian: an __[[artinian ring]]__ is a ring satisfying the descending chain condition on ideals. The symmetry is severely broken if one considers unital rings: for example every unital artinian ring is noetherian; artinian rings are intuitively much smaller than generic noetherian rings.

## In constructive mathematics

In [[classical mathematics]], Noetherian rings are [[coherent rings]]. However, in [[constructive mathematics]], it is not provable that Noetherian rings are coherent rings. 

Similarly, in [[classical mathematics]], Noetherian [[Bézout domains]] are the same as [[principal ideal domains]]. However, in [[constructive mathematics]], Noetherian Bézout domains are not the same as principal ideal domains: the ring of integers is both Noetherian and Bézout, but it is a [[principal ideal domain]] if and only if [[excluded middle]] holds. (Note that [Lombardi & Quitté 2010](#LombardiQuitté2010) define a principal ideal domain as a Noetherian Bézout domain rather than an integral domain where ever ideal is a principal ideal.)

## Related concepts

* [[Noetherian module]], [[Noetherian bimodule]]

* [[noetherian object]]

* [[Noetherian poset]]

* [[Noetherian E-∞ ring]]

## References

Introduced by [[Emmy Noether]] in

* [[Emmy Noether]], _Idealtheorie in Ringbereichen_, Mathematische Annalen 83:1 (1921), 24–66.  [doi:10.1007/bf01464225](https://doi.org/10.1007/bf01464225).

* [wikipedia](https://en.wikipedia.org/wiki/Noetherian_ring)

* [[K. R. Goodearl]], R. B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Society Student Texts __16__ (1st ed,), 1989, xviii+303 pp.; or 61 (2nd ed.), 2004, xxiv+344 pp. 

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Lurie17} [[Jacob Lurie]], *[[Higher Algebra]]*, 2017 ([pdf](https://www.math.ias.edu/~lurie/papers/HA.pdf))

[[!redirects noetherian ring]]
[[!redirects noetherian]]
[[!redirects noetherian rings]]
[[!redirects Noetherian ring]]
[[!redirects Noetherian rings]]

