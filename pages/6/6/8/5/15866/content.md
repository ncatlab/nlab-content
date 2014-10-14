
# Noncommutative differential calculus
* table of contents
{: toc}

## Disambiguation

There are several notions of noncommutative differential calculus. See related pages [[regular differential operator in noncommutative geometry]], 
[[bicovariant differential calculus]], [[differential bimodule]], [[differential monad]], [[cyclic homology]]...

This entry is about the version introduced by [[Boris Tsygan]], [[Dmitri Tamarkin]] and [[Ryszard Nest]], and studied also by Dolgushev, Kowalzig and others. 


## Definition

Let $k$ be a unital commutative ground ring. A
[[Gerstenhaber algebra]] $(V^\bullet,\cup)$ 
over $k$ is a 
$\mathbf{N}$-graded-commutative algebra 
with a graded Lie structure on $V[1]$ 
satisfying the Leibniz rule
(an analogue of a Poisson bracket in dg-world)

$$
\{ c, a\cup b\} = \{c, a\}\cup b + 
(-1)^{p q} a \cup \{ c, b\}
$$

A [[Gerstenhaber module]] $(\Omega_\bullet,\cap)$ is a
graded module over a Gerstenhaber algebra $(V^\bullet,\cup)$ 
$$
\cap : V\otimes \Omega\to\Omega,\,\,\,\,\,\,\,
V^p\otimes\Omega_n\ni a\otimes x \mapsto a\cap x
\in\Omega_{n-p}
$$
with a graded Lie algebra action of $V[1]$,
$$
\mathcal{L} : V[1]\otimes\Omega\to\Omega,\,\,\,\,\,\,
V^{p+1}\otimes\Omega_n\ni a\otimes x \mapsto \mathcal{L}_a(x)
\in\Omega_{n-p},
$$
satisfying the mixed Leibniz rule
$$
b \cap \mathcal{L}_a(x) = \{ b, a\}\cap x +
(-1)^{p q} \mathcal{L}_a(b\cap x).
$$

A Gerstenhaber module $\Omega$ over a Gerstenhaber
algebra $V$ is a __Batalin-Vilkovisky module__ 
if it is equipped with a $k$-linear differential
of degree +1,
$$
B : \Omega_\bullet\to\Omega_{\bullet+1},\,\,\,\,\,\,B^2 = 0,
$$
such that $\mathcal{L}_\alpha$ for $a\in V^p$ and $B$ satisfy the generalization of the [[Cartan's homotopy formula]]
$$
\mathcal{L}_a(x) = B(a\cap x) - (-1)^p a\cap B(x)
$$

A __Tsygan-Tamarkin-Nest noncommutative (differential) calculus__ is a pair $(V, \Omega)$ 
of a Gerstenhaber algebra $V$
and a Batalin-Vilkovisky $V$-module $\Omega$.

See also the case of [[Batalin-Vilkovisky algebra]]. 


## References

* Dmitri Tamarkin, Boris Tsygan, _Noncommutative differential calculus, homotopy BV algebras and formality conjectures_, Metods of Functional Analysis and topology, 1, 2001 [arxiv:math.KT/0002116v1](http://arxiv.org/abs/math/0002116v1)

* R. Nest, B. Tsygan, _On the cohomology ring of an algebra_, Advances in geometry, Progr. Math. __172__, Birkhauser 1999, pp. 337&#8211;370 [arxiv:math.QA/9803132](http://arxiv.org/abs/math/9803132)

* V. Dolgushev, D. Tamarkin, B. Tsygan, _Noncommutative calculus and the Gauss-Manin connection_, in: Higher structures in geometry and physics, 139&#8211;158, Progr. Math., 287, Birkh&#228;user/Springer, New York, 2011 , [arXiv:0902.2202](http://arxiv.org/abs/0902.2202)

* K. Behrend, B. Fantechi, _Gerstenhaber and Batalin-Vilkovisky structures on Lagrangian intersections_,
[pdf](https://www.math.ubc.ca/~behrend/GeBaViLa.pdf)

Many examples of such noncommutative differential calculi are constructed using [[Hopf algebroid]]s 
(Schauenburg's version) in works

* Niels Kowalzig, _Gerstenhaber and Batalin-Vilkovisky structures on modules over operads_, [arxiv:1312.1642](http://arxiv.org/abs/1312.1642);
_Batalin-Vilkovisky algebra structures on (Co)Tor and Poisson bialgebroids_ [arXiv:1305.2992](http://arxiv.org/abs/1305.2992)

* Niels Kowalzig, Ulrich Kraehmer, _Batalin-Vilkovisky structures on Ext and Tor_,  [arxiv:1203.4984](http://arxiv.org/abs/1203.4984)


[[!redirects noncommutative calculus]]
[[!redirects noncommutative differential calculus]]
[[!redirects noncommutative differential calculi]]
[[!redirects Batalin-Vilkovisky module]]
[[!redirects Batalin–Vilkovisky module]]
[[!redirects Batalin--Vilkovisky module]]
