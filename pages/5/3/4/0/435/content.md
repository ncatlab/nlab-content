
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* table of contents 
{:toc}

## Idea

A _simplicially enriched category_ is a [[category]] with a [[simplicial set]] of [[morphism]]s between any two objects. 

One may think of the 1-cells in a hom-simplicial set as a [[2-morphism]], the 2-cells as a [[3-morphism]] and generally a $(k-1)$-cell as a [[k-morphism]]. Therefore simplicially enriched categories may serves as models for [[∞-categories]]. Precisely which notion of $\infty$-category depends on which extra [[stuff, structure, property|structure and property]] one imposes.

For instance

* requiring the hom-simplicial sets to be [[Kan complex]]es makes simplicially enriched categories a model for [[(∞,1)-categories]];

* similary, equipping the $sSet$-enriched category with the structure of a $sSet_{Quillen}$-[[enriched model category]] -- a [[simplicial model category]] -- makes it a model for an $(\infty,1)$-category.

  This is discussed in more detail at [[relation between quasi-categories and simplicial categories]].

* on the other hand, equipping the $sSet$-enriched category with the structure of an $sSet_{Joyal}$-enriched model category over the Joyal-[[model structure for quasi-categories]] makes it a model for an [[(∞,2)-category]].
 

## Definition

+-- {: .un_defn}
###### Definition

A _simplicially enriched category_ is a [[enriched category|category enriched over]] the [[cartesian monoidal category]] [[sSet]] of [[simplicial sets]].

=--

+-- {: .un_remark}
###### Remark

These $sSet$-enriched categories are sometimes, somewhat imprecisely, called just _[[simplicial categories]]_.

=--

There is a related notion of [[simplicial groupoid]] with the added requirement that all arrows in the categories concerned are [[isomorphisms]].


## As models for $(\infty,1)$-categories 

Since simplicial sets that are [[Kan complex]]es are an incarnation of [[∞-groupoid]]s, an $sSet$-category all whose [[hom-object]]s happen to be [[Kan complex]]es may be regarded as a category enriched in [[∞-groupoid]]s. By the logic of [[(n,r)-category]] theory this should be a model for an [[(∞,1)-category]].

Treating simplicial categories this way as models for $(\infty,1)$-categories is one of the central tools in [[homotopy coherent category theory]].

Indeed, there is a [[model structure on simplicial categories]] whose fibrant objects are [[Kan complex|Kan-complex]]-enriched categories, and which is one model for the [[(∞,1)-category of (∞,1)-categories]].

By a web of [[Quillen equivalence]]s this is related to the other incarnations of $(\infty,1)$-categories. Notably to [[quasi-categories]] and [[complete Segal space]]s. For more on this see

* [[relation between quasi-categories and simplicial categories]].


### Properties

#### Simplicial localization

To every [[category with weak equivalences]] $(C,W)$ is associated its [[simplicial localization]] $L_W C$, which is an $sSet$-category with the property that its [[homotopy category of an (∞,1)-category]] coincides with the [[homotopy category]] $Ho_W(C)$.



#### Model structure

There is a [[model structure on sSet-categories]] that presents the [[(∞,1)-category]] [[(∞,1)Cat]].


#### Homotopy Kan extension

The notion of [[homotopy Kan extension]] and hence in particular that of [[homotopy limit]] and [[homotopy colimit]] has a direct formulation in terms of [[Kan complex|Kan-complex]]-enriched categories.  See [[homotopy Kan extension]] for more.

#### Presentation of $(\infty,1)$-topos theory

All of [[(∞,1)-topos theory]] can be modeled in terms of $sSet$-categories. ([To&#235;nVezzosi](#Toenvezzosie)). There is a notion of [[sSet-site]] $C$ that models the notion of [[(∞,1)-site]] and a [[model structure on sSet-enriched presheaves]] on $sSet$-sites that is a [[presentable (∞,1)-category|presentation]] for the [[∞-stack]] [[(∞,1)-topos]]es on $C$.



## As models for $(\infty,2)$-categories

See [[(∞,2)-category]].

## Related concepts

* [[simplicial category]]
  
  * **simplicially enriched category**

  * [[simplicial object in Cat]]

* [[simplicial groupoid]]

* [[relation between quasi-categories and simplicial categories]]

* [[topologically enriched category]]


## References
 {#References}

Discussion the context of ([[simplicial model category|simplicial]]) [[model category]] theory:

* {#Quillen67} [[Daniel Quillen]], II §1 of: *[[Homotopical Algebra]]*, Lecture Notes in Mathematics **43**, Springer (1967) &lbrack;[doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438)&rbrack;


* {#Hirschhorn02} [[Philip Hirschhorn]], Section 9.1.1 of: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* {#ToenVezzosi} [[Bertrand Toën]], [[Gabriele Vezzosi]], Section 2 of: *Topos theory*, Advances in Mathematics **193** 2 (2005) 257-372 &lbrack;[arXiv:0207028](http://arxiv.org/abs/math/0207028), [doi:10.1016/j.aim.2004.05.004](https://doi.org/10.1016/j.aim.2004.05.004)&rbrack;



* [[Jacob Lurie]], Section A.3 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

* [[Emily Riehl]], §3.6 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;


The original references in the context of [[simplicial localization]]:

* {#DwyerKanLocalizations} [[William Dwyer]], [[Daniel Kan]], _Simplicial localizations of categories_, J. Pure Appl. Algebra **17** 3 (1980), 267-284 &lbrack;<a href="https://doi.org/10.1016/0022-4049(80)90049-3">doi:10.1016/0022-4049(80)90049-3</a>&rbrack;

* {#DwyerKanEquivalences} [[William Dwyer]], [[Daniel Kan]], *Equivalences between homotopy theories of diagrams*, in: *Algebraic topology and algebraic K-theory*, Ann. of Math. Stud. **113**, Princeton University Pr
Simplicially enriched categories as models for $(\infty,1)$-categories are also discussed in


Homotopy coherent category theory on $sSet$-categories is discussed in 

*  [[Jean-Marc Cordier]] and [[Timothy Porter]], _Homotopy Coherent Category Theory_, Trans. Amer. Math. Soc. 349 (1997) 1-54, ([pdf](http://www.ams.org/journals/tran/1997-349-01/S0002-9947-97-01752-2/S0002-9947-97-01752-2.pdf))2-2.pdf))

which describes resolutions of the simplicial functor categories between two simplicial categories and

* [[Michael Batanin]], _Homotopy coherent category theory and $A_\infty$-structures in monoidal categories_ ([pdf](http://dodo.pdmi.ras.ru/~topology/books/batanin.pdf))

which shows that these resolved functor categories are in fact $sSet$-[[A-∞ categories]].


[[!redirects simplicially enriched category]]
[[!redirects simplicially enriched categories]]
[[!redirects sSet-enriched category]]
[[!redirects sSet-enriched categories]]
[[!redirects SSet-enriched category]]
[[!redirects SSet-enriched categories]]
[[!redirects SimpSet-enriched category]]
[[!redirects SimpSet-enriched categories]]
[[!redirects sSet-category]]
[[!redirects sSet-categories]]
[[!redirects SSet-category]]
[[!redirects SSet-categories]]
[[!redirects SimpSet-category]]
[[!redirects SimpSet-categories]]

