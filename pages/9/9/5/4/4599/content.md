


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

We discuss the refinement to [[higher differential geometry]] of the concept of a [[circle group]]-[[principal connection]] (on a [[circle group]]-[[principal bundle]]). Specifically we indicate how the general abstract definition in terms of [[cohesion]] reproduces in the context of [[smooth ∞-groupoid|smooth cohesion]] to the representation of circle $n$-connections by [[cocycles]] in smooth _[[Deligne cohomology]]_ ([dcct](#dcct)). 

In every [[cohesive (∞,1)-topos]] $\mathbf{H}$ there is an <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">intrinsic notion of differential cohomology</a> with coefficients in an [[abelian group|abelian]] [[group object]] $A \in \mathbf{H}$ that classifies $\mathbf{B}^{n-1}A$-[[principal ∞-bundles]] with [[connection on an ∞-bundle|∞-connection]]. 

Here we discuss the specific realization for $\mathbf{H} =$ [[Smooth∞Grpd]] the [[(∞,1)-topos]] of [[smooth ∞-groupoids]] and $A = U(1)$ the [[circle group]]. 

In this case the intrinsic differential cohomology reproduces [[ordinary differential cohomology]] and generalizes it to base spaces that may be [[smooth manifold]]s, [[diffeological space]]s, [[orbifold]]s and generally [[smooth ∞-groupoid]]s such as [[delooping]]s $\mathbf{B}G$ of 
[[smooth ∞-groupoid|smooth ∞-group]]s $G$. Differential cocycles on the latter support the [[∞-Chern-Weil homomorphism]] that sends [[nonabelian cohomology|nonabelian]] [[connection on an ∞-bundle|∞-connections]] to circle $n$-bundles whose [[curvature]] form realizes a [[characteristic class]] in [[de Rham cohomology]].


## The ambient context

Let $\mathbf{H} coloneqq $ [[Smooth∞Grpd]] be the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoid]].  As usual, write

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc) :
  Smooth \infty Grpd
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

for the terminal [[global section]] [[(∞,1)-geometric morphism]] with its extra [[left adjoint]], the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|intrinsic fundamental ∞-groupoid]] functor $\Pi$.

From this induced is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Paths">path ∞-groupoid adjunction</a>

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat}) : 
   Smooth \infty Grpd \stackrel{\leftarrow}{\to}
   Smooth \infty Grpd
$$

and the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#deRhamCohomology">intrinsic de Rham cohomology</a> adjunction

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR}) : 
   */Smooth \infty Grpd \stackrel{\overset{\mathbf{\Pi}_{dR}}{\leftarrow}}{\underset{\mathbf{\flat}_{dR}}{\to}}
   Smooth \infty Grpd
  \,.
$$

For $A$ an abelian group object there for each [[integer]] $n$ is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#CurvatureCharacteristics">universal curvature characteristic form</a>, given by a [[cocycle]]-morphism

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A
  \,.
$$

The [[cocycle]]s for _differential cohomology_ in degree $n$ with coefficients in $A$ are the points in the [[homotopy fiber]] $\mathbf{H}_{diff}(-, \mathbf{B}^n A)$ of the morphism on [[cohomology]] 

$$
  curv_* : \mathbf{H}(-, \mathbf{B}^n A) \to 
   \mathbf{H}_{dR}(-, \mathbf{B}^{n+1}A)
$$

induced by this. Every such cocycle $\nabla \in \mathbf{H}_{diff}(X,\mathbf{B}^n A)$ we may think of as an [[connection on an ∞-bundle|∞-connection]] on the $\mathbf{B}^{n-1}A$-[[principal ∞-bundle]] classified by the underlying cocycle in $\mathbf{H}(X, \mathbf{B}^n A)$.

We consider these constructions in the model $\mathbf{H} = $ [[Smooth∞Grpd]]. This is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  Smooth\infty Grpd 
  \;\coloneqq\;
  Sh_{(\infty,1)}(CartSp_{smooth})
$$

on the [[site]] [[CartSp]]${}_{smooth}$ of [[Cartesian space]]s and [[smooth function]]s between them. This is a general [[higher geometry]] context for [[differential geometry]]. For computations we can explicitly [[presentable (∞,1)-category|present]] this [[(∞,1)-category]] by a local [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,loc}$

$$
  Smooth \infty Grpd \simeq ([CartSp^{op}, sSet]_{proj, loc})^\circ
$$

