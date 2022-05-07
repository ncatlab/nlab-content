
#Contents#
* table of contents
{:toc}

## Idea

A 'stuff type' is a type of [[stuff]] that can placed on [[finite sets]], e.g. 'being a 2-colored finite set', or 'being the first of two finite sets'.  

## Definition

To make this precise, we define a __stuff type__ to be a [[functor]]

$$p: X \to core(FinSet)$$

from some [[groupoid]] $X$ to the groupoid of finite sets and bijections, which is the [[core]] of the category [[FinSet]].  Equivalently, we can think of a stuff type as a [[2-functor]] (of a suitably weakened sort, namely a [[pseudofunctor]]) 

$$F: core(FinSet)^{op} \to Gpd $$

The idea is to use the [[Grothendieck construction]] and define

$$F(n) = p^{-1}(n)$$

taking advantage of the fact that we may assume without loss of generality that $p$ is a [[fibration]].

We can think of $F$ as a suitably weakened sort of [[presheaf]] of groupoids on $core(FinSet)$.  But since a groupoid is equivalent to its opposite, we can also think of a stuff type as a functor

$$core(FinSet) \to Gpd $$

If a stuff type

$$p: X \to core(FinSet)$$

is faithful, we call it a [[structure type]].  Structure types are also called [[species]], and they can be thought of as presheaves of _sets_

$$F: core(FinSet)^{op} \to Set $$

A stuff type can also be thought of as a [[categorification|categorified]] [[generating function]].   Whereas a generating function assigns a number to each [[natural number]] (or [[finite set]]), a stuff type assigns a [[groupoid]].  Namely, the stuff type

$$F: core(FinSet)^{op} \to Gpd $$

assigns to the finite set $n$ the groupoid $F(n)$.  We can write $F$ as a power series where the coefficient of $Z^n$ is the groupoid $F(n)$.    In these terms, the structure type 'being a finite set' is
\[E^Z := \frac{1}{\overline{0!}} + \frac{1}{\overline{1!}}Z + \frac{1}{\overline{2!}}Z^2 + \cdots + \frac{1}{\overline{n!}}Z^n + \cdots,\]
where $+$ is disjoint union, $//$ is the weak quotient, $n!$ is the permutation group $S_n$, and $1$ is the one-element set (since there's only one way to be finite).

The structure type 'being a totally ordered even set' is
\[\frac{1}{1-Z^2} := \frac{0!}{\overline{0!}} + 0Z + \frac{2!}{\overline{2!}}Z^2 + 0Z^3 + \cdots,\]
since there are $n!$ ways to order a set with $n$ elements and $0$ ways for an odd set to be even.

## References

One advantage of stuff types over the more familiar structure types (i.e., species) is that they allow one to categorify the theory of [[Feynman diagram|Feynman diagrams]]:

* [[John Baez]] and [[James Dolan]], From finite sets to Feynman diagrams, in _Mathematics Unlimited - 2001 and Beyond_, vol. 1, eds. Bj&#246;rn Engquist and Wilfried Schmid, Springer, Berlin, 2001, pp. 29-50.  ([arXiv](http://arxiv.org/abs/math.QA/0004133))

* Jeffrey Morton, Categorified algebra and quantum mechanics, _Theory and Applications of Categories_, **16** (2006), 785--854. ([arXiv](http://arxiv.org/abs/math/0601458))

* [[John Baez]], Fall 2003 to Spring 2004 [seminar notes](http://math.ucr.edu/home/baez/qg-fall2003/).

For more on stuff types see:

* [[John Baez]], [Groupoidification](http://math.ucr.edu/home/baez/groupoidification/)

For the generalization of stuff types using $\infty$-groupoids, see:

* Imma Gálvez-Carrillo, Joachim Kock,
and Andrew Tonks, Homotopy linear algebra, _Proc. Roy. Soc. Edinburgh
Sect. A_, **148(2)** (2018), 293--325.  ([arXiv](https://arxiv.org/abs/1602.05082))

[[!redirects stuff types]]
