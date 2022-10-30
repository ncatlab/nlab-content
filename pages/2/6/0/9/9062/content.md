
# Lipschitz maps
* table of contents
{: toc}

## Idea

Lipschitz maps are [[functions]] between [[metric spaces]] that lie intermediate between the [[uniformly continuous maps]] and the [[short maps]].  (That is, every short map is Lipschitz, and every Lipschitz map is uniform.)

One can also consider Lipschitz maps between [[gauge spaces]] with appropriate gauges, or between [[manifolds]] with appropriate atlases.


## Definitions

Let $X$ and $Y$ be [[metric spaces]] (with the metric denoted $d$ for both).  Let $f\colon X \to Y$ be a [[function]].

+-- {: .num_defn #Lipnorm}
###### Definition

The __Lipschitz norm__ or __Lipschitz modulus__ ${\|f\|_{Lip}}$ of $f\colon X \to Y$ is the [[supremum]] of the absolute [[difference quotient]]s
$$ \frac{d(f(a), f(b))} {d(a, b)} $$
for $a \neq b$ in $X$.
=--

In general, this supremum is a [[lower real number]]; in particular, it may be infinite.  We work in the space $[0, \infty]$ of nonnegative lower reals, so that the Lipschitz norm is $0$ if $X$ is a [[subsingleton]] (so that $a \neq b$ never occurs).

+-- {: .num_defn #Lipmap}
###### Definition

The map $f\colon X \to Y$ is __Lipschitz continuous__, or simply __Lipschitz__, if its Lipschitz norm is finite.
=--

We can be more specific:

+-- {: .num_defn #specmaps}
###### Definitions

The map $f\colon X \to Y$ is __[[short map|short]]__ if its Lipschitz norm is at most $1$.  It is a __[[contraction mapping]]__ if its Lipschitz norm is strictly less than $1$.
=--


## Properties

In [[classical mathematics]], one calls $K \in [0, \infty]$ a __Lipschitz constant__ of $f\colon X \to Y$ if
$$ d(f(a), f(b)) \leq K d(a, b) $$
for all $a, b\colon X$.  Then the Lipschitz norm is the [[minimum]] of the Lipschitz constants (which is always attained, if there is any finite Lipschitz constant at all).  In [[constructive mathematics]], this procedure yields an extended [[upper real]] that is (in general) too large.  (For example, let $f$ be the sequence of [[partial sum]]s of a [[Specker sequence]], thought of as a map from $\mathbb{N} \subseteq \mathbb{R}$ to $\mathbb{R}$.)

If you want a definition that is constructively acceptable and yet involves no division, then take the Lipschitz norm of $f$ to be the supremum over those $k$ such that
$$ d(f(a), f(b)) \gt k d(a, b) $$
for some $a, b\colon X$.  (This is perhaps the best definition, as it will automatically take care of subsingletons, regardless of whether you restrict attention to $[0, \infty]$ a priori, and pseudometric spaces, even constructively.)  You can even restrict attention to (say) [[rational number|rational]] $k$, or to $a, b$ in some [[dense subspace]] of $X$ (say if $X$ is [[separable space|separable]]).

Every Lipschitz map is [[uniformly continuous map|uniformly continuous]].  Every Lipschitz map from the [[real line]] $\mathbb{R}$ to itself is [[absolutely continuous map|absolutely continuous]].

If a map $f$ between the real line and itself is [[differentiable map|differentiable]], then its Lipschitz norm is the [[supremum norm]] ${\|f'\|_\infty}$ of its [[derivative]] $f'$.  (This result can actually be generalised quite a bit, using [[Rademacher's theorem]] and its generalisations.)


## Generalisations

The definitions above generalise immediately to [[quasimetric spaces]]; there is no asymmetry between left and right, and the Lipschitz norm of $f\colon X \to Y$ is the same as that of $f^op\colon X^op \to Y^op$ (although the map from $X^op$ to $Y$, equivalently the map from $X$ to $Y^op$, may be quite different).

The definitions also generalise to [[pseudometric spaces]] if we take the supremum over those $a \neq b$ such that $d(a, b) \gt 0$.  However, we must also require that a Lipschitz map preserve metric equivalence: $d(f(a), f(b)) = 0$ if $d(a, b) = 0$.  Then we may pass to the quotient metric spaces and preserve the Lipschitz norm.

Let $X$ be a [[gauge space]], that is a set equipped with a collection of pseudometrics (the _gauge_ of $X$).  Then $X$\'s gauge is a __Lipschitz gauge__ if the [[identity function]] of $X$ is Lipschitz continuous as a map between $X$ equipped with any two of its pseudometrics.  Then we may extend $X$\'s gauge to a unique maximal Lipschitz gauge and say that $X$ (so equipped) is a __Lipschitz gauge space__.  We may then unambiguously define Lipschitz continuous maps (but not their Lipschitz norms) between any two Lipschitz gauge spaces.

Let $X$ be a [[topological manifold]], and equip $X$ with a compatible [[atlas]] whose transition maps are all Lipschitz (a __Lipschitz atlas__).  Then we may extend $X$\'s atlas to a unique maximal compatible Lipschitz atlas and say that $X$ (so equipped) is a __Lipschitz manifold__.  We may then unambiguously define Lipschitz continuous maps (but not their Lipschitz norms) between any two Lipschitz manifolds.  Assuming that our Lipschitz manifolds are [[paracompact space|paracompact]], then we may think of them as Lipschitz gauge spaces (with gauges consisting of all Lipschitz-continuous pseudometrics), recovering the same notion of Lipschitz map.


A map $f\colon X \to Y$ is __Lipschitz of order $\alpha$__, or __H&#246;lder of order $\alpha$__, if the supremum of
$$ \frac{d(f(a), f(b))} {d(a, b)^\alpha} $$
is finite.  Here, $\alpha$ may be any [[positive number]] (but is typically taken to be less than $1$).  Everything on this page generalises fairly well to these functions (changing also the definition of derivative to match).  Of course, a Lipschitz map of order $\alpha$ from $X$ to $Y$ is simply a Lipschitz map from $X^\alpha$ to $Y$, where $X^\alpha$ is $X$ with all distances raised to the power of $\alpha$.

Lipschitz (and H&#246;lder) maps also have non-uniform versions (fix $a$, but let the norm vary with $b$, which introduces an asymmetry for quasimetric spaces), as well as local versions (every point has a [[neighbourhood]] on which $f$ is Lipschitz).  I kind of get lost in all of the possibilities.

## Related pages

* [[Lipschitz domain]]
* [[corkscrew domain]]
* [[convex function]]


[[!redirects Lipschitz map]]
[[!redirects Lipschitz maps]]
[[!redirects Lipschitz continuous map]]
[[!redirects Lipschitz continuous maps]]
[[!redirects Lipschitz-continuous map]]
[[!redirects Lipschitz-continuous maps]]
[[!redirects Lipschitz function]]
[[!redirects Lipschitz functions]]
[[!redirects Lipschitz continuous function]]
[[!redirects Lipschitz continuous functions]]
[[!redirects Lipschitz-continuous function]]
[[!redirects Lipschitz-continuous functions]]
[[!redirects Lipschitz mapping]]
[[!redirects Lipschitz mappings]]
[[!redirects Lipschitz continuous mapping]]
[[!redirects Lipschitz continuous mappings]]
[[!redirects Lipschitz-continuous mapping]]
[[!redirects Lipschitz-continuous mappings]]

[[!redirects Lipschitz continuous]]
[[!redirects Lipschitz-continuous]]
[[!redirects Lipschitz continuity]]

[[!redirects Lipschitz condition]]
[[!redirects Lipschitz conditions]]


[[!redirects Lipschitz norm]]
[[!redirects Lipschitz norms]]
[[!redirects Lipschitz modulus]]
[[!redirects Lipschitz moduluses]]
[[!redirects Lipschitz moduli]]
[[!redirects modulus of Lipschitz continuity]]
[[!redirects moduluses of Lipschitz continuity]]
[[!redirects moduli of Lipschitz continuity]]

[[!redirects Lipschitz constant]]
[[!redirects Lipschitz constants]]


[[!redirects Lipschitz gauge]]
[[!redirects Lipschitz gauges]]

[[!redirects Lipschitz gauge space]]
[[!redirects Lipschitz gauge spaces]]
[[!redirects Lipschitz-gauge space]]
[[!redirects Lipschitz-gauge spaces]]


[[!redirects Lipschitz atlas]]
[[!redirects Lipschitz atlases]]
[[!redirects Lipschitz continuous atlas]]
[[!redirects Lipschitz continuous atlases]]
[[!redirects Lipschitz-continuous atlas]]
[[!redirects Lipschitz-continuous atlases]]

[[!redirects Lipschitz manifold]]
[[!redirects Lipschitz manifolds]]
[[!redirects Lipschitz continuous manifold]]
[[!redirects Lipschitz continuous manifolds]]
[[!redirects Lipschitz-continuous manifold]]
[[!redirects Lipschitz-continuous manifolds]]
