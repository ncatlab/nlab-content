#Idea#

In as far as a  [[generalized smooth space]] is a (pre)sheaf on smooth test domains, following the lore of [[space and quantity]] a generalized smooth quantity (such as a generalized smooth function or a generalized smooth section) is a co-presheaf on smooth test domains.

#Motivating example#

For $X$ a smooth manifold, the assignment
$$
  \mathbb{R}^n \mapsto C^\infty(X,\mathbb{R}^n)
$$
is clearly covariant and hence yields a co-presheaf on [[CartSp]]. Moreover, the componentwise multiplication in $\mathbb{R}$ makes this a product-preserving co-presheaf:
we naturally have 
$$
  C^\infty(X, \mathbb{R}^n \times \mathbb{R}^m)
  \simeq
  C^\infty(X,\mathbb{R}^n)
  \times
  C^\infty(X, \mathbb{R}^m)
$$
(by the universal property of the cartesian product) and the product on functions $C^\infty(X) \times C^\infty(X) \to C^\infty(X)$ can be regarded as the image of our co-presheaf under the muliplication map $\mathbb{R} \times \mathbb{R} \stackrel{p}{\to} \mathbb{R}$

$$
  C^\infty(X)
  \times
  C^\infty(X)
  =  
  C^\infty(X,\mathbb{R})
  \times
  C^\infty(X,\mathbb{R}\times \mathbb{R})
  \stackrel{C^\infty(X,p)}{\to}
  C^\infty(X,\mathbb{R})
  \simeq
  C^\infty(X)
  \,.
$$

#Definition#

A $C^\infty$-algebra is a product-preserving co-presheaf on [[CartSp]].

#Remarks#

While such a product-preserving co-presheaf $A$ induces the structure of an algebra on each of the sets $A(\mathbb{R}^n)$, with product induced from the componentwise product $\mathbb{R}^n \times \mathbb{R}^n  \to \mathbb{R}^n$, it is not a _co-presheaf with values in algebras_: the co-restriction morphisms assigned to maps $\mathbb{R}^n \to \mathbb{R}^m$ which are not just projections or injections will not be algebra homomorphisms.

But conversely this means that restricted to such maps, i.e. restricted along the inclusion $FinSet \hookrightarrow CartSp$ of [[CartSp]], $A$ does become a co-presheaf with values in algebras. 

#References#

This definition was introduced in 

* Ieke Moerdijk and Gonzalo E. Reyes, _Models for Smooth Infinitesimal Analysis_ Springer (1991)

The definition itself appears on p. 16.

#Further resources#

With smooth function algebras generalized to $C^\infty$-algebras, one may wonder what the corresponding generalization of [[NQ-supermanifold]]s and hence of $L_\infty$-[[Lie infinity-algebroid|algebroid]]s are, which are defined in terms of smooth function algebras and smooth _modules_ over these function algebras. In particular, one expects that higher [[Lie theory]] should relate [[infinity-groupoid]] [[internalization|internal to]] $Spaces := Sh(CartSp)$ to $L_\infty$-[[Lie infinity-algebroid|algebroid]]s with [[Chevalley-Eilenberg algebra]]s [[internalization|internal to]] $Quantities := MonoidalCoPreSh(CartSp)$. This idea is further developed at [[schreiber:generalized smooth L-infinity algebroid]].