as described at [[presentations of (∞,1)-sheaf (∞,1)-toposes]].

In $\mathbf{H} = $ [[Smooth∞Grpd]] a canonical choice for $A$ is the [[circle group]] 

$$
  A \coloneqq U(1) = \mathbb{R}/\mathbb{Z}
  \,.
$$

We show how the notion of _smooth circle $n$-bundles with connection_ obtained by  applying the general setup above to this case reproduces [[ordinary differential cohomology]]:

* a _circle 1-bundle with connection_ is an ordinary $U(1)$ [[principal bundle]] [[connection on a bundle|with connection]];

* a _circle 2-bundle with connection_ is a $\mathbf{B}U(1)$-[[principal 2-bundle]] [[connection on a 2-bundle|with connection]], equivalently a $U(1)$-[[bundle gerbe]] [[connection on a bundle gerbe|with connection]];

* a _circle 3-bundle_ with connection if a $\mathbf{B}^2 U(1)$-[[principal ∞-bundle|principal 3-bundle]] [[connection on an ∞-bundle|with connection]], equivalently a $U(1)$-[[bundle 2-gerbe]] with connection;

* generally, a _circle $n$-bundle with connection_ is a $\mathbf{B}^{n-1}U(1)$-[[principal ∞-bundle|principal n-bundle]] [[connection on an ∞-bundle|with connection]], equivalently a [[cocycle]] in [[Deligne cohomology]] in degree $n+1$, equivalently a [[Cheeger-Simons differential character]] in that degree.

We assume in the following that the reader is familiar with basics of [[smooth ∞-groupoid]]s.


## Flat differential cohomology {#FlatCircleCohomology}

The <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">coefficient object for flat differential cohomology</a> in $\mathbf{H} = $ [[Smooth∞Grpd]] with values in $\mathbf{B}^n U(1)$ is $\mathbf{\flat} \mathbf{B}^n U(1) = LConst \Gamma \mathbf{B}^n U(1)$. 

The <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#deRhamCohomology">coefficient object for intrinsic de Rham cohomology</a> is $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$, defined by the [[(∞,1)-pullback]]

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

The following proposition provides models for these objects in in terms of ordinary [[differential form]]s.

+-- {: .num_prop }
###### Proposition

A fibrant representative in $[CartSp^{op}, sSet]_{proj,cov}$ of $\mathbf{\flat} \mathbf{B}^n U(1)$ is

$$
  \mathbf{\flat}\mathbf{B}^n U(1)_{chn}
  \;\coloneqq\;
  \Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]
  \,,
$$

and a fibrant representative of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}
  \;\coloneqq\;
  \Xi[0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]
  \,.
$$

=--

