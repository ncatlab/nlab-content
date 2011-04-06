
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

Notice that the [[nLab:homotopy group]]s of the [[nLab:classifying space]] $B E_8$ of the [[nLab:Lie group]] [[nLab:E8]] satisfy

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

Some remarks on ways to regard similar cohomological situations from the point of view of [[∞-Chern-Weil theory]].

### Abstract definition

We shall consider here first the case of the double $C$-field, whose curvature is the image in de Rham cohomology of the proper integral class $2 a - \lambda $

Recall from the discussion at [[circle n-bundle with connection]]
that in the [[cohesive (∞,1)-topos]] $\mathbf{H} := $ [[Smooth∞Grpd]] the circle 3-bundles with local 3-form connection over an object $X \in \mathbf{H}$ are cocycles in the object $\mathbf{H}_{diff}(X, \mathbf{G}^3 U(1))$ that is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1)) &\to& H^4_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,.
$$

We consider now the analog of this definition for the universal curvature form on $\mathbf{B}^3 U(1)$ replaced by the differentially refined second [[Chern class]] of [[E8]].

$$
  \array{
    C Field(X) &\to& H^4_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B} (Spin \times E_8))
    &\stackrel{(2\mathbf{c}_2)_{dR}- (\frac{1}{2}\mathbf{p}_1)_{dR}}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,.
$$

By its <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ChernWeilTheory">intrinsic definition</a> we have that $(\mathbf{c}_2)_{dR}$ is the composite

$$
  (\mathbf{c}_2)_{dR} : 
  \mathbf{B}E_8
   \stackrel{\mathbf{c}_2}{\to}
  \mathbf{B}^3 U(1)
    \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)
$$ 

of the smooth second Chern-class with the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature form</a> on $\mathbf{B}^3 U(1)$. Similarly for $(\frac{1}{2}\mathbf{p}_2)_{dR}$.

By the pasting law for [[(∞,1)-pullback]]s, this implies that the above $(\infty,1)$-pullback may be decomposed into two consecutive pullbacks of the form

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

This immediately yields the existence of the morphism

$$
  \hat \chi : C Field(X) \to \mathbf{H}(X,\mathbf{B}^3 U(1))
    \stackrel{\tau_{\leq 0}}{\to}
    H^4_{diff}(X)
$$

that maps $C$-field configurations to [[ordinary differential cohomology]] in degree 4, whose [[curvature]] $\omega(\hat \chi)$ is the image $(\mathbf{c}_2)_{dR} :=  curv(2\mathbf{c}_2 - \frac{1}{2}\mathbf{p}_2)$ in de Rham cohomology of the second Chern-class of some $E_8$-bundle.

Notice that this also immediately implies that $\hat \xhi(C)$ has all the general properties that make its [[higher parallel transport]] over [[membrane]] worldvolumes be well-defined.


### Explicit presentation by differential form data

In order to compute the $(\infty,1)$-pullback $C Field(X)$ more explicitly, we follow the discussion at  [[differential string structure]], where presentations of this pullback in terms of [[simplicial presheaves]] arising from  [[Lie integration]] is given.

Using this we presents $\hat \mathbf{c}_2$ by

$$
  \array{
    \mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{e}_8)_{diff}
    &\to&
    \mathbf{B}^4 \mathbb{R}_{dR}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}E_8
  }
  \,.
$$

By the discussion there we have that the top morphism is a fibration (there it is shown that the analogous morphism out of $\mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{e}_8)_{ChW}$ is a fibration, but then so is this one, because the components on the left are the same but with fewer conditions on them, so that the lifts that existed before still exist here).

Over some $U \in$ [[CartSp]] and $[k] \in \Delta$ we have that $\exp(b^\mathbb{R} \to \mathfrak{e}_8)_{diff}$ is given by differential form data

$$
  \left(
    \array{ 
      F_\omega =& d A + \frac{1}{2}[A \wedge A]
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

on $U \times \Delta^k$. 
Let $\{U_i \to X\}$ be a differentiably [[good open cover]]. We hit all connected components of $\mathbf{H}(X, \mathbf{B}E_8)$ by considering in 

$$
  [CartSp^{op}, sSet](C(U_i), \exp(b \mathbb{R} \to \mathfrak{e}_8))_{diff}
$$

those cocycles that

* involve genuine $E_8$-[[connection on a bundle|connections]] (as opposed to the more general [[pseudo-connection]]s that are also contained);

* have a globally defined $C_3$-form (this is globally defined in $\exp(b\mathbb{R} \to (\mathfrak{e}_8)_\mu)_{ChW}$ since $$ )

Write therefore $(P, \nabla, C_3)$ for such a cocycle. 

For gauge transformations between two such pairs, parameterzed by the above form data patchwise on  $U \times \Delta^1$, the fact that $\mathcal{G}_4$ vanishes on $\Delta^1$ implies the <a href="http://nlab.mathforge.org/nlab/show/infinity-Chern-Weil+theory+introduction#InfGaugeTrafo">infinitesmal gauge transformation</a> law

$$
  \frac{d}{d t} C = D_U \omega_t 
   + \iota_t \langle F_{\hat A} \wedge F_{\hat A}\rangle
  \,,
$$

where $\hat A\in \Omega^1(U \times \Delta^1, \mathfrak{e}_8)$ is the shift of the 1-forms. This integrates to

$$
  C_2 = C_1 + d \omega + CS(\nabla_1,\nabla_2)
  \,,
$$

where 

* $\omega := \int_{\Delta^1} \omega_t$

* $CS(\nabla_1, \nabla_2) = \int_{\Delta^1} \langle F_{\hat \nabla} \wedge F_{\hat \nabla}\rangle $ is the relative [[Chern-Simons form]] corresponding to the shift of $E_8$-connection.

### Restriction to the boundary
  {#RestrictionToBoundaryInChernWeil}

We have seen that $C Field(Y)$ is the 3-goupoid of those [[Cech cohomology|Cech cocycles]] on $Y$ with coefficients in $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{diff}$ such that the curvature 4-form $\mathcal{G}_4$ has a fixed globally defined value. 

Consider the subobject of the [[simplicial presheaf]] $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)$ on those cells for which $C = 0$.

By the above grauge transformation law

$$
  C_2 = C_1 + d \omega + CS(A_1, A_2)
$$

this means that this picks those [[morphism]]s for which the 

$$
  CS(A_1,A_2) = \int_{\Delta^1} \langle F_{A} \wedge F_{A}\rangle 
  = 0
  \,,
$$

where $A = A_U + \lambda d t \in \Omega^1(U \times \Delta^1, \mathfrak{g})$ is the 1-form datum.

This is the case on paths for which $\iota_t F_A = 0 $, but this are exactly the paths that induce genuine [[gauge transformation]]s between $A_1$ and $A_2$, where 

$$
  \frac{d}{d t} A = d_U \lambda + [\lambda , A]
  \,.
$$

This means that cocycles with coefficients in this subobject for $C = 0$ are cocycles as described at [[differential string structure]], exhibiting the [[Green-Schwarz mechanism]] on the heterotic boundary.

## Related concepts

* [[electromagnetic field]] ("$A$-field")

* [[Kalb-Ramond field]] ("$B$-field") 

* **supergravity $C$-field**

## References

* E. Diaconescu, [[Greg Moore]], [[Dan Freed]], _The $M$-theory 3-form and $E_8$-gauge theory_ ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069))
 {#DFM}
