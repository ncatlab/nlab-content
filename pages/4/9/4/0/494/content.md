<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition 

We say that two functors $L:C\to D$ and $R:D\to C$ are **adjoint** if they form an [[adjunction]] $L \dashv R$ in the [[2-category]] [[Cat]] of categories.  This means that they are equipped with [[natural transformations]] $\eta: 1_C \to R \circ L$ and $\epsilon: L \circ R \to 1_D$ satisfying the [[triangle identities]], that is the compositions
$L \stackrel{L\eta}\to L R L\stackrel{\epsilon L}\to L$
and 
$R\stackrel{\eta R}\to R L R \stackrel{R\epsilon}\to R$ 
are identities.
The left or right adjoint of any functor, if it exists, is [[generalized the|unique up to unique isomorphism]].

We say that $L$ is the __[[left adjoint]]__ of $R$ and that $R$ is the __[[right adjoint]]__ of $L$.

In the case of [[Cat]], there are a number of equivalent characterizations of an adjunction, some of which are given below.


### In terms of Hom isomorphism

An adjunction $L\dashv R$ is equivalently given by a [[natural transformation|natural isomorphism]] of [[hom-functors]] $C^{op} \times D \to Set$

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


### In terms of representable functors

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

#### Local definition 

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


### In terms of universal arrows / universal factorization through unit and counit {#UniversalArrows}

Given $R : D\to C$, and $c\in C$, a _universal arrow_ from $c$ to $R$ is an [[initial object]] of the [[comma category]] $(c/R)$.  That is, it consists of an object $L(c)\in D$ and a morphism $i_c : :c\to R(L(c))$ -- the unit -- such that for any $d\in D$, any morphism $f : c\to R(d)$ factors through the unit $i_c$ as 

