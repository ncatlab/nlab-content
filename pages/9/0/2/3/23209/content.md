
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Denote by $Emb_n$ the [[site]] of $n$-dimensional [[smooth manifolds]] and [[open embeddings]].

An [[(∞,1)-sheaf]] $F\colon Emb_n^op\to Top$ of [[topological spaces]] is __microflexible__ if for any closed inclusion $K\to K'$ of [[compact spaces]],
the induced map $F(K')\to F(K)$ is a [[Serre microfibration]].

An [[(∞,1)-sheaf]] $F\colon Emb_n^op\to Top$ of [[topological spaces]] is __flexible__ if for any closed inclusion $K\to K'$ of [[compact spaces]],
the induced map $F(K')\to F(K)$ is a [[Serre fibration]].

## Gromov's theorem

Given an [[open manifold]] $M$,
the inclusion of microflexible sheaves into flexible sheaves
on the [[slice site]] site $Emb_n/M$ is an [[equivalence of (∞,1)-categories]].

## Related concepts

* [[h-principle]]

* [[Serre microfibration]]


## Literature

The original reference is

* [[M. L. Gromov]], _Stable mappings of foliations into manifolds_, Mathematics of the USSR-Izvestiya 3:4 (1969), 671-694.  [doi](http://dx.doi.org/10.1070/im1969v003n04abeh000796).

The canonical reference is Section 2.2.1 of

* [[Mikhael Gromov]], _Partial differential relations_, 1986, [doi](http://dx.doi.org/10.1007/978-3-662-02267-2).

See also

* [[John Francis]], *The H-principle for microflexible sheaves*, 2010 ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/20microflexible.pdf))

* [[Alexander Kupers]], Section 2 of: *Three applications of delooping to H-principles*, Geom Dedicata **202** (2019) 103–151  ([arXiv:1701.06788](https://arxiv.org/abs/1701.06788), [doi:10.1007/s10711-018-0405-7](https://doi.org/10.1007/s10711-018-0405-7))


[[!redirects microflexible sheaves]]


