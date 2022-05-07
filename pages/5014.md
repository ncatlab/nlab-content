

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### General

A **topological groupoid** is an [[internal groupoid]] in the [[category]] [[Top]].

So this is a [[groupoid]] with a [[topological space]] of [[object]]s and one of [[morphism]]s, and all structure maps (source, target, identity, composition, inverse) are [[continuous maps]]. Composition here refers to the map defined on the space of all composable morphisms. 


A topological groupoid $C$ is  called an **open topological groupoid** if the source map $s : Mor C \to Obj C$ is an [[open map]].

It is called an **[[étale groupoid]]** if in addition $s$ is a [[local homeomorphism]].


## Properties

### Relation to toposes

Every [[topos]] ([[Grothendieck topos]]) with [[point of a topos|enough points]] is the _[[classifying topos of a topological groupoid]]_. See there for more.

## Related entries

* [[Lie groupoid]]

* [[topological group]]

* [[topological stack]]

* [[amenable topological groupoid]]


## References

The notion of topological categories, hence of topological groupoids, goes back to 

* [[Charles Ehresmann]], _Catégories topologiques et categories différentiables_, Colloque de Géométrie différentielle globale, Bruxelles, C.B.R.M., (1959) pp. 137-150 ([[EhresmannCategoriesTopologiques.pdf:file]], [zbMath:0205.28202](https://zbmath.org/?q=an:0205.28202))

Their understanding as [[internal groupoids]] [[internalization|internal]] to [[TopologicalSpaces]] is often attributed to

* [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure, Série 3, Tome 80 (1963) no. 4, pp. 349-426 ([numdam:ASENS_1963_3_80_4_349_0](http://www.numdam.org/item/ASENS_1963_3_80_4_349_0))

but the simple notion of [[internalization]] and [[internal groupoids]] ([Grothendieck 1960](internalization#Grothendieck60), [61](internalization#Grothendieck61)) is hardly recognizable in this account.

Exposition:

* [[Alan Weinstein]], p. 6 of: _Groupoids: Unifying Internal and External Symmetry -- A Tour through some Examples_, Notices of the AMS volume 43, Number 7 (1996) ([pdf](http://www.ams.org/notices/199607/weinstein.pdf), [[Weinstein_Groupoids.pdf:file]])

Textbook account:

* [[Kirill Mackenzie]], Chapter II in: _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([doi:10.1017/CBO9780511661839](https://doi.org/10.1017/CBO9780511661839), [MR:896907](http://www.ams.org/mathscinet-getitem?mr=896907))

Many references on topological groupoids deal with them as models for [[topological stacks]], see there for more.

On topological groupoids as a model for [[orbispaces]]:

* {#Haefliger84} [[André Haefliger]], _Groupoides d'holonomie et classifiants_, Astérisque no. 116  (1984), p. 70-97 ([numdam:AST_1984__116__70_0](http://www.numdam.org/item/?id=AST_1984__116__70_0))

* {#Haefliger91} [[André Haefliger]], _Complexes of Groups and Orbihedra_, in: E. Ghys, A. Haefliger, A Verjovsky (eds.), _Proceedings of the Group Theory from a Geometrical Viewpoint_, ICTP, Trieste, Italy , 26 March – 6 April 1990, World Scientific 1991 ([doi:10.1142/1235](https://doi.org/10.1142/1235))

On topological groupoids as presenting [[toposes]] with [[point of a topos|enough points]]:

* [[Carsten Butz]], [[Ieke Moerdijk]], *Representing topoi by topological groupoids*, Journal of Pure and Applied Algebra Volume 130, Issue 3, 17 September 1998, Pages 223-235 (<a href="https://doi.org/10.1016/S0022-4049(97)00107-2">doi:10.1016/S0022-4049(97)00107-2</a>)

On [[exponential objects]] among [[topological groupoids]]:

* [[Susan B. Niefield]], [[Dorette A. Pronk]], *Internal groupoids and exponentiability*, Cahiers de topologie et géométrie différentielle catégoriques, [**LX** 4 (2019)](http://cahierstgdc.com/index.php/volume-lx/) ([pdf](http://cahierstgdc.com/wp-content/uploads/2019/10/Niefield-Pronk-LX-4.pdf))




[[!redirects topological groupoids]]

[[!redirects open topological groupoid]]
[[!redirects open topological groupoids]]

