
#Definition#

Let $X$ be a [[site]] with underlying category $S_X$. Write $PSh(X) = [S^{op}, Set]$ for the [[presheaf]] category of $X$ and $Sh(X)$ for the corresponding [[subcategory]] [[category of sheaves|of sheaves]].


The [[closed monoidal structure on presheaves]] restricts under the inclusion $Sh(X) \hookrightarrow PSh(X)$ to a closed monoidal structure on sheaves.

#Properties#

* For $f : X \to Y$ a left axact [[site|morphism of sites]], there is for $F \in Sh(X)$, $F \in Sh(Y)$ a natural [[isomorphism]]

$$
  f_* hom(f^{-1}G, F) \simeq hom(G, f_* F)
  \,.
$$

Here $f_*$ is the [[direct image]] and $f^{-1}$ the [[inverse image]] operation.