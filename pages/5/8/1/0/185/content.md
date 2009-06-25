#Idea#

In as far as a  [[generalized smooth space]] is a (pre)sheaf on smooth test domains, following the lore of [[space and quantity]] a generalized smooth quantity (such as a generalized smooth function or a generalized smooth section) is a co-presheaf on smooth test domains.

Product preserving co-presheaves on [[CartSp]] form a generalized notion of smooth algebras with very nice structural properties, such as required in [[geometric function theory]].

These generalized smooth algebras, usually called **$C^\infty$-rings** are examples of [[locally modeled monoid]]s.

#Motivating example#

For $X$ a smooth [[manifold]], the assignment
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

#Definitions#

+-- {: .un_defn}
###### Definition

[[CartSp]] is the full subcategory of [[Diff]]
on manifolds of the form $\mathbb{R}^n$.

=--


+-- {: .un_defn}
###### Definition

A $C^\infty$-algebra is a finite product-preserving co-presheaf on [[CartSp]], i.e. a finite product preserving functor

$$
  A : CartSp \to Set
  \,.
$$

The category of such functors and [[natural transformation]]s between them we denote by $C^\infty Alg$.


=--


+-- {: .un_defn}
###### Definition

For $X$ a smooth manifold, the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--



+-- {: .un_defn}
###### Definition (smooth tensor product)


The [[coproduct]] in $C^\infty Alg$
we call the **smooth tensor product**

$$
  \otimes_\infty : C^\infty Alg \times C^\infty Alg
   \to C^\infty Alg
  \,.
$$

=--







# Properties #

There is a [[stuff, structure, property|forgetful functor]] 

$$
  U : C^\infty Alg \to Alg
$$

from generalized smooth algebras to ordinary algebras which is given by evaluation on $\mathbb{R}$

$$
  U : A \mapsto A(\mathbb{R})
$$

and equipping the set $A(\mathbb{R})$ with the algebra structure induced on it: 

the product and sum on $A(\mathbb{R})$ is then the image of the corresponding operations on the algebra $\mathbb{R}$

$$
  \cdot_A 
  :
  A(\mathbb{R}) \times A(\mathbb{R})
  \stackrel{\simeq}{\to}
  A(\mathbb{R}\times \mathbb{R})
  \stackrel{A(\cdot)}{\to}
  A(\mathbb{R})
  \,.
$$

$$
  +_A :
  A(\mathbb{R}) \times A(\mathbb{R})
  \stackrel{\simeq}{\to}
  A(\mathbb{R} + \mathbb{R})
  \stackrel{A(\cdot)}{\to}
  A(\mathbb{R})
  \,.
$$

Moreover there is canonically a morphism of rings

$$
  \mathbb{R} \to A(\mathbb{R})
$$

given by

$$
  (* = \mathbb{R}^0 \stackrel{c}{\to} \mathbb{R})
  \mapsto
  (* = A(\mathbb{R}^0) \stackrel{A(c)}{\to} A(\mathbb{R}))
  \,.
$$

This makes $A(\mathbb{R})$ an $\mathbb{R}$-algebra.


+-- {: .un_prop}
###### Proposition ( _MoerRey_ , prop. 1.1)

$C^\infty(\mathbb{R})$ is the free smooth algebra#
on $n$ generators, in that for every $n \in \mathbb{N}$ 
and every smooth algebra $A$ there is an [[adjunction]]
isomorphism

$$
  Hom_{C^\infty Alg}(C^\infty(\mathbb{R}^n), A)
  \simeq
  Hom_{Alg}(\mathbb{R}^n, A(\mathbb{R}))
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition ( _MoerRey_ , prop. 2.5)

For $X$ and $Y$ smooth manifolds we have

$$
  C^\infty(X) \otimes_{\infty} C^\infty(Y)
  \simeq
  C^\infty(X \times Y)
  \,.
$$

=--


**Remark**

Notice that the ordinary algebraic tensor product of $C^\infty(X)(\mathbb{R})$ and $C^\infty(Y)(\mathbb{R})$ regarded as ordinary algebras does not satisfy this property, rather one has

$$
  C^\infty(X)(\mathbb{R}) \otimes C^\infty(Y)(\mathbb{R})
  \subset
  C^\infty(X \times Y)(\mathbb{R})
  \,.
$$

Turning this inclusion into an equivalence is usually called a _completion_ of the algebraic tensor product. The smooth tensor product need not be completed. 

In the context of [[geometric function theory]] this says that $C^\infty(X)$ is a "good" kind of function. The above equation is the first part of the fundamental theorem of [[geometric infinity-function theory]].


#Remarks#

* While such a product-preserving co-presheaf $A$ induces the structure of an algebra on each of the sets $A(\mathbb{R}^n)$, with product induced from the componentwise product $\mathbb{R}^n \times \mathbb{R}^n  \to \mathbb{R}^n$, it is not a _co-presheaf with values in algebras_: the co-restriction morphisms assigned to maps $\mathbb{R}^n \to \mathbb{R}^m$ which are not just projections or injections will not be algebra homomorphisms.

* But conversely this means that restricted to such maps, i.e. restricted along the inclusion $FinSet \hookrightarrow CartSp$ of [[CartSp]], $A$ does become a co-presheaf with values in algebras. 



#References#

This definition was introduced in 

* **MoerRey** Ieke Moerdijk and Gonzalo E. Reyes, _Models for Smooth Infinitesimal Analysis_ Springer (1991)

see also

* Lawvere, _Categorical dynamics_ in _Topos theoretic methods in geometry_, volume 30 of _Various Publ. Ser._, pages 1-28, Aarhus Univ. (1997)

The definition itself appears on p. 16.

A brief but useful review is also on p. 3 of

* David Spivak, _Quasi-Smooth derived manifolds_ ([pdf](http://math.berkeley.edu/~dspivak/thesis2.pdf))


[[!redirects generalized smooth algebras]]