Notice that the complex of sheaves $\mathbf{\flat}\mathbf{B}^n U(1)$ is that which defines _flat_ [[Deligne cohomology]], while that of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is essentially that which defines [[de Rham cohomology]] in degree $n \gt 1$ (see [below](#OrdinaryDeRham)). Also notice that we denoted by $d_{dR}$ also the differential $C^\infty(-,U(1)) \stackrel{d_{dR} log}{\to} \Omega^1(-)$; this is to stress that we are looking at $U(1)$ as the quotient $\mathbb{R}/\mathbb{Z}$.


+-- {: .proof}
###### Proof

Since the [[global section]] functor $\Gamma$ amounts to evaluation on the  point $\mathbb{R}^0$ and since constant simplicial presheaves on [[CartSp]] satisfy [[nLab:descent]] (on objects in $CartSp$!), we have that $\mathbf{\flat} \mathbf{B}^n U(1)$ is represented by the complex of sheaves $\Xi[const U(1) \to 0 \to \cdots \to 0]$. This is weakly equivalent to $\Xi[C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]$ by the [[Poincare lemma]] applied to each [[Cartesian space]] (using the same standard logic that proves the [[de Rham theorem]]) in that the degreewise inclusion

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

We observe that the [[pullback]] of this morphism to the point

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

is the pullback over a cospan all whose objects are fibrant and one of whose morphisms is a fibration. Therefore this is a [[homotopy pullback]] diagram in $[CartSp^{op}, sSet]_{proj}$ which models the [[(∞,1)-limit]] over $* \to \mathbf{B}^n U(1) \leftarrow \mathbf{\flat}\mathbf{B}^n U(1)$ in $PSh_{(\infty,1)}(CartSp)$. Since [[nLab:∞-stackification]] preserves finite $(\infty,1)$-limits this models also the corresponding $(\infty,1)$-limit in $\mathbf{H}$. Therefore the top left object is indeed a model for $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$.

=--

## de Rham cohomology {#OrdinaryDeRham}

The intrinsic de Rham cohomology of [[Smooth∞Grpd]] with coefficients in $\mathbb{R}$ or $U(1) = \mathbb{R}/\mathbb{Z}$ coincides with the ordinary [[de Rham cohomology]] of [[smooth manifold]]s and smooth [[simplicial manifold]]s in degree greater than 1. This we discuss here. The meaning of the discrepancy in degee 1 and lower is discussed [below](#U1GroupoidBundle).

So for this section let $n \in \mathbb{N}$ with $n \geq 2$.

Above in _[Flat U(1)-valued differential cohomology](#FlatCircleCohomology)_ we found a fibrant representative of $\mathbf{\flat}_{dR} \mathbf{B}^n U(1) \in Smooth\infty Grpd$ to be given by 

$$
  \Xi\big[
    \Omega^1(-) 
     \overset{d_{dR}}{\to} \Omega^2(-)
     \overset{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)
  \big]
$$ 

in $[CartSp^{op}, sSet]_{proj, cov}$. 

+-- {: .num_prop }
###### Proposition

For $X \in Smooth\infty Grpd$ a [[paracompact space|paracompact]] [[smooth manifold]] we have in $\mathbf{H} = Smooth \infty Grpd$ a  [[natural isomorphism]]

$$
  \pi_0 \mathbf{H}\big(
    X,\,
   \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  \big)
  \;\simeq\;
  H_{dR}^n(X)
  \,,
$$ 

where on the left we have the [intrinsic (∞,1)-topos theoretic notion of de Rham cohomology](cohesive%20%28infinity,1%29-topos#deRhamCohomology), and on the right the ordinary  notion of [[de Rham cohomology]] of a smooth manifold.

=--

+-- {: .proof}
###### Proof

Let $\{U_i \to X\}$ be a [[good open cover]]. At *[[Smooth∞Grpd]]* is discussed that then the [[Čech nerve]] $C(\{U_i\}) \to X$ is a [[cofibrant object|cofibrant]] [[resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,cov}$. Therefore we have

$$
  \mathbf{H}\big(
    X
    ,\,
    \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  \big)
  \;\simeq\;
  [CartSp^{op}, sSet]\Big(
    C(\{U_i\}),\, 
    \Xi\big[
      \Omega^1(-) 
        \overset{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)
    \big]
  \Big)
  \,.
$$

The right hand is the $\infty$-groupoid of cocylces in the [[nLab:Cech cohomology|Cech]] [[nLab:hypercohomology]] of the complex of sheaves of differential forms. A cocycle here is given by a collection

$$
  (C_i, B_{i j}, A_{i j k}, \cdots  , Z_{i_0, \cdots, i_n})
$$

of differential forms, with $C_i \in \Omega^n_{cl}(U_i)$, $B_{i j} \in \Omega^{n-1}(U_i \cap U_j)$, etc. , such that this collection is annihilated by the total differential $D = d_{dR} \pm \delta$, where $d_{dR}$ is the [[de Rham differential]] and $\delta$ the alternating sum of the [[pullback of differential forms|pullbacks]] along the face maps of the [[Čech nerve]].

It is a standard result of [[abelian sheaf cohomology]] that such cocycles represent classes in de Rham cohomology. 

But for the record and since the details of this computation will show up again at some mildly subtle points in further discussion below, we spell this out in some detail.

We can explicitly construct coboundaries connecting such a generic cocycle to one of the form 

$$
  (F_i, 0, 0, \cdots, 0)
$$

by using a [[partition of unity]] $\big(\rho_i \in C^\infty(X)\big)$ subordinate to the cover $\{U_i \to X\}$, i.e. $x \in U_i \Rightarrow \rho_i(x) = 0$ and $\sum_i \rho_i = 1$.

For consider 

$$
  \begin{aligned}
     & 
    \big(
      C_i,\, 
      B_{i j},\, 
      A_{i j k},\, 
      \cdots,\, 
      Y_{i_1, \cdots, i_{n}},\, 
      Z_{i_1, \cdots, i_{n+1}}
    \big)
    \\
     \pm\; & 
    D 
    \big(
      0 ,\, 
      0 ,\, 
      \cdots ,\, 
      \textstyle{\sum_{i_0}} 
        \rho_{i_0} Z_{i_0, i_1 ,\cdots, i_{n}},\,
     0
    \big)
    \\
    =\;
    & 
    \big(
      C_i, \,
      B_{i j}, \, 
      A_{i j k}, \,
      \cdots, \,
      Y_{i_1, \cdots, i_{n}}
       + 
      \mathrm{d}_{dR}
        \textstyle{\sum_{i_0}} 
        \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}} ,\, 
      0
    \big)   
    \,,
  \end{aligned}
$$

where we used with $(\delta Z)_{i_1, \cdots, i_{n+2}} = 0$ that

$$
  \begin{aligned}
    \big(
      \delta \textstyle{\sum} \rho Z
    \big)_{i_1, \cdots, i_{n+1}}
    & =
    \pm
    \textstyle{\sum_{i_0}} \rho_{i_0}
    \textstyle{\sum_{k = 1}^{n+1}}
    (-1)^k
    Z_{i_0, i_1 \cdots, \hat i_k, \cdots, i_{n+1}}
    \\
    & =
    \pm
    \textstyle{\sum_{i_0}} \rho_{i_0}
    Z_{i_1 ,\cdots, i_{n+1}}    
    \\
    & =
    \pm
    Z_{i_1 ,\cdots, i_{n+1}}
    \,.
  \end{aligned}
$$

> (up to some sign which one can work out...)

By recursively adding coboundaries this way, we can annihilate all the higher Cech-components of the original cocycle and arrive at a cocycle of the form $(F_i, 0, \cdots, 0)$. 

Such a cocycle being $D$-closed says precisely that $F_i = F|_{U_i}$ for $F \in \Omega^n_{cl}(X)$ a globally defined closed differential form. Moreover, coboundaries between two cocycles both of this form 

$$
  (F_i, 0, \cdots , 0) = (F'_i, 0, \cdots, 0) + D(\lambda_i, \lambda_{i j}, \cdots)
$$

are necessarily themselves of the form $(\lambda_i, \lambda_{i j}, \cdots) =  (\lambda_i, 0 ,\cdots, 0)$ with $\lambda_i = \lambda|_{U_i}$ for $\lambda \in \Omega^{n-1}(X)$ a globally defined differential $n$-form and $F = F' + d_{dR} \lambda$.

=--



## Differential cohomology
 {#DifferentialCohomology}


The intrinsic <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#DiffCohWithGroupalCoeffs">definition of the ∞-groupoid of cocycles for the intrinsic  differential cohomology</a> in $\mathbf{H} = Smooth\infty Grpd$ with coefficients $\mathbf{B}^n U(1)$ is the object $\mathbf{H}_{diff}(X,\mathbf{B}^n U(1))$ in the [[(∞,1)-pullback]]

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

in [[∞Grpd]].

We show now that for $n \geq 1$ this reproduces the [[Deligne cohomology]] $H(X,\mathbb{Z}(n+1)_D^\infty)$ of $X$:

+-- {: .num_theorem #DeligneCohomologyTheorem}
###### Theorem

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]] we have

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

+-- {: .num_remark }
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

From the tradtional point of view of differential cohomology this may be what one expects to see, but from the intrinsic $(\infty,1)$-topos theoretic point of view it is quite unnatural -- since it violates the [[principle of equivalence]] -- to fix that set of objects of the $\infty$-groupoid. Of intrinsic meaning is only the set of their equivalences classes.

=--



### Circle bundles with connection {#CircleBundlesConnection}

Before discussing [the full theorem](#DeligneCohomologyTheorem), it is instructive to start by looking at the special case $n=1$ in some detail, which is about ordinary  $U(1)$-[[principal bundle]]s [[connection on a bundle|with connection]]. 

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

Accordingly we have for the double [[delooping]] the model

$$
  \mathbf{B}^2 U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \to 0  \to 0    
  \;)
$$

and for the [[universal principal ∞-bundle|universal principal 2-bundle]]

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
pullback in [[sSet]] we also want to resolve the curvature characteristic morphism $\mathbf{B}U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ by a fibration. We claim that this may be obtained by choosing the resolution 
$\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B} U(1)_{diff,chn}$ given by

$$
  \mathbf{B}U(1)_{diff} 
  \;\coloneqq\;
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

By the [[Poincaré lemma]] applied to each [[Cartesian space]], this is indeed a fibration.

In the [next section](#AbGerbesConnection) we give the proof of this (simple) claim. Here in the warmup phase we instead want to discuss the geometric interpretation of this resolution, along the lines of the section <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#CurvatureCharacteristicsI">curvature characteristics of 1-bundles</a> in the [[schreiber:differential cohomology in an (∞,1)-topos -- survey|survey-part]].


+-- {: .num_prop }
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

* $INN(U(1))$ is the [[2-group]] $\Xi(U(1) \to U(1))$, which is a  [[groupal model for universal principal ∞-bundles|groupal model for the universal U(1)-principal bundle]] $\mathbf{E}U(1)$;

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
    [CartSp^{op},sSet](C(\{U_i\}), \flat_{dR}\mathbf{B}^2 U(1))
  }
$$

(because the bottom vertical morphism is a fibration, by the fact that our model for $\mathbf{B}_{diff} U(1) \to \flat_{dR}\mathbf{B}^2 U(1)$ is a fibration, that $C(\{U_i\})$ is cofibrant and using the axioms of the [[nLab:sSet]]-[[nLab:enriched model category]] $[CartSp^{op}, sSet]_{proj}$).

+-- {: .num_prop}
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
      (a_{i j} \in \Omega^1(U_i \cap U_j))
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


### Circle bundles with pseudo-connection 
 {#CircleBunlePseudoConnection}

In the above discussion of extracting ordinary connections on ordinary $U(1)$-principal bundles from the abstract topos-theoretic definition of differential cohomology, we argued that a certain homotopy pullback may be computed by choosing in the Cech-hypercohomology of the complex of sheaves $(\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))$ over a manifold $X$ those cohomology representatives that happen to be represented by globally defined 2-forms on $X$. We saw that the homotopy fiber of _pseudo-connections_ over these 2-forms happened to have connected components indexed by _genuine_ connections.

But by the general abstract theory, up to isomorphism the differential cohomology computed this way is guaranteed to be independent of all such choices, which only help us to compute things.

To get a feeling for what is going on, it may therefore be useful to re-tell the analgous story with pseudo-connections that are not genuine connections.

By the very fact that $\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff}U(1)$ is a weak equivalence, it follows that every pseudo-connection is equivalent to an ordinary connection as cocycles in $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}_{diff}(G))$. 

If we choose a [[nLab:partition of unity]] $(\rho_i \in C^\infty(X,\mathbb{R}))$ subordinate to the cover $\{U_i \to X\}$, then we can construct the corresponding coboundary explicitly:

let $(A_i g_{ij}, a_{i j})$ be an arbitrary pseudo-connection cocycle. Consider the Cech-hypercohomology coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i}, 0)$. This lands in the shifted cocycle

