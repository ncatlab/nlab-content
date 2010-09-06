
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

> This entry originates from the personal web of [[Urs Schreiber]] as a section of the page [[schreiber:differential cohomology in an (∞,1)-topos -- examples]]. It was moved here when [[Domenico Fiorenza]] indicated inclination to join in the work on [[∞-Chern-Weil theory]]. See also there.

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[ordinary differential cohomology|Ordinary differential cohomology]] is well known to be modeled by

1. [[Cheeger-Simons differential character]]s;

1. [[Deligne cohomology]];\p

1. abelian $n$-[[nLab:gerbe]]s ([[nLab:bundle gerbe]]s) with connection.

In degree 2 it classifies ordinary [[nLab:circle group]]-[[nLab:principal bundles]] [[nLab:connection on a bundle|with connection]].

We discuss here how this ordinary differential cohomology theory is reproduced as the [[schreiber:differential cohomology in an (∞,1)-topos|intrinsic differential cohomology]] of the [[(∞,1)-topos]] $\mathbf{H} = $ [[nLab:?LieGrpd]] with coefficients in the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle Lie n-groups</a> $\mathbf{B}^{n+1} U(1)$. We may think of this as describing connections on $\mathbf{B}^n U(1)$-[[nLab:principal ∞-bundle]]s in $\infty Lie Grpd$ in the sense described in detail at [[∞-Chern-Weil theory]].



## Flat $U(1)$-valued differential cohomology {#FlatCircleCohomology}

The <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#LocalSystem">coefficient object for flat differential cohomology</a> in $\mathbf{H} = \infty LieGrpd$ with values in $\mathbf{B}^n U(1)$ is $\mathbf{\flat} \mathbf{B}^n U(1) = LConst \Gamma \mathbf{B}^n U(1)$. 

The <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#IntrinsicForms">coefficient object for intrinsic de Rham cohomology</a> is $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$, defined by the [[nLab:(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} \mathbf{B}^n U(1) &\to&
    \mathbf{\flat} \mathbf{B}^n U(1)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}^n U(1)
  }
  \,.
$$

The following proposition provides models for these objects in in terms of ordinary [[nLab:differential form]]s.

+-- {: .un_prop }
###### Proposition

A fibrant representative in $[CartSp^{op}, sSet]_{proj,cov}$ of $\mathbf{\flat} \mathbf{B}^n U(1)$ is

$$
  \mathbf{\flat}\mathbf{B}^n U(1)_{chn}
  :=
  \Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]
  \,,
$$

and a fibrant representative of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}
  :=
  \Xi[0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]
  \,.
$$

=--

Notice that the complex of sheaves $\mathbf{\flat}\mathbf{B}^n U(1)$ is that which defines _flat_ [[nLab:Deligne cohomology]], while that of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is essentially that which defines [[nLab:de Rham cohomology]] in degree $n \gt 1$ (see [below](#OrdinaryDeRham)).


+-- {: .proof}
###### Proof

Since the [[nLab:global section]] functor $\Gamma$ amounts to evaluation on the  point $\mathbb{R}^0$ and since constant simplicial presheaves on [[nLab:CartSp]] satisfy [[nLab:descent]] (on objects in $CartSp$!), we have that $\mathbf{\flat} \mathbf{B}^n U(1)$ is represented by the complex of sheaves $\Xi[const U(1) \to 0 \to \cdots \to 0]$. This is weakly equivalent to $\Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]$ by the [[nLab:Poincare lemma]] applied to each [[nLab:Cartesian space]] (using the same standard logic that proves the [[nLab:de Rham theorem]]) in that the degreewise inclusion

$$
  \array{
    const U(1) &\to& 0 &\to& \cdots &\to& 0
    \\
    \downarrow && \downarrow && && \downarrow
    \\
    C^\infty(-,U(1)) &\stackrel{d_{dR}}{\to}&     
    \Omega^1(-) &\to& \cdots &\to& \Omega^n_{cl}(-)
  }
$$

is objectwise a [[nLab:quasi-isomorphism]].

Therefore a fibration in $[CartSp^{op}, sSet]_{proj}$ representing the counit $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^n U(1)$ is the image under $\Xi$ of

$$
  \array{
    C^\infty(-,U(1)) &\to& \Omega^1(-) &\to & \cdots &\to& \Omega^n_{cl}(-)
    \\
    \downarrow^{\mathrlap{=}} && \downarrow && && \downarrow
    \\
    C^\infty(-, U(1)) &\to& 0 &\to& \cdots &\to& 0
  }
  \,.
$$

We observe that the [[nLab:pullback]] of this morphism to the point

$$
  \array{
    \Xi[0 \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    &\to&
    \Xi[C^\infty(-,U(1)) \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    \\
    \downarrow && \downarrow
    \\
    \Xi[0 \to 0 \to \cdots \to 0]
    &\to&
    \Xi[C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
  }
$$

is the pullback over a cospan all whose objects are fibrant and one of whose morphisms is a fibration. Therefore this is a [[nLab:homotopy pullback]] diagram in $[CartSp^{op}, sSet]_{proj}$ which models the [[nLab:(∞,1)-limit]] over $* \to \mathbf{B}^n U(1) \leftarrow \mathbf{\flat}\mathbf{B}^n U(1)$ in $PSh_{(\infty,1)}(CartSp)$. Since [[nLab:∞-stackification]] preserves finite $(\infty,1)$-limits this models also the corresponding $(\infty,1)$-limit in $\mathbf{H}$. Therefore the top left object is indeed a model for $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$.

=--

## Ordinary de Rham cohomology in degree $\gt 1$ {#OrdinaryDeRham}

The intrinsic de Rham cohomology of [[nLab:?LieGrpd]] with coefficients in $\mathbb{R}$ or $U(1) = \mathbb{R}/\mathbb{Z}$ coincides with the ordinary [[nLab:de Rham cohomology]] of [[nLab:smooth manifold]]s and smooth [[nLab:simplicial manifold]]s in degree greater than 1. This we discuss here. The meaning of the discrepancy in degee 1 and lower is discussed [below](#U1GroupoidBundle).

So for this section let $n \in \mathbb{N}$ with $n \geq 2$.

Above in _[Flat U(1)-valued differential cohomology](#FlatCircleCohomology)_ we found a fibrant representative of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1) \in \infty LieGrpd$ to be given by 

$$
  \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2(-)
  \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)]
$$ 

in $[CartSp^{op}, sSet]_{proj, cov}$. 

+-- {: .un_prop }
###### Proposition

For $X \in \infty LieGrpd$ a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] we have in for $\mathbf{H} = \infty LieGrpd$ a 
[[nLab:natural isomorphism]]

$$
  H_{dR}(X,\mathbf{B}^n U(1))
  :=
  \pi_0 \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  H_{dR}^n(X)
  \,,
$$ 

where on the left we have the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#deRham">intrinsic (∞,1)-topos theoretic notion of de Rham cohomology</a>, and on the right the ordinary  notion of [[nLab:de Rham cohomology]] of a smooth manifold.

=--

+-- {: .proof}
###### Proof

Let $\{U_i \to X\}$ be a [[nLab:good open cover]]. At [[nLab:?LieGrpd]] is discussed that then the [[nLab:Cech nerve]] $C(\{U_i\}) \to X$ is a cofibrant [[nLab:resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,cov}$. Therefore we have

$$
  \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  [CartSp^{op}, sSet](C(\{U_i\}), \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)])
  \,.
$$

The right hand is the $\infty$-groupoid of cocylces in the [[nLab:Cech cohomology|Cech]] [[nLab:hypercohomology]] of the complex of sheaves of differential forms. A cocycle is given by a collection

$$
  (C_i, B_{i j}, A_{i j k}, \cdots  , Z_{i_0, \cdots, i_n})
$$

of differential forms, with $C_i \in \Omega^n_{cl}(U_i)$, $B_{i j} \in \Omega^{n-1}(U_i \cap U_j)$, etc. , such that this collection is annihilated by the total differentoal $D = d_{dR} \pm \delta$, where $d_{dR}$ is the de Rham differential and $\delta$ the alternating sum of the pullbacks along the face maps of the [[nLab:Cech nerve]].

It is a standard result of [[nLab:abelian sheaf cohomology]] that such cocycles represent classes in de Rham cohomology. 

But for the record and since the details of this computation will show up again at some mildly subtle points in further discussion below, we spell this out in some detail.

We can explicitly construct coboundaries connecting such a generic cocycle to one of the form 

$$
  (F_i, 0, 0, \cdots, 0)
$$

by using a [[nLab:partition of unity]] $(\rho_i \in C^\infty(X))$ subordinate to the cover $\{U_i \to X\}$, i.e. $x \in U_i \Rightarrow \rho_i(x) = 0$ and $\sum_i \rho_i = 1$.

For consider 

$$
  \begin{aligned}
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}, Z_{i_1, \cdots, i_{n+1}})
     \\
     + & D (0, 0, \cdots, \sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}},0)
     \\
     =
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}
     + d_{dR}\sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}}, 0)   
  \end{aligned}
  \,,
