#Idea#

A special case of the general notion of a [[derived functor]] on the [[homotopy category]] of a [[homotopical category]] is that of a derived functor on the [[category of chain complexes]] of an [[abelian category]]. This is the original case in which derived functors were considered in [[homological algebra]]. This entry discusses special aspects of this special situation.

+--{: .query}
[[Mike Shulman|Mike]]: Somewhere, we should talk about derived functors in the very traditional sense of "extending the image of a short exact sequence to a long exact sequence."
=--

#Derived functors in homological algebra#

Here are some peculiarities of the concept of derived functors in [[homological algebra]], mostly due to historical reasons:

1. Every functor $F : C \to C'$ of [[abelian category|abelian categories]] canonically induces a functor $K(F) : K(C) \to K(C')$ of [[category of chain complexes|categories of chain complexes]]. The (right, say) _derived functor_ $R F$ of $F$ is the derived functor of $K(F)$ and usually only functors of chain complexes of the form $K(F)$ are considered.

1. Similarly the output of the derived functor is usually taken to be in $C'$ by postcomposing with the [[homology]] functor. One writes $R^k F := H^k \circ R F$. The derived functor $R F$ in its totality as a functor with values in $K(C)$ is then sometimes denoted $R^\bullet F$.


#Definition#

#Examples#

The most famous derived functors are the derived version of the hom-functor and the tensor product functor, whose derived functors are traditionally denoted $Ext$ and $Tor$.

## Ext ##

Consider

$$
  Hom^\bullet : K(C)^{op} \times K(C) \to K(Ab)
$$
$$
  (X', Y') \mapsto tot Hom^{\bullet, \bullet}(X', Y')
$$

Then

$$
  Ext^k(X,Y) \simeq H^k(R Hom(X, Y))
$$

(...)

## Tor ##

(...)