$$
  (A'_i \coloneqq A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}, g_{i j}, a'_{i j})
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
  \nabla = (A_i \coloneqq 0, g_{i j}, a_{i j})
  \,.
$$

This fixes the pseudo-components to be $a_{i j} = - d g_{i j}$. By the above discussion, this pseudo-connection with vanishing connection 1-forms is equivalent, as a pseudo-connection, to the ordinary connection cocycle with connection forms $(A_i \coloneqq \sum_{i_0} \rho_{i_0} d g_{i_0 i})$. This is a <a href="http://ncatlab.org/nlab/show/connection+on+a+bundle#Properties">standard formula</a> for equipping $U(1)$-principal bundles with Cech cocycle $(g_{i j})$ with a connection.

### $U(1)_0$-groupoid bundles {#U1GroupoidBundle}

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

This may be understood as a cocycle for a _groupoid_ principal bundle, for the 0-truncated groupoid with $U(1)$ as its space of objects. Such a cocycle extends to a flat cocycle precisely if $f$ is _constant_ as a function. The corresponding **curvature 1-form** is $d_{dR} f$ and this is precisely the obstruction to constancy of $f$ already, in that $f$ is constant if and only if $d_{dR} f$ vanishes. _Not_ (necessarily) if it vanishes _in de Rham cohomology_ . 

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

