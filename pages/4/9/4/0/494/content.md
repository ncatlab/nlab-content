The following lists equivalent definitions for two [[functor]]s

$$
  L : C \to D
$$
$$
  R : D \to C
$$
to define a **pair of adjoint functors**, denoted 
$$
  L \vdash R
  \,,
$$ 
with 

* $L$ the **left adjoint** 

and 

* $R$ the **right adjoint** 

of the pair.

For either $L$ or $R$ given, the corresponding right or left adjoint, respectively, is, if it exists, [[generalized the|unique up to unique isomorphism]].

#Definition in terms of representable functors#

Given $L : C \to D$, by precomposition it defines a functor
$$
  L^* : [D^{op}, Set] \to [C^{op}, Set]
$$
of [[presheaf]] categories. By restriction along the [[Yoneda embedding]] $Y : D \to [D^{op}, Set]$ this yields the functor
$$
 \bar L : D \stackrel{Y}{\to}
  [D^{op}, Set] \stackrel{L^*}{\to}
  [C^{op}, Set]
 \,.
$$

Notice that
$$
  \bar L : d \mapsto Hom_D(L(-),d) \in [D^{op}, Set]
  \,.
$$
If for all $d \in D$ this presheaf $\bar L(d)$ is [[representable functor|representable]], then it is functorially so in that there exists a functor $R : D \to C$ such that
$$
  \bar L \simeq Y \circ R
  \,.
$$

Then $L \vdash R$.


#Definition in terms of Hom isomorphism#

There is a [[natural transformation|natural isomorphism]] of [[hom-functor]]s $C^{op} \times D \to Set$

$$
  Hom_D(L(-),-) \simeq Hom_C(-,R(-))
  \,.
$$

In other words, for all $c \in C$ and $d \in D$ there is a bijection of sets

$$
  Hom_D(L(c),d) \simeq Hom_C(c,R(d))
$$

naturally in $c$ and $d$. This isomorphism is the **adjunction isomorphism** and the image of an element under this isomorphism is its [[adjunct]].


#Definition in terms of adjunction #

The pair $L \vdash R$ is precisely an [[adjunction]] in the
[[2-category]] [[Cat]] of categories.