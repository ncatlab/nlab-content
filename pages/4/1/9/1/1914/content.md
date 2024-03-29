
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

Given two $k$-times [[differentiable manifolds]] (or [[smooth manifolds]]), then a _diffeomorphism_ 

$$
  f
   \;\colon\;
  X 
    \longrightarrow
  Y
$$

is a [[differentiable function]]
such that there exists an [[inverse]] differentiabe function $f^{-1}$ (a function which is an [[inverse function]] on the underlying sets and is itself [[differentiable function|differentiable]] to the given degree).

Diffeomorphisms are the [[isomorphisms]] in the corrresponding [[category]] [[Diff]] of [[differentiable manifolds]]/[[smooth manifolds]].

## Properties

### Relation to homeomorphisms {#RelationHomeomorphism}

It is clear that

+-- {: .num_lemma}
###### Observation

Every diffeomorphism is in particular a [[homeomorphism]] between the underlying [[topological spaces]].

=--

The converse in general fails. There exist differentiable maps with only continuous inverse.  There are also differentiable bijections whose inverse is not even continuous.

+-- {: .num_example}
###### Example

The function $f : \mathbb{R} \to \mathbb{R}$ given by $x \mapsto x^3$ is a homeomorphism but not a diffeomorphism. The diffeomorphism property fails at the origin, where the differential $d f : T_0 \mathbb{R} \to T_0 \mathbb{R}$ is not onto.

=--


But there is a rich collection of theorems about cases when the converse is true after all.

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, the **[[open n-ball]]** $\mathbb{B}^n$ is the open subset

$$
  \mathbb{B}^n = \{ \vec x \in \mathbb{R}^n | \sum_{i = 1}^n (x^i)^2 \lt 1 \}
  \subset \mathbb{R}^n
$$

of the [[Cartesian space]] $\mathbb{R}^n$ of all points of [[distance]] lower than 1 from the origin. This inherits the structure of a [[smooth manifold]] from the embedding into $\mathbb{R}^n$.

=--

+-- {: .num_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is homeomorphic to $\mathbb{B}^d$ is also diffeomorphic to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 

> What's a good/canonical textbook reference for this?

+-- {: .num_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$.

=--


+-- {: .num_theorem}
###### Theorem

For $X$ and $Y$ smooth manifolds of dimension $d = 1$, $d = 2$ or $d = 3$ we have:

if there is a homeomorphism from $X$ to $Y$, then there is also a diffeomorphism.

=--

See the corollary on p. 2 of ([Munkres](#Munkres)).

### Relation to homotopy equivalences
 {#RelationToHomotopyEquivalences}

For the following kinds of manifolds $\Sigma$ it is true that every [[homotopy equivalence]] 

$$
  \alpha \colon \Pi(\Sigma) \stackrel{\simeq}{\longrightarrow} \Pi(\Sigma)
$$

(hence every [[equivalence of infinity-groupoids|equivalence]] of their [[fundamental infinity-groupoids]]) is [[homotopy|homotopic]] to a [[diffeomorphism]]

$$
  a \colon \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma
$$

i.e. that given $\alpha$ there is $a$ with

$$
  \alpha \simeq \Pi(a)
  \,.
$$


* for $\Sigma$ any [[surface]] ([Zieschang-Vogt-Coldeway](#ZieschangVogtColdeway))

* for $\Sigma$ a [[Haken 3-manifold]] ([Waldhausen](#Waldhausen68)) 

* for $\Sigma$ any  [[hyperbolic manifold]] of finite [[volume]] and of [[dimension]] $\geq 3$ (by [[Mostow rigidity theorem]]) (check)

A review of results and relevant literature is also on the first page of ([Hass-Scott 92](#HassScott92))-

## Related concepts

* [[diffeomorphism group]]

* [[coordinate transformation]]

* [[general covariance]]

* [[super-diffeomorphism]]

## References

* {#Ozols} V. Ozols, _Largest normal neighbourhoods_ 
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672)) ([AMS](http://www.ams.org/journals/proc/1976-061-01/home.html): [pdf](http://www.ams.org/journals/proc/1976-061-01/S0002-9939-1976-0431220-4/S0002-9939-1976-0431220-4.pdf))


* {#Munkres} [[James Munkres]], _Obstructions to the smoothing of piecewise-differentiable homeomorphisms_  Bull. Amer. Math. Soc. Volume 65, Number 5 (1959), 332-334.  ([Euclid](http://projecteuclid.org/euclid.bams/1183523321))([AMS](http://www.ams.org/journals/bull/1959-65-05/): [pdf](http://www.ams.org/journals/bull/1959-65-05/S0002-9904-1959-10345-1/S0002-9904-1959-10345-1.pdf))

* {#ZieschangVogtColdeway} Zieschang, Vogt and Coldeway, _Surfaces and planar discontinuous groups_

* {#Waldhausen68} [[Friedhelm Waldhausen]], _On Irreducible 3-Manifolds Which are Sufficiently Large_, Annals of Mathematics
Second Series, Vol. 87, No. 1 (Jan., 1968), pp. 56-88 ([JSTOR](http://www.jstor.org/stable/1970594))

* {#HassScott92} Joel Hass, Peter Scott, _Homotopy equivalence and homeomoprhism of 3-manifolds_, Topology, Vol. 31, No. 3 (1992) pp. 493-517  ([pdf](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/29969/0000331.pdf?sequence=1))

[[!redirects diffeomorphisms]]
[[!redirects diffeomorphic]]