in $\mathbf{H} = $ [[Smooth∞Grpd]] that gives the  [[fiber sequence]] $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^{n} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)$ which controls the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#GroupalCurvature">obstruction theory for flat connections</a> by a [[nLab:homotopy pullback]] realized suitably as an ordinary pullback of fibrations in $[CartSp^{op}, Ch_\bullet] \stackrel{\Xi}{\hookrightarrow} [CartSp^{op}, sSet]_{proj}$.



+-- {: .num_observation}
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
  \;\coloneqq\;
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

in $[CartSp^{op}, sSet]$ for the canoncal curvature characteristic class $curv : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ in [[Smooth∞Grpd]] with the special property that it did model the abstract [[(∞,1)-topos]]-theoretic class under the [[Dold-Kan correspondence]] precisely in terms of the familiar [[Deligne cohomology]] coefficient complex.

There is another model for the curvature class in $[CartSp^{op}, sSet]$, one that is useful for constructing the [∞-Chern-Weil homomorphism](#InfChernWeil) that maps from [[nonabelian cohomology]] in $Smooth \infty Grpd$ to $U(1)$-valued differential cohomology. This second model is the one naturally adapted to the construction of the object $\mathbf{B}^n U(1)$ by [[Lie integration]] from its [[∞-Lie algebra]] $b^{n-1} \mathbb{R}$. This is described at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegration">∞-Lie groupoid -- Lie integration</a>. 

For distinguishing the two models, we will indicate the former one by the subscript ${}_{chn}$ and the one described now by the subscript ${}_{simp}$.

+-- {: .num_defn }
###### Convention 

Here and in the following we adopt for differential forms on simplices the following notational convention:

* by $\Omega^\bullet(\Delta^n)$ we denote the complex of smooth differential forms on the standard smooth $n$-simplex with **sitting instants**: for every $k \in \mathbb{N}$ every $k$-face of $\Delta^n$ has a neighbourhood of its boundary such that the form restricted to that neighbourhood is constant in the direction perpendicular to that boundary.

* for $U \in CartSp$ we write $\Omega^\bullet(U \times \Delta^k)_{vert}$ for the complex of [[vertical differential form]]s with respect to the trivial simplex bundle $U \times \Delta^k \to U$.

=--

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$, define the [[simplicial presheaf]] $\mathbf{B}^n U(1)_{simp} \in [CartSp^{op}, sSet]$ by

$$
  \mathbf{B}^n U(1)_{simp}
  \;\coloneqq\;
  \mathbf{cosk}_{n+1}
  (
  (U, [k]) \mapsto 
   Hom_{dgAlg}(
     CE(b^{n-1}\mathbb{R}), 
     \Omega^\bullet(U \times \Delta^k)_{vert})
  )
  /\mathbf{B}^n \mathbb{Z}
  \,.
$$

Here $CE(b^{n-1}\mathbb{R})$ is the [[Chevalley-Eilenberg algebra]] of $b^{n-1}\mathbb{R}$, which is simply the graded-commutative [[dg-algebra]] (over $\mathbb{R}$) on a single generator in degree $n$ with vanishing differential.

Moreover, $\mathbf{cosk}_{n+1}(-)$ is the [[coskeleton]]-operation and the quotient is by constant $n$-forms $\omega \in \Omega^n_{cl}(U \times \Delta^k)_{vert}$ such that $\int_{\Delta^n}\omega \in \mathbb{Z}$. We take the quotient as a quotient of abelian [[simplicial group]]s (the group operation is the addition of differential forms).

=--

+-- {: .num_lemma }
###### Observation

Under the [Dold-Kan correspondence](#DoldKan) the [[Moore complex|normalized chain complex]] of $\mathbf{B}^n U(1)_{sim}$ is

$$
  N_\bullet(\mathbf{B}^n U(1)_{simp})
  =
  (
  \cdots
  \to
  \Omega^n_{cl}((-)\times \Delta^{n+1})_{vert}/\sim
  \stackrel{\sum_k (-1)^k \partial_k^* }{\to}
  \Omega^n_{cl}((-)\times \Delta^{n})_{vert}/\sim
  \to
  0 
  \to
  \cdots
  \to
  0
)
  \,,
$$

where $\partial_k : \Delta^n \to \Delta^{n+1}$ denotes the embedding of the $k$th face of the smooth $(n+1)$-[[simplex]].

=--

Here and in the following we indicate the homologically trivial part of the normalized chain complex of an $(n+1)$-coskeletal simplicial abelian group just by ellipses.

+-- {: .num_prop }
###### Proposition

The evident [[fiber integration]] of differential forms over simplices 

$$
  \int_{\Delta^n} : \Omega^\bullet(U \times \Delta^n)
   \to \Omega^\bullet(U)
$$

yields a morphism 

$$
  \int_{\Delta^\bullet} : \mathbf{B}^n U(1)_{simp} \stackrel{\simeq}{\to}
  \mathbf{B}^n U(1)
$$

in $[CartSp^{op}, sSet]_{proj}$, which is a weak equivalence.

=--

This is discussed at [[Lie integration]].

+-- {: .num_defn }
###### Definition

Write

$\mathbf{\flat} \mathbf{B}^n \mathbb{R}_{simp}$ for the [[simplicial presheaf]]

$$
  \mathbf{\flat}\mathbf{B}^n \mathbb{R}_{simp}
  \;\coloneqq\;
  \mathbf{cosk}_{n+1}
  (
    (U,[k])
    \mapsto
    Hom_{dgAlg}(
      CE(b^{n-1}\mathbb{R}),
      \Omega^{\bullet}(U \times\Delta^k)
    )
  )
$$

and write $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp} \in [CartSp^{op}, sSet]$ for the simplicial presheaf

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{simp}
  \;\coloneqq\;
  \mathbf{cosk}_{n+1}
  (
    (U,[k])
    \mapsto
    Hom_{dgAlg}(
      CE(b^{n-1}\mathbb{R}),
      \Omega^{\bullet \geq 1, \bullet}(U \times\Delta^k)
    )
  )
  \,,
$$

where on the right we have the subcomplex of $\Omega^\bullet(U \times \Delta^k)$ on those forms that are non-vanishing on some vector field tangent to $U$.

=--

At <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#DifferentialCoefficientsOfLieInt">∞-Lie groupoid -- Lie integrated ∞-groups -- Differential coefficients</a> the following is shown:

+-- {: .num_lemma }
###### Lemma

The evident [[fiber integration]] over simplices induces morphisms of simplicial presheaves

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat} \mathbf{B}^n U(1)_{simp}
  \to 
  \mathbf{\flat} \mathbf{B}^n U(1)_{chn}
