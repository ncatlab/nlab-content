#Contents#
* automatic table of contents goes here
{:toc}

## Gluing of quasicoherent sheaves via localizations

The [[quasicoherent sheaves]] have natural analogues in some formalisms of [[noncommutative algebraic geometry]]. The Zariski open sets generalize to some nice class of flat localizations, and then one can consider faithfully flat descent. However the analogues of a cover and sheaf condition are more subtle.

Let $A$ be an [[abelian category]] and $\{B_\lambda\}_{\lambda\in\Lambda}$ a finite family of abelian categories; and $Q^*_\lambda : A\to B_\lambda$ exact localization functors having fully faithful right adjoints $Q_{\lambda *}:B_\lambda\to A$. We say that the family ${Q_{\lambda *}}_{\lambda\in\Lambda}$ is conservative if a morphism in $A$ is invertible iff $Q_{\lambda *}(f)$ is invertible for each $\lambda$. 

There is a standard way to construct a [[comonad]] $G$ on the product category $\prod_\lambda B_\lambda$. Under the conditions of a comonadic version of Barr's monadicity theorem one can reconstruct $A$ as the category equivalent to the category of $G$-comodules. 

For Gabriel localizations of categories of modules over rings, such a gluing theorem, called "globalization theorem" is in A. Rosenberg's 1988 Stockholm book and obtained independently in Willaert-van Oystaeyen 1995 article, in both cases proved by nontrivial localization theory. Applying [[comonadicity theorems]] is much more straightforward.

On the other hand the family of all cocovers (conservative families) by flat localizations and the family of all nice localizations do not have as good properties as the families of open sets and covers in topology. For example, the intersection operation on open sets is commutative, while the consecutive application of two localization functors depends on the order among the two in general. For example, the [[Ore localization]] of a ring $R$ on a left Ore subset $S\subset S^{-1}R$ is a ring; but the localization of that localized ring $S^{-1}R$ by applying the localization functor for another Ore subset $T\subset R$ is $T^{-1}R\otimes_R S^{-1} R$ which is not necessarily a ring in a natural way. In fact it has a canonical structure of a ring exactly in the case when the two Ore localization functors commute as functors on the original category of left modules over $R$. The considerations of this compatibility of localization functors has been studied in the language of torsion theories by Verschoeren and van Oystaeyen in 1970s. In fact, this situation is akin to semiseparatedness condition on schemes introduced by Thomason-Trobaugh: a scheme is semiseparated if it has an affine cover where the intersection of any two affines is again affine. Every separated scheme is semiseparated. Examples of [[noncommutative scheme]]s are rarely semiseparated in the sense of cocovers by flat localizations: for example most quantum flag varieties are not semiseparated. 

Another problem is that the family of all cocovers by flat  localizations (even for the categories of modules) is typically not a Grothendieck cotopology: in the dual language of topologies the stability axiom fails, even if one modifies the notion of the pullback form categorical product to the dual of the operation of meet for torsion theories. In terms of torsion theories, this stems from the fact that the lattice of torsion theories is not a distributive lattice. 

* Z. &#352;koda, _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276).

## Flat descent for modules over rings

For the purposes of the descent for modules over rings, comonads can be replaced by [[corings]]. Alternatively the descent data can be represented by connections for the Amitsur complex. Symmetries are important in that analysis.

* P. Nuss, Noncommutative descent and non-abelian cohomology,  $K$-Theory  12  (1997),  no. 1, 23--74. 

* T. Brzezi&#324;ski, R. Wisbauer, Corings and comodules, London Math. Soc. Lec. Note Series 309, Cambridge 2003.

* C. Menini, D. &#350;tefan, Descent theory and Amitsur cohomology of triples, 
J. Algebra 266 (2003), no. 1, 261--304. 

## Galois descent

In noncommutative case, the faithfully flat descent along torsor (equivalence of the $G$-equivariant quasicoherent sheaves on the $G$-scheme $X$ and the quasicoherent sheaves on $X/G$) is well understood when the group is replaced by )the opposite) to a [[Hopf algebra]] and when the base and total noncommutative schemes are affine. This is the case of Hopf-Galois descent and generalizations for entwinings. One can combine this vertical descent with the horizontal descent on localizations, provided the localizations are compatible with the coactions of the Hopf algebra. 

Coring language is also very natural in generalizing the Galois theory to noncommutative rings. 

## Nonflat descent

Unlike the descent for the categories of quasicoherent sheaves, where apart from semiseparatedness, the descent problem has a natural solution (say in comonadic language) the descent for affine schemes fails. In that case, Grothendieck essentially used the symmetry in commutative case. Another problem is that localizations are hard to find, especially very noncommutative rings (roughly those of infinite Gelfand-Kirillov dimensions) do not have nice covers by flat localizations. Cohn localizations sometimes work but they are not flat; therefore the descent has to be replaced by some sort of nonflat descent, for example the descent at the [[derived algebraic geometry|derived]] level.
That kind of analogues are not really noncommutative schemes as they are not locally affine in Zariski-like (=faithfully flat by localizations) topology.

## Gluing for sheaves of sets on $NAff$

Yet another question is how to generalize the functor of points approach to [[schemes]] and locally affine spaces in some Grothendieck topology on $Aff$ (or $Aff/S$) to the noncommutative setup. Rosenberg for that reason introduced considerations of sheaves on/in [[Q-categories]] which can be used to define noncommutative algebraic spaces of various kinds in functor of points approach. In some cases, like noncommutative smooth topology (Kontsevich-Rosenberg) usual Grothendieck topologies on $NAff$ suffice. 





