> This article is about [[metrizable topological space|metrizable]] [[complete space|complete]] [[topological vector spaces]].  For the [[locally convex vector space|locally convex]] special case, see the article [[Fréchet space]].

\tableofcontents

## Terminology

There are two inequivalent definitions of [[Fréchet spaces]] found in the literature.
The original definition due to [[Stefan Banach]] defines [[Fréchet spaces]] as [[metrizable topological space|metrizable]] [[complete space|complete]] [[topological vector spaces]].

Later [[Bourbaki]] (Topological vector spaces, Section II.4.1) added the condition of [[locally convex vector space|local convexity]].
However, many authors continue to use the original definition due to Banach.

The term “F-space” can refer to either of these definitions, although in the modern literature it is more commonly used to refer to the non-locally convex notion.

The [[nLab]] uses “F-space” to refer to the non-locally convex notion and “[[Fréchet space]]” to refer to the locally convex notion.

## Idea

An __F-space__ is a [[topological vector space]] whose topology is induced by a complete F-norm.

An __F-norm__ is a non-homogeneous variant of a [[norm]]: a translation-invariant [[metric]] on a [[vector space]] that satisfies properties in between being a [[G-norm]] (on the underlying [[abelian group]] of the vector space) and being a norm.  As with norms, there is a semi- variant.


## Definitions

Let $K$ be a [[topological field]] (typically the [[real numbers]] or the [[complex numbers]], but conceivably only a [[topological ring]], or at least a [[commutative ring|commutative]] one); we will call the elements of $K$ _scalars_.  Let $V$ be a [[vector space]] (or [[module over a ring|module]]) over $K$; we will call the elements of $V$ _vectors_.  Let $\|{-}\|$ be a [[function]] from (the underlying set of) $V$ to the set of [[real numbers]].

+-- {: .num_defn #Gseminorm}
###### Definition

If

1. ${\|0_V\|} = 0$ (or even just ${\|0\|} \leq 0$),
2. ${\|{-x}\|} = {\|x\|}$ (or even just ${\|{-x}\|} \leq {\|x\|}$) for each vector $x$, and
3. ${\|x + y\|} \leq {\|x\|} + {\|y\|}$ for each vector $x$ and vector $y$ (the [[triangle inequality]]),

then ${\|{-}\|}$ is a __[[G-seminorm]]__.
=--

This is enough to prove that ${\|x\|} \geq 0$ for each $x$ in $V$, making $(x,y) \mapsto {\|y - x\|}$ (precisely) a translation-invariant [[pseudometric]] on $V$.

Note that addition $(x,y) \mapsto x + y\colon V \times V \to V$ is a [[short map]] under this pseudometric and so certainly [[continuous map|continuous]].

+-- {: .num_defn #Fseminorm}
###### Definition

If

1. $\|{-}\|$ is a G-seminorm and
2. scalar multiplication $(a,x) \mapsto a x\colon K \times V \to V$ is continuous (relative to the topology on $K$ and the pseudometric on $V$),

then $\|{-}\|$ is an __F-seminorm__.
=--

If the topology on $K$ is given by an [[absolute value]] $|{-}|$, then we can go further:

+-- {: .num_defn #seminorm}
###### Definition

If

1. ${\|x + y\|} \leq {\|x\|} + {\|y\|}$ for each vector $x$ and vector $y$ and
2. ${\|a x\|} = {|a|} {\|x\|}$ for each scalar $a$ and vector $x$,

then $\|{-}\|$ is a __[[seminorm]]__.
=--

Every seminorm is automatically an F-seminorm.

No longer assuming anything further about $K$, there are some subsidiary definitions:

+-- {: .num_defn #Fnorm}
###### Definition

If

1. $\|{-}\|$ is an F-seminorm and
2. $x = 0_V$ whenever $x$ is a vector and ${\|x\|} = 0$,

then $\|{-}\|$ is an __F-norm__.
=--

Thus an F-norm is precisely an F-seminorm whose induced pseudometric is a [[metric]].  (Compare the relationship between [[G-norms]] and [[norms]] with G-seminorms in \ref{Gseminorm} and seminorms in \ref{seminorm} above.)

+-- {: .num_defn #Fspace}
###### Definition

If

1. $\|{-}\|$ is an F-norm and
2. $x$ converges under the metric on $V$ whenever $x$ is a [[net]] of vectors and $\lim_{i,j} {\|x_j - x_i\|} = 0$ in $\mathbb{R}$,

then $(V,{\|{-}\|})$ is an __F-space__.
=--

In other words, an F-space is a vector space equipped with an F-norm whose induced metric is [[complete metric|complete]] (or equivalently such that the topology on $V$ is [[complete topological group|complete]]).

+-- {: .num_defn #Frechetspace}
###### Definition

If

1. $(V,{\|{-}\|})$ is an F-space and
2. $(V,{\|{-}\|})$ is [[locally convex space|locally convex]] as a topological vector space,

then $(V,{\|{-}\|})$ is a __[[Fréchet space]]__.
=--

Finally, $F Sp$ is the [[category]] whose [[objects]] are F-spaces and whose morphisms are [[short linear maps]]; that said, often people really study the [[essential image]] of that category within the category of [[topological vector spaces]], or [[equivalence of categories|equivalently]] the category whose objects are F-spaces and whose morphisms are [[continuous map|continuous]] linear maps.  (This is especially so with Fr&#233;chet spaces, which have a common alternative definition that makes no reference to a canonical metric.)


## Examples

The usual examples of F-spaces that are not Fr&#233;chet spaces are the [[Lebesgue spaces]] $l^p$ for $0 \lt p \lt 1$.  These use a modified $p$-[[p-norm|norm]] in which
$$ {\|x\|_p} = \sum_i {|x_i|^p} $$
(so without the $p$th root) to ensure that the [[triangle inequality]] (\ref{Gseminorm}.3) holds.


## Properties

The uniqueness theorem for [[complete space|complete]] [[norms]] in [[dream mathematics]] applies also to F-norms: assuming [[excluded middle]], [[dependent choice]], and the (classically false) [[Borel property]], two complete F-norms on a given [[vector space]] over the [[real numbers]] induce the same topology.  See [[norm#dreamUnique]].

## Related concepts

* [[Fréchet space]]

## References

* Nigel Kalton, _Quasi-Banach spaces_, Handbook of the geometry of Banach spaces, Volume 2, 1099–1130.  North-Holland, Amsterdam, 2003.  ISBN: 0-444-51305-1.


category: analysis

[[!redirects F-space]]
[[!redirects F-spaces]]
[[!redirects F space]]
[[!redirects F spaces]]

[[!redirects F-norm]]
[[!redirects F-norms]]
[[!redirects F norm]]
[[!redirects F norms]]

[[!redirects F-seminorm]]
[[!redirects F-seminorms]]
[[!redirects F seminorm]]
[[!redirects F seminorms]]
