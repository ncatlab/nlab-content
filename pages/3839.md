


This entry is about the article

* [[Daniel Dugger]]:

  \linebreak

  **Combinatorial model categories have presentations** 

  \linebreak

   Adv. Math. **164** 1 (2001) 177-201 

  [arXiv:math/0007068](http://arxiv.org/abs/math/0007068)

  [doi:10.1006/aima.2001.2015](https://doi.org/10.1006/aima.2001.2015)

on [[combinatorial model categories]] and their identifications with [[Bousfield localization of model categories|Bousfield localizations]] of [[model categories of simplicial presheaves]].

> **Abstract.** _We show that every combinatorial model category can be obtained, up to Quillen equivalence, by localizing a model category of diagrams of simplicial sets. This says that any combinatorial model category can be built up from a category of "generators" and a set of "relations" --- that is, any combinatorial model category has a presentation._ 

This builds on the companion paper

* [[Dan Dugger]], _[[Universal homotopy theories]]_

This shows that, up to [[Quillen equivalence]], every [[combinatorial model category]] $A$ arises as the [[Bousfield localization of model categories|left Bousfield localization]] of the global projective [[model structure on simplicial presheaves]] $[C^{op}, sSet_{Quillen}]_{proj}$, for some [[small category]] $C$

$$
  A \simeq 
  [C^{op}, sSet_{Quillen}]_{proj, loc}
  \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  [C^{op}, sSet_{Quillen}]_{proj}
  \,.
$$


Notice (as discussed at the relevant entries) that 

* every combinatorial model category can be enhanced to a [[combinatorial simplicial model category]];

* that the full [[enriched category|enriched]] subcategories $A^\circ$ of these on fibrant-cofibrant objects are the [[locally presentable (∞,1)-categories]];

* that under this correspondence the global [[model structure on simplicial presheaves]] models the corresponding [[(∞,1)-category of (∞,1)-presheaves]]

  $$
    PSh_{(\infty,1)}(C)
    \simeq
    A^{\circ}
    \,.
  $$

Under this correspondence, [[Dugger's theorem]] is precisely the [[model category]]-theoretic analog of the theorem that every [[locally presentable (∞,1)-category]] $D$ is a [[localization of an (∞,1)-category|(∞,1)-categorical localization]] of an [[(∞,1)-category of (∞,1)-presheaves]]

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{}{\hookrightarrow}}
  PSh_{(\infty,1)}(C)
  \,.
$$

This [[(∞,1)-category]] theortic interpretation of [[Dugger's theorem]] is proposition A.3.7.6 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

category: reference