
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The notion of  _reflective $(\infty,1)$-subcategory_ is the generalization of the notion of [[reflective subcategory]] from [[category theory]] to [[(∞,1)-category]] theory.

## Definition 


### Reflective $(\infty,1)$-subcategory

A [[full and faithful (∞,1)-functor]]

$$
  R : D \hookrightarrow C
$$

exhibits $D$ as a **reflective $(\infty,1)$-subcategory** (of $C$) if it has a left [[adjoint (∞,1)-functor]] $L : C \to D$.

$$
  (L \dashv R) : D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}}
  C
  \,.
$$


The [[(∞,1)-functor]] $R$ or its composite 

$$
  Loc := R \circ L : C \to C
$$ 

may be understood as exhibiting a [[localization of an (∞,1)-category]].


### Local objects and local morphisms

One finds, as discussed [below](#Properties), that reflective subcategories may be entirely characterized by the class of morphisms that the localization functor $Loc : C \to C$ sends to weak equivalences.


+-- {: .un_def}
###### Definition
**(local objects, local equivalences)**

Let $S \subset Mor(C)$ be a class of morphisms. 

* An object $c \in C$ is called an **$S$-[[local object]]** if for all morphisms $f : x \to y$ in $C$ the induced morphism

  $$
    Hom_C(f,c) : Hom_C(y,c) \to Hom_C(x,c)
  $$

  is an equivalence (of [[∞-groupoid]]s).

* An morphism $f : x \to y$ in $C$ is called an **$S$-[[local morphism]]** or **$S$-[[local equivalence]]** if for all $S$-[[local object]]s $c  \in C$ we have that 

  $$
    Hom_C(f,c) : Hom_C(y,c) \to Hom_C(x,c)
  $$

  is an equivalence (of [[∞-groupoid]]s).


=--

Notice that the class of $S$-equivalences always contains $S$ itself. Hence passing from a collection $S$ to its class $\bar S$ of $S$-equivalences is a kind of saturation procedure. This is formalized by the following definition, whose justification is given by the propositions [below]{#Properties}.

+-- {: .un_def}
###### Definition
**(strongly saturated class of morphisms)**


For $C$ an [[(∞,1)-category]] with small [[limit in a quasi-category|colimits]], a class $S \subset C_1$ of morphisms in $C$ is said to be **strongly saturated** if its satisfies the following three conditions

1. It is stable under [[pushout]]s;

1. The full [[sub-quasi-category|subcategory]] of the [[(∞,1)-category of (∞,1)-functors]] $Func(\Delta[1], C)$ on $S$ has all colimits;

1. it satisfies the [[category with weak equivalences|2-out-of-3 property]].

=--

Notice that this definition has some immediate consequences:

The identity $Id_\emptyset$ on the [[initial object]] of $C$, which is the initial object in $Func(\Delta[1],C)$ is in $S$, since it is the colimit of the empty diagram. Moreover, every [[equivalence in a quasi-category|equivalence]] is a [[pushout]] of $Id_{\emptyset}$$ so

* A strongly saturated class contains every [[equivalence in a quasi-category|equivalence]].

Given any collection $\{S_i\}_i$ of strongly saturated classes of morphisms in $C$, their intersection is clearly also strongly saturated. Therefore for every collection $S$ of morphisms, there is a smallest strongly saturated class $\bar S$ containing it. We say that $S$ **generates** the strongly saturated class $\bar S$. If $S$ is a [[small set]], then $\bar S$ is said to be **of small generation**. 

The smallest strongly saturated class of morphism in $C$ is that containing only the equivalences of $C$.

Of importance are the strongly saturated classes arising as follows.

+-- {: .un_lemma}
###### Lemma


For $C$ and $D$ two $(\infty,1)$-categories that have small colimits, and for $F : C \to D$ an [[(∞,1)-functor]] that preserves small colimits, given a strongly saturated class of morphisms $S$ in $D$, its preimage $F^{-1}(S)$ is a strongly saturated class in $C$.


In particular the class of morphisms in $C$ sent to equivalences by $F$ is strongly saturated.

=--


+-- {: .un_lemma}
###### Lemma

The class of $S_0$-[[local equivalence]]s for $S_0$ any class of morphisms is strongly saturated.

=--

+-- {: .proof}
###### Proof


For each object $c \in C$ let $j(c) : C \to \infty Grpd^{op}$ be the functor [[representable functor|represented]] by $c$. Let $S_c$ be the class of morphisms sent by $j(c)$ to weak equivalences in [[∞Grpd]]. Since $j(c)$ preserves small colimits, this is a strongly saturated class, by the above lemma. Now observe that $S$ is the intersection $S = \cap_c S_c$ where $c$ ranges over the $S_0$-[[local object]]s.

=--


In the following this language of local morphisms is used to characterize reflect $(\infty,1)$-subcategories.

## Properties {#Properties}


The following proposition asserts that localizations are entirely determined by the corresponding [[local object]]s.

+-- {: .un_prop}
###### Proposition

Let 

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} C
$$

be a localization of the $(\infty,1)$-category $C$ and let 

$$
  Loc : C \stackrel{L}{\to} D \overset{R}{\hookrightarrow} C
$$

be the corresponding localization [[(∞,1)-monad]]. Write $S \subset Mor(C)$ for the collection of morphisms that $Loc$ sends to [[equivalence in a quasi-category|equivalences]].

Then

* an object $c \in C$ is an $S$-[[local object]] precisely if it is in essential image of $Loc$ (equivalent to an object of the form $Loc x$);

* every $S$-[[local morphism]] is already in $S$.



=--


+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop 5.5.4.2]]. The reasoning is entirely analogous to the 1-categorical case (see for instance [[localization]], [[reflective subcategory]] and [[geometric embedding]]).


