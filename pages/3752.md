
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _semicategory_ or _non-unital category_ is like that of _[[category]]_ but omitting the requirement of [[identity]]-morphisms.

This generalizes the notions of [[semigroup]], [[semiring]], etc: 

* a [[semigroup]] is (the [[hom-set]] of) a semicategory with a single object;

* a [[semiring]] is (the [[hom-set]] of) a semicategory [[enriched category|enriched]] in [[Ab]] with a single object.

Semicategories, like categories, appear as [[semipresheaf|semipresheaves]] on the category with two objects and two morphisms.  

## Definition

+-- {: .num_defn #SemiCategory}
###### Definition

A (small) **semicategory** or **non-unital category** $\mathcal{C}$ consists of 

* a [[set]] $\mathcal{C}_0$ of _[[objects]]_;

* a set $\mathcal{C}_1$ of _[[morphisms]]_ (or _arrows_);

* two [[functions]] $s, t : \mathcal{C}_1 \to \mathcal{C}_0$ called _source_ (or _domain_) and _target_ (or _codomain_);

  * one writes $f : x \to y$ if $s(f) = x$ and $t(f) = y$;

* a [[function]] $\circ \colon \mathcal{C}_1 \times_{t,s} \mathcal{C}_1 \to \mathcal{C}_1$ ([[composition]]) from the set of pairs of morphisms such that the target of the first is the source of the second;

such that the following properties are satisfied:

* source and target are respected by composition: $s(g \circ f) = s(f)$ and $t(g\circ f) = t(g)$;

* composition is _[[associativity|associative]]_: $(h \circ g)\circ f = h\circ (g \circ f)$ whenever $t(f) = s(g)$ and $t(g) = s(h)$.

=--

+-- {: .num_remark}
###### Remark

If one added to this definition the existence of a function $i \colon C_0 \to C_1$ such that for all $c \in C_0$ the morphism $i(c)$ is an [[identity]] on $c$ under the given [[composition]], then one has the defintion of a [[category]].

However, having [[identities]] is just an extra [[property]] on a semi-category, not extra [[structure]]. For more on this see below at _[Relation to categories](#RelationToCategories)_.

=--

+-- {: .num_remark}
###### Remark

One often writes $hom(x,y)$, $hom_C(x,y)$, or $C(x,y)$ for the collection of morphisms $f : x \to y$; the latter two have the advantage of making clear which category is being discussed.  People also often write $x \in C$ instead of $x \in C_0$ as a short way to indicate that $x$ is an object of $C$.  Also, some people write $Ob(C)$ and $Mor(C)$ instead of $C_0$ and $C_1$.

=--

+-- {: .num_defn #SemiFunctor}
###### Definition

For $\mathcal{C}, \mathcal{D}$ two semicategories, a [[semi-functor]] $F \colon \mathcal{C} \to \mathcal{D}$ is a pair of [[functions]] $F_0 \colon \mathcal{C}_0 \to \mathcal{D}_0$, $F_1 \colon \mathcal{C}_1 \to \mathcal{D}_1$ that respects all the given [[structure]] in the obvious way.

Write $SemiCat$ for the ([[large category|large]]) [[category]] whose objects are semicategories, and whose morphisms are semifunctors.

=--

## Properties

### Relation to categories
 {#RelationToCategories}

We discuss the relation of semicategories to [[categories]]. (See for instance the beginning of ([Harpaz](#Harpaz)) for a quick review of basics, with an eye towards their generalization to the relation between [[complete Segal spaces]] and [[complete semi-Segal spaces]].)

+-- {: .num_defn #ForgetfulFromCatToSemicat}
###### Definition

There is an evident [[forgetful functor]]

$$
  U \colon Cat \to SemiCat
$$

from the [[category]] [[Cat]] of [[categories]] to that of semicategories, def. \ref{SemiFunctor}, given simply by forgetting the identity-assigning map $i \colon \mathcal{C}_0 \to \mathcal{C}_1$ in a category.

=--

+-- {: .num_defn #SetNeutralElementsInEndoSemiMonoids}
###### Definition

For $\mathcal{C}$ a semi-category, def. \ref{SemiCategory}, write

$$
  Id(\mathcal{C}_1) \hookrightarrow \mathcal{C}_1
$$

for the [[subset]] on those morphisms which are [[endomorphisms]] on some object $x \in \mathcal{C}_0$ and such that they are neutral elements in their endomorphisms [[semimonoids]] $End_{\mathcal{C}}(x)$.
=--

+-- {: .num_prop #CategoriesAreSemicategoriesWithUnits}
###### Proposition

A semicategory is the semicategory underlying a category, hence is in the image of the functor $U$ of def. \ref{ForgetfulFromCatToSemicat}, precisely if every object has a neutral [[endomorphism]], hence precisely if the composite diagonal function in

$$
  \array{
    Id(\mathcal{C}_1) &\hookrightarrow& \mathcal{C}_1
    \\
    & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{s}}
    \\
    && \mathcal{C}_0
  }
$$

is an [[isomorphism]], where the horizontal function is that of def. \ref{SetNeutralElementsInEndoSemiMonoids}. 

Moreover, if a semicategory lifts to a category, it does so in a unique way: the functor $U \colon Cat \to SemiCat$ is an [[injection]] on [[isomorphism classes]].
 
=--

+-- {: .num_remark}
###### Remark

Equivalently one could use the target map instead of the source map in the formulation of prop. \ref{CategoriesAreSemicategoriesWithUnits}.

=--

+-- {: .num_remark}
###### Remark

The diagram appearing in prop. \ref{CategoriesAreSemicategoriesWithUnits} is a simple version of the [[univalence]] condition appearing in definition of a [[complete semi-Segal space]], a [[category object in an (infinity,1)-category|semi-category object in an (infinity,1)-category]]. See there for more on this.

=--

+-- {: .num_prop #idempotents}
###### Proposition


The functor $U$ of def. \ref{ForgetfulFromCatToSemicat} has a [[left adjoint]], which [[free functor|freely]] adjoins identity morphisms to a semicategory in the obvious way.  It also has a [[right adjoint]], which sends a semicategory $S$ to the category whose objects are the [[idempotents]] of $S$ and whose morphisms are the morphisms of $S$ that commute suitably with them, as described at [[Karoubi envelope]].  Indeed, the [[monad]] on [[Cat]] generated by this latter [[adjunction]] is exactly the monad for _[[idempotent completion]]_, also called [[Cauchy completion]].  (Note, however, that this is not a [[2-monad]], because the right adjoint of $U$ is not a [[2-functor]].)

=--

### Transitive relations

A [[transitive relation]] is a semicategory [[enriched category|enriched]] on [[truth values]], or a semicategory $C$ where thete is at most one morphism from every object $a$ to object $b$ in $C$

### Nerves and semi-simplicial sets

The [[nerve]] of a semicategory is a [[semi-simplicial set]] which satisfies the [[Segal conditions]].

## Examples

Start with the category of metric spaces and short maps. An occasionally useful semicategory can be formed from it by considering the nonempty spaces and strictly contractive functions. 

This is a semicategory, since:

* the composition of two strictly contractive functions is strictly contractive
* identity maps are not contractive (they are trivial isometries)

The interest in this semicategory arises from the fact that all morphisms $f : A \to A$ have unique fixed points, by Banach's fixed point theorem. 

## In higher category theory

The concept of semicategory has more or less evident analogs and generalizations in [[higher category theory]].

For models of higher categories by [[simplicial set]]s, i.e. presheaves on the [[simplex category]] (such as [[Kan complex]]es, [[quasi-categories]], [[weak complicial set]]s)  the corresponding semi-category notion is obtained by discarding the degeneracy maps (which are the identity-assigning maps in the simplicial framework), i.e. by considering just presheaves on the subcategory $\Delta_+ \subset \Delta$ on injective morphisms (see the discuss of $\Delta_+$ at [[Reedy model structure]] for more details).

Accordingly, there is the semi-category analog of a [[Segal space]], called a _[[semi-Segal space]]_.

[[Simpson's conjecture]] says that every $\infty$-category has a model where all [[composition]] operations are strict and only the [[unit law]]s hold up to [[coherent]] homotopies. This would mean that the $\infty$-semicategory underlying any $\infty$-category can always be chosen to be strict.

## Related concepts

* [[semipresheaf]]

* [[regular semicategory]]

* [[non-unital ring]]

* [[semi-simplicial set]]

* [[semi-Segal space]]

[[!include oidification - table]]

## References

Enriched semicategory theory is developed in 

* {#MBB02}M.-A. Moens, U. Bernani-Canani, [[Francis Borceux|F. Borceux]], _On regular presheaves and regular semi-categories_ , Cah. Top. G&#233;om. Diff. Cat. **XLIII** no.3 (2002) pp.163-190. ([numdam](http://www.numdam.org/item?id=CTGDC_2002__43_3_163_0))

This is turned one notch further in

* {#Stubbe05}[[Isar Stubbe]], _Categorical structures enriched in a quantaloid : regular presheaves, regular semicategories_ , Cah. Top. G&#233;om. Diff. Cat. **XLVI** no.2 (2005) pp.99-121. ([numdam](http://www.numdam.org/item/CTGDC_2005__46_2_99_0))

Semicategories and semigroups are mentioned in section 2 in

* W. Dale Garraway, _Sheaves for an involutive quantaloid_,  Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 4 (2005), p. 243-274  ([numdam](http://www.numdam.org/item?id=CTGDC_2005__46_4_243_0))

Semicategories with an eye towards their generalization to [[semi-Segal spaces]] are briefly discussed at the beginning of 

* {#Harpaz} [[Yonatan Harpaz]], _Quasi-unital $\infty$-Categories_ ([arXiv:1210.0212](http://arxiv.org/abs/1210.0212))
 
Structures obtained by further relaxing also the [[associativity]] law are discussed in 

* Salvatore Tringali, _Plots and Their Applications - Part I: Foundations_  ([arXiv:1311.3524](http://arxiv.org/abs/1311.3524))

Topologically enriched semicategories are used for studying some aspects of concurrency theory in computer science. It is necessary to work with semicategories to have functorial definitions of the branching and merging homologies of a concurrent system. A starting point for reading the theory can be the paper

* {#Gaucher} [[Philippe Gaucher]], _Flows revisited: the model category structure and its left determinedness_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, vol LXI-2 (2020) ([published](http://cahierstgdc.com/wp-content/uploads/2020/04/GAUCHER-LXI-2.pdf), [arXiv:1806.08197](https://arxiv.org/abs/1806.08197))

Semi-categories, semi-adjunctions and semi-cartesian closed categories have been used to study the [[lambda calculus]] since 

* Susumu Hayashi, _Adjunction of semifunctors: Categorical structures in nonextensional lambda calculus_, Theoretical Computer Science
Volume 41, 1985, Pages 95-104 [doi:10.1016/0304-3975(85)90062-3](https://doi.org/10.1016/0304-3975%2885%2990062-3)

[[!redirects semicategories]]

[[!redirects semi-category]]
[[!redirects semi-categories]]


[[!redirects category without units]]
[[!redirects categories without units]]

