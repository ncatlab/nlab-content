
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
with the left-hand side guaranteed to exist if the right-hand side exists as a finite real number (but the left-hand side may exist even if the right-hand side diverges, the usual distinction between [[absolute convergence]] and [[conditional convergence]]).

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


### As a unit ball with extra structure

Since the [[forgetful functor]] $Hom_Ban(\mathbb{R},-)\colon Ban \to Set$, taking each Banach space to its closed [[unit ball]], is [[faithful functor|faithful]], it\'s natural to consider a Banach space as this ball with [[extra structure]].  We can always do this by [[abstract nonsense]]: define a Banach space to be a [[set]] $B$ equipped with a [[bijection]] to the closed unit ball of some complete normed vector space.

However, we can also do this in a more explicit way, constructing a Banach space as a [[structured set]].  The key is that, while a vector space supports any finite [[linear combinations]] (and a complete TVS supports some infinite ones), the unit ball of a Banach space supports linear combinations (finite or infinite) whose coefficients\' absolute values sum to at most $1$.  (As a special case, this includes convex-linear combinations, where all coefficients are positive and sum to $1$, so the unit ball is a [[convex space]].)

So we define a __Banach space__ to be set $B$ (the _underlying set_, or _closed unit ball_ to be unambiguous, whose elements are called _short vectors_ to distinguish them from the more general elements of the underlying vector space of $B$) equipped with, for each multiset $A$ of scalars whose absolute values sum to at most $1$, an $A$-indexed operation on $B$, such that these operations are compatible as linear combinations, together with a function $\|{-}\|$ from $B$ to the [[unit interval]] $[0,1]$ satisfying homogeneity, definiteness, normalizability (defined below), and the infinitary triangle inequality that makes $B$ into a complete metric space.

To be more explicit:

*  Given a set $I$ (thought of as an [[index set]]), a _short $I$-sequence of scalars_ is a scalar-valued function $a$ on $I$ (whose values are written $a_i$ for $i$ in $I$) such that $\sum_{i\colon I} {|{a_i}|} \leq 1$ (with, in [[constructive mathematics]], the classically redundant assumption that the left-hand side of this inequality exists).  In other words, $a$ is in the [[sequence space]] $l^1(I)$.
*  Similarly, an _$I$-sequence of short vectors_ is a $B$-valued function $x$ on $I$ (whose values are written $x_i$ for $i$ in $I$), with no requirements.
*  For each set $I$, each short $I$-sequence $a$ of scalars, and each $I$-sequence $x$ of short vectors, we require a short vector $\sum_{i\colon I} a_i x_i$.  (Special cases include the empty sum $0$, $-x = -1 x$, and $\frac 1 2 x + \frac 1 2 y$, but not $x + y$.)
*  For each short vector $x$, we require $1 x = x$ and $0 x = 0$ (although the latter is redundant with a homogenous definite norm).
*  For each set $I$, each $I$-indexed family $J$ of sets (so $J_i$ is a set for each $i$ in $I$), each short $I$-sequence $a$ of scalars, each $I$-indexed family $b$ of short $J_i$-sequences of scalars (so $b_{i,j}$ is a scalar for each $i$ in $I$ and $j$ in $J_i$, and $\sum_{j\colon J_i} {|{b_{i,j}}|} \leq 1$ for each $i$ in $I$), and each $I$-indexed family $x$ of $J_i$-sequences of short vectors (so $x_{i,j}$ is an element of $B$ for each $i$ in $I$ and $j$ in $J_i$), we require $\sum_{i\colon I} a_i \sum_{j\colon J_i} b_{i,j} x_{i,j} = \sum_{i\colon I} \sum_{j\colon J_i} a_i b_{i,j} x_{i,j}$ (which makes sense since $\sum_{i\colon I} \sum_{j\colon J_i} {|{a_i}|}\, {|{b_{i,j}}|} \leq 1$).  (This is what it means for the linear-combination operations to be _compatible_ as linear combinations.)

