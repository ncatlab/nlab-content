#Idea#

In as far as a  [[generalized smooth spaces|generalized smooth space]] is a (pre)sheaf on smooth test domains, following the lore of [[space and quantity]] a generalized smooth quantity (such as a generalized smooth function or a generalized smooth section) is a co-presheaf on smooth test domains.

#Motivating example#

For $X$ a smooth manifold, the assignment
$$
  \mathbb{R}^n \mapsto C^\infty(X,\mathbb{R}^n)
$$
is clearly covariant and hence yields a co-presheaf on [[CartesianSpaces]]. Moreover, the componentwise multiplication in $\mathbb{R}$ makes this a product-preserving co-presheaf:
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

A $C^\infty$-algebra is a product-preserving co-presheaf on [[CartesianSpaces]].

#References#

This definition was introduced in 

* Ieke Moerdijk and Gonzalo E. Reyes, _Models for Smooth Infinitesimal Analysis_ Springer (1991)

