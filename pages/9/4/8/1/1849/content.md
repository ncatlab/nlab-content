
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The field content of 11-dimensional [[nLab:supergravity]] contains a field called the _supergravity C-field_ or _M-theory 3-form_ , which is locally a 3-form and globally _some_ variant of a [[circle n-bundle with connection|circle 3-bundle with connection]]. There have been several suggestions for what _precisely_ its correct global description must be.


## The DFM-model
 {#DFMmodel}

### Construction via $E_8$ gauge fields

In ([DFM, section 3](#DFM)) the following definition is considered and argued to be a good model of the supergravity $C$-field.


Notice that the [[homotopy group]]s of the [[classifying space]] $B E_8$ of the [[Lie group]] [[E8]] satisfy

$$
  \pi_i B E_8 = 
   \left\{
     \array{
       \mathbb{Z} | i = 4
       \\
       0 | i \neq 4, i \leq 15
     }
   \right.
  \,.
$$

Therefore for $X$ a [[nLab:manifold]] of [[nLab:dimension]] $dim X \leq 5$ there is a canonical [[nLab:morphism]]

$$
  H^1(X, E_8)
  \simeq
  H^4(X, \mathbb{Z})
  \,.
$$

+-- {: .num_defn}
###### Definition

Let $X$ be a [[nLab:smooth manifold]] of [[nLab:dimension]] $dim X \lt 15$.
For each  $a \in H^4(X, \mathbb{Z})$. choose an [[nLab:E8]]-[[nLab:principal bundle]] $P \to X$ which represents $a$ under the above isomorphism.

Write then

$$
  \mathbf{E}(X) \in Grpd
$$

for the [[nLab:groupoid]] whose 

* [[nLab:object]]s are triples $(P,\nabla,c)$ where 

  * $P$ is one of the chosen $E_8$-bundles, 

  * $\nabla$ is a [[nLab:connection on a bundle|connection]] on $P$;

  * $c \in \Omega^3(X)$ is a degree-3 [[nLab:differential form]] on $X$.

* [[nLab:morphism]]s $\omega : (P, \nabla_1, c_1) \to (P, \nabla_2, c_2)$
  are parameterized by their source and target triples together with a closed 3-form  $\omega \in \Omega^3_{\mathbb{Z}}(X)$ with integral [[period]]s, subject to the condition that

  $$
    c_2 -c_1 = CS(\nabla_1,\nabla_2) + F_\omega
    \,,
  $$

  where 

  * $CS(\nabla_1, \nabla_2)$ is the relative [[nLab:Chern-Simons form]] corresponding to the linear path of connections from $\nabla_1$ to $\nabla_2$ 

  * and $F_\omega$ is the [[nLab:curvature]] 4-form of the differential cohomology class.

* the [[nLab:composition]] of morphisms 

  $$    
    (\omega_2 \circ \omega_1 )
     :
    (P,\nabla_1, C_1)
      \stackrel{\omega_1}{\to}
    (P, \nabla_2, C_2)
      \stackrel{\omega_2}{\to}
    (P, \nabla_3, C_3)
  $$

  is given by

  $$
    \omega_1 + \omega_2 + \langle (\nabla_2-\nabla_1)\wedge(\nabla_3-\nabla2) \rangle
   \,.
  $$

=--

See ([DFM, (3.22), (3.23)](#DFM)).

Here we think of $X$ as equipped with a [[pseudo-Riemannian manifold|pseudo]] [[Riemannian manifold|Riemannian structure]] and [[spin connection]] $\omega$ and think of each object $(P,\nabla,C)$ of $\mathbf{E}(X)$ as inducing an degree-4 cocycle in [[ordinary differential cohomology]] with [[curvature]] 4-form

$$
  \mathcal{G}_{\nabla,c} = tr F_\nabla \wedge F_\nabla - \frac{1}{2} tr R_\omega \wedge R_\omega + d c
  \,.
$$

### Orientation and fractional classes

Ordinarily, given a $Spin \times E_8$-bundle $P \to Y$ with first fractional [[Pontryagin class]]

$$
  \lambda := \frac{1}{2}p_1(P)
$$

and second [[Chern class]]

$$
  a := c_2(P)
$$

the $C$-field is supposed to have a [[curvature]] class in [[de Rham cohomology]] given by 

$$
  a_{dR} + \frac{1}{2} \lambda_{dR} \in H_{dR}^4(Y)
  \,.
$$

Since in general $\lambda = \frac{1}{2}p_1(P)$ is not further divisible in integral cohomology, this means that this cannot be the curvature of any [[differential character]]/[[bundle 2-gerbe]]/[[circle n-bundle with connection|circle 3-bundle with connection]], since these are necessarily the images in de Rham cohomology of their integral classes.

See also ([DFM, section 12.1](#DFM)) where it is argued that this is related to boundaries and orientation double covers.


### Restriction to the boundary

By [DFM, section 12](#DFM) on a manifold $Y$ with boundary $X = \partial Y$ we are to impose $C|_{\partial Y} = 0$. 

See the discussion [below](#RestrictionToBoundaryInChernWeil) for how this reproduces the [[Green-Schwarz mechanism]] for heterotic [[supergravity]] on the boundary.





## Description in $\infty$-Chern-Weil theory

Some remarks on ways to regard the $C$-field from the point of view of [[∞-Chern-Weil theory]].

### Abstract definition

We shall consider the sum of two $C$ fields,  whose curvature is the image in de Rham cohomology of the proper integral class $2 a - \lambda $

Recall from the discussion at [[circle n-bundle with connection]]
that in the [[cohesive (∞,1)-topos]] $\mathbf{H} := $ [[Smooth∞Grpd]] the circle 3-bundles with local 3-form connection over an [[object]] $Y \in \mathbf{H}$ (for instance a [[smooth manifold]], or an [[orbifold]]) are [[object]]s in the [[3-groupoid]] $\mathbf{H}_{diff}(X, \mathbf{G}^3 U(1))$ that is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(Y, \mathbf{B}^3 U(1)) &\to& H^4_{dR}(Y)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
$$

in [[∞Grpd]].

(Recall from the discussion there that if desired one may pass to the canonical presentation of this by the [[model structure on simplicial presheaves]] over [[CartSp]] and that in this explicit presentation we may replace $H^4_{dR}(Y)$ with the more familiar $\Omega^4_{cl}(Y)$. )

We consider now the analog of this definition for the universal curvature form on $\mathbf{B}^3 U(1)$ replaced by the difference of the differentially refined second [[Chern class]] of [[E8]] and the first fractional [[Pontryagin class]] of the [[spin group]]. The resulting $(\infty,1)$-pullback we tentatively call $C Field(Y)$.

$$
  \array{
    C Field(Y) &\to& H^4_{dR}(Y)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(Y, \mathbf{B} (Spin \times E_8))
    &\stackrel{(2\mathbf{c}_2)_{dR}- (\frac{1}{2}\mathbf{p}_1)_{dR}}{\to}&
    \mathbf{H}(Y, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,.
$$

Notice that by its <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ChernWeilTheory">intrinsic definition</a> we have that $(\mathbf{c}_2)_{dR}$ is the composite

$$
  (\mathbf{c}_2)_{dR} : 
  \mathbf{B}E_8
   \stackrel{\mathbf{c}_2}{\to}
  \mathbf{B}^3 U(1)
    \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)
$$ 

of the smooth second Chern-class with the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature form</a> on $\mathbf{B}^3 U(1)$. Similarly for $(\frac{1}{2}\mathbf{p}_2)_{dR}$.


This implies by the [[pasting law]] for [[(∞,1)-pullback]]s that the above $(\infty,1)$-pullback may be decomposed into two consecutive pullbacks of the form

$$
  \array{
    C Field(X) &\stackrel{\hat \chi}{\to}& \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))
     &\stackrel{\omega}{\to}&
     H^4_{dR}(X)
   \\
    \downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}E_8)
    &\stackrel{2\mathbf{c}_2- \frac{1}{2}\mathbf{p}_2}{\to}&
   \mathbf{H}(X, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
   \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,,
$$

where on the right we find the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">defining pullback</a> for (the [[cocycle]] [[3-groupoid]] of) [[ordinary differential cohomology]].

This immediately implies the following two properties

1. There exists canonically a morphism

   $$
     \hat \chi : C Field(X) \to \mathbf{H}(X,\mathbf{B}^3 U(1))
       \stackrel{\tau_{\leq 0}}{\to}
       H^4_{diff}(X)
   $$

   that maps $C$-field configurations to [[ordinary differential cohomology]] in degree 4, whose [[curvature]] $\omega(\hat \chi)$ is the image $(\mathbf{c}_2)_{dR} :=  curv(2\mathbf{c}_2 - \frac{1}{2}\mathbf{p}_2)$ in de Rham cohomology of the second Chern-class of some $E_8$-bundle.

1. The differential cocycle $\hat \chi(C)$ has all the general properties that make its [[higher parallel transport]] over [[membrane]] worldvolumes be well-defined. (Apart from the coefficient of $\lambda$, this is the only requirement from which [DFM](#DFM) deduce their model.)


### Explicit presentation by differential form data

In order to compute the $(\infty,1)$-pullback $C Field(X)$ more explicitly, we follow the discussion at  [[differential string structure]], where presentations of this pullback in terms of [[simplicial presheaves]] arising from  [[Lie integration]] is given.

Write now

$$
  \mathfrak{g} := \mathfrak{e}_8 \times \mathfrak{e}_8 \times \mathfrak{so}(10,1)
$$

for the [[Lie algebra]] of $G := E_8 \times E_8 \times Spin(10,1)$ and write

$$
  \mu := \mu_{\mathfrak{e}_8} + \mu_{\mathfrak{e}_8} - \mu_{\mathfrak{so}(10,1)}
$$

for the sum of the canonical [[Lie algebra cohomology|Lie algebra cocycles]] in [[transgression]] with the respective [[Killing form]] [[invariant polynomial]]s.

Write

$$
  \mathfrak{e}_8 \times \mathfrak{so}(10,1) 
   \to \mathfrak{g}
$$

for the canonical [[diagonal]] embedding
Write 

$$
  \array{
    \mathbf{c} := 
    &
    \mathbf{cosk}_3(
       \exp(\mathfrak{e}_8 \times \mathfrak{so}(10,1))
    )
    &\stackrel{\Delta}{\to}&
    \mathbf{cosk}_3(
       \exp(\mathfrak{g})
    )
     &
      \stackrel{\exp(\mu)}{\to}
     &
    \mathbf{B}^3 U(1)_c
    \\
    \downarrow^{\simeq} 
     \\
     \mathbf{B}G
  }
$$

for the corresponding smooth [[characteristic class]]. See [[∞-Chern-Weil homomorphism]] for details. By the discussion there we present 
$\hat \mathbf{c}$ by

$$
  \array{
    \mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{diff}
    &\to&
    \mathbf{B}^4 \mathbb{R}_{dR}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}E_8
  }
  \,.
$$

By the discussion at [[differential string structure]] we have that the top morphism is a [[fibration]] in the global projective [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj}$ (there it is shown that the analogous morphism out of $\mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{e}_8)_{ChW}$ is a fibration, but then so is this one, because the components on the left are the same but with fewer conditions on them, so that the lifts that existed before still exist here).

Over some $U \in$ [[CartSp]] and $[k] \in \Delta$ we have that $\exp(b^\mathbb{R} \to \mathfrak{g}_\mu)_{diff}$ is given by differential form data

$$
  \left(
    \array{ 
      F_A =& d A + \frac{1}{2}[A \wedge A]
      \\
      C_3 =& \nabla B := d B + CS(A) - H_3 
      \\
      \mathcal{G}_4  =& d H_3
      \\
      d F_A =& - [A \wedge F_A]
      \\
      d C_3 =&  \langle F_A \wedge F_A\rangle - \mathcal{G}_4
      \\
      d \mathcal{G}_4 =& 0
    }
  \right)_i
  \;\;\;\;
  \stackrel{
    \array{
       t^a & \mapsto A^a
       \\
       r^a & \mapsto F^a_A
       \\
       b & \mapsto B
       \\
       c & \mapsto C_3
       \\
       h & \mapsto H_3
       \\
       g & \mapsto \mathcal{G}_4
    }
  }{\leftarrow}|
  \;\;\;\;
  \left(
    \array{  
       r^a  =& d t^a + \frac{1}{2}C^a{}_{b c} t^b \wedge t^c + 
       \\
       c = & d b + cs - h     
       \\
       g  =& d h
       \\
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d c =& \langle -,-\rangle - g 
       \\
       d g =&  0 
    }
  \right)
$$

on $U \times \Delta^k$. Here, recall, $A$ takes values in $\mathfrak{g} = \mathfrak{e}_8 \times \mathfrak{e} \times \mathfrak{so}(10,1)$, so that for instance the $\mathcal{G}_4$-curvature is in detail given by

\[
  \label{TheFourCurvature}
  \mathcal{G}_4
  =
  d H_3  
  = 
  \langle F_{A^L_{\mathfrak{e}_8}} \wedge F_{A^L_{\mathfrak{e}_8}} \rangle
  + 
  \langle F_{A^R_{\mathfrak{e}_8}} \wedge F_{A^R_{\mathfrak{e}_8}} \rangle
  -
  \langle F_{\omega} \wedge F_{\omega} \rangle
  -
  d C_3
  \,,
\]

where $\omega$ denotes the [[spin connection]].

Let $\{U_i \to X\}$ be a differentiably [[good open cover]]. We hit all connected components of $\mathbf{H}(X, \mathbf{B}G)$ by considering in 

$$
  [CartSp^{op}, sSet](C(U_i), \exp(b \mathbb{R} \to \mathfrak{g}_\mu))_{diff}
$$

those cocycles that

* involve genuine $G$-[[connection on a bundle|connections]] (as opposed to the more general [[pseudo-connection]]s that are also contained);

* have a globally defined $C_3$-form.

Write therefore $(P, \nabla, C_3)$ for such a cocycle. 

For gauge transformations between two such pairs, parameterized by the above form data patchwise on  $U \times \Delta^1$, the fact that $\mathcal{G}_4$ vanishes on $\Delta^1$ implies the <a href="http://nlab.mathforge.org/nlab/show/infinity-Chern-Weil+theory+introduction#InfGaugeTrafo">infinitesmal gauge transformation</a> law

$$
  \frac{d}{d t} C = D_U \omega_t 
   + \iota_t \langle F_{\hat A} \wedge F_{\hat A}\rangle
  \,,
$$

where $\hat A\in \Omega^1(U \times \Delta^1, \mathfrak{e}_8)$ is the shift of the 1-forms. This integrates to

\[
  \label{CGaugeTransformation}
  C_2 = C_1 + d \omega + CS(\nabla_1,\nabla_2)
  \,,
\]

where 

* $\omega := \int_{\Delta^1} \omega_t$

* $CS(\nabla_1, \nabla_2) = \int_{\Delta^1} \langle F_{\hat \nabla} \wedge F_{\hat \nabla}\rangle $ is the relative [[Chern-Simons form]] corresponding to the shift of $G$-connection.



### Restriction to the boundary
  {#RestrictionToBoundaryInChernWeil}

We have seen that $C Field(Y)$ is the 3-goupoid of those [[Cech cohomology|Cech cocycles]] on $Y$ with coefficients in $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{diff}$ such that the curvature 4-form $\mathcal{G}_4$ has a fixed globally defined value. 

Consider the [[subobject]] 

$$
  \exp(b \mathbb{R} - \mathfrak{g}_\mu)_{diff}^{C = 0}
  \hookrightarrow
  \exp(b \mathbb{R} - \mathfrak{g}_\mu)_{diff}
$$

of the [[simplicial presheaf]] $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)$ on those [[object]]s and [[k-morphism]]s for which $C = 0$.

By the [[gauge transformation]] law (eq:CGaugeTransformation)

$$
  C_2 = C_1 + d \omega + CS(A_1, A_2)
$$

this means that this picks those [[morphism]]s for which the [[Chern-Simons form]] vanishes

$$
  CS(A_1,A_2) = \int_{\Delta^1} \langle F_{A} \wedge F_{A}\rangle 
  = 0
  \,,
$$

where $A = A_U + \lambda d t \in \Omega^1(U \times \Delta^1, \mathfrak{g})$ is the 1-form datum (with $t$ the canonical coordinate on the 1-[[simplex]] $\Delta^1 = [0,1]$).

Notice that on the [[semisimple Lie algebra]] and [[compact Lie algebra]] $\mathfrak{e}_8$ the [[Killing form]] \langle -,-\rangle in non-degenerate and positive definite (or negative definite, depending on convention). The latter condition means that this integral vanishes precisely if

$$
  \iota_{\partial_t} \langle F_A \wedge F_A \rangle = 0
  \,.
$$

This is the case on paths for which $\iota_t F_A = 0 $, but this are exactly the paths that induce genuine [[gauge transformation]]s between $A_1$ and $A_2$, where 

$$
  \frac{d}{d t} A = d_U \lambda + [\lambda , A]
  \,.
$$

This means that cocycles with coefficients in this subobject for $C = 0$ are cocycles as described at [[differential string structure]], exhibiting the [[Green-Schwarz mechanism]] on the heterotic boundary, witnessed by the restriction of the curvature equation (eq:TheFourCurvature) to vanishing $C$-field

\[
  d H_3^L  
  = 
  \langle F_{A^L_{\mathfrak{e}_8}} \wedge F_{A^L_{\mathfrak{e}_8}} \rangle
  -
  \frac{1}{2}\langle F_{\omega} \wedge F_{\omega} \rangle
\]


## Related concepts

* [[electromagnetic field]] ("$A$-field")

* [[Kalb-Ramond field]] ("$B$-field") 

* **supergravity $C$-field**

## References

The state-of-the-art in the literature concerning attempts to find the correct mathematical model for the supergravity C-field seems to be

* E. Diaconescu, [[Greg Moore]], [[Dan Freed]], _The $M$-theory 3-form and $E_8$-gauge theory_ ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069))
 {#DFM}

The discussion from the point of view of the $\infty$-Chern-Weil homomorphism is part of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _Higher differemtial $Spin^c$-structures_
 {#FiSaSc}