$$

where we use that from $(\delta Z)_{i_1, \cdots, i_{n+2}} = 0$ it follows that

$$
  \begin{aligned}
    (\delta \sum \rho Z)_{i_1, \cdots, i_{n+1}}
    &=
    \sum_{i_0} \rho_{i_0}
    \sum_{k = 1}^{n+1}
    (-1)^k
    Z_{i_0, i_1 \cdots, \hat i_k, \cdots, i_{n+1}}
    \\
    & =
    \sum_{i_0} \rho_{i_0}
    Z_{i_1 ,\cdots, i_{n+1}}    
    \\
    & =
    Z_{i_1 ,\cdots, i_{n+1}}
  \end{aligned}
  \,.
$$

> where I am suppressing some evident signs...

By recurseively adding coboundaries this way, we can annihilate all the higher Cech-components of the original cocycle and arrive at a cocycle of the form $(F_i, 0, \cdots, 0)$. 

Such a cocycle being $D$-closed says precisely that $F_i = F|_{U_i}$ for $F \in \Omega^n_{cl}(X)$ a globally defined closed differential form. Moreover, coboundaries between two cocycles both of this form 

$$
  (F_i, 0, \cdots , 0) = (F'_i, 0, \cdots, 0) + D(\lambda_i, \lambda_{i j}, \cdots)
$$

are necessarily themselves of the form $(\lambda_i, \lambda_{i j}, \cdots) =  (\lambda_i, 0 ,\cdots, 0)$ with $\lambda_i = \lambda|_{U_i}$ for $\lambda \in \Omega^{n-1}(X)$ a globally defined differential $n$-form and $F = F' + d_{dR} \lambda$.

=--



## Curved $U(1)$-valued differential cohomology


The intrinsic <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#DiffCohWithGroupalCoeffs">definition of the ∞-groupoid of cocycles for the intrinsic  differential cohomology</a> in $\mathbf{H} = \infty LieGrpd$ with coefficients $\mathbf{B}^n U(1)$ is the object $\mathbf{H}_{diff}(X,\mathbf{B}^n U(1))$ in the [[nLab:(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n U(1)) &\to & H_{dR}(X,\mathbf{B}^{n+1} U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$

in [[nLab:∞Grpd]].

We show now that for $n \geq 1$ this reproduces the [[nLab:Deligne cohomology]] $H(X,\mathbb{Z}(n+1)_D^\infty)$ of $X$:

{#DeligneCohomologyTheorem}
+-- {: .un_theorem }
###### Theorem

For $X$ a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] we have

$$
  H_{diff}(X,\mathbf{B}^n U(1))
  \simeq
  \left( 
     \;\; H(X,\mathbb{Z}(n+1)_D^\infty) \;\;
  \right)
  \times_{\Omega_{cl}^{n+1}(X)} H_{dR}^{n+1}_{int}(X)
  \,.
$$

=--

Here on the right we have the subset of Deligne cocycles that picks for each integral de Rham cohomology class of $X$ only one curvature form representative.

We give the proof [below](#ProofOfDeligneTheorem) after some preliminary expositional discussion.

+-- {: .un_remark }
###### Remark

The restriction to single representatives in each de Rham class is a reflection of the fact that in the above $(\infty,1)$-pullback diagram the morphism $H_{dR}(X,\mathbf{B}^{n+1}U(1)) \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}U(1))$ by definition picks one representative in each connected component. Using the [above model](#OrdinaryDeRham) of the intrinsic de Rham cohomology in terms of globally defined differential froms, we could easily get rid of this restriction by considering instead of the above $(\infty,1)$-pullback the homotopy pullback

$$
  \array{
    \mathbf{H}'_{diff}(X,\mathbf{B}^n U(1)) &\to & \Omega_{cl}^{n+1}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$

where now the right vertical morphism is the inclusion of the set of objects of our concrete model for the  $\infty$-groupoid $\mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))$. With this definition we get the isomorphism

