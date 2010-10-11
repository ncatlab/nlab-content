
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

A **diffeomorphism** is a [[smooth function]] $f: X \to Y$ beween [[smooth manifolds]] such that there exists an [[inverse]] smooth function $f^{-1}$ (a function which is a set-theoretic inverse and at the same time smooth).

Diffeomorphisms are precisely the [[isomorphism]]s in the [[category]] [[Diff]] of [[smooth manifold]]s

## Properties

### Relation to homeomorphisms {#RelationHomeomorphism}

It is clear that

+-- {: .un_lemma}
###### Observation

Every diffeomorphism is in particular a [[homeomorphism]] between the underlying [[topological space]]s.

=--

The converse in general fails. There exist differentiable maps with only continuous inverse.  There are also differentiable bijections whose inverse is not even continuous.

+-- {: .un_example}
###### Example

The function $f : \mathbb{R} \to \mathbb{R}$ given by $x \mapsto x^3$ is a homeomorphism but not a diffeomorphism. The diffeomorphism property fails at the origin, where the differential $d f : T_0 \mathbb{R} \to T_0 \mathbb{R}$ is not onto.

=--


But there is a rich collection of theorems about cases when the converse is true after all.

+-- {: .un_def}
###### Definition

For $n \in \mathbb{N}$, the **[[open n-ball]]** $\mathbb{B}^n$ is the open subset

$$
  \mathbb{B}^n = \{ \vec x \in \mathbb{R}^n | \sum_{i = 1}^n (x^i)^2 \lt 1 \}
  \subset \mathbb{R}^n
$$

of the [[Cartesian space]] $\mathbb{R}^n$ of all points of [[distance]] lower than 1 from the origin. This inherits the structure of a [[smooth manifold]] from the embedding into $\mathbb{R}^n$.

=--

+-- {: .un_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is homeomorphic to $\mathbb{B}^d$ is also diffeomorphic to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 

> What's a good/canonical textbook reference for this?

+-- {: .un_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$.

=--


+-- {: .un_theorem}
###### Theorem

For $X$ and $Y$ smooth manifolds of dimension $d = 1$, $d = 2$ or $d = 3$ we have:

if there is a homeomorphism from $X$ to $Y$, then there is also a diffeomorphism.

=--

See the corollary on p. 2 of ([Munkres](#Munkres)).


## References

* V. Ozols, _Largest normal neighbourhoods_ 
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))
{#Ozols}

* James Munkres, _Obstructions to the smoothing of piecewise-differentiable homeomorphisms_  Bull. Amer. Math. Soc. Volume 65, Number 5 (1959), 332-334.  ([web](http://projecteuclid.org/euclid.bams/1183523321))
{#Munkres}

[[!redirects diffeomorphisms]]
[[!redirects diffeomorphic]]