$$

and

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{simp}
  \to 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)_{chn}
$$

that are weak equivalences in $[CartSp^{op}, sSet]_{proj}$.

=--



+-- {: .num_defn }
###### Definition

Write $\mathbf{B}^n  U(1)_{diff,simp}$ for the simplicial presheaf given by 

$$
  \mathbf{B}^n  U(1)_{diff,simp}
  \;\coloneqq\;
  \mathbf{cosk}_{n+1}
  (
    U,[k]
    \mapsto
   \left\{
     \array{
        \Omega^\bullet(U \times \Delta^k)_{vert}
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
  ) / \mathbf{B}^n \mathbb{Z}
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
     W(b^{n-1}\mathbb{R}) &\leftarrow& CE(b^n \mathbb{R})
  }
$$

described at [[nLab:∞-Lie algebra cohomology]].

=--

+-- {: .num_remark }
###### Remark

The set of square diagrams of [[dg-algebra]]s above is over $(U,[k])$ the set of $n$-forms $\omega$ on $U \times \Delta^k$ whose [[curvature]] $(n+1)$-form $d \omega$ has no component with all legs along $\Delta^k$.

=--

+-- {: .num_prop }
###### Proposition

The morphism given by [[fiber integration]] of differential forms over the simplex factor fits into a diagram

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



+-- {: .num_prop }
###### Proposition

Fiber integration induces a weak equivalence

$$
  \int_{\Delta^\bullet} : 
  \mathbf{B}^n \mathbb{R}_{diff,simp}
  \stackrel{\simeq}{\to}
  \mathbf{B}^n \mathbb{R}_{diff, chn}
$$

=--

+-- {: .proof}
###### Proof

Observe that $\mathbf{B}^n \mathbb{R}_{diff,simp}$ is the [[pullback]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{simp} \to \mathbf{\flat}\mathbf{B}^{n+1} \mathbb{R}_{simp}$ along the evident forgetful morphism from

$$
  (U,[k]) \mapsto \{\Omega^\bullet(U \times \Delta^k) \leftarrow
  W(b^{n-1} \mathbb{R})\}
  \,.
$$

This forgetful morphism is evidently a fibration (because it is a degreewise surjection under Dold-Kan), hence this pullback models the [[homotopy fiber]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R} \to \mathbf{\flat} \mathbf{B}^{n+1} \mathbb{R}$. Since by the above fiber integration gives a weak equivalence of pulback diagrams the claim follows.


=--



+-- {: .num_defn }
###### Definition

Write $\mathbf{B}^n U(1)_{conn,simp} \hookrightarrow \mathbf{B}^n U(1)_{diff,simp}$ for the sub-presheaf which over $(U,[k])$ is the set of those forms $\omega$ on $U \times \Delta^k$ such that the [[curvature]] $d \omega$ has no leg along $\Delta^k$.

=--

+-- {: .num_cor }
###### Corollary

Under fiber integration over simplices, $\mathbf{B}^n U(1)_{conn,simp}$ is [[quasi-isomorphism|quasi-isomorphic]] to the [[Deligne cohomology]]-complex.


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

In summary this gives us the following alternative perspective on connections on $\mathbf{B}^{n-1}U(1)$-[[principal ∞-bundle]]s: such a connection is a cocycle with values in the $\mathbf{B}^n \mathbb{Z}$-quotient of the  $(n+1)$-coskeleton of the simplicial presheaf which over $(U,[k])$ is the set of diagrams of [[dg-algebra]]s

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

### In homotopy type theory
 {#InHomtopyTypeTheory}

We discuss the formulation of the above in the [[homotopy type theory]]-[[internal language]] of the [[(∞,1)-topos]] $\mathbf{H} = $ [[Smooth∞Grpd]].

Given the two functions

$$
  \Omega^{(n+1)}_{cl} \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)
$$

(inclusion of the set of closed $(n+1)$-forms into the $(n+1)$-groupoid of de Rham cocycles)

and

$$
  curv : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)
$$

(the universal curvature class / Maurer-Cartan form of the circle $(n-1)$-group)

the [[smooth ∞-groupoid|smooth]] [[moduli ∞-stack]] of circle $n$-bundles with connection from [above](#DifferentialCohomology) is expressed in [[homotopy type theory]] as

$$
  \mathbf{B}^n U(1)_{conn} 
  \simeq
  \left\{
    P  : \mathbf{B}^n U(1) | \exists F \in \Omega^{n+1}_{cl} . curv(P) = F
  \right\}
  \,.
$$

Spelled out this expresses $\mathbf{B}^n U(1)_{conn}$  as

* the [[dependent sum]] over $\mathbf{B}^n U(1)$ of

* the [[dependent sum]] over $\Omega^n_{cl}$ of

* the [[substitution]] by $curv$ of

* the [[dependent type|dependent]] [[identity type]] on $\mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)$.

See the discussion at _[[homotopy pullback]]_ for why this is indeed interpreted by the homotopy pullback $\mathbf{B}^n U(1) \times_{\mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)} \Omega^{n+1}_{cl}$.

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