$$
  H'_{diff}(X,\mathbf{B}^n U(1))
  \simeq
  H(X,\mathbb{Z}(n+1)_D^\infty)
  \,.
$$

From the tradtional point of view of differential cohomology this may be what one expects to see, but from the intrinsic $(\infty,1)$-topos theoretic point of view it is quite unnatural -- and in fact "[[nLab:evil]]" -- to fix that set of objects of the $\infty$-groupoid. Of intrinsic meaning is only the set of their equivalences classes.

=--



### Circle bundles with connection {#CircleBundlesConnection}

Before discussing [the full theorem](#DeligneCohomologyTheorem), it is instructive to start by looking at the special case $n=1$ in some detail, which is about ordinary  $U(1)$-[[nLab:principal bundle]]s [[nLab:connection on a bundle|with connection]]. 

This contains in it already all the relevant structure of the general case, but the low categorical degree is more transparently written out and will allow us to pause to highlight some maybe noteworthy aspects of the situation, such as the phenomenon of _pseudo-connections_ [below](#CircleBunlePseudoConnection).

In terms of the [Dold-Kan correspondence](#DoldKan) the object $\mathbf{B}U(1) \in \mathbf{H}$ is modeled in $[CartSp^{op}, sSet]$ by

$$
  \mathbf{B}U(1)
  =
  \Xi(\;
    C^\infty(-,U(1)) \to 0    
  \;)
  \,.
$$

Accordingly we have for the double [[nLab:delooping]] the model

$$
  \mathbf{B}^2 U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \to 0  \to 0    
  \;)
$$

and for the [[nLab:universal principal ∞-bundle|universal principal 2-bundle]]

$$
  \mathbf{E}\mathbf{B}U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-, U(1)) \to 0    
    \;
  )
  \,.
$$

In this notation we have also the constant presheaf

$$
  \mathbf{\flat} \mathbf{B}^2 U(1)
  = 
  \Xi(
    \;
     const U(1) \to 0 \to 0
    \;
  )  
  \,.
$$

Above we already found the model 

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  = 
  \Xi(0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))
  \,.
$$

In order to compute the differential cohomology 
$\mathbf{H}_{diff}(-,\mathbf{B}U(1))$ by an ordinary
pullback in [[nLab:sSet]] we also want to resolve the curvature characteristic morphism $\mathbf{B}U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ by a fibration. We claim that this may be obtained by choosing the resolution 
$\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B} U(1)_{diff,chn}$ given by

$$
  \mathbf{B}U(1)_{diff} 
  :=
  \Xi(
    \;
    C^\infty(-,U(1))
    \oplus
    \Omega^1(-)
    \stackrel{d_{dR} \oplus Id}{\to}
    \Omega^1(-)
    \;
  )
$$

with the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)$ given by

$$
  \array{
    C^\infty(-,U(1)) 
    \oplus
    \Omega^1(-)
    &\stackrel{d_{dR} + Id}{\to}&
    \Omega^1(-)
    \\
    \downarrow^{\mathrlap{p_2}} && \downarrow^{\mathrlap{d_{dR}}}
    \\
    \Omega^1(-) &\stackrel{d_{dR}}{\to}&
    \Omega^2_{cl}(-)
  }
  \,.
$$

By the [[nLab:Poincare lemma]] applied to each [[nLab:Cartesian space]], this is indeed a fibration.

In the [next section](#AbGerbesConnection) we give the proof of this (simple) claim. Here in the warmup phase we instead want to discuss the geometric interpretation of this resolution, along the lines of the section <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#CurvatureCharacteristicsI">curvature characteristics of 1-bundles</a> in the [[schreiber:differential cohomology in an (∞,1)-topos -- survey|survey-part]].


+-- {: .un_prop }
###### Proposition

We have the following geometric interpretation of the above models:

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& *
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1)
    }
  \right\}
  =
  \left\{
    \mathbf{\Pi}_2(U) \to \mathbf{B}^2 U(1)
  \right\}
$$

and

$$
  \mathbf{B}U(1)_{diff}
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& \mathbf{B}U(1)
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1))
    }
  \right\}
  \,.
$$

And in this presentation the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{B}^2 U(1)$ is given over $U \in CartSp$ by forming the pasting composite

$$
  \array{
    U &\to& \mathbf{B}U(1) &&& underlying\;cocycle
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1)) &&& connection
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1) &&& curvature
  }
$$

and picking the lowest horizontal morphism.

=--

Here the terms mean the following:

* $INN(U(1))$ is the [[nLab:2-group]] $\Xi(U(1) \to U(1))$, which is a 
  [[nLab:groupal model for universal principal ∞-bundles|groupal model for the universal U(1)-principal bundle]] $\mathbf{E}U(1)$;

* $\mathbf{\Pi}_2(U)$ is the [[nLab:path 2-groupoid]] with homotopy class of 2-dimensional paths as 2-morphisms

* the groupoids of diagrams in braces have as objects commuting diagrams in $[CartSp^{op}, sSet]$ as indicated, and horizontal 2-morphisms fitting into such diagrams as morphisms.

Using the discussion at [[nLab:2-groupoid of Lie 2-algebra valued forms]] (<a href="http://arxiv.org/abs/0802.0663">SchrWalII</a>) we have the following:


1. For $X$ a [[nLab:smooth manifold]], morphisms in $[CartSp^{op}, 2Grpd]$ of the form $tra_A : \Pi_2(X) \to \mathbf{E}\mathbf{B}U(1)$ are in bijection with smooth 1-forms $A \in \Omega^1(X)$: the 2-functor sends a path in $X$ to the the [[nLab:parallel transport]] of $A$ along that path, and sends a surface in $X$ to the exponentiated integral of the curvature 2-form $F_A = d A$ over that surface. The [[nLab:Bianchi identity]] $d F_A = 0$ says precisely that this assignment indeed descends to homotopy classes of surfaces, which are the 2-morphisms in $\Pi_2(X)$.

