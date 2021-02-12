
#Contents#
* table of contents
{:toc}

## Idea


In [[physics]] and [[data analysis]], where an [[observable]] is typically a [[function]] $X \overset{f}{\longrightarrow} \mathbb{R}^n$ from a given data set $X$ to the set of [[real numbers]] $\mathbb{R}^1$, or to an [[n-tuple]] of such (varying in a [[Cartesian space]] $\mathbb{R}^n$), an _iso-hypersurface_ or _level-hypersuface_ is a [[level set]] of this observable, hence the [[subset]] of $X$ consisting all those points $x \in X$ on which this observable $f$ takes the same given value $f(x) = c$. 

For example, if $X$ is a model for the Earth's atmosphere, and if $f$ assigns to each point $x \in X$ the atmospheric [[pressure]] $p(x)$ at this point -- in some suitable [[physical units]] and to some suitable approximation --, then an iso-surface for $p$ is an _[[isobar]]_: a [[surface]] of [[constant function|constant]] [[pressure]].

For such a [[level set]] to actually be a [[hypersurface]], hence a [[differentiable manifold|differentiable]]/[[smooth manifold|smooth]] [[submanifold]], some regularity conditions on $f$ need to be satisfied, such as that $f$ is a [[differentiable function]] to suitable degree, and, crucially, that its value $c$ (whose [[pre-image]] is formed) is a _[[regular value]]_.

Phrased this way, the construction of iso-hypersurfaces turns out to be a central topic also in areas of pure mathematics, such as in [[differential topology]] and [[cobordism theory]], where the formation of [[pre-images]] of [[regular values]] inside $\mathbb{R}^n$ is known as part of the [[Pontryagin construction]].

Curiously, this means that[[Pontryagin's theorem]] applies to iso-hypersurfaces, saying here that, as the value $c$ of the [[observable]] $f$ varies, the shape ([[topology]]) of the corresponding iso-hypersurfaces changes (at most) by a _[[cobordism]]_, and that the resulting ([[normally framed submanifold|normally framed]]) [[cobordism class]] of all these hypersurfaces corresponds to the class of $f$ in the $n$-[[Cohomotopy theory]] of the data set $X$.

While Pontryagin's theorem is ancient, the idea that it thus implies the possibility of [[topological data analysis]] via [[Cohomotopy theory]] of [[observables]] and [[cobordism theory]] of their iso-hypersurfaces appears only recently ([Franek-Krčál 16](#FranekKrcal16), [Franek-Krčál 17](#FranekKrcal17)).

## Examples 

* [[isobar]]


## References

### General

See also 

* Wikipedia, _[Isosurface](https://en.wikipedia.org/wiki/Isosurface)_



[[!include cohomotopy in topological data analysis -- references]]





[[!redirects isosurfaces]]

[[!redirects iso-surface]]
[[!redirects iso-surfaces]]

[[!redirects iso-hypersurface]]
[[!redirects iso-hypersurfaces]]


