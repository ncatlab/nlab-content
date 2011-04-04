
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

The field content of 11-dimensional [[nLab:supergravity]] contains a field called the _supergravity C-field_ or _M-theory 3-form_ , which is locally a 3-form and globally _some_ variant of a [[circle n-bundle with connection|circle 3-bundle with connection]]. There have been several suggestions for what _precisely_ its correct global description must be.


## The DFM-model

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

+-- {: .un_defn}
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

## Description in $\infty$-Chern-Weil theory

Here we describe a natural construction in [[∞-Chern-Weil theory]] which assigns to every [[smooth manifold]] [[3-groupoid]] of structures consisting of pairs of a [[circle n-bundle with connection|circle 3-bundle]] and an [[E8]]-[[principal bundle]] that differentially twist each other via the refined [[Chern-Weil homomorphism]] induced by the [[Killing form]] on $\mathfrak{e}_8$. We show that the 1-[[truncated|truncation]] of this 3-groupoid is the 1-grooupoid of such structures that is considered in ([DFM](#DFM)).

(...)

See the discussion at [[differential string structure]] for the moment





## Related concepts

* [[electromagnetic field]] ("$A$-field")

* [[Kalb-Ramond field]] ("$B$-field") 

* **supergravity $C$-field**

## References

E. Diaconescu, [[nLab:Greg Moore]], [[nLab:Dan Freed]], _The $M$-theory 3-form and $E_8$-gauge theory_ ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069))
 {#DFM}
