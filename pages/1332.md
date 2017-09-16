#Definition for ordinary categories#

Let $C$ be a [[category]] and $S$ a collection of [[morphism]]s in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]

$$
  C(-,c) : C^{op} \to Set
$$

sends morphisms in $S$ to [[isomorphism]]s in [[Set]], i.e. if
for every $s : a \to b$ in $S$, the functor

$$
  C(s,c) : C(b,c) \to C(a,c)
$$

is a bijection

#Definition for $(\infty,1)$-categories#

**Definition [def. 5.5.4.1](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=383) in [[Higher Topos Theory|HTT]]**

Let $C$ be an [[(infinity,1)-category]] and $S$ a collection of morphisms in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]

$$
  C(-,c) : C^{op} \to \infty Top
$$

evaluated on $s \in S$ induces isomorphism in the homotopy category of [[Top]].

#Remarks#


* a [[reflective (infinity,1)-subcategory]] can be realized as the full subcategory on $S$-local objects, where $S$ is the collection of morphisms sent by the corresponding [[localization of an (infinity,1)-category]] to equivalences