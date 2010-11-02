
# Equivalence of $2$-categories
* table of contents
{: toc}

## Definition

An **equivalence of 2-categories** is the appropriate notion of [[equivalence of categories|equivalence]] between [[2-categories]].  As used on the nLab, where all [[n-categories]] are usually by default "weak," this consists of:

* (Weak) [[2-functors]] (aka [[pseudofunctors]]) $F\colon C\to D$ and $G\colon D\to C$, and
* [[pseudonatural transformations]] $G F \to Id_C$ and $F G \to Id_D$ which are themselves [[equivalences]], i.e. there are pseudonatural transformations forming their inverses up to isomorphism.

In the literature this sort of equivalence is often called a **biequivalence**, as it has traditionally been associated with [[bicategories]], the standard algebraic definition of weak 2-category.  There is a stricter notion of equivalence for strict 2-categories, which traditionally is called just a *2-equivalence* and which on the nLab is called a [[strict 2-equivalence]].


## Internalization

Just as the notion of [[equivalence of categories]] can be [[internalization|internalized]] in any 2-category, the notion of equivalence for 2-categories can be internalized in any 3-category in a straightforward way.  The version above for 2-categories then results from specializing this general definition to the (weak) 3-category $2 Cat$ of 2-categories, (weak) 2-functors, pseudonatural transformations, and modifications.

There is one warning to keep in mind here.  Every 3-category is equivalent to a [[semi-strict n-category|semi-strict]] sort of 3-category called a [[Gray-category]], since it is a category [[enriched category|enriched]] over the monoidal category [[Gray]] of strict 2-categories and strict 2-functors.  Of course $Gray$ itself is a Gray-category, but as such it is [not](http://arxiv.org/abs/math/0612299) equivalent to the weak 3-category $2 Cat$ of weak 2-categories and *weak* 2-functors.

In particular, an "internal (bi)equivalence" in $Gray$ consists of *strict* 2-functors $F,G$ together with pseudonatural equivalences relating $G F$ and $F G$ to identities.  This is a notion of equivalence of intermediate strictness between the fully weak notion and the fully strict one.


[[!redirects equivalence of 2-categories]]
[[!redirects equivalences of 2-categories]]
[[!redirects equivalence of bicategories]]
[[!redirects equivalences of bicategories]]
[[!redirects biequivalence]]
[[!redirects biequivalences]]
