# Definition #

We say that two functors $L:C\to D$ and $R:D\to C$ are **adjoint** if they form an [[adjunction]] $L \dashv R$ in the [[2-category]] [[Cat]] of categories.  This means that they are equipped with [[natural transformation]]s $\eta:1_C \to R L$ and $\epsilon:L R \to 1_D$ satisfying the [[triangle identities]], that is the compositions
$
L \stackrel{L\eta}\to LRL\stackrel{\epsilon L}\to L
$
and 
$R\stackrel{\eta R}\to RLR \stackrel{R\epsilon}\to R$ 
are identities.
The left or right adjoint of any functor, if it exists, is [[generalized the|unique up to unique isomorphism]].

In the case of [[Cat]], there are a number of equivalent characterizations of an adjunction, some of which are given below.


#Definition in terms of Hom isomorphism#

An adjunction $L\dashv R$ is equivalently given by a [[natural transformation|natural isomorphism]] of [[hom-functor]]s $C^{op} \times D \to Set$

$$
  Hom_D(L(-),-) \simeq Hom_C(-,R(-))
  \,.
$$

In other words, for all $c \in C$ and $d \in D$ there is a bijection of sets

$$
  Hom_D(L(c),d) \simeq Hom_C(c,R(d))
$$

naturally in $c$ and $d$.  This isomorphism is the **adjunction isomorphism** and the image of an element under this isomorphism is its [[adjunct]].

Given such an adjunction isomorphism, $\eta$ and $\epsilon$ can be recovered as the adjuncts of identity morphisms.  The [[Yoneda lemma]] ensures that the entire adjunction isomorphism can be recovered from them by composition: the adjunct of $f:L(c)\to d$ is $R(f) \eta$, and the adjunct of $g:c \to R(d)$ is $\epsilon L(g)$.  The triangle identities are precisely what is necessary to ensure that this _is_ an isomorphism.


#Definition in terms of representable functors#

A functor $L:C\to D$ has a right adjoint if and only if for all $d$, the [[presheaf]] $Hom_D(L(-),d):D^{op}\to Set$ is [[representable functor|representable]], i.e. there exists an object $R(d)$ and a natural isomorphism
$$Hom_D(L(-),d) \cong Hom_C(-,R(d)).$$
There is then a unique way to define $R$ on arrows so as to make these isomorphisms natural in $d$ as well.

In more fancy language, by precomposition $L$ defines a functor
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
such that
$$
  \bar L : d \mapsto Hom_D(L(-),d) \in [D^{op}, Set]
  \,.
$$
If for all $d \in D$ this presheaf $\bar L(d)$ is [[representable functor|representable]], then it is functorially so in that there exists a functor $R : D \to C$ such that
$$
  \bar L \simeq Y \circ R
  \,.
$$

## Local definition ##

This definition has the advantage that it yields useful information even if the adjoint functor $R$ does not exist globally, i.e. as a functor on all of $D$:

it may happen that
$$
  \bar L(d) := Hom_D(L(-),d) \in [D^{op}, Set]
$$
is [[representable functor|representable]] for _some_ $d$ but not for all $d$. The representing object may still usefully be thought of as $R(d)$.

This _global_ versus _local_ evaluation of adjoint functors induces the global/local pictures of the defintions

* [[limit]] / [[homotopy limit]]

* [[Kan extension]]

as discussed there.

# Definition in terms of universal arrows #

Given $R:D\to C$, and $c\in C$, a _universal arrow_ from $c$ to $R$ is an initial object of the [[comma category]] $(c/R)$.  That is, it consists of an object $L(c)\in D$ and an arrow $\eta:c\to R(L(c))$ such that for any $d\in D$, any arrow $g:c\to R(d)$ factors as $R(f) \eta$ for a unique $f:L(c)\to d$.  In particular, we have a bijection
$$Hom_C(c,R(d)) \cong Hom_D(L(c),d)$$
which it is easy to see is natural in $d$.  Again, in this case there is a unique way to make $L$ into a functor so that this isomorphism is natural in $c$ as well.

Note that this definition is simply obtained by applying the [[Yoneda lemma]] to the definition in terms of representable functors.


#Examples#

* see [[examples of adjoint functors]].