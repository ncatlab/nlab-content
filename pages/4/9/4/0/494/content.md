<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


# Definition #

We say that two functors $L:C\to D$ and $R:D\to C$ are **adjoint** if they form an [[adjunction]] $L \dashv R$ in the [[2-category]] [[Cat]] of categories.  This means that they are equipped with [[natural transformation]]s $\eta: 1_C \to R \circ L$ and $\epsilon: L \circ R \to 1_D$ satisfying the [[triangle identities]], that is the compositions
$L \stackrel{L\eta}\to L R L\stackrel{\epsilon L}\to L$
and 
$R\stackrel{\eta R}\to R L R \stackrel{R\epsilon}\to R$ 
are identities.
The left or right adjoint of any functor, if it exists, is [[generalized the|unique up to unique isomorphism]].

We say that $L$ is the __[[left adjoint]]__ of $R$ and that $R$ is the __[[right adjoint]]__ of $L$.

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


# Definition in terms of correspondences #

Every [[distributor]]

$$
  k : C^{op} \times D \to S
$$

defines a category
$C *^k D$ with $Obj(C *^k D) = Obj(C) \sqcup Obj(D)$ and 

$$
  Hom_{C^{op} \times D}(X,Y)
  = 
  \left\{
    \array{
      Hom_C(X,Y) & if X, Y \in C
      \\
      Hom_{D}(X,Y) & if X,Y \in D
      \\
      k(X,Y) & if X \in C and Y \in D
      \\
      \emptyset & otherwise
    }
  \right.
  \,.
$$

This category naturally comes with a functor to the [[interval]] category

$$
  C *^k D \to \Delta^1
  \,.
$$

Now, every functor $L : C \to D$ induces a [[distributor]]

$$
  k_f(X,Y) = Hom_D(f(X), Y)
$$

and every functor $R : D \to C$ induces a [[distributor]]

$$
  k_g(X,Y) = Hom_C(X, R(Y))
  \,.
$$

The functors $L$ and $R$ are adjoint precisely if the [[distributor]]s that they define in the above way are equal. This in turn is the case if
$C \star^L D \simeq (D^{op} \star^{R^{op}} C^{op})^{op}$.

We say that $C \star^k D$ is the [[cograph of a functor|cograph of the functor]] $k$. See there for more on this.

# Definition for $(\infty,1)$-functors #


The above characterization of adjoint functors in terms of categories over the interval is used in section 5.2.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

(motivated from the discussion of correspondences in section 2.3.1) 

to give a definition of adjunction between [[(infinity,1)-functor]]s. 

+-- {: .un_defn}
###### Definition

Let $C$ and $D$ be [[quasi-category|quasi-categories]]. 
An **adjunction** between $C$ and $D$ is 

* a morphism of [[simplicial set]]s $K \to \Delta^1$

* which is

  * a [[Cartesian fibration]]

  * a [[coCartesian fibration]]

* such that $C \simeq K_{0}$ and $D\simeq K_{1}$.

=--

For more on this see 

* [[adjoint (∞,1)-functor]].


#Examples#

* see [[examples of adjoint functors]].


#Properties#

Let $L \dashv R$ be a pair of adjoint functors. We have the following

* ($R$ is [[full and faithful functor|full and faithful]])
  $\Leftrightarrow$ ($\epsilon : L \circ R \stackrel{\simeq}{\to} Id_D$)

* ($L$ is [[full and faithful functor|full and faithful]]) $\Leftrightarrow$ ($\eta : Id_C \stackrel{\simeq}{\to} R \circ L$)

* the following are equivalent

  * $L$ and $R$ are both [[full and faithful functor|full and faithful]];

  * $L$ is an [[equivalence of categories|equivalence]];

  * $R$ is an [[equivalence of categories|equivalence]];


#Videos#

* The Catsters [list](http://www.youtube.com/view_play_list?p=54B49729E5102248)


[[!redirects adjoint functors]]
[[!redirects adjoint pair of functors]]