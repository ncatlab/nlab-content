
In the context of [[localization of an (infinity,1)-category]] or the corresponding 1-categorical [[Bousfield localization]] _local equivalences_ are those morphisms that are seen as equivalences by [[local object]]s.

More concretely, let $S$ be a subset of morphisms. Recall that an $S$-[[local object]] $X$ is one such that for all $s : A \to B$ in $S$ the induced morphism 

$$
  Hom(s,X) : Hom(B,X) \to Hom(A,X)
$$

is an equivalence. 

Conversely, a morphism $f : V \to W$ is is an $S$-**local equivalence** if for every $S$-[[local object]] $X$ the induced morphism

$$
  Hom(f,X) : Hom(W,X) \to Hom(V,X)
$$

is an equivalence.

In the context of [[simplicial model category|simplicial model categories]]
"equivalence" means: [[model structure on simplicial sets|weak equivalence]] of simplicial sets.

#References#

The model category theoretic notion is discussed in section A.3.7 of

* [[Jacob Lurie]], [[Higher Topos Theory]] .