* [[Chern-Simons circle 7-bundle]].

## Properties

### Moduli

[[!include moduli of higher lines -- table]]


## Related concepts

* [differential cohomology diagram -- Examples -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)

* [[contact geometry]]

* [[higher U(1)-gauge theory]]

* [[principal infinity-connection]]

* [[curving]]. [[higher Courant groupoid]]

* [[prequantum n-bundle]], [[quantomorphism n-group]]

* [[Super Gerbes]]

## References


The above discussion is from 

* {#dcct} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .

Discussion of [[Deligne cohomology]] as classifying highe [[bundle gerbes]] ([[bundle 2-gerbes]], etc.) [[connection on a bundle gerbe|with connection]]:

* [[Pawel Gajer]], _Geometry of Deligne cohomology_, Invent. Math., 127(1):155-207 (1997) ([arXiv:alg-geom/9601025](http://arxiv.org/abs/alg-geom/9601025), [doi:10.1007/s002220050118](https://doi.org/10.1007/s002220050118))


[[!redirects circle n-bundles with connection]]
[[!redirects circle n-bundles with connections]]


[[!redirects circle n-bundle]]
[[!redirects circle n-bundles]]

[[!redirects line bundle with connection]]
[[!redirects line bundles with connection]]
[[!redirects line n-bundle with connection]]
[[!redirects line n-bundles with connection]]


[[!redirects circle bundle with connection]]
[[!redirects circle bundles with connection]]
[[!redirects circle-bundle with connection]]
[[!redirects circle-bundles with connection]]


[[!redirects circle 2-bundle with connection]]
[[!redirects circle 2-bundles with connection]]

[[!redirects circle 3-bundle with connection]]
[[!redirects circle 3-bundles with connection]]

[[!redirects circle n-connection]]
[[!redirects circle n-connections]]


