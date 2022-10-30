
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Indexed monoidal categories
* table of contents
{: toc}

## Definition

### Index monoidal category

An **indexed monoidal category** is a kind of [[indexed category]], consisting of a base [[category]] $S$ and a [[pseudofunctor]] $S^{op} \to MonCat$ to the [[2-category]] of [[monoidal categories]] and [[strong monoidal functors]] between them. We write this as $A\mapsto (C^A, \otimes_A, I_A)$.  

By the usual [[Grothendieck construction]], this pseudofunctor can be regarded as a [[fibration]].  And if $S$ has [[finite products]], then the "fiberwise" monoidal structures $\otimes_A$ can also be "Grothendieckified" into an "[[external tensor product]]"
$$ \boxtimes\colon C^A \times C^B \to C^{A\times B}$$
defined by $M\boxtimes N = \pi_2^\ast M \otimes_{A\times B} \pi_1^\ast N$.  This makes the total category of the fibration a [[monoidal category]] and the fibration itself a strong [[monoidal functor]] (where $S$ is regarded as equipped with its [[cartesian monoidal category|cartesian monoidal structure]]); this is called a **[[monoidal fibration]]**.  Moreover, we can recover $\otimes_A$ from $\boxtimes$ via $M\otimes_A N = \Delta_A^\ast (M\boxtimes N)$, so the two structures have the same information. ([Shulman 08](#Shulman08)).

### Indexed closed monoidal category
 {#Closed}

If all the fibers are not just monoidal but [[closed monoidal categories]] and the [[base change]] morphisms are not just strong monoidal but also strong [[closed monoidal functors]], then the indexed monoidal category is an indexed _closed monoidal category_ ([Shulman 08, def. 13.1](#Shulman08), [Shulman 12, theorem 2.14](#Shulman12)).

If in addition all fibers are [[symmetric monoidal category|symmetric monoidal]] one might also call this a system of [[Wirthmüller contexts]] of [[six operations]]. If furthermore all fibers have all [[dual objects|duals]], then this is also what should be called [[categorical semantics]] for [[dependent linear type theory]].


## Examples

* $S=Sets$, $C^A=$ $A$-indexed families of objects of $C$, for any monoidal category $C$.
* $S=Gpd$, $C^A=$ $A$-diagrams of objects of $C$
* $S=$ any category with pullbacks, $C^A = S/A$
* $S=Top$, $C^A=$ [[parametrized spectra]] over $A$
* $S=Grp$ or $TopGrp$, $C^A=$ sets or spaces with an action by $A$
* The homotopy category of any of the above equipped with a homotopy theory

In many cases, the reindexing functors $f^\ast\colon C^B \to C^A$ induced by a morphism $f\colon A\to B$ in $S$ all have left adjoints $f_!$.  If these left adjoints satisfy the [[Beck-Chevalley condition]] for all pullback squares in $S$, then the indexed category is traditionally said to have **indexed coproducts**.  For many applications, though, we only need this condition for a few pullback squares, which coincidentally (?) happen to be those that are pullbacks in any category with finite products (whether or not it even has all pullbacks).




## Related concepts

* [[external tensor product]]

* [[dependent linear type theory]], [[Wirthmüller context]]

## References

The definition is due to

* {#Shulman08} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))
 

Discussion of [[traces]] and of [[dual objects]] in indexed monoidal categories is in

* [[Kate Ponto]], [[Mike Shulman]], _Duality and traces in indexed monoidal categories_, ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555),  [blog](http://golem.ph.utexas.edu/category/2011/11/traces_in_indexed_monoidal_cat.html))

This also presents a [[string diagram]] calculus for indexed monoidal categories, extending that for monoidal [[hyperdoctrines]] in 

* {#BradyTrimble98} Geraldine Brady, [[Todd Trimble]], _[[A string diagram calculus for predicate logic]]_ (1998)

Generalization to [[enriched categories]] is in

* {#Shulman12} [[Mike Shulman]], _Enriched indexed categories_ ([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))
 


[[!redirects indexed monoidal category]]
[[!redirects indexed monoidal categories]]

[[!redirects indexed closed monoidal category]]
[[!redirects indexed closed monoidal categories]]