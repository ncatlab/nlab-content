
> under construction

#Contents#
* table of contents
{:toc}

## Idea

Logarithmic geometry is a slight variant of [[algebraic geometry]] (resp. [[analytic geometry]]) where [[schemes]] (resp. analytic spaces) and morphisms with mild ("logarithmic") [[singularities]] still behave as [[smooth schemes]] (resp. smooth analytic spaces).

Where an [[affine variety]] is the formal dual to a [[commutative ring]] $(R,\times, +)$, the analog in logarithmic geometry is such a ring equipped with

1. a [[monoid]] $K$ and a [[monoid]] [[homomorphism]] $\alpha \colon K \longrightarrow (R, \times)$;

1. such that $\alpha^{-1}(R^\times) \simeq R^\times$;

where $R^\times$ is the [[group of units]] of $R$. These two items together are called a _log-structure_ on $R$ (or a _pre-log structure_ if the condition in the second item does not necessarily hold).

The archetypical example of a logarithmic structure, which gives the concept its name,is that describing logarithmic singularities at closed immersions which are locally of the form of the [[zero locus]]

$$
  D \coloneqq \{x_1 x_2 \cdots x_k = 0\} \hookrightarrow \mathbb{A}^n
$$

of the product of $k$ variables inside the $n$-dimensional [[affine space]]. The log-structure on $\mathbb{A}^n$ reflecting this is 

$$
  \mathbb{N}^k \longrightarrow \mathcal{O}_{\mathbb{A}^n}
$$

given by the exponential map

$$
  (n_i) \mapsto \prod_i x_i^{n_i}
$$

(e.g. [Pottharst, p. 4](#Pottharst))

The definition of [[Kähler differential forms]] in logarithmic geometry is such that the differential 1-forms on the corresponding log scheme here are generated over $\mathcal{O}_{\mathbb{A}^n}$ by the ordinary differentials $d x^i$ for $k \lt i \leq n$ and by the [[differential forms with logarithmic singularities]] at $D$ which are
$\frac{1}{x^i} d x^i = d log x^i$ for $1 \leq i \leq k$.

(e.g. [Pottharst, p. 5](#Pottharst))



## Examples

### Affine line

Given the [[affine line]] $\mathbb{A}^1$ with function ring 
$\mathcal{O}(\mathbb{A}^1) = \mathbb{Z}[t]$ then there is a log structure given by the canonical map

$$
  \alpha
  \colon
  \mathbb{N} \hookrightarrow \mathbb{Z}[\mathbb{N}] = \mathbb{Z}[t]
  \,.
$$

The sheaf of differential forms on the resulting log-scheme is that of the ordinary affine line and one more generating section which is the [[differential form with logarithmic singularities]]

$$
  \frac{1}{t} dt = d log(t)
$$

(e.g. [Pottharst, p. 4-5](#Pottharst))

This phenomenon gives the name to logarithmic geometry.

### Complex plane

Working over $\mathbb{C}$ consider the multiplicative sub-monoid $\mathbb{R}_{\geq 0} \times S^1 \subset \mathbb{C} \times \mathbb{C}$ and the map

$$
  \mathbb{R}_{\geq 0 } \times S^1 \longrightarrow \mathbb{C}
$$

given by product operation. This defines a log-structure on $\mathbb{C}$. The corresponding log-space is often denoted $T$ (e.g. [Kato-Nakayama 99, p. 5](#KatoNakayama99), [Ogus01, section 3.1](#Ogus01)).

Given any log-scheme $X$ over $\mathbb{C}$, then the underlying [[topological space]] $X^{log}$ has as points the log-scheme homomorphisms $T \longrightarrow X$. ([Ogus 01, def. 3.1.1](#Ogus01))



## Related concepts

* [[differential form with logarithmic singularities]]

* [[logarithmic connection]]

* [[logarithmic motivic homotopy theory]]

* [exponential sequence in logarithmic geometry](exponential+exact+sequence#InLogarithmicGeometry)

## References

Logarithmic geometry originates with Fontaine and [[Luc Illusie]] in the 1980s.

* [[Kazuya Kato]], _Logarithmic structures of Fontaine-Illusie_, in _Algebraic Analysis, Geometry and Number Theory_, The Johns Hopkins University Press (1989), 191-224.

* [[Luc Illusie]], _Logarithmic spaces (according to Kato)_, in: Barsotti-Symposium in Algebraic Geometry (ed. V. Cristante and [[William Messing]]), Academic Press: Perspectives in Math. 15 (1994), 183-203

* [[Luc Illusie]], [[Arthur Ogus]], _G&#233;om&#233;trie logarithmique_ ([pdf](http://math.harvard.edu/~tdp/Illusie-Log.geometry.lecture.notes-single-page.pdf))

* [[Luc Illusie]], _An overview of the work of K. Fujiwara, K. Kato, and C. Nakayama on logarithmic &#769;etale cohomology_. Ast&#233;risque, (279):271&#8211;322, 2002. 
Cohomologies p-adiques et applications arithm&#233;tiques, II.

* {#KatoNakayama99} [[Kazuya Kato]], Chikara Nakayama, _Log Betti cohomology, log &#233;tale cohomology, and log de Rham cohomology of log schemes over ${\bf C}$_, Kodai Math. J. Volume 22, Number 2 (1999), 161-186 ([Euclid](http://projecteuclid.org/euclid.kmj/1138044041))


Brief surveys include

* {#Pottharst} Pottharst, _Logarithmic structures on schemes_ ([pdf](http://math.bu.edu/people/potthars/writings/log.str.pdf))

* [[Arthur Ogus]], _Logarithmic geometry_, talk slides 2009 ([pdf](http://math.berkeley.edu/~ogus/preprints/colloqhandout.pdf))

* [[Dan Abramovich]], _Logarithmic geometry and moduli_, talk slides 2014 ([pdf](http://www.math.brown.edu/~abrmovic/LOGGEOM/lectures-beamer.pdf))

Lecture notes include

* {#Ogus01} [[Arthur Ogus]], _Lectures on logarithmic algebraic geometry_, TeXed notes, 2001, [pdf](http://math.berkeley.edu/~ogus/preprints/log_book/logbook.pdf)

See also

* Dan Abramovich, Qile Chen, Danny Gillam, Yuhao Huang, Martin Olsson, Matthew Satriano, Shenghao Sun, _Logarithmic geometry and moduli_, [arxiv/1006.5870](http://arxiv.org/abs/1006.5870)

* [[Martin C. Olsson]], _Logarithmic geometry and algebraic stacks_, Ann. Sci. Ecole Norm. Sup. (4), 36(5):747{791, 2003.

* Jakob Stix, section 3 of _Projective Anabelian Curves in Positive Characteristic and Descent Theory for Log-Etale Covers_, 2002 ([pdf](https://www.mathi.uni-heidelberg.de/~stix/preprints/STIXdissB.pdf))

Discussion in the context of [[higher algebra]] ([[brave new algebra]]) is in

* [[John Rognes]], _Topological logarithmic structures_ 2009 ([pdf](http://folk.uio.no/rognes/papers/oslo09.pdf))

[[!redirects log geometry]]

[[!redirects logarithmic algebraic geometry]]
[[!redirects log-scheme]]
[[!redirects log-schemes]]