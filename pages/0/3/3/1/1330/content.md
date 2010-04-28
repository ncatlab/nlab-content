
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _[[localization]]_ of an [[(∞,1)-category]] $C$ is a functor $L : C \to C_0$ to an $(\infty,1)$-subcategory $C_0 \hookrightarrow C$ such that with $c$ any object there is a morphism connecting it to its localization 

$$
  c \to L(c)
$$

in a suitable way. This "suitable way" just says that 
$f$ is left adjoint to the fully faithful inclusion functor.


Since localizations are entirely determined by which morphisms in $C$ are sent to equivalences in $C_0$, they can be thought of as sending $C$ to the result of "inverting" all these morphisms, a process familiar from forming the [[homotopy category]] of a [[homotopical category]].


For more details see [[reflective (∞,1)-subcategory]]

## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-functor]] $L : C \to C_0$ is called a **localization** of the [[(∞,1)-category]] $C$ if it has a right [[adjoint (∞,1)-functor]] $i : C_0 \hookrightarrow C$ that is [[full and faithful (∞,1)-functor|full and faithful]].

$$
  (L \dashv i) : C_0 \stackrel{\overset{L}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  C
  \,.
$$

In other words: $L$ is a localization if it is the **reflector** of a [[reflective (∞,1)-subcategory]] $C_0 \hookrightarrow C$.

=--

This is [[Higher Topos Theory|HTT, def. 5.2.7.2]].


## Properties

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

be the corresponding localization [[(∞,1)-monad]]. Write $S \subset Mor(C)$ for the collection of morphisms that $L$ sends to [[equivalence in a quasi-category|equivalences]].

Then

* an object $c \in C$ is an $S$-[[local object]] precisely if it is in essential image of $L$ (equivalent to an object of the form $Loc x$);

* every $S$-[[local morphism]] is already in $S$.



=--


+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop 5.5.4.2]]. The reasoning is entirely analogous to the 1-categorical case (see for instance [[reflective subcategory]]).


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

which in total is given by precomposition with the unit $i_z : z \to L z $ of the adjunction.

If $z$ is itself in the image of $Loc$, then this means that precomposition with the unit $z \to Loc z$ is an isomorphism in the [[homotopy category of an (infinity,1)-category|homotopy]] of $Loc C$, hence by the [[Yoneda lemma]] is itself an isomorphism in the homotopy category, hence $i_z : z \to Loc z$ is a weak equivalence if $z$ is itself in the image of $Loc$.

Applying this statement to the commuting square

$$
  \array{
    s &\stackrel{i_s}{\to} & L s
    \\
    \downarrow && \downarrow^{\mathrlap{Loc i_s}}
    \\
    Loc s &\stackrel{i_{Loc s}}{\to}& Loc Loc s
  }
$$

and using that precomposition with $i_s$ gives an equivalence here (by the above) we find that $Loc i_s \simeq i_{Loc s}$ is a weak equivalence, and hence that $i_s$ is in $S$, for all $s \in C$.

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

Conversely, to show that for $s \in C$ an $S$-local object, we have that $s$ is int he essential image of $Loc$ use that since $i_s : s \to Loc s$ is in $S$, we have an equivalence  $Hom_C(i_s, s) : Hom_C(Loc s, s) \stackrel{\simeq}{\to} Hom_C(s,s)$.  The pre-image of the identity under this equivalence is hence a left-inverse $Loc s \to s$ of $s \to Loc s$. 


...

=--



## Examples

* Locaizations of $(\infty,1)$-categories are modeled by the notion of left [[Bousfield localization of model categories]]. 

  One precise statement is: localizations of [[(∞,1)-category of (∞,1)-presheaves]] $C = PSh_{(\infty,1)}(K)$ are [[presentable (∞,1)-category|presented]] by the left Bousfield localizations of the global projectibe [[model structure on simplicial presheaves]] on the [[simplicial category]] incarnation of $K$.

* [[∞-stackification]] is the localization of an [[(∞,1)-category]] of [[(∞,1)-presheaves]] to the $(\infty,1)$-subcategory [[(infinity,1)-category of (infinity,1)-sheaves|of (∞,1)-sheaves]].


## References

This is the topic of section 5.2.7  and 5.5.4 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects localization of an (∞,1)-category]]
[[!redirects localisation of an (infinity,1)-category]]
[[!redirects localization of an (∞,1)-category]]
[[!redirects localizations of an (infinity,1)-category]]
[[!redirects localizations of an (∞,1)-category]]
[[!redirects localisations of an (infinity,1)-category]]
[[!redirects localizations of an (∞,1)-category]]
[[!redirects localizations of (infinity,1)-categories]]
[[!redirects localizations of (∞,1)-categories]]
[[!redirects localisations of (infinity,1)-categories]]
[[!redirects localizations of (∞,1)-categories]]
[[!redirects localization of (infinity,1)-categories]]
[[!redirects localization of (∞,1)-categories]]
[[!redirects localisation of (infinity,1)-categories]]
[[!redirects localization of (∞,1)-categories]]