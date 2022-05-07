
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Banach spaces
* table of contents
{: toc}

## Idea

A Banach space $\mathcal{B}$ is both a [[vector space]] (over a [[normed field]] such as $\mathbb{R}$) and a [[complete space|complete]] [[metric space]], in a compatible way. Hence a complete [[normed vector space]].

A source of simple Banach spaces comes from considering a [[Cartesian space]] $\mathbb{R}^n$ (or $K^n$ where $K$ is the normed field) with the norm:

$$ {\|(x_1,\ldots,x_n)\|_p} \coloneqq \root p {\sum_{i = 1}^n {|x_i|^p}} $$

where $1 \leq p \leq \infty$ (this doesn't strictly make sense for $p = \infty$, but taking the limit as $p \to \infty$ and reading $\mathbb{R}^\infty = \underset{\longrightarrow}{\lim}_n \mathbb{R}^n$ as the [[direct limit]] (as opposed to the [[inverse limit]]) we arrive at the formula ${\|(x_1,\ldots,x_n)\|_\infty} \coloneqq \max_i {|x_i|}$).

However, the theory of these spaces is not much more complicated than that of finite-dimensional vector spaces because they all have the same underlying topology.  When we look at infinite-dimensional examples, however, things become trickier.  Common examples are [[Lebesgue spaces]], [[Hilbert spaces]], and [[sequence spaces]].

In the literature, one most often sees Banach spaces over the field $\mathbb{R}$ of [[real numbers]]; Banach spaces over the field $\mathbb{C}$ of [[complex numbers]] are not much different, since they are also over $\mathbb{R}$.  But people do study them over [[p-adic numbers]] too.  _Unless otherwise stated, we assume $\mathbb{R}$ below._


## Definitions

Let $V$ be a [[vector space]] over the field of [[real number]]s.  (One can generalise the choice of [[field]] somewhat.)  A **pseudonorm** (or **[[seminorm]]**) on $V$ is a function
$$ {\| - \|}\colon V \to \mathbb{R} $$
such that:

1.  $ {\|0\|} \geq 0 $;
2.  $ {\|r v\|} = {|r|} {\|v\|} $ (for $r$ a [[scalar]] and $v$ a vector);
3.  $ {\|v + w\|} \leq {\|v\|} + {\|w\|} $.

It follows from the above that ${\|v\|} \geq 0$; in particular, ${\|0\|} = 0$.  A **[[norm]]** is a pseudonorm that satisfies a converse to this: $v = 0$ if ${\|v\|} = 0$.

A [[norm]] on $V$ is **complete** if, given any infinite [[sequence]] $(v_1, v_2, \ldots)$ such that
\[ \label{Cauchy} \lim_{m,n\to\infty} {\left\| \sum_{i=m}^{m+n} v_i \right\|} = 0 ,\]
there exists a (necessarily unique) **sum** $S$ such that
\[ \label{converge} \lim_{n\to\infty} {\left\| S - \sum_{i=1}^n v_i \right\|} = 0 ;\]
we write
$$ S = \sum_{i=1}^\infty v_i $$
(with the right-hand side undefined if no such sum exists).

Then a **Banach space** is simply a vector space equipped with a complete norm.  As in the real line, we have in a Banach space that
$$ {\left\| \sum_{i=1}^\infty v_i \right\|} \leq \sum_{i=1}^\infty {\|v_i\|} ,$$
with the left-hand side guaranteed to exist if the right-hand side exists as a finite real number (but the left-hand side may exist even if the right-hand side diverges, the usual distinction between absolute and conditional convergence).

If we do not insist on the space being complete, we call it a **normed (vector) space**.  If we have a [[topological vector space]] such that the topology comes from a norm, but we do not make an actual choice of such a norm, then we talk of a **normable space**.


### Banach spaces as metric spaces

The three axioms for a pseudonorm are very similar to the three axioms for a [[pseudometric]].

Indeed, in any pseudonormed vector space, let the **distance** $d(v,w)$ be
$$ d(v,w) = {\|w - v\|} .$$
Then $d$ is a pseudometric, which is __translation-invariant__ in that
$$ d(v+x,w+x) = d(v,w) $$
always holds.  Conversely, given any translation-invariant pseudometric $d$ on a vector space $V$, let ${\|v\|}$ be
$$ {\|v\|} = d(0,v) .$$
Then ${\|-\|}$ satisfies the axioms (1--3) for a pseudonorm, except that it may satisfy (2) only for $r = 0, \pm 1$.  (In other words, it is only a [[G-pseudonorm]].)  It will actually be a pseudonorm iff the pseudometric satisfies a homogeneity rule:
$$ d(r v,r w) = {|r|} d(v,w) .$$
Thus pseudonorms correspond precisely to homogeneous translation-invariant pseudometrics.

Similarly, norms correspond to homogenous translation-invariant metrics and complete norms correspond to complete homogeneous translation-invariant metrics.  Indeed, (eq:Cauchy) says that the sequence of partial sums is a [[Cauchy sequence]], while (eq:converge) says that the sequence of partial sums converges to $S$.

Thus a Banach space may equivalently be defined as a vector space equipped with a complete homogeneous translation-invariant metric.  Actually, one usually sees a sort of hybrid approach: a Banach space is a normed vector space whose corresponding metric is complete.


### Maps between Banach spaces
{#morphisms}

If $V$ and $W$ are pseudonormed vector spaces, then the **norm** of a linear function $f\colon V \to W$ may be defined in either of these equivalent ways:

*  $ {\|f\|} = \sup \{ {\|f v\|} \;|\; {\|v\|} \leq 1 \} $;
*  $ {\|f\|} = \inf \{ r \;|\; \forall{v},\; {\|f v\|} \leq r {\|v\|} \} $.

(Some other forms are sometimes seen, but these may break down in degenerate cases.)

For finite-dimensional spaces, any linear map has a well-defined finite norm.  In general, the following are equivalent:

*  $f$ is [[continuous map|continuous]] (as measured by the pseudometrics on $V$ and $W$) at $0$;
*  $f$ is continuous (everywhere);
*  $f$ is [[uniformly continuous map|uniformly continuous]];
*  $f$ is [[Lipschitz map|Lipschitz continuous]];
*  ${\|f\|}$ is finite (and, in [[constructive mathematics]], [[located real number|located]]);
*  $f$ is [[bounded map|bounded]] (as measured by the [[bornologies]] given by the pseudometrics on $V$ and $W$).

In this case, we say that $f$ is **bounded**.  If $f\colon V \to W$ is not assumed to be linear, then the above conditions are no longer equivalent.

The bounded linear maps from $V$ to $W$ themselves form a pseudonormed vector space $\mathcal{B}(V,W)$.  This will be a Banach space if (and, except for degenerate cases of $V$, only if) $W$ is a Banach space.  In this way, the category $Ban$ of Banach spaces is a [[closed category]] with $\mathbb{R}$ as the unit.

The clever reader will note that we have not yet defined $\mathbf{Ban}$ as a category! (surprisingly in the _nLab_) There are many (nonequivalent) ways to do so.

In [[functional analysis]], the usual notion of '[[isomorphism]]' for Banach spaces is a bounded bijective linear map $f\colon V \to W$ such that the [[inverse function]] $f^{-1}\colon W \to V$ (which is necessarily linear) is also bounded. In this case one can accept all bounded linear maps between Banach spaces as morphisms.  Analysts sometimes refer to this as the "isomorphic category".

Another natural notion of isomorphism is a surjective linear isometry. In this case, we take a morphism to be a **[[short map|short]]** [[linear map]], or [[short linear map|linear contraction]]: a linear map $f$ such that ${\|f\|} \leq 1$.  This category, which is what category theorists generally refer to as $\mathbf{Ban}$, is sometimes referred to as the "isometric category" by analysts. Note that this makes the 'underlying set' (in the sense of $\mathbf{Ban}$ as a [[concrete category]] like any closed category) of a Banach space its (closed) **unit ball**
$$ Hom_Ban(\mathbb{R},V) \cong \{ v \;|\; {\|v\|} \leq 1 \} $$
rather than the set of all vectors in $V$ (the underlying set of $V$ as a vector space).

+-- {: .query}
Yemon Choi: This is really here to remind myself how to make query boxes. But while I'm at it, is it really OK to refer to the "unit ball functor" as "taking the underlying set"? I notice that on the discussion about internal homs at [[internal hom]] it is claimed that "Every closed category is a [[concrete category]] (represented by $I$), and the underlying set of the internal hom is the external hom" which seems to require "underlying set" to be interpreted in this looser sense.

_Toby_:  Sure, but the point of putting 'underlying set' in scare quotes is precisely to point out that the category-theoretic underlying set is not what one would normally expect.
=--

+-- {: .query}
Mark Meckes: I've expanded this section in part to be consistent with analysts' terminology.  I've made some assumptions about category theorists' conventions which might not be correct.  (If I find time I might write about other categories of Banach spaces that analysts think about.)

_Toby_:  Looks good to me!
=--

From a category-theorist\'s perspective, the isomorphic category is really the [[full image]] of the [[inclusion functor]] from $Ban$ to $TVS$ (the category of [[topological vector spaces]]), which may be denoted $Ban_{TVS}$.  If you\'re working in $Ban_{TVS}$, then you only care about the topological linear structure of your space (although you do also care that it can be derived from some metric); if you\'re working in $Ban$, then you care about all of the structure on the space.


## Examples

Many examples of Banach spaces are parametrised by an exponent $1 \leq p \leq \infty$.  (Sometimes one can also try $0 \leq p \lt 1$, but these generally don\'t give Banach spaces.)

*  The [[Cartesian space]] $\mathbb{R}^n$ is a Banach space with
   $$ {\|(x_1,\ldots,x_n)\|_p} = \root p {\sum_i {|x_i|^p}} .$$
   (We can allow $p = \infty$ by taking a limit; the result is that ${\|x\|_\infty} = \max_i {|x_i|}$.)  Every finite-dimensional Banach space is isomorphic to this for some $n$ and $p$; in fact, once you fix $n$, the value of $p$ is irrelevant up to isomorphism.

*  The [[sequence space]] $l^p$ is the set of infinite [[sequence]]s $(x_1,x_2,\ldots)$ of real numbers such that
   $$ {\|(x_1,x_2,\ldots)\|_p} = \root p {\sum_i {|x_i|^p}} $$
   exists as a finite real number.  (The only question is whether the sum converges.  Again $p = \infty$ is a limit, with the result that ${\|x\|_\infty} = \sup_i {|x_i|}$.)  Then $l^p$ is a Banach space with that norm.  These are all versions of $\mathbb{R}^\infty$, but they are no longer isomorphic for different values of $p$.  (See [[isomorphism classes of Banach spaces]].)

*  More generally, let $A$ be any [[set]] and let $l^p(A)$ be the set of [[function]]s $f$ from $A$ to $\mathbb{R}$ such that
   $$ {\|f\|_p} = \root p {\sum_{x: A} {|f(x)|^p}} $$
   exists as a finite real number.  (Again, ${\|f\|_\infty} = \sup_{x\colon A} {|f(x)|}$.)  Then $l^p(A)$ is a Banach space.  (This example includes the previous examples, for $A$ a countable set.)

*  On any [[measure space]] $X$, the [[Lebesgue space]] $\mathcal{L}^p(X)$ is the set of measurable almost-everywhere-defined real-valued functions on $X$ such that
   $$ {\|f\|_p} = \root p {\int {|f|^p}} $$
   exists as a finite real number.  (Again, the only question is whether the integral converges.  And again $p = \infty$ is a limit, with the result that ${\|f\|_\infty}$ is the [[essential supremum]] of ${|f|}$.)  As such, $\mathcal{L}^p(X)$ is a complete pseudonormed vector space; but we identify functions that are equal almost everywhere to make it into a Banach space.  (This example includes the previous examples, for $X$ a set with counting measure.)

*  Any [[Hilbert space]] is Banach space; this includes all of the above examples for $p = 2$.


## Operations on Banach spaces

The category $Ban$ of Banach spaces is [[complete category|small complete]], [[cocomplete category|small cocomplete]], and [[symmetric monoidal closed category|symmetric monoidal closed]] with respect to its standard internal hom (described at [[internal hom]]). Some details follow.

* The category of Banach spaces admits small [[product]]s. Given a small family of Banach spaces $\{X_\alpha\}_{\alpha \in A}$, its product in $Ban$ is the subspace of the vector-space product
$$\prod_{\alpha \in A} X_\alpha$$
consisting of $A$-tuples $\langle x_\alpha \rangle$ which are _uniformly_ bounded (i.e., there exists $C$ such that $\forall \alpha \in A: {\|x_\alpha\|} \leq C$), taking the least such upper bound as the norm of $\langle x_\alpha \rangle$. This norm is called the $\infty$-norm; in particular, the product of an $A$-indexed family of copies of $\mathbb{R}$ or $\mathbb{C}$ is what is normally denoted as $l^{\infty}(A)$.

* The category of Banach spaces admits [[equalizer]]s. Indeed, the equalizer of a pair of maps $f, g: X \rightrightarrows Y$ in $Ban$ is the [[kernel]] of $f-g$ under the norm inherited from $X$ (the kernel is closed since $f-g$ is continuous, and is therefore complete). In fact every equalizer is even a [[section]] by the [[Hahn-Banach theorem]]. Every [[extremal monomorphism]] is even already an equalizer (and a section): Let $f\colon X \to Y$ be an extremal monomorphism, $\iota\colon \Im(f) \to Y$ the embedding of $Im(f)$ into the codomain of $f$ and $f\prime \colon X \to Im(f)$ $f$ with restricted codomain. Since $f\prime$ is an epimorphism, $f=\iota f\prime$, and $f$ extremal, $f\prime$ is an isomorphism, thus $f$ is an embedding.

* The category of Banach spaces admits small [[coproduct]]s. Given a small family of Banach spaces $\{X_\alpha\}_{\alpha \in A}$, its coproduct in $Ban$ is the completion of the vector space coproduct 
  $$\bigoplus_{\alpha \in A} X_\alpha$$ 
  with respect to the norm given by
  $$ {\left\| \bigoplus_{s \in S} x_s \right\|} = \sum_{s \in S} {\|x_s\|} ,$$
  where $S \subseteq A$ is finite and ${\|x_s\|}$ denotes the norm of an element in $X_s$. This norm is called the $1$-norm; in particular, the coproduct of an $A$-indexed family of copies of $\mathbb{R}$ or $\mathbb{C}$ is what is normally denoted as $l^1(A)$.

* The category of Banach spaces admits [[coequalizer]]s. Indeed, the coequalizer of a pair of maps $f, g: X \rightrightarrows Y$ is the [[cokernel]] of $f-g$ under the quotient norm (in which the norm of a coset $y + C$ is the minimum norm attained by elements of $y + C$; here $C$ is the [[image]] $(f-g)(X)$, which is closed). It is standard that the quotient norm on $Y/C$ is complete given that the norm on $Y$ is complete.

* To describe the tensor product $X \otimes_{Ban} Y$ of two Banach spaces (making $Ban$ symmetric monoidal closed with respect to its usual internal hom), let $F(X \times Y)$ be the free vector space generated by the set $X \times Y$, with norm on a typical element defined by 
$$ {\left\| \sum_{1 \leq i \leq n} a_i (x_i \otimes y_i) \right\|} = \sum_{1 \leq i \leq n} {|a_i|} {\|x_i\|} \cdot {\|y_i\|}.$$
Let $\overline{F}(X \times Y)$ denote its completion with respect to this norm. Then take the cokernel of $\overline{F}(X \times Y)$ by the closure of the subspace spanned by the obvious bilinear relations. This quotient is $X \otimes_{Ban} Y$.

In the literature on Banach spaces, tensor product above is usually called the __projective tensor product__ of Banach spaces; see other [[tensor product of Banach spaces]].  The product and coproduct are considered __direct sums__; see other [[direct sums of Banach spaces]].

To be described:

*  duals ($p + q = p q$); 
*  completion ($Ban$ is a [[reflective subcategory]] of $PsNVect$ (pseudo-normed vector spaces)).
*  $Ban$ as a (somewhat larger) category with duals.


## Integration in Banach spaces

This paragraph describes some aspects of integration theory in Banach spaces that are relevant to understand the literature about [[AQFT]]. In the given context, elements of a Banach space $\mathcal{B}$ are sometimes called vectors, a function or measure taking values in $\mathcal{B}$ are therefore called vector functions and vector measures. Functions and measures taking values in the [[field]] that the Banach space is defined upon as a vector space are called scalar functions and scalar measures. 

We will consider two types of integrals:

* integrals of vector functions with respect to a scalar measure, specifically the Bochner integral,

* integrals of scalar functions with respect to a vector measure, specifically the spectral integral of a normal operator on a Hilbert space.


### Bochner integral

The Bochner integral is a direct generalization of the Lesbegue integral to functions that take values in a Banach space. Whenever you encounter an integral of a function taking values in a Banach space in the [[AQFT]] literature, it is safe to assume that it is meant to be a Bochner integral. Two points already explained by Wikipedia are of interest:

1. A version of the dominated convergence theorem is true for the Bochner integral.
2. There are theorems that are not valid for the Bochner integral, notably the Radon-Nikodym theorem does not hold in general.

* [Wikipedia] (http://en.wikipedia.org/wiki/Bochner_integral)

_reference_: Joseph Diestel: "Sequences and Series in Banach Spaces" ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0542.46007&format=complete)), chapter IV. 


### The spectral integral

The integral with respect to the spectral measure of a bounded normal operator on a Hilbert space is an example of a Banach space integral with respect to a vector measure.
In this paragraph we present a well known, but somewhat less often cited result, that is of use in some proofs in some approaches to [[AQFT]], it is the version of the dominated convergence theorem for the given setting.

Let A be a bounded normal operator on a Hilbert space and E be it's spectral measure (the "resolution of identity" in the terms of Dunford and Schwartz). Let $\sigma(A)$ be the spectrum of A. For a bounded complex Borel function f we then have
$$
           f(A) \coloneqq \int_{\sigma(A)} f(\lambda) E(d\lambda)
$$

+-- {: .un_theorem}
###### Theorem (dominated convergence)
If the uniformly bounded sequence $\{f_n\}$ of complex Borel functions converges at each point of $\sigma(A)$ to the function $f$, then $f_n(A) \to f(A)$ in the strong operator topology.
=--

+-- {: .proof}
See Dunford, Schwartz II, chapter X, corollary 8.
=--

## Properties

### Relation to bornological spaces

Every [[inductive limit]] of [[Banach spaces]] is a [[bornological vector space]]. ([Alpay-Salomon 13, prop. 2.3](#AlpaySalomon13))

Conversely, every [[bornological vector space]] is an inductive limit of [[normed spaces]], and of [[Banach spaces]] if it is quasi-complete ([Schaefer-Wolff 99](#SchaeferWolff99))

## Related concepts

* [[reflexive Banach space]]
* [[projective Banach space]]

* [[Banach analytic space]]

[[!include analytic geometry ingredients -- table]]

## References

Named after [[Stefan Banach]].

* Walter Rudin, _Functional analysis_
* Dunford, Nelson; Schwartz, Jacob T.: "Linear operators. Part I: General theory." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0635.47001&format=complete)), "Linear operators. Part II: Spectral theory, self adjoint operators in Hilbert space." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0635.47002&format=complete))

* Z. Semadeni, _Banach spaces of continuous functions_, vol. I, Polish scientific publishers. Warszawa 1971

* {#AlpaySalomon13} Daniel Alpay, Guy Salomon, _On algebras which are inductive limits of Banach spaces_ ([arXiv:1302.3372](http://arxiv.org/abs/1302.3372))

* {#SchaeferWolff99} H. H. Schaefer with M. P. Wolff, _Topological vector spaces_, Springer 1999

* [[Jiří Rosický]], _Are Banach spaces monadic?_, ([arXiv:2011.07543](https://arxiv.org/abs/2011.07543))


category: analysis

[[!redirects Banach space]]
[[!redirects Banach spaces]]
[[!redirects Banach vector space]]
[[!redirects Banach vector spaces]]

[[!redirects Ban]]


[[!redirects norm isomorphism]]
[[!redirects norm-isomorphic]]
[[!redirects norm isomorphic]]
