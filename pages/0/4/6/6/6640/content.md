
# Noncommutative symmetric functions
* table of contents
{: toc}

## Idea

Noncommutative symmetric functions are a generalisation of [[symmetric functions]].  Many concepts and ideas extend from symmetric functions to noncommutative symmetric functions and the way in which they extend sheds light on their behaviour for ordinary symmetric functions.

Noncommutative symmetric functions also arise in their own right as interesting objects of study.

## Definition

+--{: .num_defn #nsymm}
###### Definition
The graded [[Hopf algebra]] of **noncommutative symmetric functions**, $\NSymm$, is defined in the following way.

1. As an algebra, it is $\mathbb{Z}\langle Z_1, Z_2, \dots \rangle$, the free algebra in countably many indeterminants over $\mathbb{Z}$.
1. The comultiplication is given by $\Delta Z_n = \sum_{i + j = n} Z_i \otimes Z_j$, where $Z_0 = 1$.
1. The counit is $\epsilon(Z_n) = 0$ for $n \ge 1$.
1. The antipode is $\iota(Z_n) = \sum_{wt(\alpha) = n} (-1)^{length(\alpha)} Z_\alpha$, where $\alpha = [\alpha_1, \cdots, \alpha_k]$ is a word in $\{1,2,\dots\}$ with $length(\alpha) = k$ and $wt(\alpha) = \sum \alpha_i$.
1. The degree of $Z_n$ is $n$.
=--

## Properties

1. The object $\NSymm$ represents a functor from not-necessarily-commutative rings to groups given by sending $B$ to formal power series in $B$ with leading term $1$, $B \mapsto 1 + t B[\![t]\!]$.

1. It is dual to the Hopf algebra of [[quasi-symmetric functions]].

1. The Hopf algebra of [[symmetric functions]] is a quotient of $\NSymm$.  The quotient mapping is given by sending $Z_i$ to the $i$th symmetric function.

## References

### Full research articles 

* G. Duchamp, F. Hivert, J.-Y. Thibon, _Noncommutative symmetric functions VI: free quasi-symmetric functions and related algebras_, Internat. J. Alg. Comput. 12 (2002), 671&#8211;717.
* [[I. M. Gelfand]], D. Krob, A. Lascoux, B. Leclerc, V. S. Retakh, J.-Y. Thibon, _Noncommutative symmetric functions_, Adv. in Math. __112__ (1995), 218&#8211;348, [hep-th/9407124](http://arxiv.org/abs/hep-th/9407124)
* Jean-Christophe Novelli, Jean-Yves Thibon, _Noncommutative symmetric functions and Lagrange inversion_, [math.CO/0512570](http://arxiv.org/abs/math/0512570); _Noncommutative symmetric functions and an amazing matrix_ [arxiv/1109.1184](http://arxiv.org/abs/1109.1184)
* Lenny Tevlin, _Noncommutative Monomial Symmetric Functions_, Formal Power Series and Algebraic Combinatorics Nankai University, Tianjin, China, 2007, proceedings [pdf](http://www.fpsac.org/FPSAC07/SITE07/PDF-Proceedings/Talks/83.pdf)
* D. Krob, J.-Y. Thibon, _Noncommutative symmetric functions IV:
Quantum linear groups and Hecke algebras at $q = 0$_, [pdf](http://hal.inria.fr/docs/00/05/79/10/PDF/ncsf4.pdf)


### Long surveys and lecture notes

* Michael Hazewinkel, _Symmetric functions, noncommutative symmetric functions and quasisymmetric functions_, [pdf](http://oai.cwi.nl/oai/asset/10344/10344B.pdf)
* [[V. Retakh]] and R. Wilson, Advanced Course on Quasideterminants and Universal Localization: [pdf](http://castellet.cat/Publications/quaderns/Quadern41.pdf) (see the part _Factorization of Noncommutative Polynomials
and Noncommutative Symmetric Functions_)


### Expositions/short summaries

* Mike Zabrocki, _Non-commutative symmetric functions II:
Combinatorics and coinvariants_, slides from a talk [pdf](http://garsia.math.yorku.ca/~zabrocki/talks/coinvariants.pdf), III: A representation theoretical approach [pdf](http://garsia.math.yorku.ca/~zabrocki/talks/reptheory.pdf)
* Lenny Tevlin, _Introduction to quasisymmetric and noncommutative
symmetric functions_, slides, Fields Institute 2010  [pdf](http://www.fields.utoronto.ca/programs/scientific/10-11/schubert/Noncommutative-Symmetric-and-Quasi-Symmetric-Functions-Fields-2010.pdf)


[[!redirects noncommutative symmetric function]]
[[!redirects noncommutative symmetric functions]]
