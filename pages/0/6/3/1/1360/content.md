
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A _simplicial model category_ is a model or presentation for an [[(∞,1)-category]] that is half way in between a bare [[model category]] and a [[Kan complex]]-[[enriched category]].

Specifically, a simplicial model category is an [[SSet]]-[[enriched category]] $C$ together with the structure of a [[model category]] on its underlying [[category]] $C_0$ such that both structures are compatible in a reasonable way.

One important use of simplicial model categories comes from the fact that the full [[SSet]]-subcategory $C^\circ \hookrightarrow C$ on the fibrant-cofibrant objects -- which is not just [[SSet]]-enriched but actually [[Kan complex]]-enriched -- is the [[(∞,1)-category]]-enhancement of the [[homotopy category]] of the [[model category]] $C_0$.

For generalizations of this construction with [[SSet]] replaced by another [[monoidal model category]] see [[enriched homotopical category]].



#Definition#

A **simplicial model category** is an [[enriched model category]] which is enriched over [[SSet]].


This means that a simplicial model category is

* an [[SSet]]-[[enriched category]]

  * which is [[power]]ed and [[copower]]ed over [[SSet]]

* with the structure of a [[model category]] on the underlying category $C_0$

* such that for every cofibration $i : A \to B$ and every fibration $p : X \to Y$ in $C_0$ the morphism of [[simplicial set]]s $C(B,X) \stackrel{i^* \times p_*}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)$ is a fibration;

* and such that this fibration is an acyclic fibration whenever either $i$ or $p$ are acyclic.

#Examples#

* The most well-developed model/presentation for the [[hypercompletion]] of the [[(∞,1)-category of (∞,1)-sheaves]] on an ordinary (i.e. 1-categorical) [[site]] $S$ is the [[Kan complex]]-[[enriched category]] $C^\circ \hookrightarrow C$ for $C = [S^{op}, SSet]$ the simplicial model category of [[simplicial presheaves]] on $S$ equippped with the [[model structure on simplicial presheaves]].



#References#

section 9.1.5 of

* Hirschhorn, _Model categories and their localization_

section A.3 in

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects simplicial model categories]]