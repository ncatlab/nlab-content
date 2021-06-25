
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A *groupoid object* in an ambient [[category]] $\mathcal{C}$ is equivalently

* a [[groupoid]] [[internalization|internal]] to $\mathcal{C}$;

* an [[internal category]] in $\mathcal{C}$ equipped with an [[inverse]]-assigning morphism.

This notion is the [[horizontal categorification]] of that of a [[group object]].  

## Definitions

Let $C$ be a [[category with finite limits]], and let $\Grpd$ be the category of small [[groupoids]].   We can define groupoid objects representably:

+-- {: .un_defn}
###### Definition

A **groupoid object in** $C$ is a functor $F\colon C\to \Grpd$ such that

1. there is an object $g_0\in C_0$ such that there is a [[natural isomorphism]] $F(c)_0\simeq C(c,g_0)$

1. there is an object $g_1\in C_0$ such that there is a natural isomorphism $F(c)_1\simeq C(c,g_1)$
=--

We can also define them more explicitly:

+-- {: .un_defn}
###### Definition
A **groupoid object in** $C$ is an [[internal category]] $A$ such that there is an "inverse-assigning morphism" $i\colon A_1 \to A_1$ satisfying certain axioms...
=--

## Examples

* A groupoid in $\Top$ is a [[topological groupoid]].

* A groupoid in $\Diff$ is a [[Lie groupoid]].  (Note that $\Diff$ does not have all pullbacks, but by suitable conditions on the source and target map we can ensure that the requisite pullbacks do exist.)


## Related concepts

* [[monoid]], [[monoid object]], [[monoid object in an (∞,1)-category]]

* [[group]], **group object**, [[group object in an (∞,1)-category]]

* [[groupoid]], [[groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[infinity-groupoid]], [[infinity-groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[ring]], [[ring object]]

## References

The general definition of internal categories seems to have first been formulated in:

* {#Grothendieck61} [[Alexander Grothendieck]], p. 106 (9 of 21) of: [[FGA]] _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-III.pdf))

following the general principle of [[internalization]] formulated in

* {#Grothendieck60} [[Alexander Grothendieck]], p. 370 (3 of 23) in: [[FGA]] *Technique de descente et théorèmes d'existence en géométrie algébriques. II: Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195 ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/SB_1958-1960__5__369_0), [pdf](http://www.numdam.org/item/SB_1958-1960__5__369_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-II.pdf))

The concept of [[topological groupoids]] and [[Lie groupoids]] goes back to

* [[Charles Ehresmann]], _Catégories topologiques et categories différentiables_, Colloque de Géométrie différentielle globale, Bruxelles, C.B.R.M., (1959) pp. 137-150 ([[EhresmannCategoriesTopologiques.pdf:file]], [zbMath:0205.28202](https://zbmath.org/?q=an:0205.28202))

and their understanding as categories internal to [[TopologicalSpaces]] and to [[SmoothManifolds]] is often attributed to

* [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure, Série 3, Tome 80 (1963) no. 4, pp. 349-426 ([numdam:ASENS_1963_3_80_4_349_0](http://www.numdam.org/item/ASENS_1963_3_80_4_349_0))

but it seems that the definition is not actually contained in there, certainly not in its simple and widely understood form due to [Grothendieck 61](#Grothendieck61).

For more references see at *[[internal category]]* and *[[internalization]]*. 

[[!redirects groupoid objects]]

[[!redirects internal groupoid]]
[[!redirects internal groupoids]]

[[!redirects groupoid internal]]
[[!redirects groupoids internal]]

