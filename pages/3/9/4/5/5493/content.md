# Contents
* contents
{:toc}

## Idea

A **sesquicategory** is a [[2-category]] in which the [[interchange law]] need not hold.


## Definition

Sesquicategories can be defined just as for [[2-categories]] except with the interchange law left out.

Alternatively, a sesquicategory may be given as a category $C$ together with a functor $H \colon C^{op} \times C \to Cat$ whose composite $ob \circ H \colon C^{op} \times C \to Cat \to Set$ with the underlying-set functor is equal to the hom functor of $C$.

A third definition says that a sesquicategory is given by a category $C$ together with a [[span]] $H \rightrightarrows hom_C$ of [[profunctors]] and transformations $\hom_C \to H \leftarrow H \times_{\hom_C} H$ making $H$ into an [[internal category]] in $[C^{op} \times C, Set]$.


## Remarks

A [[premonoidal category]] is the same as a sesquicategory with exactly one object.

The name 'sesquicategory' literally means $1\frac{1}{2}$-category, although they are actually *more* general than $2$-categories (which are of course more general than $1$-categories).


[[!redirects sesquicategory]]
[[!redirects sesquicategories]]
