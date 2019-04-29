
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--

#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Whitehead product** is a bilinear operation on the elements of the [[homotopy groups]] of a [[pointed space|pointed]] [[CW-complex]] $X$, which makes them a [[super Lie algebra]] over the [[ring]] of [[integers]] (often called a _graded quasi-Lie algebra_).

More specifically, it takes as input $\alpha\in\pi_r(X)$ and $\beta\in\pi_s(X)$ and produces $[\alpha,\beta]_{Wh}\in\pi_{r+s-1}(X)$.  The operation satisfies a graded [[Jacobi identity]] ([Hilton 55, Theorem B](#Hilton55)).

There is also a **generalized Whitehead product** where we can take more general homotopy classes ([[continuous maps]] up to [[homotopy]]) $\alpha\in [S^\cdot Y,X]$ and $\beta\in [S^\cdot Z,X]$ to produce a class $[\alpha,\beta]_{Wh}\in[Y\star Z,X]$. Here $S^\cdot$ denotes the [[reduced suspension]] operation on pointed spaces and $\star$ denotes the [[join of spaces|join]] of CW-complexes. Notice that $pt\star Z = C^\cdot(Z)$ and the reduced [[cone]] of a point is $C^\cdot(pt)=S^1$. Thus for $Y=Z=pt$ the generalized Whitehead product reduced to the usual Whitehead product.

The Whitehead products form one of the [[primary homotopy operation]]s and in fact with [[composition operation]]s and $\pi_1$-actions generate all such operations. This is related to the definition of [[Pi-algebra]].

In the context of [[simplicial group]]s, representing [[connected]] [[homotopy type]]s, there is a formula for the Whitehead product in terms of a [[Samelson product]], which in turn is derived from a [[shuffle]] product which is a sort of non-commutative version of the [[Eilenberg-Zilber map]].  These simplicial formulae come from an analysis of the structure of the [[product of simplices]]. (The formula for the Whitehead product is due to [[Dan Kan]] and can be found in the old survey article of [[Ed Curtis]].  The proof that it works was never published.)

## Examples

+-- {: .num_example}
###### Example


For $X = S^2$ the [[2-sphere]], consider the following two [[elements]] of its [[homotopy groups]] ([[homotopy groups of spheres|of spheres]], as it were):

1. $id_{S^2} \in \pi_2\big( S^2 \big)$ (represented by the [[identity function]] $S^2 \to S^2$)

1. $h_{\mathbb{C}} \in \pi_3\big(  S^3 \big)$ (represented by the [[complex Hopf fibration]])

Then the Whitehead product satisfies

$$
  \big[
    id_{s^2},
    \; 
    id_{S^2}
  \big]
  \;=\;
  2 \cdot h_{\mathbb{C}}
  \,.
$$

=--


\linebreak

## References

### General

Named after [[J. H. C. Whitehead]].

The concept originates with

* {#HiltonWhitehead53} [[Peter Hilton]], [[J. H. C. Whitehead]], _Note on the Whitehead Product_, Annals of Mathematics Second Series, Vol. 58, No. 3 (Nov., 1953), pp. 429-442  ([jstor:1969746](https://www.jstor.org/stable/1969746))

* {#Hilton55} [[Peter Hilton]], _On the homotopy groups of unions of spheres_, J. London Math. Soc., 1955, 30, 154–172 ([[Hilton55.pdf:file]])


See also 

* Wikipedia _[Whitehead product](http://en.wikipedia.org/wiki/Whitehead_product)_

Discussion of Whitehead products specifically of [[homotopy groups of spheres]]:

* {#James56} [[Ioan Mackenzie James]], _On the Suspension Triad_, Annals of Mathematics Second Series, Vol. 63, No. 2 (Mar., 1956), pp. 191-247 ([arXiv:1969607](https://www.jstor.org/stable/1969607))

* {#James57} [[Ioan Mackenzie James]], _On the Suspension Sequence_, Annals of Mathematics Second Series, Vol. 65, No. 1 (Jan., 1957), pp. 74-107 ([arXiv:1969666](https://www.jstor.org/stable/1969666))


Discussion of Whitehead products in [[homotopy type theory]]:

* [[Guillaume Brunerie]], section 3.3 of _On the homotopy groups of spheres in homotopy type theory_ ([arXiv:1606.05916](https://arxiv.org/abs/1606.05916))


### In rational homotopy theory
  {#ReferencesInRationalHomotopyTheory}

Discussion of Whitehead products in [[rational homotopy theory]]:

* {#Quillen69} [[Daniel Quillen]], section I.5 of _Rational Homotopy Theory_, Annals of Mathematics Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](https://www.jstor.org/stable/1970725))


* Christopher Allday, _Rational Whitehead products and a spectral sequence of Quillen_, Pacific J. Math. Volume 46, Number 2 (1973), 313-323 ([euclid:1102946308](https://projecteuclid.org/euclid.pjm/1102946308))

* Christopher Allday, _Rational Whitehead product and a spectral sequence of Quillen, II_, Houston Journal of Mathematics, Volume 3, No. 3, 1977 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.434.8821&rep=rep1&type=pdf))

* [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]], _Real homotopy theory of Kähler manifolds_, Invent Math (1975) 29: 245 ([doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853))

* Peter Andrews, Martin Arkowitz, _Sullivan's Minimal Models and Higher Order Whitehead Products_, Canadian Journal of Mathematics, 30(5), 961-982, 1978 ([doi:10.4153/CJM-1978-083-6](https://doi.org/10.4153/CJM-1978-083-6))

* Francisco Belchí, [[Urtzi Buijs]], José M. Moreno-Fernández, Aniceto Murillo, _Higher order Whitehead products and $L_\infty$ structures on the homology of a DGL_, Linear Algebra and its Applications, Volume 520 (2017), pages 16-31 ([arXiv:1604.01478](https://arxiv.org/abs/1604.01478))
    


* Takahito Naito, _A model for the Whitehead product in rational mapping spaces_ ([arXiv:1106.4080](https://arxiv.org/abs/1106.4080))


[[!redirects Whitehead products]]