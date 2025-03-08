
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

**Cat** is a name for the [[category]] or [[2-category]] of all [[category|categories]].  

This is also the archetypical [[2-topos]].

## Definition

To avoid set-theoretic problems related to [[Russell's paradox]], it is typical to restrict $Cat$ to [[small category|small categories]].  But see [[CAT]] for alternatives.

To be explicit, define **Cat** to be the category with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]];

* composition of morphisms the evident composition of functors.


This is probably the most common meaning of $Cat$ in the literature.

We more often use **Cat** to stand for the [[strict 2-category]] with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].
* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here the [[vertical composition]] of 2-morphisms is the evident composition of component maps of natural transformations, whereas the [[horizontal composition]] is given by their [[Godement product]].


Finally, we can use **Cat** for the [[bicategory]] with:

* [[small category|small categories]] as [[object|objects]],
* [[anafunctor|anafunctors]] as [[morphism|morphisms]].
* [[ananatural transformation|ananatural transformations]] as [[2-morphism|2-morphisms]].

To be really careful, this version of $Cat$ is an [[anabicategory]].

## Properties

### Cartesian closed structure 
 {#CartesianClosedStructure}

The category $Cat$, at least in its traditional version comprising small categories only, is [[cartesian closed]]: the [[exponential objects]] are [[functor categories]].  Direct proofs can be found in:

* p. 98 of [[Categories Work]], 2nd ed.
* remark below Definition 4.3.9 in [[Category Theory in Context]]
* [[Steve Awodey]], *Category Theory*, Second Edition, Sections 7.5-7.7.

A more indirect proof could proceed by identifying $Cat$ via the [[nerve]] construction as a [[reflective subcategory]] of [[sSet]], which is cartesian closed as it is a [[presheaf category]], and showing that this subcategory is an [[exponential ideal]].

### Size issues

As a $2$-category, $Cat$ could even include (some) [[large category|large categories]] without running into Russell's paradox.  More precisely, if $U$ is a [[Grothendieck universe]] such that $\Set$ is the category of all $U$-small sets, then you can define $\Cat$ to be the 2-category of all $U'$-small categories, where $U'$ is some Grothendieck universe containing $U$.  That way, you have $\Set \in \Cat$ without contradiction.  (This can be continued to [[higher category theory|higher categories]].)

By the [[axiom of choice]], the two definitions of $Cat$ as a $2$-[[2-category|category]] are [[equivalence of categories|equivalent]].  In contexts without choice, it is usually better to use anafunctors all along; if necessary, use $Str Cat$ for the strict $2$-category.  Even without choice, a functor or anafunctor between categories is an [[equivalence]] in the anabicategory $Cat$ iff it is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  However, the weak inverse of such a functor may not be a functor, so it need not be an equivalence in $Str Cat$.  We can regard $Cat$ as obtained from $Str Cat$ using [[homotopy theory]] by "formally inverting" the essentially surjective and fully faithful functors as [[weak equivalences]].


### Limits and colimits

\begin{remark}\label{OrdinaryLimitsAndColimits}
*(ordinary limits and colimits of categories)*
\linebreak
  The [[1-category]] [[Cat]] of [[small categories]] is [[bicomplete category|bicomplete]]:

1. The [[limit]] of a [[diagram]] $\mathcal{C}_{(-)} \,\colon\, I \to Cat$ is computed componentwise: the sets of objects and of morphisms of the limiting category $\underset{\longleftarrow}{\lim} F$ are the limits in [[Set]] of $Obj(\mathcal{C}_{(-)}) \,\colon\, I \to Set$ and of $Mor(\mathcal{C}_{(-)}) \,\colon\, I \to Set$, respectively, equipped with the universally induced structure maps.

1. The [[colimit]] of a [[diagram]] $\mathcal{C}_{(-)} \,\colon\, I \to Cat$ is on [[objects]] still the colimit of the underlying diagram of sets of objects, but on morphisms it is more complicated, since in the naive colimit of sets of morphisms some morphisms may become composable that were not composable before.

   An exception is the case of [[coproducts]] of categories, which are just given componentwise by [[disjoint union]]. With this, it is (by [this Prop](colimit#ColimitsInTermsOfCoequalizers)) sufficient that [[coequalizers]] of functors exist. 

   Explicit formulas for coequalizers of categories are given in [Bednarczyk, Borzyszkowski & Pawlowski 1999, §4](#BednarczykBorzyszkowskiPawlowski99). 

   Moreover, formulas for [[pushouts]] in [[Cat]] of injective functors are discussed in [MacDonald & Scull 2009](#MacdonalScull09).

\end{remark}


See also discussion at [MO:q/272479](https://math.stackexchange.com/q/272479/58526).




## Related concepts

* [[elementary theory of the category of categories]]

* [[canonical model structure on Cat]]

[[!include categories of categories - contents]]


## References

The structure of the [[2-category]] of categories ([[vertical composition]], [[horizontal composition]] and [[whiskering]] of [[natural transformations]]) was first described in:

* {#Godement58} [[Roger Godement]], Appendix (pp. 269) of: *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

(towards the goal of describing the [[standard resolution]] of [[abelian sheaves]]).

Dedicated discussion in the spirit of [[formal category theory]]:

* {#Law66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp. 1-20 in: [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

* [[John Gray]], _[[Adjointness for 2-Categories|Formal category theory: adjointness for 2-categories]]_, Lecture Notes in Mathematics, **391**, Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack;


See also most references at _[[category]]_ and at _[[category theory]]_, such as:

* [[Horst Schubert]], §3 in: *Categories*, Springer (1972) &lbrack;[doi:10.1007/978-3-642-65364-3](https://doi.org/10.1007/978-3-642-65364-3)&rbrack;

  > (with size issues dealt with via [[Grothendieck universes]])

* [[Saunders MacLane]], §II.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

  > (size issues ignored by considering only the category of [[small categories]])


On [[colimits]] in the [[1-category]] of small categories:

[[coequalizers]]:

* {#BednarczykBorzyszkowskiPawlowski99} [[Marek A. Bednarczyk]], [[Andrzej M. Borzyszkowski]], [[Wieslaw Pawlowski]], Section 4 of: *Generalized congruences -- epimorphisms in $\mathcal{C}at$*, Theory and Applications of Categories **5** 11 (1999) 266-280 &lbrack;[tac:5-11](http://www.tac.mta.ca/tac/volumes/1999/n11/5-11abs.html), [dml:120226](https://eudml.org/doc/120226?lang=fr&limit=5)&rbrack;


certain [[pushouts]]:

* {#MacdonalScull09} [[John MacDonald]], [[Laura Scull]], _Amalgamations of categories_, Canad. Math. Bull. **52** 2 (2009) 273–284 &lbrack;[pdf](http://faculty.fortlewis.edu/Scull_L/pushouts.pdf), journal:[pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/A414F5D3FA9FB08ACBBB72143C70FE28)&rbrack;

Proof that the [[funny tensor product]] of [[categories]] is the only other [[symmetric closed monoidal category|symmetric closed monoidal structure]] on [[Cat]] besides the [[cartesian monoidal category|cartesian monoidal structure]]:

* {#FoltzLairKelly80} [[François Foltz]], [[Christian Lair]], [[G. M. Kelly]], *Algebraic categories with few monoidal biclosed structures or none*, Journal of Pure and Applied Algebra **17** 2 (1980) 171-177 &lbrack;[pdf](https://core.ac.uk/download/pdf/82322397.pdf), <a href="https://doi.org/10.1016/0022-4049(80)90082-1">doi:10.1016/0022-4049(80)90082-1</a>&rbrack;



category: category

[[!redirects category of categories]]
[[!redirects 2-category of categories]]