$$
  \array{
    && c 
    \\
    & {}^{\mathllap{i_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R L c &&\underset{R \tilde f}{\to}&& R d
    \\
    \\
    L c &&\underset{\tilde f}{\to}&& d
  }
$$

for a unique $\tilde f:L(c)\to d$ -- the [[adjunct]] of $f$.  

In particular, we have a bijection

$$
  Hom_C(c,R(d)) \cong Hom_D(L(c),d)
$$

which it is easy to see is [[natural isomorphism|natural]] in $d$.  Again, in this case there is a unique way to make $L$ into a functor so that this isomorphism is natural in $c$ as well.

Note that this definition is simply obtained by applying the [[Yoneda lemma]] to the definition in terms of representable functors.


To derive this characterization starting with a natural hom-isomorphism $Hom_{C}(L(-),-) \stackrel{\simeq}{\to} Hom_D(-,R(-))$ let $\tilde f : L c \to d$ be the image of $f : c \to R d$ under the bijection $Hom_C(c, R d) \stackrel{\simeq}{\to} Hom_D(L c, d)$ and consider the naturality square

$$
  \array{
    c , L c &&&& Hom_D(L c, L c) &\stackrel{\simeq}{\to}& Hom_C(c, R L c)
    \\
    \uparrow^{\mathrlap{Id}}, \downarrow^\mathrlap{\tilde f} 
    &&&&
    \downarrow && \downarrow^{\mathrlap{R (\tilde f)\circ(-) }}
    \\
    c, d
    &&&&
    Hom_D(L c, d) &\stackrel{\simeq}{\to}& Hom_C(c, R d)
  }
  \,.
$$

Let also the unit $i_c : c \to R L c$ be the image of the [[identity]] $Id_{L c}$ under the hom-isomorphism and chase this identity through the commuting diagram to obtain

$$
  \array{
    (L c \stackrel{Id_{L c}}{\to} L c) &\mapsto& 
     (c \stackrel{i_x}{\to} R L c)
    \\
    \downarrow && \downarrow
    \\
    (L c \stackrel{\tilde f}{\to} d) &\mapsto& 
    (f : c \stackrel{i_c}{\to} R L c \stackrel{R \tilde f}{\to} R d) 
  }
  \,.
$$

**Example** This definition in terms of universal factorizations through the unit and counit is of particular interest in the case that $R$ is a [[full and faithful functor]] exhibiting $D$ as a [[reflective subcategory]] of $C$. In this case we may think of $L$ as a [[localization]] and of objects in the essental image of $R$ as **local objects**. Then the above says that:

* every morphism $c \to R d$ from $c$ into a local object factors throught the localization of  $c$.




### In terms of cographs/correspondences 

Every [[profunctor]]

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

Now, every functor $L : C \to D$ induces a [[profunctor]]

$$
  k_f(X,Y) = Hom_D(f(X), Y)
$$

and every functor $R : D \to C$ induces a [[profunctor]]

$$
  k_g(X,Y) = Hom_C(X, R(Y))
  \,.
$$

The functors $L$ and $R$ are adjoint precisely if the [[profunctors]] that they define in the above way are equal. This in turn is the case if
$C \star^L D \simeq (D^{op} \star^{R^{op}} C^{op})^{op}$.

We say that $C \star^k D$ is the [[cograph of a functor|cograph of the functor]] $k$. See there for more on this.

### For $(\infty,1)$-functors 


The above characterization of adjoint functors in terms of categories over the interval is used in section 5.2.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

(motivated from the discussion of correspondences in section 2.3.1) 

to give a definition of adjunction between [[(infinity,1)-functors]]. 

+-- {: .un_defn}
###### Definition

Let $C$ and $D$ be [[quasi-category|quasi-categories]]. 
An **adjunction** between $C$ and $D$ is 

* a morphism of [[simplicial sets]] $K \to \Delta^1$

* which is

  * a [[Cartesian fibration]]

  * a [[coCartesian fibration]]

* such that $C \simeq K_{0}$ and $D\simeq K_{1}$.

=--

For more on this see 

* [[adjoint (∞,1)-functor]].




## Properties



Let $L \dashv R$ be a pair of adjoint functors. We have the following

* ($R$ is [[full and faithful functor|full and faithful]])
  $\Leftrightarrow$ ($\epsilon : L \circ R \stackrel{\simeq}{\to} Id_D$)

* ($L$ is [[full and faithful functor|full and faithful]]) $\Leftrightarrow$ ($\eta : Id_C \stackrel{\simeq}{\to} R \circ L$)

* the following are equivalent

  * $L$ and $R$ are both [[full and faithful functor|full and faithful]];

  * $L$ is an [[equivalence of categories|equivalence]];

  * $R$ is an [[equivalence of categories|equivalence]].

* $L$ [[preserved limit|preserves]] all [[colimits]] that may exist in $C$, while $R$ preserves all [[limits]] in $D$.  For a partial converse, see the [[adjoint functor theorem]].





## Examples {#Examples}


* A pair of adjoint functors $(L \dashv R)$ where $R$ is a [[full and faithful functor]] exhibits a [[reflective subcategory]]. 

  In this case $L$ may be regarded as a [[localization]]. The fact that the adjunction provides universal factorization through unit and counit in this case means that every morphism $f : c \to R d$ into a local object factors through the localization of $c$.

* A pair of adjoint functors that is also an [[equivalence of categories]] is called an [[adjoint equivalence]].

* A pair of adjoint functors where $C$ and $D$ have finite [[limit]]s and $L$ preserves these finite limits is a [[geometric morphism]]. These are one kind of morphisms between [[topos]]es. If in addition $R$ is full and faithful, then this is a [[geometric embedding]].

* The left and right adjoint functors $p_!$ and $p_*$ (if they exist) to a functor $p^* : [K',C] \to [K,C]$ between [[functor categories]] obtained by precomposition with a functor $p : K' \to K$ of [[diagram]] categories are called the left and right [[Kan extension]] functors along $p$

  $$
    (Lan_p \dashv p^* \dashv Ran_p)
    :=
    (p_1 \dashv p^* \dashv p*) : 
    [K,C]
     \stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}}}
    [K',C]
    \,.
  $$

  If $K' = {*}$ is the [[terminal category]] then this are the [[limit]] and [[colimit]] functors on $[K,C]$.

  If $C = $ [[Set]] then this is the [[direct image]] and [[inverse image]] operation on [[presheaves]].


* if $R$ is regarded as a [[forgetful functor]] then its left adjoint $L$ is a regarded as a [[free functor]].


* If $C$ is a category with small [[colimit]]s and $K$ is a [[small category]] (a [[diagram]] category)  and $Q : K \to C$ is any functor, then this induces a [[nerve and realization]] pair of adjoint functors

  $$
    (|-|_Q \dashv N_Q) : C \stackrel{\overset{|-|_Q}{\leftarrow}}{\underset{N_Q}{\to}}
    [K^{op}, Set]
  $$

  between $C$ and the [[category of presheaves]] on $K$, where

  * the [[nerve]] functor is given by

    $$
      N_Q(c) := Hom_C(Q(-),c) : k \mapsto Hom_C(Q(k),c)
    $$

  * and the realization functor is given by the [[coend]]

    $$
      |F|_Q := \int^{k \in K} Q(k)\cdot F(k)
      \,,
    $$

    where in the integrand we have the canonical [[copower|tensoring]] of
    $C$ over [[Set]] ($Q(k) \cdot F(k) = \coprod_{s \in F(k)} Q(k)$).

  A famous examples of this is obtained for $C = $ [[Top]], $K = \Delta$
  the [[simplex category]] and $Q : \Delta \to Top$ the functor that sends
  $[n]$ to the standard topological $n$-[[simplex]]. In this case
  the nerve functor is the 
  [[fundamental infinity-groupoid|singular simplicial complex]] functor
  and the realization is ordinary [[geometric realization]].

## References

A video of a pedagogical introduction to adjoint functors is provided by

* [[The Catsters]] ([list](http://www.youtube.com/view_play_list?p=54B49729E5102248))


[[!redirects adjoint functors]]
[[!redirects adjoint pair of functors]]
[[!redirects universal arrow]]
[[!redirects universal arrows]]
