#Idea#

The [[homotopy category]] of an [[(infinity,1)-category]] $C$ is, roughly, the best [[category|1-categorical]] approximation to $C$.  It has the same objects as $C$, and its morphisms are [[equivalence]] classes of 1-morphisms in $C$.


#Definition#

Of course, the formal definition depends on what definition we choose for $(\infty,1)$-categories.  If we use [[simplicially enriched category|simplicially]] or topologically enriched categories, we can obtain the homotopy category by simply taking [[path component]]s of the hom-spaces (that is, applying the functor $\pi_0$ homwise).  Similar, but more complicated, definitions work for [[complete Segal space]]s and [[Segal category|Segal categories]].

For [[quasi-category|quasi-categories]], one can write down a similar definition, but there is also a more direct construction: the [[nerve|simplicial nerve]] functor $N :$ [[Cat]] $\to$ [[SSet]] has a [[left adjoint]]
$$
 h : SSet \to Cat
 \,.
$$
and the homotopy category of a quasi-category (a [[simplicial set]] with extra [[stuff, structure, property|properties]]) is its image $h C$ under this functor.


#References#

[Section 1.2.3, p. 33](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=33) of

* [[Jacob Lurie]], [[Higher Topos Theory]]