1. Moreover [[nLab:k-morphism|2-morphisms]] of the form $(\lambda,\alpha) : tra_A \to \tra_{A'}$ in $[CartSp^{op}, 2Grpd]$ are in bijection with pairs consisting of a $\lambda \in C^\infty(X,U(1))$ and a 1-form $\alpha \in \Omega^1(X)$ such that $A' = A + d_{dR} \lambda - \alpha$. 

1. And finally [[nLab:k-morphism|3-morphisms]] $h : (\lambda, \alpha) \to (\lambda', \alpha')$ are in bijection with $h \in C^\infty(X,U(1))$ such that $\lambda' = \lambda \cdot h$ and $\alpha' = \alpha + d_{dR} h$.


By the same reasoning we find that the coefficient object for flat $\mathbf{B}^2 U(1)$-valued differential cohomology is

$$
  \mathbf{\flat}\mathbf{B}^2 U(1)
  =
  [\Pi_2(-), \mathbf{B}^2U(1)]
  =
  \Xi(
    C^\infty(-,U(1))
    \stackrel{d_{dR}}{\to}
    \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-)
  )
  \,.
$$


So by the above definition of differential cohomology in $\mathbf{H}$ we find that $\mathbf{B}U(1)$-differential cohomology of a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$ is given by choosing any [[nLab:good open cover]] $\{U_i \to X\}$, taking $C(\{U_i\})$ to be the [[nLab:Cech nerve]], which is then a cofibrant replacement of $X$ in $[CartSp^{op}, sSet]_{proj,cov}$ and forming the ordinary pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H^2_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    [CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))
    &\stackrel{curv}{\to}&
    [CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}^2_{dR} U(1))
  }
$$

(because the bottom vertical morphism is a fibration, by the fact that our model for $\mathbf{B}_{diff} U(1) \to \mathbf{B}^2_{dR}U(1)$ is a fibration, that $C(\{U_i\})$ is cofibrant and using the axioms of the [[nLab:sSet]]-[[nLab:enriched model category]] $[CartSp^{op}, sSet]_{proj}$).

+-- {: .un_prop}
###### Observations

A cocycle in $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))$ is

1. a collection of functions

   $$
     (g_{i j } \in C^\infty(U_i \cap U_j, U(1)))
    $$

    satsifying $g_{i j} g_{j k} = g_{i k}$ on $U_i \cap U_j \cap U_k$;
  
1. a collection of 1-forms

   $$
      (A_i \in \Omega^1(U_i))
   $$
  
1. a collection of 1-forms


    $$
      (a_{i j} \in \Omega^(U_i \cap U_j))
    $$

    such that

    $$
      A_j = A_i + d_{dR} g_{i j} + a_{i j}
    $$

    on $U_i \cap U_j$ and

    $$
      a_{i j} + a_{j k} = a_{i k}
    $$

    on $U_i \cap U_j \cap U_k$.

The curvature-morphism takes such a cocycle to the cocycle

$$
  (d A_i, a_{i j}, )
$$

in the [above model](#OrdinaryDeRham) $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))$ for intrinsic de Rham cohomology.


Every cocycle with nonvanishing $(a_{i j})$ is in $[C(\{U_i\}), \mathbf{B}_{diff}U(1)]$ coboundant to one with vanishing $(a_{i j})$ 
   
=--

+-- {: .proof}
###### Proof

The first statements are effectively the definition and the construction of the above models. The last statement is as in the [above discussion](#OrdinaryDeRham) of our model for ordinary de Rham cohomology: given a cocycle with non-vanishing closed $a_{i j}$, pick a partition of unity $(\rho_i \in C^\infty(X))$ subordinate to the chosen cover and the coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i})$. This connects $(A_i,a_{i j}, g_{i j})$ with the cocycle $(A'_i, a'_{i j}, g_{i j})$ where

$$
  A'_i = A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}
$$

and

$$
  \begin{aligned}
    a'_{i j} 
      & = A'_j - A'_i - d g_{i j} 
     \\ 
      & = a_{i j} + 
      - \sum_{i_0}( a_{i_0 i} - a_{i_0 j} )
    \\
    & = 0    
  \end{aligned}
  \,.
$$

=--

So in total we have found the following story:

1. In order to compute the curvature characteristic form of a [[nLab:Cech cohomology]] cocycle $g : C(\{U_i\}) \to \mathbf{B}U(1)$ of a $U(1)$-principal bundle, we first lift it 

   $$
     \array{
       && \mathbf{B}_{diff}U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
   $$

   to an equivalent $\mathbf{B}_{diff}U(1)$-cocycle, and this amounts to putting (the Cech-representatitve of) a _pseudo-connection_ on the $U(1)$-principal bundle.

1. From that lift the desired curvature characteristic is simply projected out

   $$
     \array{
       && \mathbf{B}_{diff}U(1) &\stackrel{curv}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
     \,,
   $$

   and we find that it lives in the sheaf [[nLab:hypercohomology]] that models ordinary de Rham cohomology.

1. Therefore we find that in each _cohomology class_ of curvatures, there is at least one representative which is an ordinary globally defined 2-form. Moreover, the pseudo-connections that map to such a representative are precisely the _genuine_ connections, those for which the $(a_{i j})$-part of the cocycle vaishes.

So we see that ordinary connections on ordinary circle bundles are a means to model the homotopy pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H_{dR}^2(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}U(1)) &\to& \mathbf{H}_{dR}(X,\mathbf{B}U(1)) 
  }
$$

in a 2-step process: first the choice of a pseudo-connection realizes the bottom horizontal morphism as an [[nLab:anafunctor]], and then second the restriction imposed by forming the ordinary pullback chooses from all pseudo-connections precisely the genuine connections.

The general version of this story is discussed in detail at <a href="#Connections">differential cohomology in an (∞,1)-topos -- Local (pseudo-)connections.</a>


### Circle bundles with pseudo-connection {#CircleBunlePseudoConnection}

In the above discussion of extracting ordinary connections on ordinary $U(1)$-principal bundles from the abstract topos-theoretic definition of differential cohomology, we argued that a certain homotopy pullback may be computed by choosing in the Cech-hypercohomology of the complex of sheaves $(\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))$ over a manifold $X$ those cohomology representatives that happen to be represented by globally defined 2-forms on $X$. We saw that the homotopy fiber of _pseudo-connections_ over these 2-forms happened to have connected components indexed by _genuine_ connections.

But by the general abstract theory, up to isomorphism the differential cohomology computed this way is guaranteed to be independent of all such choices, which only help us to compute things.

To get a feeling for what is going on, it may therefore be useful to re-tell the analgous story with pseudo-connections that are not genuine connections.

By the very fact that $\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff}U(1)$ is a weak equivalence, it follows that every pseudo-connection is equivalent to an ordinary connection as cocoycles in $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}_{diff}(G))$. 

