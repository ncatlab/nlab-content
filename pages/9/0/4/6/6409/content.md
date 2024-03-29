
> This page is about valuations on [[rings]]/[[fields]]. For valuation in [[measure theory]] see [[valuation (measure theory)]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[Wikipedia](https://en.wikipedia.org/wiki/Valuation_%28algebra%29) says very succinctly

> A **valuation** is a [[function]] on a [[field]] that provides a measure of size or multiplicity of elements of the field. They generalize to commutative [[algebra]] the notion of size inherent in consideration of the degree of a pole or multiplicity of a zero in [[complex analysis]], the degree of divisibility of a number by a prime number in number theory, and the geometrical concept of contact between two algebraic or analytic varieties in algebraic geometry.

Sometimes one also discusses *exponential* (or *multiplicative*) *valuations* (also called valuation functions, and viewed as generalized [[absolute values]]) which look more like [[norms]], and their [[equivalence classes]], [[places]]. See at _[[absolute value]]_ for more on this common sense.


See also [[discrete valuation]] and [[valuation ring]].



## Definition

Given a [[total order|totally ordered]] [[abelian group]] $G$, a $G$-valued __valuation__ $v$ on a (commutative) [[field]] $K$ is a (typically required to be surjective) [[function]] $v:K\to G\cup \infty$ such that $v(K^\times)\subset G$ and 

* $v$ defines a [[homomorphism]] of [[groups]] $v|_K : K^\times\to G$ where $K^\times$ is the [[multiplicative group]] of $K$

* $v(0) = \infty$

* $v(x+y) \geq min\{ v(x),v(y)\}$

with usual conventions for $\infty$.  A field equipped with a valuation is a __valued field__.

If the abelian group is the group of [[integers]] $\mathbb{Z}$, then we talk about [[discrete valuation | discrete valuations]].

## Properties

### Valuative criteria

In [[algebraic geometry]] there are very important theorems, due to Chevalley, called the [[valuative criterion of properness]] and [[valuative criterion of separatedness]].

### Valuation rings and ideals

The **valuation ring** of a valued field is the subring of elements of valuation $\ge 0$.  The **valuation ideal** is the ideal in the valuation field consisting of elements of valuation $\gt 0$.

### Valuation uniformity

Any valued field admits a **valuation [[uniformity]]**, where each $g\in G$ generates an [[entourage]] $\{ (x,y) \mid v(x-y)\ge g \}$.  For a discrete valuation, the restriction of this uniformity to the valuation ring coincides with the [[adic topology]] generated by the valuation ideal; but in general this need not be the case.

A **complete valued field** is a valued field whose valuation unifomity is complete.  A non-complete valued field can be completed.


## Examples

### Rational functions

For any field $k$, the field $k(t)$ of formal [[rational functions]] in a variable $t$ has a discrete valuation given by the difference in the *lowest* nonzero degree of the numerator and denominator.  Thus for instance

$$\frac{3t + 2t^3- 7t^4}{2t^2 - 8t^9}$$

would have valuation $1-2 = -1$.  The valuation ring contains the [[polynomial ring]] $k[t]$, but is strictly larger, for instance it contains $\frac{x^2}{x+1}$.  The restriction of the valuation ideal to $k[t]$ does coincide with $(t)$ however.  The valued field $k(t)$ is not complete; its completion is the field $k[[t]]$ of [[formal power series]].

### Generalized rational functions

For any field $k$, a **[[generalized polynomial]]** with exponents in $G$ is a finite formal sum of monomials $a q^\ell$, where $a\in k$ and $\ell\in G$; this defines a ring $k[q^G]$.  The field $k(q^G)$ of **[[generalized rational function|generalized rational functions]]** is the [[field of fractions]] of $k[q^G]$.  It is a valued field with value group $G$, with valuation defined analogously to the case of ordinary rational functions.  As there, its valuation ring contains $k[q^G]$ but is larger.

It is not generally complete.  At least in good cases (e.g. if $G$ is Archimedean in the sense that positive integers are cofinal therein, such as $\mathbb{R}$), its completion should be the subfield of the field $k((q^G))$ of [[Hahn series]] consisting of those Hahn series of order type $\omega$ that converge to themselves in the topology of $k((q^G))$.

### $p$-adic valuations

The field $\mathbb{Q}$ admits a $p$-adic valuation, whose completion is the field $\mathbb{Q}_p$ of [[p-adic numbers]].


## Related concepts

[[!include analytic geometry ingredients -- table]]

## Literature 

* {#BoschGuntzerRemmert84} S. Bosch, U. G&#252;ntzer, [[Reinhold Remmert]], _[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry_, 1984 ([pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf))


* Wikipedia, *[valuation (algebra)](http://en.wikipedia.org/wiki/Valuation_%28algebra%29)*

* {#FroehlichCassels67} [[Albrecht Fröhlich]], [[J. W. S. Cassels]] (eds.), _Algebraic number theory_, Acad. Press 1967, with many reprints; Fröhlich, Cassels, Birch, Atiyah, Wall, Gruenberg, Serre, Tate, Heilbronn, Rouqette, Kneser, Hasse, Swinerton-Dyer, Hoechsmann, systematic lecture notes from the instructional conference at Univ. of Sussex, Brighton, Sep. 1-17, 1965 (ISBN:9780950273426, [pdf](https://www.math.arizona.edu/~cais/scans/Cassels-Frohlich-Algebraic_Number_Theory.pdf), [errata pdf](https://www.ma.imperial.ac.uk/~buzzard/errata.pdf) by [[Kevin Buzzard]])

* {#Cassels86} [[J. W. S. Cassels]], Chapter 2 in: *Local Fields*, Cambridge University Press, 1986 (ISBN:9781139171885, [doi:10.1017/CBO9781139171885](https://doi.org/10.1017/CBO9781139171885)) 


* [[Serge Lang]], _Algebraic number theory_, GTM __110__, Springer 1970, 2000

* [[Ehud Hrushovski]], [[David Kazhdan]], _The value ring of geometric motivic integration and the Iwahori Hecke algebra of $SL 2$_, [math.LO/0609115](http://arxiv.org/abs/math/0609115); _Integration in valued fields_, in Algebraic geometry and number theory, 261&#8211;405, Progress. Math. __253__, Birkh&#228;user Boston, [pdf](http://math.huji.ac.il/~ehud/papers/intv-060428.pdf)
* A H Lightstone, Abraham Robinson, _Nonarchimedean fields and asymptotic expansions_, North-Holland Publ. 1976

check out ([Scholze 11, def. 22, remark 2.3](perfectoid%20space#Scholze11))


[[!redirects valuations]]
[[!redirects valued field]]
[[!redirects valued fields]]

