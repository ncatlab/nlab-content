
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The [[integrability of G-structures]] exists to first order, precisely if a certain [[torsion]] [[obstruction]] vanishes. This is the first in an infinite tower of tensor invariants in [[Spencer cohomology]] associated with a $G$-structure that obstruct its integrability (local flatness) ([Guillemin 65](#Guillemin65)).


The _torsion of a $G$-structure_ is defined to be the space in which the invariant part of the [[torsion of a Cartan connection]] takes values, for any [[Cartan connection]] compatible with the $G$-structure (see at _[Cartan connection -- Examples -- G-Structure](Cartan%20connection#ExampleGStructures)_) ([Sternberg 64, from p. 317 on](#Sternberg64), [Guillemin 65, section 4](#Guillemin65)), for review see also ([Lott 90, p.10](#Lott90), [Joyce 00, section 2.6](#Joyce00)).

The order $k$-torsion of a $G$-structure (counting may differ by 1) is an element in a certain [[Spencer cohomology]] [[cohomology group|group]] ([Guillemin 65, prop. 4.2](#Guillemin65)) and is the [[obstruction]] to lifting an order-$k$-[[integrable G-structure]] to order $k+1$ ([Guillemin 65, theorem 4.1](#Guillemin65)).


## Related concepts

* [[torsion of a Cartan connection]]

## References

### General

Historical origin of the notion in [[Cartan geometry]]:

* {#Cartan22} [[Élie Cartan]], *Sur une généralisation de la notion de courbure de Riemann et les espaces á torsion*, C. R. Acad. Sci. **174** (1922) 593-595 .

* {#Cartan23} [[Élie Cartan]], *Sur les variétés à connexion affine et la théorie de la relativité généralisée (première partie)*, Annales scientifiques de l’École Normale Supérieure, Sér. 3, **40** (1923) 325-412 \[<a href="http://www.numdam.org/item?id=ASENS_1923_3_40__325_0">doi:ASENS_1923_3_40__325_0</a>\]

Historical review:

* [[Erhard Scholz]], *E. Cartan’s attempt at bridge-building between Einstein and the Cosserats – or how translational curvature became to be known as "torsion"*, The European Physics Journal H **44** (2019) 47-75 \[<a href="https://doi.org/10.1140/epjh/e2018-90059-x">doi:10.1140/epjh/e2018-90059-x</a>\]


Textbook accounts include

* {#Sternberg64} [[Shlomo Sternberg]], section VII of _Lectures on differential geometry_, Prentice Hall 1964; Russian transl. Mir 1970

Discussion including the higher order obstructions in [[Spencer cohomology]] to [[integrability of G-structures]] is in

* {#Guillemin65} [[Victor Guillemin]], _The integrability problem for $G$-structures_, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([jstor:1994134](http://www.jstor.org/stable/1994134))


Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion with an eye towards [[special holonomy]] is in

* {#Joyce00} [[Dominic Joyce]], section 2.6 of _Compact manifolds with special holonomy_, Oxford University Press 2000

Further mentioning of the higher order torsion invariants includes

* {#Bryant05} [[Robert Bryant]], section 4.2 of _Some remarks on $G_2$-structures_, Proceedings of the 12th G&#246;kova Geometry-Topology Conference 2005, pp. 75-109 [pdf](http://gokovagt.org/proceedings/2005/ggt05-bryant.pdf)

Discussion specifically for kinematical groups:

* [[José Figueroa-O'Farrill]], _On the intrinsic torsion of spacetime structures_ ([arXiv:2009.01948](https://arxiv.org/abs/2009.01948))


See also

* Wikipedia, _[Torsion of a G-structure](https://en.wikipedia.org/wiki/G-structure#Torsion_of_a_G-structure)_

Formalization in [[homotopy type theory]] (so far only for infinite-order torsion):

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_ (2017)



[[!include Cartan structural equations and Bianchi identities -- references]]


[[!redirects torsion of G-structures]]


[[!redirects torsion invariants of G-structures]]