If we choose a [[nLab:partition of unity]] $(\rho_i \in C^\infty(X,\mathbb{R}))$ subordinate to the cover $\{U_i \to X\}$, then we can construct the corresponding coboundary explicitly:

let $(A_i g_{ij}, a_{i j})$ be an arbitrary pseudo-connection cocycle. Consider the Cech-hypercohomology coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i}, 0)$. This lands in the shifted cocycle

$$
  (A'_i := A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}, g_{i j}, a'_{i j})
  \,,
$$

and we can find the new pseudo-components $a'_{i j}$ by 

$$
  a'_{i j} = A'_j - A'_i - d_{dR} g_{i j}
  \,.
$$

Using the computation 

$$
  \begin{aligned}
    \sum_{i_0} \rho_{i_0} (a_{i_0 i} - a_{i_0 j}
    &=
    - \sum_{i_0} \rho_{i_0} (a_{i i_0} + a_{i_0 j}
    \\
    & = \sum_{i_0} \rho_{i_0} a_{i j}
    \\
    & = a_{i j}
  \end{aligned}
$$

we find that these indeed vanish.

The most drastic example for this is a lift $\nabla$ of a cocycle $g = (g_{i j})$ in 

$$
  \array{
    && \mathbf{B}_{diff} U(1)
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
  }
$$

is one which takes all the ordinary curvature forms to vanish identically

$$
  \nabla = (A_i := 0, g_{i j}, a_{i j})
  \,.
$$

This fixes the pseudo-components to be $a_{i j} = - d g_{i j}$. By the above discussion, this pseudo-connection with vanishing connection 1-forms is equivalent, as a pseudo-connection, to the ordinary connection cocycle with connection forms $(A_i := \sum_{i_0} \rho_{i_0} d g_{i_0 i})$. This is a <a href="http://ncatlab.org/nlab/show/connection+on+a+bundle#Properties">standard formula</a> for equipping $U(1)$-principal bundles with Cech cocycle $(g_{i j})$ with a connection.

### $Disc(U(1))$-groupoid bundles {#U1GroupoidBundle}

We saw above that the intrinsic coefficient object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ yields ordinary de Rham cohomology in degree $n \gt 1$. For $n = 1$ we [have](#FlatCircleCohomology) that $\mathbf{\flat}_{dR} \mathbf{B}U(1)$ is given simply by the 0-[[nLab:truncated]] sheaf of 1-forms, $\Omega^1(-) : CartSp^{op} \to Set \hookrightarrow sSet$. Accordingly we have for $X$ a paracompact smooth manifold

$$
  \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}U(1)) = 
  \Omega^1_{cl}(X)
$$ 

instead of $H^1_{dR}(X)$.

There is a good reason for this discrepancy: for $n \geq 1$ the object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is the recipient of the intrinsic curvature characteristic morphism

$$
  curv_{\mathbf{B}^{n-1} U(1)} : \mathbf{B}^{n-1} U(1) \to 
   \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  \,.
$$

For $X \to \mathbf{B}^{n-1} U(1)$ a [[nLab:cocycle]] (an $(n-2)$-gerbe without connection), the cohomology class of the composite $X \to \mathbf{B}^{n-1} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is precisely the obstruction to the existence of a flat extension $X \to \mathbf{\flat} \mathbf{B}^{n-1} U(1) \to \mathbf{B}^{n-1} U(1)$ for the original cocycle.

For $n = 2$ this is the usual [[nLab:curvature]] 2-form of a [[nLab:line bundle]], for $n = 3$ it is curvature 3-form of a [[nLab:bundle gerbe]], etc. But for $n = 1$ we have that the original cocycle is just a map of spaces

$$
  f : X \to U(1)
  \,.
$$

This can be understoody as a cocycle for a _groupoid_ principal bundle, for the 0-truncated groupoid with $U(1)$ as its space of objects. Such a cocycle extends to a flat cocycle precisely if $f$ is _constant_ as a function. The corresponding **curvature 1-form** is $d_{dR} f$ and this is precisely the obstruction to constancy of $f$ already, in that $f$ is constant if and only if $d_{dR} f$ vanishes. _Not_ (necessarily) if it vanishes _in de Rham cohomology_ . 

This is the simplest example of a general statement about curvatures of higher bundles: the curvature 1-form is not subject to gauge transformations.


### Circle $n$-bundles with connection {#AbGerbesConnection}

We now generalize the [above discussion](#CircleBundlesConnection) on the derivation of the notion of [[nLab:connection on a bundle|connections on circle bundles]] from abstract topos-theory to a proof of the full [theorem above](#DeligneCohomologyTheorem) on the derivation of general [[nLab:Deligne cohomology]].


The main step is to model the double [[nLab:(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}^n U(1) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1) &\to&
    \mathbf{\flat} \mathbf{B}^{n+1} U(1)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}^{n+1} U(1)
  }
$$

in $\mathbf{H} = $ [[nLab:?LieGrpd]] that gives the  [[nLab:fiber sequence]] $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^{n} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)$ which controls the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#GroupalCurvature">obstruction theory for flat connections</a> by a [[nLab:homotopy pullback]] realized suitably as an ordinary pullback of fibrations in $[CartSp^{op}, Ch_\bullet] \stackrel{\Xi}{\hookrightarrow} [CartSp^{op}, sSet]_{proj}$.



+-- {: .un_observation}
###### Observation 

We have commuting diagrams 

$$ 
  \array{
    \Xi(\;
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    &\to&
    \Xi(\;
     C^\infty(-,U(1)) \stackrel{Id + d_{dR}}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    { \Omega^{n-1}(-) \atop \oplus \Omega^n(-)}
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    \\
    \downarrow && \downarrow^{\mathrlap{(Id, p_2, p_2, \cdots, p_2,d_{dR})}}
    \\
    \Xi(
    \; 0 \stackrel{}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-))    
    &\to&
    (C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to} 
    \Omega^2(-)
    \stackrel{d_{dR}}{\to}
    \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-)
    \;)
    \\
    \downarrow && \downarrow
    \\
    \Xi(
     \; 0 \to 0 \to 0 \to \cdots \to 0\;)
    &\to&
    \Xi(
     \; C^\infty(-,U(1)) \to 0 \to 0 \to \cdots \to 0
     \;)
  }
$$

in $[CartSp^{op},sSet]_{proj}$ where

* the objects are fibrant models for the corresponding objects in the
  above $(\infty,1)$-pullback diagram;

