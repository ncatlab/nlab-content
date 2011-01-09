# Contents
* contents
{:toc}

## Idea

A **sesquicategory** is a [[2-category]] in which the [[interchange law]] need not hold.


## Definition

Sesquicategories can be defined just as for [[2-categories]] except with the interchange law left out.  (In order for this to make sense, one has to spell the definition out explicitly enough that the interchange law is a separate axiom.  In partircular, a sesquicategory does not have a composition functor $\hom(y,z)\times \hom(x,y)\to\hom(x,z)$.)

Alternatively, a (strict) sesquicategory may be given as a category $C$ together with a functor $H \colon C^{op} \times C \to Cat$ whose composite $ob \circ H \colon C^{op} \times C \to Cat \to Set$ with the underlying-set functor is equal to the hom functor of $C$.

A third definition says that a (strict) sesquicategory is given by a category $C$ together with a [[span]] $H \rightrightarrows hom_C$ of [[profunctors]] and transformations $\hom_C \to H \leftarrow H \times_{\hom_C} H$ making $H$ into an [[internal category]] in $[C^{op} \times C, Set]$.


## Remarks

A [[premonoidal category]] is the same as a sesquicategory with exactly one object.

A [[Gray-category]] does not have an underlying [[strict 2-category]], but it does have an underlying strict sesquicategory.  Thus, if one wants to define Gray-[[computads]], it is natural to work with "sesqui-computads" as a partway stage; see for instance [[toddtrimble:Surface diagrams]]

The name 'sesquicategory' literally means $1\frac{1}{2}$-category, although they are actually *more* general than $2$-categories (which are of course more general than $1$-categories).  Probably the reason for the name is that a sesquicategory is "part of the way" from a 1-category to a 2-category; you add the 2-cells and some of the structure, but you leave out one of the axioms.


[[!redirects sesquicategory]]
[[!redirects sesquicategories]]
