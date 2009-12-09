* a table of contents that doesn't contain itself
{:toc}

# Idea #

A [[homotopical category]] is a [[category]] $C$ equipped with the information that some of its [[morphisms]], specifically, a subcategory $W \supset Core(C)$, are to be regarded as "weakly invertible".  One way to make this notion precise is through the concept of __simplicial localization__:

The _simplicial localization_ $L C$ of a category $C$ is an [[(infinity,1)-category]] realized concretely as a [[simplicially enriched category]] which is such that the original category injects into it,  $C \hookrightarrow L C$, such that every morphism in $C$ that is labeled as a weak equivalence becomes an action equivalence in the sense of morphisms in [[(infinity,1)-categories]] in $L C$. And $L C$ is in some sense universal with this property.

Passing to the [[homotopy category of an (infinity,1)-category]] of $L C$ then reproduces the [[homotopy category]] that can also directly be obtained from $C$:

$$
  Ho_C(a,b) \simeq \Pi_0 (L C(a,b))
$$

(where $\Pi_0$ gives the  [[simplicial homotopy group|0th simplicial homotopy groupoid]]).

If the homotopical structure on $C$ extends to that of a (combinatorial) [[model category]], then there is another procedure to obtain a simplicially enriched category from $C$, the [[presentable (infinity,1)-category|(infinity,1)-category presented by a combinatorial model category]]. This $(\infty,1)$-category is equivalent to the one obtained by simplicial localization but typically more explicit and more tractable. See also [[localization of a simplicial model category]].

# Hammock localization #

&#8230; (see section 4.1 in the reference below) &#8230;

# Remarks #

If the [[homotopical category]] in question happens to carry the structure of a [[model category]] there are other tools for computing the [[SSet]]-[[hom object]] of the simplicial localization. These are described at [[(infinity,1)-categorical hom-space]]. 

# References #

A comprehensive survey of the general topic involved here can be found in the following paper:

* [[Tim Porter]], _$S$-Categories, $S$-groupoids, Segal categories and quasicategories_ ([arXiv](http://arxiv.org/abs/math/0401274))

Hammock localization is described in Section 4.1 there.

A useful quick collection of facts can be found at the beginning of Section 2 in the following paper:

* Clark Barwick, _On (enriched) Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))