* the two right vertical morphisms are fibrations;

* the two squares are [[nLab:pullback]] squares.

Therefore this is a [[nLab:homotopy pullback]] in $[CartSp^{op}, sSet]_{proj}$ that realizes the  $(\infty,1)$-pullback in question in the [[nLab:(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(CartSp)$. Since [[nLab:∞-stackification]] preserves finite [[nLab:(∞,1)-limit]]s, it therefore also presents the above $(\infty,1)$-pullback in $\mathbf{H} = Sh_{(\infty,1)}(CartSp)$.

=--

+-- {: .proof}
###### Proof

For the lower square we had discussed this already [above](#OrdinaryDeRham). For the upper square the same type of reasoning applies. The main point is to find the chain complex in the top right such that it is a [[nLab:resolution]] of the point and maps by a fibration onto our model for $\mathbf{\flat}\mathbf{B}^n U(1)$. The top right complex is

$$
  \array{
    &&
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
     \\
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \cdots  &
     {}^{\mathrlap{id}}\nearrow& 
     \\
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
  }
$$

and the vertical map out of it into $C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n(-) \stackrel{d_{dR}}{\to} \Omega^{n+1}_{cl}(-)$ is in positive degree the projection onto the lower row and in degree 0 the de Rham differential. This is manifestly surjective (by the [[nLab:Poincare lemma]] applied to each object $U \in $ [[nLab:CartSp]]) hence this is a fibration.

The pullback object in the top left is in this notation

$$
  \mathbf{B}^n U(1)_{diff,chn}
  :=
  \Xi
  \left(
    \array{
      C^\infty(-,U(1)) 
       &\stackrel{d_{dR}}{\to}&
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
       \\
       \oplus 
       &{}^{\mathrlap{id}}\nearrow& \oplus 
       &{}^{\mathrlap{id}}\nearrow& \cdots  &
       {}^{\mathrlap{id}}\nearrow& 
       \\
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
    }
  \right)
$$

and in turn the top left vertical morphism $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is in positive degree the projection on the lower row and in degree 0 the de Rham differential.

=--

Notice that the evident forgetful morphism $\mathbf{B}^n U(1) \stackrel{}{\leftarrow} \mathbf{B}^n_{diff} U(1)$ is indeed a weak equivalence.

With this description we now have the proof of the [above theorem](#DeligneCohomologyTheorem)

{#ProofOfDeligneTheorem}
+-- {: .proof}
###### Proof (equivalence of with Deligne cohomology)

Since the above model for $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is a fibration and $C(\{U_i\})$ is cofibrant, also 

$$
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{B}^n_{diff}U(1))
  \to
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^n U(1))
$$

is a [[nLab:Kan fibration]] by the fact that $[CartSp^{op}, sSet]_{proj}$ is an $sSet_{Quillen}$-[[nLab:enriched model category]]. Therefore the homotopy pullback is computed as an ordinary pullback.  

By the [above discussion of de Rham cohomology](#OrdinaryDeRham) we have that we can assume the morphism $H_{dR}^{n+1}(X) \to [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^{n+1})$ picks only cocylces represented by globally defined closed differential forms $F \in \Omega^{n+1}(X)$.

By the nature of the chain complexes apearing in the above proof, we see that the elements inm the fiber over such a globally defined form are precisely the cocycles with values only in the "upper row complex"

$$
  C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-)
  \stackrel{d_{dR}}{\to}
  \cdots 
  \stackrel{d_{dR}}{\to}
  \Omega^n(-)
  \,.
$$

This is precisely the complex of sheaves that defines [[nLab:Deligne cohomology]] in degree $(n+1)$.

=--


### Models from $\infty$-Lie integration {#U1FromLieIntegration}

In the [previous section](#FlatCircleCohomology) we discussed a model 

$$
  \array{
    \mathbf{B}^n U(1)_{diff,chn}
    &\stackrel{curv_{chn}}{\to}& 
    \mathbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)_{chn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n U(1) 
  }
$$

in $[CartSp, sSet]$ for the canoncal curvature characteristic class $curv : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ in [[nLab:?LieGrpd]] with the special property that it did model the abstract [[nLab:(∞,1)-topos]]-theoretic class under the [[nLab:Dold-Kan correspondence]] precisely in terms of the familiar [[nLab:Deligne cohomology]] coefficient complex.

Now we describe another model for the curvature class in $[CartSp^{op}, sSet]$, one that is useful for constructing the [∞-Chern-Weil homomorphism](#InfChernWeil) that maps from [[nLab:nonabelian cohomology]] in $\infty Lie Grpd$ to $U(1)$-valued differential cohomology.

This second model is the one naturally adapted to the construction of the object $\mathbf{B}^n U(1)$ by [[nLab:Lie integration]] from its [[nLab:∞-Lie algebra]] $b^{n-1} \mathbb{R}$. This is described at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegration">∞-Lie groupoid -- Lie integration</a>. 

For distinguishing the two models, we will indicate the former one by the subscript ${}_{chn}$ and the one described now by the subscript ${}_{simp}$.

+-- {: .un_def }
###### Convention 

Here and in the following we adopt for differential forms on simplices the following notational convention:

* by $\Omega^\bullet(\Delta^n)$ we denote the complex of smooth differential forms on the standard smooth $n$-simplex with **sitting instants**: for every $k \in \mathbb{N}$ every $k$-face of $\Delta^n$ has a neighbourhood of its boundary such that the form restricted to that neighbourhood is constant in the direction perpendicular to that boundary.

* for $U \in $ [[nLab:CartSp]] we write $\Omega^\bullet(U \times \Delta^n)$ for the complex $\Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n)$.

* for $U \in CartSp$ we write $C^\infty(U) \otimes \Omega^\bullet(\Delta^n)$ for the total complex with differential the de Rham differential on $\Delta^n$.

=--

+-- {: .un_def }
###### Definition

For $n \in \mathbb{N}$, define the [[nLab:simplicial presheaf]] $\mathbf{B}^n U(1)_{simp} \in [CartSp^{op}, sSet]$ by

$$
  \mathbf{B}^n U(1)_{simp}
  :=
  \mathbf{cosk}_{n+1}
  (
  (U, [k]) \mapsto 
   Hom_{dgAlg}(CE(b^{n-1}\mathbb{R}), C^\infty(U)\otimes\Omega^\bullet(\Delta^k ))
  )
  /\mathbf{B}^n \mathbb{Z}
  \,.
$$

Here $\mathbf{cosk}_{n+1}(-)$ is the [[nLab:simplicial skeleton|coskeleton]]-operation and the quotient is by constant $n$-forms $\omega \in \Omega^n_{cl}(\Delta^n)\otimes C^\infty(U)$ such that $\int_{\Delta^n}\omega \in \mathbb{Z}$.

=--

+-- {: .un_lemma }
###### Observation

Under the [Dold-Kan correspondence](#DoldKan) the [[nLab:Moore complex|normalized chain complex]] of $\mathbf{B}^n U(1)_{sim}$ is

$$
  N_\bullet(\mathbf{B}^n U(1)_{simp})
  =
  (
  \cdots
  \to
  \Omega^n_{cl}(\Delta^{n+1})\otimes C^\infty(-)/\sim
  \stackrel{\sum_k (-1)^k \delta_k^* }{\to}
  \Omega^n_{cl}(\Delta^{n})\otimes C^\infty(-)/\sim
  \to
  0 
  \to
  \cdots
  \to
  0
)
  \,,
$$

where $\delta_k : \Delta^n \to \Delta^{n+1}$ denotes the embedding of the $k$th face of the smooth $(n+1)$-[[nLab:simplex]].

=--

Here and in the following we indicate the homologically trivial part of the normalized chain complex of an $(n+1)$-coskeletal simplicial abelian group just by ellipses.

+-- {: .un_lemma }
###### Observation

The evident [[nLab:fiber integration]] of differential forms over simplices 

$$
  \int_{\Delta^n} : \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
   \to \Omega^\bullet(U)
$$

yields a morphism 

$$
  \int_{\Delta^\bullet} : \mathbf{B}^n U(1)_{simp} \stackrel{\simeq}{\to}
  \mathbf{B}^n U(1)
$$

in $[CartSp^{op}, sSet]_{proj}$, which is a weak equivalence.

=--

+-- {: .proof}
###### Proof

By the [Dold-Kan](#DoldKan)-[[nLab:adjunction]] $(N_\bullet \dashv \Xi)$ and the above observation, it is sufficient to check that 

$$
  \array{
    \cdots
    &\to&
    \Omega^n_{cl}(\Delta^{n+1})\otimes C^\infty(-)/\sim
    &\stackrel{\sum_k (-1)^k \delta_k^* }{\to}&
    \Omega^n_{cl}(\Delta^{n})\otimes C^\infty(-)/\sim
    &\to&
    0 
    &\to&
    \cdots
    &\to&
    0  
    \\
    &&
    \downarrow^{\mathrlap{\int_{\Delta^{n+1}}}}
    &&
    \downarrow^{\mathrlap{\int_{\Delta^{n}}}}
    &&
    \downarrow
    &&
    &&
    \downarrow
    \\
    \cdots &\to& 0 &\to& C^\infty(-, U(1)) &\to& 0 &\to& \cdots &\to& 0
  }
$$

is a chain complex morphism and a [[nLab:quasi-isomorphism]].

To see that we have a chain map, let $\omega$ be a $U$-familiy of closed $n$-forms on $\Delta^{n+1}$. Then 

$$
  \int_{\Delta^n} \sum_k (-1)^k \delta_k^* \omega
  =
  \pm \int_{\partial \Delta^{n+1}} \omega
  =
  \pm \int_{\Delta^{n+1}} d_{\Delta^n} \omega
  =
  0
  \,.
$$

This means that the left square in the above diagram does commute. To see the quasi-isomorphism, it suffices to notice that an $n$-form on the $n$-sphere extends to a closed $n$-form on the $(n+1)$-ball precisely if its integral over the $n$-sphere vanishes. 

=--

+-- {: .un_def }
###### Definition

Write $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp} \in [CartSp^{op}, sSet]$ for the [[nLab:simplicial presheaf]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp}
  :=
  cosk_{n+1}
  (
    (U,[k])
    \mapsto
    Hom_{dgAlg}(
      CE(b^{n-1}\mathbb{R}),
      \Omega^{\bullet \geq 1}(U) \otimes \Omega^\bullet(\Delta^k)
    )
  )
  \,.
$$

=--

+-- {: .un_lemma }
###### Lemma

The homology sheaves of the corresponding sheaf of normalized chain complexes $N_\bullet(\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp})$ are concentrated in degree $(n-1)$, where they equal $\Omega^1_{cl}(-)$.

=--

+-- {: .proof}
###### Proof

For $k \leq (n-1)$ the chain differential $\sum_k (-1)^k \delta_k^*$ is onto: for $\omega \in \Omega^bullet(U\times \Delta^{k-1})$ closed and of degree $n$ there is $\lambda$ with $d \lambda = \omega$, consider the closed form

$$
  f(t_{k}) \wedge \omega  - d f(t_k) \wedge \lambda 
  \in
  \Omega^bullet(U \times \Delta^{k})
  \,,
$$

where $f : [0,1] \to [0,1]$ is a smooth function non-increasing function with $f(0) = 1$ and $f(1) = 0$ and constant in a neighbourhood of the boundary of $[0,1]$, and where we use the standard coordinates of $\Delta^k = \{t_1 \leq t_2 \leq \cdots \leq t_k \} \subset \mathbb{R}^k$. By the fact that $\omega$ has sitting instants, this form is such that its restriction only to one face of $\Delta^{n-1}$ is non-vanishing, where it equals $\omega$. 

This construction fails for $k = n$ because there it may happen that $\lambda$ has all legs along $\Delta^{n-1}$, such that the above construction is not guaranteed to land in $\Omega^{\bullet \geq 1}(U) \otimes \Omega^\bullet(\Delta^n)$. Therefore we pick up a nontrivial homology group in this degree.

(...)

=--

+-- {: .un_lemma }
###### Lemma

The evident [[nLab:fiber integration]] over simplices induces a morphism of simplicial presheaves

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{simp}
  \to 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{chn}
$$

which is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

To see that we have a chain map let $\omega$ be a closed $n$-form on $U \times \Delta^k$ (with at least one leg along $U$). Then

$$
  \int_{\Delta^{k-1}} \sum_j (-1)^k \delta^*_j \omega
  = 
  \int_{\partial \Delta^k} \omega
  =
  \int_{\Delta^k} d_{\Delta^{k}} \omega
$$

is the result of going one way around the squares in the chain map. Since $\omega$ is closed, this is

$$
  \cdots = 
  -\int_{\Delta^k} d_{U}\omega
  =
  d_U \int_{\Delta^k} \omega
  \,,
$$

which is the result of going the other way around.

=--



+-- {: .un_def }
###### Definition

Write $\mathbf{B}^n  U(1)_{diff,simp}$ for the simplicial presheaf given by 

$$
  \mathbf{B}^n  U(1)_{diff,simp}
  :=
  \mathbf{cosk}_{n+1}
  (
    U,[k]
    \mapsto
   \left\{
     \array{
        C^\infty(U)\otimes' \Omega^\bullet(\Delta^k)
        &\leftarrow&
        CE(b^{n-1}\mathbb{R})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet(U \times \Delta^k )
        &\leftarrow&
        W(b^{n-1} \mathbb{R})
     }
   \right\}
  )
  \,.
$$

Let the morphism

$$
  curv_{simp}
  :
  \mathbf{B}^n U(1)_{diff,simp}
  \to 
  \mathbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)_{simp}
$$

be the one given by postcomposition with the square of [[nLab:dg-algebra]]s

$$  
  \array{
     CE(b^{n-1}\mathbb{R}) &\leftarrow& 0
     \\
     \uparrow && \uparrow
     \\
     W(b^{n-1}\matbb{R}) &\leftarrow& CE(b^n \mathbb{R})
  }
$$

described at [[nLab:∞-Lie algebra cohomology]].

=--

+-- {: .un_remark }
###### Remark

The set of square diagrams of [[nLab:dg-algebra]]s above is over $(U,[k])$ the set of $n$-forms $\omega$ on $U \times \Delta^k$ whose [[nLab:curvature]] $(n+1)$-form $d \omega$ has no component with all legs along $\Delta^k$.

=--



+-- {: .un_prop }
###### Proposition

The morphism given by [[nLab:fiber integration]] of differential forms over the simplex factor fits into a diagram

$$
  \array{
    \mathbf{B}^n U(1)_{diff,simp} &\stackrel{curv_{simp}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{simp}
    \\
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}} && 
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}}
    \\
    \mathbf{B}^n U(1)_{diff,chn} &\stackrel{curv_{chn}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}    
  }
  \,,
$$

where the vertical morphisms are weak equivalences. 

=--

+-- {: .proof}
###### Proof

For $k \geq 1$, going one way around the chain map squares, a pair $(\omega, d \omega)$ on $U \times \Delta^k$ is mapped to the pair whose first component is

$$
  \int_{\Delta^{k-1}} \sum_j (-1)^k \delta_j^* \omega
  = 
  \int_{\Delta^k} d_{\Delta^k} \omega
  =
  \int_{\Delta^k} d \omega - d_U \omega
  =
  d_U \int_{\Delta^k} \omega + \int_{\Delta^k } d \omega
$$

and whose second component is $d_U \int \Delta^k d \omega$.

Going the other way round we first get the pair 
$(\int_{\Delta^k \omega}, \int_{\Delta^k} d \omega)$. Then the differental of $\mathbf{B}^n U(1)_{diff,chn}$ maps this precisely to the above pair.

For $k = 0$ the same logic applies, with the second part in each pair discarded.

=--

+-- {: .un_def }
###### Definition

Write $\mathbf{B}^n U(1)_{conn,simp} \hookrightarrow \mathbf{B}^n U(1)_{diff,simp}$ for the sub-presheaf which over $(U,[k])$ is the set of those forms $\omega$ on $U \times \Delta^k$ such that the [[nLab:curvature]] $d \omega$ has no leg along $\Delta^k$.

=--

+-- {: .un_cor }
###### Corollary

Under fiber integration over simplices, $\mathbf{B}^n U(1)_{conn,simp}$ is [[nLab:quasi-isomorphism|quasi-isomorphic]] to the [[nLab:Deligne cohomology]]-complex.


=--



$$
  \array{
     && 
     \mathbf{B}^n U(1)_{conn,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     U(1)(n)_D^\infty
     &&&
     connection
     \\
     & \nearrow & \downarrow && \downarrow
     \\
     \hat X &\to& 
     \mathbf{B}^n U(1)_{diff,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{B}^n U(1)_{diff,chn}
     &&&
     pseudo-connection
     \\
     & \searrow & \downarrow && \downarrow
     \\
     && \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{simp}
      &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}
     &&&
     curvature
  }
  \,.
$$

In summary this gives us the following alternative perspective on connections on $\mathbf{B}^{n-1}U(1)$-[[nLab:principal ∞-bundle]]s: such a connection is a cocycle with values in the $\mathbf{B}^n \mathbb{Z}$-quotient of the  $(n+1)$-coskeleton of the simplicial presheaf which over $(U,[k])$ is the set of diagrams of [[nLab:dg-algebra]]s

$$
  \array{
    C^\infty(U)\otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    CE(b^{n-1}\mathbb{R})
    &&&
    underlying\;cocycle
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    W(b^{n-1}\mathbb{R})    
    &&& 
    connection
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes C^\infty(\Delta^k) &\leftarrow& CE(b^n \mathbb{R})
    &&&
    curvature
  }
$$

where the restriction to the top morphism is the underlying cocycle and the restriction to the bottom morphism the curvature form.

The generalization to such diagram cocycles from $b^{n-1}\mathbb{R}$ to general [[nLab:∞-Lie algebra]]s $\mathfrak{g}$ we discuss below in [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection).

## Examples

For $n = 1$ a circle $n$-bundle with connection in the sense discussed here is indeed an ordinary hermitian [[line bundle]] or equivalently $U(1)$-[[principal bundle]] with connection.

For $n = 2$ a circle 2-bundle with connection is equivalent to a [[bundle gerbe]] with connection (at least over a smooth manifold. Over an [[orbifold]] the definition given here does produce the correct [[equivariant cohomology]], which is different from that of bundle gerbes that are equivariant in the ordinary sense.)

Classes of examples of higher circle bundles with connection are provided by [[∞-Chern-Weil theory]] which provides homomorphisms of the form

$$
  \mathbf{H}_{conn}(X,\mathbf{B}G) \to \mathbf{H}_{diff}(X, \mathbf{B}^n U(1))
  \,.
$$

See for instance 

* [[Chern-Simons circle 3-bundle]]

for the class of circle 3-bundles that arise as differential refinements of degree 4 [[characteristic class]]es such as the [[Pontryagin class]].



[[!redirects circle n-bundles with connection]]
[[!redirects circle n-bundles with connections]]