*  For each short vector $x$, we require a _norm_ $\|{x}\|$, a scalar ranging from $0$ to $1$.
*  For each short scalar $a$ (so $|{a}| \leq 1$) and each short vector $x$, we require ${\|{a x}\|} = {|{a}|}\, {\|{x}\|}$.  (This is _homogeneity_.)
*  For each set $I$, each short $I$-sequence $a$ of scalars, and each $I$-sequence $x$ of short vectors, we require ${\|{\sum_{i\colon I} a_i x_i}\|} \leq \sum_{i\colon I} {|{a_i}|}\, {\|{x_i}\|}$.  (This is the infinitary _[[triangle inequality]]_.)
*  For each short vector $x$, if ${\|{x}\|} = 0$, then we require $x = 0$ (this is _definiteness_).
*  For each short vector $x$, if ${\|{x}\|} \gt 0$, then we require a short vector $\hat{x}$ such that $x = {\|{x}\|}\, \hat{x}$ (this is what I\'m calling _normalizability_).  (By homogeneity, ${\|{\hat{x}}\|} = 1$.)

*  For each short vector $x$ and short vector $y$, although we cannot form $x - y$, we can define the _distance_ $d(x,y)$ to be $2 {\|{\frac 1 2 x - \frac 1 2 y}\|}$.  (Then for each scalar $a \geq 2$, $d(x,y) = a {\|{\frac 1 a x - \frac 1 a y}\|}$, using homogeneity.)
*  If $(x_1, x_2, x_3, \ldots)$ is a [[Cauchy sequence]] (or [[net]] in constructive mathematics), we require that the sequence converges.  (We automatically get $ \lim _ { n \to \infty } \sum _ { i = 1 } ^ n a _ i x _ i = \sum _ { i = 1 } ^ \infty a _ i x _ i $ from what has come before, but not every Cauchy sequence takes this form.)

We can then define a _vector_ to be a formal scalar multiple of a short vector.  Specifically, a vector is an [[equivalence class]] of pairs $(a,x)$, where $a$ is a scalar and $x$ is a short vector, where $(a,x)$ is equivalent to $(b,y)$ iff $\frac a c x = \frac b c y$ for some nonzero scalar $c$ such that ${|{\frac a c}|} \leq 1$ and ${|{\frac b c}|} \leq 1$, which without loss of generality can be $c = \max ({|{a}|},{|{b}|},1)$.  Similarly, we can define $[(a,x)] + [(b,y)] = [(c,\frac a c x + \frac b c y)]$, where now $c = \max (\frac 1 2 {|{a}|},\frac 1 2 {|{b}|},\frac 1 2)$ or any other nonzero scalar such that ${|{\frac a c}|} + {|{\frac b c}|} \leq 1$.  (More generally, we can define finitary linear combinations of vectors, although not always infinitary ones, even if the coefficients are a short sequence; that's an advantage of the unit ball.)  And we can define $b [(a,x)]$ even more easily as $[(a b,x)]$, and ${\|{[(a,x)]}\|} \coloneqq {|{a}|}\, {\|{x}\|}$.  This makes the set of vectors into a Banach space in the usual sense, and its closed unit ball is equivalent to $B$, consisting of all vectors of the form $[(1,x)]$.


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

* {#Coequalizers} The category of Banach spaces admits [[coequalizers]]. Though one may expect the coequalizer of a pair of maps $f,g: X \rightrightarrows Y$ to be the [[cokernel]] of $f-g$ under the quotient norm (in which the norm of a coset $y + C$ is the minimum norm attained by elements of $y + C$; here $C$ is the [[image]] $(f-g)(X)$), these spaces are not Banach spaces in general, as the image of a map $f$ need not be closed (indeed, the inclusion $i: \ell_1 \hookrightarrow c_0$ has dense image in $c_0$), and so the quotient space may not be complete. However, the quotient by the closure of $(f-g)(X)$ suffices.

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
2. There are theorems that are not valid for the Bochner integral, notably the [[Radon-Nikodym theorem]] does not hold in general.

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

### Further properties

* [[Krein-Smulian theorem]]



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
