
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Contex
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _free category_ on a "set of arrows", hence on a [[directed graph]], is the ([[strict category|strict]]) [[category]] whose 

* [[objects]] are the [[vertices]] of the graph

* [[morphisms]] are the [[tuples]] of [[composition|composable]] [[edges]], hence the morphisms [[free construction|freely generated]] from these (directed) edges. 

  These morphisms may also be thought of as the "paths" that one may trace out in the directed graph by traversing in each step along an arrow, and therefore free categories are also called _[[path categories]]_.

{#MorePrecisely} More formally, there is a [[forgetful functor]] $U$ from the [[1-category]] [[Cat|$Cat^{strct}_{smll}$]] of [[small categories|small]] [[strict categories]] (and [[functors]] between them) to that of [[directed graphs]] (assigning the [[underlying]] graph of morphisms, i.e. forgetting the [[composition]]-operation); and the free category construction is the [[left adjoint]] $F$ to this functor:

$$
  Cat^{strct}_{smll}
  \underoverset
    {\underset{U}{\longrightarrow}}
    {\overset{F}{\longleftarrow}}
    {\;\;\bot\;\;\;}
  DiGrph
$$

{#FreeGroupoid} Often this is considered in [[composition]] with the "localization" functor that constructs the [[free groupoid]] on a given category:

$$
  Grpd^{strct}_{smll}
  \underoverset
    {\underset{U_{Grpd}}{\longrightarrow}}
    {\overset{F_{Grpd}}{\longleftarrow}}
    {\;\;\bot\;\;\;}
  Cat^{strct}_{smll}
  \underoverset
    {\underset{U_{Cat}}{\longrightarrow}}
    {\overset{F_{Cat}}{\longleftarrow}}
    {\;\;\bot\;\;\;}
  DiGrph
$$

(which relates to the [[Milnor construction]], see [Goerss & Jardine (2009), V.7](Dwyer-Kan+loop+groupoid#GoerssJardine09))

## Related concepts

* [[free groupoid]], [[core groupoid]]

* [[free diagram]]

* [[free monoid]], [[free operad]]

* [[free topos]]


## References

This notion of  *free category on a graph* has a section on it in

* [[Francis Borceux]], _Handbook of categorical Algebra vol. 1_ , Cambridge UP 1994.

and also in 

* {#MacLane} [[Saunders MacLane]], _[[Categories for the Working Mathematician]]_ , Springer 1998.

The following is another source for this, even an open source:

* {#BarrWells}[[Michael Barr]] and [[Charles Wells]], _Category Theory for Computing Science_ [PDF](http://www.math.mcgill.ca/triples/Barr-Wells-ctcs.pdf)

The path categories of context free grammars are explored in

* {#Latch} Dana Latch, _The connection between the fundamental groupoid and a unification algorithm for syntactil algebras (extended abstract)_ , Cah. Top. G&#233;om. Diff. Cat. **XXXII** (1991).  ([link](http://www.numdam.org/item?id=CTGDC_1991__32_3_203_0))

* {#Walters1} [[Bob Walters]], _The free category with products on a multigraph_ , JPAA **62** (1989). ([link](http://www.sciencedirect.com/science/article/pii/0022404989901527))

* {#Walters2} [[Bob Walters]], _A note on context-free languages_ , JPAA **62** (1989). ([link](http://www.sciencedirect.com/science/article/pii/0022404989901515))

Since the perspective on categories as 'graphs with operations' is closely related to their 'logico-deductive' side, it figures prominently in the work of [[Jim Lambek]] and [[Phil Scott]] (cf. the references at [[free topos]]).





[[!redirects free categories]]

[[!redirects free category on a quiver]]
[[!redirects free categories on quivers]]
