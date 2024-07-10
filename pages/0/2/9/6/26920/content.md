
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea

Quantum nilpotent algebras are a class of [[associative algebras]] which are defined as iterated [[Ore extensions]] of a special type.

## Definition

Let $K$ be a [[ground ring]]. An iterated [[Ore extension]]
$$
K[x_1][x_2;\sigma_2,\delta_2][x_3;\sigma_3,\delta_3]\cdots
[x_n;\sigma_n,\delta_n]
$$
where $\sigma_j$ is an automorphism of 
$$
A_{j-1} = K[x_1][x_2;\sigma_2,\delta_2][x_3;\sigma_3,\delta_3]\cdots
[x_{j-1};\sigma_{j-1},\delta_{j-1}]
$$
and $\delta_j$ is the $\sigma_j$-derivation of $A_{j-1}$ is a quantum nilpotent algebra if it is equipped with a rational action of the torus $(K^\times)^l$ such that

* $x_1,\ldots,x_n$ are eigenvectors of the action

* each $\delta_j$ is a locally nilpotent $\sigma_j$-derivation of $A_{j-1}$

* For every $j\in\{1,\ldots,n\}$, there exists $h_j\in (K^\times)^l$ such that $(h_j\cdot )|_{A_{j-1}} = \sigma_j$ and $h_j\cdot x_j = q_j x_j$ for some $q_j\in K^\times$ which is not a root of unity.

It follows that $\sigma_j\circ\delta_j = q_j \delta_j\sigma_j$ (this was stated as a requirement in the original definition).

## Properties

Quantum nilpotent algebras are a framework where the so called derivative elimination algorithm can be applied. 

## References

* [[K. R. Goodearl]], [[Milen Yakimov|M. T. Yakimov]], _Quantum cluster algebras and quantum nilpotent algebras_, Proc. Natl. Acad. Sci. USA 111(27):9696--9703  (2014) [doi](https://doi.org/10.1073/pnas.1313071111)
* [[S. Launois]], T. H. Lenagan, B. M. Nolan, _Total positivity is a quantum phenomenon: the Grassmannian case_, Memoirs of the Amer. Math. Soc. _1448_ (2023) 123 p.

category: algebra

[[!redirects quantum nilpotent algebras]]