First notice the following general statements about the unit $i : Id_C \to Loc$.
Recall that by the assumption that $D \hookrightarrow C$ is a [[full and faithful (∞,1)-functor]] we have that the counit $L R \to Id_D$ is an equivalence. 

From this it follows by repeatedly using the 
hom-equivalence defining [[adjoint (∞,1)-functor]]s that for $z,x \in C$ 
we have an equivalence

$$
  \begin{aligned}
    Hom_C(Loc z, Loc x)
    &=
    Hom_C(R L z, R L x)
    \\
    & \simeq
    Hom_D(L R L z, L x)
    \\
    & \simeq
    Hom_D(L z, L x)
    \\
    & \simeq
    Hom_C(z, Loc x)
  \end{aligned}
$$

which in total is given by precomposition with the unit $i_z : z \to Loc z $ of the adjunction.

If $z$ is itself in the image of $Loc$, then this means that precomposition with the unit $z \to Loc z$ is an isomorphism on [[hom-set]]s in the [[homotopy category of an (infinity,1)-category|homotopy category]] of $Loc C$, hence by the [[Yoneda lemma]] is itself an isomorphism in the homotopy category, hence $i_z : z \to Loc z$ is a weak equivalence if $z$ is itself in the image of $Loc$.

Applying this statement to the commuting square

$$
  \array{
    s &\stackrel{i_s}{\to} & Loc s
    \\
    \downarrow && \downarrow^{\mathrlap{Loc i_s}}
    \\
    Loc s &\stackrel{i_{Loc s}}{\to}& Loc Loc s
  }
$$

and using that precomposition with $i_s$ gives an equivalence here (by the above) we find that $Loc i_s \simeq i_{Loc s}$, hence that $Loc i_s$ is a weak equivalence, and hence that $i_s$ is in $S$, for all $s \in C$.

Now to show that for all $x \in X$ the object $Loc x$ is $S$-local, let $f : y \to z$ be in $S \subset Mor(C)$ and consider the induced square

$$
  \array{
    Hom_C(Loc z, Loc x) &\stackrel{\simeq}{\to}& Hom_C(Loc y, Loc x)
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_C(z, Loc x) &\to& Hom_C(y, Loc x)
  }
  \,.
$$

Here the vertical morphisms are equivalences by the above remark, and the top morphism is an equivalence by the assumoption that $f$ in in $S$. It follows that the bottom morphism is an equivalence. This says that $Loc x$ is $S$-local, for all $x \in C$.

Conversely, to show that for $s \in C$ an $S$-local object, we have that $s$ is in the essential image of $Loc$ use that since $i_s : s \to Loc s$ is in $S$, we have an equivalence  $Hom_C(i_s, s) : Hom_C(Loc s, s) \stackrel{\simeq}{\to} Hom_C(s,s)$.  The pre-image of the identity under this equivalence is hence a left-inverse $Loc s \to s$ of $s \to Loc s$. But this means that $Loc s \to s$ is itself in $S$ (since the morphisms in $S$ evidently satisfy [[category with weak equivalences|2-out-of-three]]), hence by applying the same argument again, we find that the left inverse $Loc s \to s$ has itself a left inverse. That implies that it is actually an inverse of $s \to Loc s$, hence that this is an equivalence. So this shows that the $S$-local $s$ is indeed in the essential iamge of $Loc$.


Finally, to show that every $S$-local morphism is already in $S$, let $f : x \to y$ be such an $S$-local morphism and consider the square

$$
  \array{
    x &\stackrel{f}{\to}& y
    \\
    \downarrow^{\mathrlap{i_x}} && \downarrow^{\mathrlap{i_y}}
    \\
    Loc x &\stackrel{Loc f}{\to}& Loc y
  }
  \,.
$$

By the above we know now that the vertical morphisms here are also $S$-local. It follows that the image of $Loc f : Loc x \to Loc y$ on the homtopy category of $Ho(Loc C)$ corepresents an isomorphism, hence by the [[Yoneda lemma]] that $Lof f$ is a weak equivalence. Hence $f$ is indeed in $S$.


=--


One can turns this around and define or construct reflective $(\infty,1)$-subcategories by specifying collections of local morphisms.



+-- {: .un_prop}
###### Proposition

Let $C$ be a [[presentable (∞,1)-category]] and $S$ a small collection of morphisms of $C$. 

Then the full [[sub-quasi-category|sub-(∞,1)-category]] 

$$
  R : D \hookrightarrow C
$$ 

on $S$-[[local object]]s is a reflective $(\infty,1)$-subcategory. 

If $L : C \to D$ denotes the left [[adjoint (∞,1)-functor]] of the inclusion, then for $f \in Mor(C)$ a morphism, the following are equivalent

* $f$ is an $S$-[[local equivalence]];

* $f$ belongs to the stringly saturated class $\bar S$ generated by $S$;

* the morphism $L f$ is an equivalence.



=--

+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop. 5.5.4.15]]



=--


[[!redirects reflective (infinity,1)-subcategories]]
[[!redirects reflective (∞,1)-subcategory]]
[[!redirects reflective (∞,1)-subcategories]]