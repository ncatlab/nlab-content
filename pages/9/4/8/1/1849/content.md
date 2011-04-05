
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
  are parameterized by their source and target triples together with a [[nLab:cocycle]] $\omega \in H_diff{X}$ in the [[nLab:ordinary differential cohomology]] of $X$, subject to the condition that

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


## Description in $\infty$-Chern-Weil theory

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
    \mathbf{H}(X, \mathbf{B} E_8)
    &\stackrel{\hat \mathbf{c}_2}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,.
$$

In order to compute this $(\infty,1)$-pullback, we follow the discussion at  [[differential string structure]], where presentations of this pullback in terms of [[simplicial presheaves]] arising from  [[Lie integration]] is given.

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
      C_3 =& \nabla B := d B + CS(A) - Q_3 
      \\
      \mathcal{G}_4  =& d Q_3
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
       q & \mapsto Q_3
       \\
       g & \mapsto \mathcal{G}_4
    }
  }{\leftarrow}|
  \;\;\;\;
  \left(
    \array{  
       r^a  =& d t^a + \frac{1}{2}C^a{}_{b c} t^b \wedge t^c + 
       \\
       c = & d b + cs - q     
       \\
       g  =& d q
       \\
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d c =& \langle -,-\rangle - g 
       \\
       d g =&  0 
    }
  \right)
$$

on $U \times \Delta^k$. (Notice that compared to the discussion at [[differential string structure]] we have renamed $H$ to $C$ and $C$ to $Q$ to fit standard notation as far as possible.) 

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

(...)



## Related concepts

* [[electromagnetic field]] ("$A$-field")

* [[Kalb-Ramond field]] ("$B$-field") 

* **supergravity $C$-field**

## References

* E. Diaconescu, [[Greg Moore]], [[Dan Freed]], _The $M$-theory 3-form and $E_8$-gauge theory_ ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069))
 {#DFM}
