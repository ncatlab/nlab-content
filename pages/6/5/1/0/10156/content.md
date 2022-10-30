
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The 2-[[sphere]] $S^2$ is naturally equipped with the structure of a [[symplectic manifold]] with symplectic form its canonical [[volume form]], up to a constant factor. As such, one can consider its [[geometric quantization]]. 

From the point of view of [[physics]], this is a [[mechanical system]] that describes a rigid [[rotor]] or [[spinor]] in 3-dimenensional [[Euclidean space]] (and just the rotation/spin degrees of freedom, not the translational degrees of freedom). Accordingly, the coresponding [[Hilbert space|Hilbert]]-[[space of quantum states]] carries a natural [[Hamiltonian action]] by the [[angular momentum]] [[quantum operators]] that generate the rotation of the sphere.

More abstractly in [[mathematics]], the 2-sphere is naturally identified with a [[coadjoint orbit]] of the [[special unitary Lie algebra]]/[[special unitary group]] $\mathfrak{su}(2)/SU(2)$ (and hence of the [[spin group]] $Spin(3)$, by one of the [exceptional isomorphisms](spin+group#ExceptionalIsomorphisms)). As such the [[geometric quantization]] of the 2-sphere is a special case of the general [[orbit method]]. In this case it identifies the quantization of the [[Hamiltonian action]] of $SU(2)$ on $S^2$ in terms of [[quantum operators]] acting on the [[space of quantum states]] with an [[irreducible representation]] of $SU(2) \simeq Spin(3)$.

## Details

### Basic parameterizations

For all of the following it is useful to choose an adapted [[atlas]] of [[coordinate charts]] on the 2-sphere, namely that induced by regarding it as the [[Riemann sphere]].

+-- {: .num_defn #RiemannSphere}
###### Definition

Choose any point $x_{\infty} \in S^2$. Then the complement $S^2 - \{x_\infty\}$ is [[diffeomorphism|diffeomorphic]] to the [[plane]] $\mathbb{R}^2$, which in turn we regard as the [[complex plane]]. Hence 

$$
  \mathbb{C} \simeq U_{+} \coloneqq (S^2 - \{x_\infty\}) \hookrightarrow S^2
$$

is one [[coordinate chart]] on the 2-sphere. Accordingly, removing the antipodal point

$$
  x_0 \coloneqq 0 \in \mathbb{C} \simeq U_+
$$

yields another [[coordinate chart]]

$$
  \mathbb{C} \simeq U_{-} \coloneqq (S^2 - \{x_0\}) \hookrightarrow S^2
  \,.
$$

We denote the canonical complex coordinate function on $U_{+/-}$ by $z_{+/-}$, respectively. In terms of these the canonical identification of the two coordinate charts on their common overlap

$$
  (\mathbb{C} - \{0\}) 
  \simeq 
  S^2 - \{x_0, x_\infty\} \simeq (U_+ - \{x_0\}) 
  \to 
  (U_- - \{x_\infty\}) 
  \simeq
  (S^2 - \{x_0, x_\infty\})
  \simeq
  (\mathbb{C} - \{0\})
$$

is given by

$$
  z \mapsto z^{-1}
  \,.
$$

Hence on $S^2 - \{x_0, x_\infty\}$ the two coordinate functions are complex inverses of each other

$$
  z_+ = (z_-)^{-1}
  \,.
$$

This defines an [[atlas]] by two open charts which defines the 2-[[sphere]] as a [[smooth manifold]]. Since both patches are complex planes and the transition function is a [[holomorphic function]] this moreover gives $S^2$ the structure of a [[complex manifold]]. As such it is called the _[[Riemann sphere]]_.

=--


### The symplectic structure

By the canonical embedding

$$
  S^2 \hookrightarrow \mathbb{R}^3
$$

into the 3-[[dimension|dimensional]] [[Cartesian space]] as the unit 2-sphere given by

$$
  S^2 = \left\{ (x_1, x_2, x_2) \in \mathbb{R}^3 \;|\; (x_1)^2 + (x_2)^2 + (x_3)^2 = 1 \right\}
$$

the 2-[[sphere]] inherits a [[Riemannian metric]] as the [[pullback of a differential form|pullback]] of the canonical metric $\sum_{i = 1} ^3  d x_i \otimes d x_i$  on $\mathbb{R}^3$. 

+-- {: .num_prop}
###### Proposition

In the [[coordinate charts]] of def. \ref{RiemannSphere}, the canonical functions

$$
  x_i \colon (S^2 - \{x_\infty\}) \hookrightarrow \mathbb{R}^3 \stackrel{x_i}{\to} \mathbb{R}
$$

have the expressions

* $x_1 = \frac{1}{2} \frac{z_+ + \overline{z}_+}{1 - {\vert z_+\vert}^2}$

* $x_2 = -\frac{i}{2} \frac{z_+ - \overline{z}_+}{1 - {\vert z_+\vert}^2}$

* $x_3 = 1 - \frac{1}{1 + {\vert z_+\vert}^2}$.


=--

+-- {: .num_prop}
###### Proposition

The canonical [[Riemannian metric]] on $S^2$ induces the [[volume form]] $\omega_1 \in \Omega^2(S^2)$ given in the [[coordinate charts]] of def. \ref{RiemannSphere} by

$$
  \omega_1
  =  
  \frac{1}{(1 + {\vert z\vert}^2)^2}
  d z \otimes d \overline{z} 
  \,.
$$

More generally, for $S^2 \hookrightarrow \mathbb{R}^3$ embedded as the 2-sphere of [[radius]] $k \in (0,\infty)$, the corresponding volume form is 

$$
  \omega_k
  =  
  \frac{k}{(1 + {\vert z\vert}^2)^2}
  d z \otimes d \overline{z} 
  \,.
$$


=--

+-- {: .num_prop #KaehlerStructure}
###### Proposition

Equipped with this [[Riemannian metric]] for $k \in (0,\infty)$ and with the [[complex manifold]] structure of def. \ref{RiemannSphere} the 2-sphere is a [[Kähler manifold]] with 

* [[Kähler potential]] 

  $$
    K_k(z,\overline{z}) = - k log(1 + {\vert z^2\vert})
    \,.
  $$

* [[Kähler form]] 
 
  $$
   \begin{aligned}\omega_k & = \partial \overline{\partial} K_k \\  & = \frac{k}{(1 + {\vert z\vert}^2)^2}
  d z \otimes d \overline{z} \end{aligned}
  \,.
  $$


=--










### The Hamiltonian $SU(2)$-action

(...)

### The prequantum line bundle and the metaplectic correction

+-- {: .num_remark}
###### Remark

Hermitian [[complex line bundles]] on the 2-sphere are classified by $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$. By the [[clutching construction]] a line bundle given by two trivializing sections $\sigma_1, \sigma_2$ of the trivial line bundle on the coordinate patch $\mathbb{C}$ has class the [[winding number]] of the transition function

$$
  S^1 \hookrightarrow \mathbb{C} - \{0\}
  \stackrel{s_2 s_1^{-1}}{\to} \mathbb{C}^\times
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the discussion there, a [[spin structure]] on $S^2$ is equivalently a [[square root]] $\sqrt{\Omega^{1,0}} \in \mathbf{Line}_{\mathbb{C}}(S^2)$ of the [[canonical line bundle]] $\Omega^{1,0}$, which here is simply the holomorphic 1-form bundle.

=--

+-- {: .num_prop}
###### Proposition

The [[first Chern class]] of the [[canonical line bundle]] on the 2-sphere is

$$
  c_1\left(\Omega^{2,0}\left(S^2\right)\right)
  = 
  2
  \in 
  \mathbb{Z} \simeq H^2(S^2, \mathbb{Z})
$$

(up to a unique choice of sign, which determines the [[isomorphism]] on the right). Accordingly the 2-sphere has an essentially unique [[spin structure]] whose [[theta characteristic]] $\sqrt(\Omega^{2,0})$ is the complex line bundle with [[first Chern class]]

$$
  c_1\left(\sqrt{\Omega^{2,0}\left(S^2\right)}\right)
  = 
  1
  \in 
  \mathbb{Z} \simeq H^2(S^2, \mathbb{Z})
  \,.
$$


=--

+-- {: .proof}
###### Proof


The canonical section of the holomorphic 1-form bundle on $\mathbb{C}$ is simply the canonical 1-form $d z$ itself. By the [[coordinate charts]] of def. \ref{RiemannSphere} we have on $\mathbb{C} - \{0\}$

$$
  d z_- = d (z_+^{-1}) = - z_+^{-2} d z_+
$$

and so the transition function of the canonical bundle in this local trivialization is 

$$
  - z^{-2} \colon (\mathbb{C}-\{0\}) \to \mathbb{C}^\times
  \,.
$$

This has [[winding number]] $\pm 2$. Therefore the [[first Chern class]] of the holomorphic 1-form bundle $\Omega^{1,0}$ is $c_1(\Omega^{1,0}) =  \pm 2$ (the sign being an arbitrary convention, determined by the identification $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$).

And so it follows that there is a unique spin structure, namely given by choosing $\sqrt{\Omega^{1,0}}$ to be the line bundle on $S^2$ with first Chern class $\pm 1$.

=--

+-- {: .num_defn }
###### Definition

By prop. \ref{KaehlerStructure} we can take the symplectic potential to be

$$
  \begin{aligned}
    \theta_\pm 
     & \coloneqq
    \overline{\partial}K
    \\
    & = k \frac{z_\pm \, d \overline{z}_{\pm}}{1 + {\vert z_\pm\vert}^2}
  \end{aligned}
  \,.
$$

=--


### The K&#228;hler polarization

(...)

### The space of quantum states

(...)

### The action of $SU(2)$ by quantum observables

(...)

## References

For general references see at _[[orbit method]]_ and at _[[geometric quantization]]_. 

Reviews with an emphases on the quantization of the 2-sphere include

* J. Maes, _An introduction to the orbit method_ Master thesis (2011) ([pdf slides](http://www.imus.us.es/FSMYT12/Talk_Jeroen_Maes.pdf), [web](http://igitur-archive.library.uu.nl/student-theses/2011-0622-200341/UUindex.html))

