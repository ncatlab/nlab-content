#Definition#

Let $C$ be a [[category with weak equivalences]] and let $D$ be a small category. Take the [[functor category]] $[D,C]$ to be a [[category with weak equivalences]] by taking the weak equivalences to be those [[natural transformation]]s which are objectwise weak equivalences in $D$. 

The **homotopy limit** of a functor $F : D \to C$ is the image of $F$ under the right [[derived functor]] of the [[limit]] functor $lim_D : [D,C] \to C$ with respect to the above homotopical structure on $[D,C]$:
$$
  holim_D F := (R lim_D)F
  \,.
$$

#Examples#

As with every [[derived functor]], the concrete computation of a homotopy limit depends on which properties the objects we compute it on satisfy. 

* Let $D = \{ 1\to 0 \leftarrow 2\}$ be the pullback [[diagram]]. So that limits over it compute [[pullback]]s.  and assume that $F : D \to C$ is such that
$$
  F(1) \to F(0) \leftarrow F(2)
$$
satisfies
  * $F(i)$ is fibrant for all $i$;
  * and either $F(1) \to F(0)$ or $F(2) \to F(0)$ is a fibration;
then
  * $holim_D F$ exists;
  * and is weakly equivalent to the ordinary limit $holim_D F \stackrel{\simeq}{\to} lim_D F$.
Conversely this means that on an arbitrary pullback diagram  $holim_D F$ can be computed by finding a natural transformation $F \Rightarrow F'$ whose component morphisms are weak equivalences and such that $F'$ satisfies the above conditions.

#References#

The defintion of homotopy (co)limit itself is given for instance as definition [4.1, p. 14](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=14) in

* Wojciech Chacholski and Jerome Scherer, _Homotopy theory of diagrams_ ([arXiv](http://arxiv.org/abs/math.AT/0110316))

The rest of this article is concerned with discussing how to compute the homotopy (co)limits concretely. For instance the above statement on the computation of homotopy pullbacks is proposition [2.5, p. 15](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=15)
