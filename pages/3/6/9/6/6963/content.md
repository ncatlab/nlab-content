
# $\mathcal{M}$-categories
* table of contents
{: toc}

## Idea

An $\mathcal{M}$-category is a [[category]] with two classes of [[morphisms]]: *tight* and *loose*.

A [[categorification]] of the concept of $\mathcal{M}$-category to $2$-[[2-category|categories]] is the concept of $\mathcal{F}$-[[F-category|category]].  (There are other possible categorifications, such as locally $\mathcal{M}$-enriched $2$-categories, or locally $\mathcal{M}$-enriched $\mathcal{F}$-categories.)  In particular, every $\mathcal{M}$-category is an $\mathcal{F}$-category with only identity $2$-[[2-morphism|morphisms]], and an $\mathcal{F}$-category becomes an $\mathcal{M}$-category upon forgetting its nonidentity $2$-cells.


## Definitions {#def}

{#mono} Let $\mathcal{M}$ (or $Mono$) be the category whose [[objects]] are [[injections]] ([[monomorphisms]] in the [[category of sets]]) and whose [[morphisms]] are [[commutative squares]]. $\mathcal{M}$ is a [[reflective subcategory]] of the [[arrow category]] $Set^\to$ (the [[Sierpinski topos]]), where the reflector [[product-preserving functor|preserves products]]; as a result, $\mathcal{M}$ is [[complete category|complete]], [[cocomplete category|cocomplete]] [[cartesian closed category]]. (In fact, $\mathcal{M}$ is a Grothendieck [[quasitopos]], as discussed [here](free+cartesian+category#Subset): it is the category of [[separated presheaves]] for the [[double negation topology]] on $Set^\to$.) 

A ([[locally small category|locally small]]) __$\mathcal{M}$-category__ is simply a [[category enriched]] over $\mathcal{M}$. In other words, where the hom-objects are pairs of sets $(T, L)$ where $T \subseteq L$. 

In more detail, an __$\mathcal{M}$-category__ consists of the following data:

* a [[class]] of __[[objects]]__;
* for each pair $x, y$ of objects, a [[set]] $L(x,y)$ of __loose [[morphisms]]__;
* for each pair $x, y$ of objects, a [[subset]] $T(x,y)$ of $L(x,y)$ of __tight morphisms__;
* for each object $x$, a tight __[[identity morphism]]__ $id_x$; and
* for each triple $x, y, z$ of objects, a [[binary operation]] __[[composition]]__ $\circ_{x,y,z}$ from $L(y,z)$ and $L(x,y)$ to $L(x,z)$ such that:

  * $f \circ g$ is tight whenever $f, g$ are;
  * $\id_y \circ f = f = f \circ \id_x$ whenever this makes sense; and
  * $(f \circ g) \circ h = f \circ (g \circ h)$ whenever this makes sense.

Equivalently, an __$\mathcal{M}$-category__ is a [[category]] of objects and __loose__ morphisms together with a [[wide subcategory]] of __tight__ morphisms.

Note that the "underlying ordinary category" of an $\mathcal{M}$-category, in the usual sense that that phrase is used in [[enriched category]] theory, is its category of *tight* morphisms. This is because the underlying ordinary category is induced by a monoidal change-of-base functor $\hom(I, -) \colon \mathcal{M} \to Set$ represented by the monoidal unit $I = (1, 1)$, where we have 

$$\hom_{\mathcal{M}}((1, 1), (T, L)) \cong T.$$  

Nevertheless, it is frequently also useful to think of the category of loose morphisms as a sort of "underlying ordinary category" of an $\mathcal{M}$-category. This is effected by the monoidal change-of-base functor $\hom_{\mathcal{M}}((0, 1), -) \colon \mathcal{M} \to Set$, where we have 

$$\hom_{\mathcal{M}}((0, 1), (T, L)) \cong L.$$ 


## Examples

*  Every $\dagger$-[[dagger-category|category]] is an $\mathcal{M}$-category in which the tight morphisms are the [[unitary isomorphisms]].  In particular, [[Hilbert spaces]] form an $\mathcal{M}$-category with [[unitary operators]] as tight morphisms.

*  A more interesting way to make Hilbert spaces into an $\mathcal{M}$-category [[Hilb]] uses (as in the $\dagger$-category $Hilb$) all [[bounded linear operators]] as loose morphisms but only [[short linear operators]] (those with norm at most $1$) as tight morphisms.  This gives the same tight isomorphisms as the $\dagger$-category $Hilb$ (but also has non-invertible tight morphisms).

*  Similarly, [[Ban]] (the category of [[Banach spaces]]) is an $\mathcal{M}$-category with all bounded linear operators as loose morphisms but only short linear operators as tight morphisms.  In [[functional analysis]], a loose isomorphism in $Ban$ is traditionally called an '[[norm isomorphism|isomorphism]]' while a tight isomorphism is called a '[[global isometry]]'.

*  We can make [[Met]] (the category of [[metric spaces]]) into an $\mathcal{M}$-category is several ways, with [[short maps]] contained in [[Lipschitz map]]s contained in [[uniformly continuous maps]] contained in [[continuous maps]]; we can also take Lipschitz maps contained in [[bounded maps]].  (For linear operators between Banach spaces, the continuous and bounded operators are the same and are already Lipschitz.)

*  Any [[strict category]] is an $\mathcal{M}$-category with [[equality|equalities]] as the tight morphisms.  (Thus the wide subcategory of tight morphisms is [[skeletal category|skeletal]].)  In particular, the [[category of sets]] (or any category) in [[material set theory]] is an $\mathcal{M}$-category.

*  A more interesting way to make [[material set theory]]\'s [[category of sets]] into an $\mathcal{M}$-category has all [[subset]] inclusions as tight morphisms.  Again the tight isomorphisms are simply the equalities.

*  Given any category $C$ and object $a$ of $C$, the [[subobjects]] of $a$ form an $\mathcal{M}$-category whose category of loose morphisms is the [[full subcategory]] of $C$ on the subobjects of $a$ and whose category of tight morphisms is the [[subobject poset]] of $a$.

*  Similarly, [[quotient objects]] form an $\mathcal{M}$-category.

*  The __[[core]]__ of every category $C$ is an $\mathcal{M}$-category whose loose morphisms are the morphisms of $C$ and whose tight morphisms are the [[isomorphisms]] of $C$.

*  $\mathcal{M}$ itself is an $\mathcal{M}$-category whose objects are sets equipped with a specified subset, whose tight morphisms are functions which map the subset into each other, and whose loose morphisms are arbitrary functions.

*  Given any [[faithful functor]] $F\colon C \to D$, we may make $C$ into an $\mathcal{M}$-category whose tight morphisms are the original morphisms of $C$ and whose loose morphisms from $x$ to $y$ are the $D$-morphisms from $F(x)$ to $F(y)$.  This includes all of the examples above; up to [[equivalence of categories|equivalence]], this includes all examples.

* Let $T$ be a strict 2-monad on a strict 2-category. Then the strict $T$-algebras form an $\mathcal{M}$-category $T \mathrm{Alg}$ where tight morphisms are the strict algebra morphisms and the loose morphisms are the pseudo algebra morphsims. This is just a decategorified version of the $\mathcal{F}$-category of $T$-algebras, which also includes the 2-cells between algebras. 

* More generally, any strict $\mathcal{F}$-category can be made into an $\mathcal{M}$-category by forgetting the non-identity 2-cells. 

## Applications

* Any $\mathcal{M}$-category whose tight morphisms form a [[preorder]] can be made into a [[strict category]] in a canonical way: declare two objects to be equal if they are *tightly* isomorphic.  This is an unusual sort of strict category in that its "equality predicate" on objects may not be literal equality (even in a foundational system where the latter makes sense).  Many strict categories that arise in practice underlie $\mathcal{M}$-categories, such as the category of sets in material set theory.

  Note that two *equivalent* $\mathcal{M}$-categories with posetal tight categories (in the usual sense of equivalence for enriched categories) have *isomorphic* underlying strict categories (in the appropriate sense, i.e. making use of the stipulated equality predicate on objects to define "isomorphism").  In this way, some examples which may seem on the surface to be [[evil]], by referring to an isomorphism of categories, can alternatively be described non-evilly by recognizing the presence of a neglected $\mathcal{M}$-enrichment.

* For instance, let $G = Gal(E/F)$ be the [[Galois group]] of a finite [[Galois extension]] $E/F$.  Then there is an $\mathcal{M}$-category whose objects are intermediate [[fields]] $F\subset K\subset E$, whose loose maps are arbitrary field homomorphisms that fix $F$ pointwise, and whose tight maps are those which commute with the inclusions into $E$.  There is also an $\mathcal{M}$-category whose objects are [[orbits]] $G/H$, whose loose maps are arbitrary maps of $G$-sets, and whose tight maps are those which commute with the quotient maps from $G$.  The fundamental theorem of classical [[Galois theory]] says that these two $\mathcal{M}$-categories are equivalent *as $\mathcal{M}$-categories*.

  This is a stronger statement than saying that their underlying strict categories, as above, are isomorphic, which is yet stronger than saying that their underlying categories of loose maps are equivalent.  See [this post](http://article.gmane.org/gmane.science.mathematics.categories/5877) by [[Peter May]].


## Related Concepts 

* [[relative category]] 

* [[F-category]]

## References

$\mathcal{M}$-categories are mentioned as $Subset$-categories (thinking of $\mathcal{M}$ as the category of [[subset]] inclusions) in

*  [[John Power]] (2002), Premonoidal categories as categories with algebraic structure, Theoretical Computer Science 278, [pdf](http://www.inf.ed.ac.uk/publications/online/0413.pdf).

We discussed them in the [[nlabmeta:n-Forum]] as part of a discussion of the category of [[Banach spaces]]:

*  [[Mark Meckes]] et al (2011), Banach space, n-Forum, ([discussion link](https://nforum.ncatlab.org/discussion/3289/banach-space/)).


[[!redirects M-category]]
[[!redirects M-categories]]
[[!redirects Subset-category]]
[[!redirects Subset-categories]]
