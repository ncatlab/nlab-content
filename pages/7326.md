
* table of contents
{: toc}

##Idea

A  [[groupoid]] [[presented stack|presenting]] an [[orbifold]] (as a [[stack]]) is called an **orbifold groupoid** if it satisfies certain properties. Since in the literature there are different notions of orbifolds, there are different sets of properties the presenting groupoids are required to satisfy.

The most common definition requires the presenting groupoid to be [[étale groupoid|étale]] and [[proper groupoid|proper]]. Note that these properties can be defined not only in smooth- or topological context. See for the moment [[open map]], the section on infinitesimal cohesion in [[cohesive (infinity,1)-topos]], and [[proper geometric morphism]].





## Definitions

+-- {: .num_defn}
###### Definition
(sse (smooth stable &#233;tale) groupoid ([^Mc Duff])


An **sse groupoid** is a groupoid being

* [[étale groupoid|étale]]

* [[stable groupoid|stable]]

* [[Lie groupoid|Lie]]
=--

+-- {: .num_defn}

###### Definition
(ep (&#233;tale proper) groupoid )[^Mc Duff]

An **ep groupoid** is a groupoid being

* [[étale groupoid|étale]]

* [[stable groupoid|stable]]

* [[Lie groupoid|Lie]]

* [[proper groupoid|proper]]

Since this is the most common choice of axioms a groupoid presenting an orbifold is meant to satisfy it is the default class of orbifold groupoids.

Note that this definition is redundant since properness implies stability.

Note that what [^H. Hofer] calls ''ep-groupoid'' is ''&#233;tale and proper'' but not Lie in the ordinary sense: Since the underlying category is that of sc-spaces, &#233;tale becomes sc-&#233;tale and also ''proper'' is understood in some modified sense.


=--

There is further terminology applicable to orbifold groupoids:

+-- {: .num_defn}
###### Definition
([^Mc Duff])
Let $C$ be a groupoid, let $|C|=C_0/C_1$ denote its [[orbit space]].

$C$ is called

* **nonsingular** if every $C(c,c)$ is trivial

* **effective** / **faithful**  if for ever $c\in C_0$ and for every $f\in C(c,c)$ and for every neighborhood $f\in V\subset C_1$ of $f$ there is an $f^'\in V$ such that $s(f^')\not =t(f^')$

* **(path)connected** if $|C|$ is (path)connected.
=--


+-- {: .num_defn}
###### Definition
(wnb (weighted nonsingular branched) groupoid  )[^Mc Duff]

A **wnb (weighted nonsingular branched) groupoid** is a pair $(C,\Lambda)$ where $C$ is a oriented nonsingular sse Lie groupoid and $\Lambda:|C|_H\to (0,\infty)$ is a weighting function satisfying:

For each $p\in |C|_H$ there is an open neighborhood $p\in N:=N(p)\subset |C|_H$ of $p$ and disjoint open subsets $U_1 ,...,U_j\subset \pi^{-1}_H(N)\subset C_0$ -called **local branches** and positive weights $m_1 ,...,m_j$ such that

1. (covering) $\pi^{-1}_H(N)=|U_1|\cup ...\cup |U_j|\subset |C|$

1. (local regularity) all projections $\pi_H:U_i\to |U_i|_H$ is a homeomorphism onto a relatively closed subset of $N$.

1. (weighting) $\Lambda(q)=\Sigma_{i:q\in |U_i|_H}m_i$ for all $q\in N$

where $|C|_H$ denotes the maximal Hausdorff quotient of $|C|$ (If $C$ is proper we have $|C|=|C|_H$ and $\pi_H:C_0\to |C|_H$ the canonical projection. Points $p\in |C|_H$ having more than one inverse image are called **branch points**.


The tuple $(N,U_i,m_i)=(N^p,U^p_i,m^p_i)$ is called a **local branching structure at** $p$. $C$ is called **compact** if $|C|_H$ is.

Note that here the properness axiom is relaxed.
=--

#### Relation of the axioms

Given an ep groupoid, the properness axiom implies that the orbit space of the orbifold groupoid is Hausdorff.

Properness implies stability.


## Related concepts

* [[stack]]

* [[Lie groupoid]]

* [[orbifold]]

## References

The original paper is

* [[Ieke Moerdijk]], [[Dorette A. Pronk]], _Orbifolds, Sheaves and Groupoids_.  K-Theory 12:1 (1997), 3-21.  [doi](https://doi.org/10.1023/a:1007767628271).

An expository account is in

* [[Ieke Moerdijk]], _Orbifolds as groupoids: an introduction_.  Orbifolds in Mathematics and Physics, Contemporary Mathematics (2002), 205-222.  [doi:10.1090/conm/310/05405](http://dx.doi.org/10.1090/conm/310/05405), [arXiv:math/0203100](https://arxiv.org/abs/math/0203100).

Other sources:

[^Mc Duff]: [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_.  Journal of Symplectic Geometry 4:3 (2006), 259-315. 
 [doi:10.4310/jsg.2006.v4.n3.a2](http://dx.doi.org/10.4310/jsg.2006.v4.n3.a2).

[^H. Hofer]: [[Helmut H. W. Hofer]], _Polyfolds and Fredholm Theory_.  Oxford University Press (2017), [doi](http://dx.doi.org/10.1093/oso/9780198784913.003.0004).


category: Lie theory


[[!redirects orbifold groupoids]]
[[!redirects orbifold groupoid]]