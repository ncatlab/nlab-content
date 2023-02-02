
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[localization]] is a universal functor from a given category $C$ with respect to the inversion of some family $\Sigma$ of morphisms in $C$; sometimes one says also quotient category. In topos theory and some other subjects one often restricts to the situation when $\Sigma$ is a [[calculus of left fractions]], and the corresponding localization functor has a [[right adjoint]] (which is then necessarily fully faithful); even more, one often requires that the localization functor is also [[left exact]], hence [[exact functor|exact]]. 

One may then speak of _colocalization_ as the [dual](duality#abstractformalaxiomatic_duality) version of localization, a universal functor into a quotient category where now $\Sigma$ admits a [[calculus of right fractions]] and the corresponding quotient functor has a [[left adjoint]].  See also at _[[right Bousfield localization]]_.


The theory of colocalization in [[co-Grothendieck categories]] has some features of its own as compared to the localization in [[Grothendieck categories]]. Namely, while by Gabriel-Popescu's theorem, every Grothendieck category is a localization of a category of modules over a fixed unital ring, their dual categories may be presented
in terms of the theory of linear topological rings with some compactness properties, which is the content of [[Gabriel-Oberst duality]] theory. 

## Related concepts

* [[right Bousfield delocalization]]

## References

* C. N&#259;st&#259;sescu, B. Torrecillas, _Colocalization on Grothendieck categories with applications to coalgebras_, J. Algebra __185__ (1996), 108&#8211;124 ([pdf](http://www.sciencedirect.com/science/article/pii/S0021869396903154))

A textbook exposition is in the chapter 6, _Duality_ of

* [[Nicolae Popescu]], _Abelian categories with applications to rings and modules_, London Math. Soc. Monographs 3, Academic Press 1973. xii+467 pp. [MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)

In derived and triangulated categories:

* Shoham Shamir, _Colocalization functors in derived categories and torsion theories_, [arxiv/0910.4724](http://arxiv.org/abs/0910.4724)
* Hvedri Inassaridze, Tamaz Kandelaki, Ralf Meyer, _Localisation and colocalisation of triangulated categories at thick subcategories_, [arxiv/0912.2088](http://arxiv.org/abs/0912.2088)

category: algebra
[[!redirects colocalisation]]