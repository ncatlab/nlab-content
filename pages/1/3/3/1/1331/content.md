
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The notion of  _reflective $(\infty,1)$-subcategory_ is the generalization of the notion of [[reflective subcategory]] from [[category theory]] to [[(∞,1)-category]] theory.

## Definition 

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

Let $C$ be a [[presentable (∞,1)-category]] and $S$ a small collection of morphisms of $C$. Let $\bar S$ denote the [[strongly saturated class of morphisms]] generated by $S$. Let $C' \hookrightarrow C$ be denote the full [[sub-quasi-category|sub-(∞,1)-category]] consistsing of $S$-[[local objects]]. Then 

* For each object $c \in C$ there exists a morphism $s : C \to C'$ such that $C'$ is $S$-local and s belongs to $\bar S$.

* $C'$ is a [[presentable (∞,1)-category]]

* $C' \hookrightarrow C$ is a [[reflective (∞,1)-subcategory]].

* For every morphism $f$ of $C$ the following are equivalent:

  * the morphism $f$ is an $S$-equivalence;

  * the morphism $f$ belongs to $\bar S$;

  * for $L : C \to C'$ the [[localization of an (infinity,1)-category|localization functor]] left adjoint to $C' \hookrightarrow C$ the induced morphism $L f$ is an equivalence.

=--


This is [[Higher Topos Theory|HTT, prop. 5.5.4.15]]


[[!redirects reflective (infinity,1)-subcategories]]
[[!redirects reflective (∞,1)-subcategory]]
[[!redirects reflective (∞,1)-subcategories]]