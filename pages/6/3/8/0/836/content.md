
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



# $2$-posets
* table of contents
{: toc}


A **2-poset** is any of several concepts that generalize ([[categorify]]) the notion of [[partial order|posets]] one step in [[higher category theory]]. One does not usually hear about $2$-posets by themselves but instead as special cases of [[2-category|$2$-categories]], such as the [[locally posetal 2-category|locally posetal]] ones.

$2$-posets can also be called **(1,2)-categories**, being a special case of [[(n,r)-categories]].  The concept generalizes to [[n-poset|$n$-posets]].


## Definition

### Explicit definition

A **2-poset** is a [[category]] $C$ such that 

1. For each object $A:Ob(C)$ and $B:Ob(C)$, there is a binary relation $\leq_{A, B}$ on $Hom(A, B)$ 
2. For each object $A:Ob(C)$ and $B:Ob(C)$ and morphism $R:Hom(A, B)$, $R \leq_{A, B} R$. 
3. For each object $A:Ob(C)$ and $B:Ob(C)$ and morphism $R:Hom(A, B)$, $S:Hom(A, B)$, $T:Hom(A, B)$, $R \leq_{A, B} S$ and $S \leq_{A, B} T$ implies $R \leq_{A, B} T$. 
4. For each object $A:Ob(C)$ and $B:Ob(C)$ and morphism $R:Hom(A, B)$, $S:Hom(A, B)$, $R \leq_{A, B} S$ and $S \leq_{A, B} R$ implies $R = S$. 

$C$ is only a **2-proset** if $C$ only satisfies 1-3. 

### From infinity-categories

Fix a meaning of $\infty$-[[infinity-category|category]], however weak or strict you wish. Then a __$2$-poset__ is an $\infty$-category such that all parallel pairs of $j$-morphisms are [[equivalence|equivalent]] for $j \geq 2$. Thus, up to [[equivalence of categories|equivalence]], there is no point in mentioning anything beyond $2$-morphisms, not even whether two given parallel $2$-morphisms are equivalent. This definition may give a concept more general than a locally posetal $2$-category for your preferred definition of $2$-category, but it will be equivalent if you ignore irrelevant data.


## Examples

* [[Pos]]
* [[Rel]]
* [[simplex category]]
* [[Lat]]
* [[DistLat]]
* [[Frm]]
* [[Locale]]
* [[HeytAlg]]
* [[BoolAlg]]

* [[allegory]]
* [[bicategory of relations]]
* [[first-order hyperdoctrine with equality]]

Just as the motivating example of a $2$-category is the $2$-category [[Cat]] of categories, so the motivating example of a $2$-poset is the $2$-poset [[Pos]] of posets.

## Related concepts

* [[dagger 2-poset]]

* [[n-poset]]

  * [[poset]]

  * **2-poset**


[[!redirects 2-posets]]
[[!redirects 2-proset]]
[[!redirects 2-prosets]]
[[!redirects (1,2)-category]]
[[!redirects (1,2)-categories]]
[[!redirects locally ordered 2-category]]
[[!redirects locally ordered 2-categories]]
[[!redirects locally ordered]]
