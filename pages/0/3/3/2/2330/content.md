
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea
 {#Idea}

Following the general concept of *[[(n,r)-category|$(n,r)$-category]]*, a *$(0,1)$-category* is a [[category]] whose [[hom-objects]] are [[(-1)-groupoids]], hence which for every [[pair]] of [[objects]] $a,b$ have either no morphism $a \to b$ or an [[essentially unique]] one.

More in detail, recall that:

* an [[(n,1)-category]] is an [[(∞,1)-category]] such that every [[hom-space|hom ∞-groupoid]] is [[n-truncated|(n-1)-truncated]].

* a [[0-truncated]] [[∞-groupoid]] is equivalently a set;

* a [[(-1)-truncated]] [[∞-groupoid]] is a [[subsingleton]].

Therefore:

+-- {: .num_remark}
###### Remark
**([[relation between preorders and (0,1)-categories]])**
\linebreak
An $(0,1)$-category is [[equivalence of categories|equivalently]] [[preordered]].

Since every hom-$\infty$-groupoid is [[(-1)-truncated]], it is a [[subsingleton]], so there is at most one morphism from any object to any other; hence the $(0,1)$-category is [[preordered]] by the relation on objects that there exists an element of the hom-$\infty$-groupoid between two objects.
=--

## Segal / Rezk completeness

In the [[higher category theory]] literature, there is a distinction between $(\infty,1)$-categories and $(n, 1)$-categories which satisfy a [[Segal completeness]] or [[Rezk completeness]] condition and those which do not, which leads to a distinction between whether $(\infty,1)$-categories and $(n, 1)$-categories by default are Segal / Rezk complete or not: 

1. Those authors who start with $(\infty,1)$-categories and define $(0, 1)$-categories from [[(-1)-truncations]] of the hom-$\infty$-groupoids tend to assume Segal / Rezk completeness by default, where a $(0, 1)$-category which are not Segal complete / Rezk complete is then called a **$(0, 1)$-[[precategory]]**, or when defined [[internal logic|internally]], a **[[Segal category|Segal]] $(0, 1)$-category**. 

2. Those authors who build $(n, 1)$-categories from components tend not to assume Segal / Rezk completeness by default, where a $(0, 1)$-category which does satisfy [[Segal completeness]] or [[Rezk completeness]] is called a **[[univalent category|univalent]] $(0, 1)$-category**, or when defined [[internal logic|internally]], a **[[complete Segal space|complete Segal]] $(0, 1)$-category** or **[[Rezk category|Rezk]] $(0, 1)$-category**. Furthermore, since the hom-$(n - 1)$-groupoids are [[subsingletons]], one can equivalently call such a $(0, 1)$-category **[[gaunt category|gaunt]]** or **[[skeletal category|skeletal]]**, since those conditions are equivalent to Segal completeness / Rezk completeness for $(0, 1)$-categories. 

This distinction is important even for $(0, 1)$-categories because it denotes the difference between a [[preorder]] and a [[partial order]] as a $(0, 1)$-category, and also any mathematical structures derived from preorders vs partial orders, such as the order-theoretic definitions of [[presemilattices]] vs [[semilattices]], [[prelattices]] vs [[lattices]], or [[Heyting prealgebras]] vs [[Heyting algebras]]. In the case of $(0, 1)$-groupoids, this is the difference between a [[setoid]] and a [[set]], and thus between [[algebraic structures]] defined using [[equivalence relations]] vs using [[equality]], such as the algebraic definitions of [[presemilattices]] vs [[semilattices]], [[prelattices]] vs [[lattices]], or [[Heyting prealgebras]] vs [[Heyting algebras]]. See also the [[relation between preorders and (0,1)-categories]] for additional details. 

## Extra stuff, structure, property

Here we assume that $(0,1)$-categories are Segal / Rezk complete:

* A $(0,1)$-category with the structure of a [[site]] is a [[(0,1)-site]]: a [[posite]].

* A $(0,1)$-category with the structure of a [[cartesian monoidal category]] is a [[meet-semilattice]].

* A $(0,1)$-category with the structure of a [[cocartesian monoidal category]] is a [[join-semilattice]].

* A $(0,1)$-category with the structure of both a [[cartesian monoidal category]] and a [[cocartesian monoidal category]] is a [[lattice]].

* A $(0,1)$-category with the structure of a [[topos]] is a [[(0,1)-topos]]: a [[Heyting algebra]].

* A $(0,1)$-category with the structure of a [[Grothendieck topos]] is a [[Grothendieck (0,1)-topos]]: a [[frame]] or [[locale]].

* A $(0,1)$-category which is also a [[groupoid]] (that is, every morphism is an isomorphism) is a $(0,0)$-category (which may think of as either a $0$-category or as a $0$-groupoid), which is the same as a [[set]] (up to equivalence) or a [[symmetric proset]] (up to isomorphism).

## Related concepts

* [[relation between preorders and (0,1)-categories]]

* [[(-2)-groupoid]]

* [[(-1)-groupoid]]

* [[0-groupoid]]

* [[1-groupoid]]

* [[2-groupoid]]

* [[3-groupoid]]

* [[4-groupoid]]

* [[n-groupoid]]

* [[∞-groupoid]]

* [[(0,0)-category]]

* [[(1,0)-category]]

* [[(n,0)-category]]

* [[(∞,0)-category]]

* [[0-category]]

* [[1-category]]

* [[2-category]]

* [[3-category]]

* [[4-category]]

* [[n-category]]

* [[∞-category]]

* **(0,1)-category**

* [[(1,1)-category]]

* [[(2,1)-category]]

* [[(n,1)-category]]

* [[(∞,1)-category]]

* [[(1,2)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]


[[!redirects (0,1)-category]]
[[!redirects (0,1)-categories]]

[[!redirects (0,1)-precategory]]
[[!redirects (0,1)-precategories]]

[[!redirects univalent (0,1)-category]]
[[!redirects univalent (0,1)-categories]]
