
> beware, some prefactors may still need harmonizing...

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The 2-[[sphere]] $S^2$ is naturally equipped with the structure of a [[symplectic manifold]] with symplectic form its canonical [[volume form]], up to a constant factor. As such, one can consider its [[geometric quantization]]. 

From the point of view of [[physics]], this yields a [[quantum mechanical system]] that describes a rigid [[rotor]] or [[spinor]] in 3-dimenensional [[Euclidean space]] (and just the rotation/spin degrees of freedom, not the translational degrees of freedom). Accordingly, the coresponding [[Hilbert space|Hilbert]]-[[space of quantum states]] carries a natural [[Hamiltonian action]] by the [[angular momentum]] [[quantum operators]] that generate the rotation of the sphere.

More abstractly in [[mathematics]], the 2-sphere is naturally identified with a [[coadjoint orbit]] of the [[special unitary Lie algebra]]/[[special unitary group]] $\mathfrak{su}(2)/SU(2)$ (and hence of the [[spin group]] $Spin(3)$, by one of the [exceptional isomorphisms](spin+group#ExceptionalIsomorphisms)). As such the [[geometric quantization]] of the 2-sphere is a special case of the general [[orbit method]] for producing [[irreducible representations]] of suitable [[Lie groups]] by [[geometric quantization]]. In this case it identifies the quantization of the [[Hamiltonian action]] of $SU(2)$ on $S^2$ in terms of [[quantum operators]] acting on the [[space of quantum states]] with an [[irreducible representation]] of $SU(2) \simeq Spin(3)$.

## Details

The following walks through all the ingredients and steps of the geometric quantization of the 2-spere. Several of the ingredients/steps described are not specific to the 2-sphere but apply generally in [[geometric quantization]], or more specifically in [[Kähler polarization]] quantization, but are spelled out again for completeness. Similarly, much of the discussion is really about the [[complex geometry]] of the [[Riemann sphere]].

### The symplectic geometry

We introduce first the 2-sphere with its canonical structure of a [[symplectic manifold]] and [[Kähler manifold]].

#### Coordinate charts

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

In the following we often just write "$z$" for "$z_+$" or "$z_-$" when the chart $U_+$ or $U_-$ is understood.

By the canonical embedding

$$
  S^2 \hookrightarrow \mathbb{R}^3
$$

into the 3-[[dimension|dimensional]] [[Cartesian space]] as the unit 2-sphere given by

$$
  S^2 = \left\{ (x_1, x_2, x_2) \in \mathbb{R}^3 \;|\; (x_1)^2 + (x_2)^2 + (x_3)^2 = 1 \right\}
$$

the 2-[[sphere]] inherits a [[Riemannian metric]] as the [[pullback of a differential form|pullback]] of the canonical metric $\sum_{i = 1} ^3  d x_i \otimes d x_i$  on $\mathbb{R}^3$. 

+-- {: .num_prop #TheThreeCanonicalFunctions}
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


#### Symplectic and Kähler structure


+-- {: .num_prop}
###### Proposition

The canonical [[Riemannian metric]] on $S^2$ induces the [[volume form]] $\omega_1 \in \Omega^2(S^2)$ given in the [[coordinate charts]] of def. \ref{RiemannSphere} by

$$
  \omega_1
  =  
  \frac{1}{(1 + {\vert z\vert}^2)^2}
  d z \wedge d \overline{z} 
  \,.
$$

More generally, for $S^2 \hookrightarrow \mathbb{R}^3$ embedded as the 2-sphere of [[radius]] $k \in (0,\infty)$, the corresponding volume form is 

$$
  \omega_k
  =  
  \frac{k}{(1 + {\vert z\vert}^2)^2}
  d z \wedge d \overline{z} 
  \,.
$$


=--

+-- {: .num_prop #KaehlerStructure}
###### Proposition

Equipped with this [[Riemannian metric]] for $k \in (0,\infty)$ and with the [[complex manifold]] structure of def. \ref{RiemannSphere} the 2-sphere is a [[Kähler manifold]] with 

* [[Kähler potential]] on $U_\pm$ given by

  $$
    K_k(z_\pm,\overline{z}_\pm) = - k ln(1 + {\vert z_\pm^2\vert})
    \,.
  $$

* [[Kähler form]] on $U_\pm$ given by
 
  $$
   \begin{aligned}\omega_k & = \partial \overline{\partial} K_k \\  & = \frac{k}{(1 + {\vert z\vert}^2)^2}
  d z_{} \wedge d \overline{z} \end{aligned}
  \,.
  $$


=--

+-- {: .num_remark #KaehlerFormIsInvariant}
###### Remark

The above [[Kähler form]] indeed has the same coordinate expression on both patches $U_\pm$: on $U_+ \cap U_- \simeq (S^2 - \{x_0, x_\infty\})$ we have

$$
  \begin{aligned}
    \frac{k}{(1 + {\vert z_+\vert}^2)^2}
  d z_{+} \wedge d \overline{z}_+ 
    & =    
    \frac{k}{(1 + {\vert z_-\vert}^{-2})^2}
  (-z_-^{-2} d z_{-}) \wedge (-\overline{z}_-^{-2} d \overline{z}_-)
    \\
    & = 
    \frac{k}{{\vert z_-\vert^4}(1 + {\vert z_-\vert}^{-2})^2}
   d z_{-} \wedge d \overline{z}_-
    \\
    & = 
    \frac{k}{(1 + {\vert z_-\vert}^{2})^2}
   d z_{-} \wedge d \overline{z}_-    
  \end{aligned}
 \,.
$$

=--

In the following we leave the subscript $(-)_k$ implicit and write just "$\omega$" and "$K$" etc, the dependency on the parameter $k$ being understood. 










### The prequantum geometry

We first discuss the [[complex line bundles]] on the 2-sphere

* _[Without connection](#PrequantumBundleWithoutConnection)_

and then consider genuine [[prequantum line bundles]]

* _[With connection](#PrequantumConnection)_ .

#### Prequantum bundle without connection
 {#PrequantumBundleWithoutConnection}

+-- {: .num_remark}
###### Remark

Hermitian [[complex line bundles]] are classified via their [[first Chern class]] (just as [[circle group]]-[[principal bundles]]) by second [[ordinary cohomology]] with [[integer]] [[coefficients]], which for the 2-sphere is

$$
  H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}
  \,.
$$


By the [[clutching construction]] a line bundle given by two trivializing sections $\sigma_\pm$ on $U_{\pm}$, respectively, of the trivial line bundle on the coordinate patch $\mathbb{C}$ has class the [[winding number]] of the transition function

$$
  S^1 \hookrightarrow \mathbb{C} - \{0\}
  \stackrel{s_2 s_1^{-1}}{\to} \mathbb{C}^\times
  \,.
$$

=--

+-- {: .num_defn #StandardCechCocycle}
###### Definition

For $k \in \mathbb{Z} \simeq H^2(S^2, \mathbb{Z})$ we take the standard [[Cech cohomology|Cech cocycle]] representing this class to be that given on $U_+ \cap U_- \simeq S^2 - \{x_0, x_\infty\}$ by the transition function

$$
  f(z_+) \coloneqq z_+^{-k} = z_-^{k} 
  \,.
$$

=--

+-- {: .num_remark #SpinStructureByThetaCharacteristic}
###### Remark

By the discussion there, a [[spin structure]] on $S^2$ is equivalently a [[square root]] $\sqrt{\Omega^{1,0}} \in \mathbf{Line}_{\mathbb{C}}(S^2)$ of the [[canonical line bundle]] $\Omega^{1,0}$, which here is simply the holomorphic 1-form bundle.

=--

+-- {: .num_prop #CanonicalBundleAndSquareRoot}
###### Proposition

The [[first Chern class]] of the [[canonical line bundle]] on the 2-sphere is

$$
  c_1\left(\Omega^{1,0}\left(S^2\right)\right)
  = 
  2
  \in 
  \mathbb{Z} \simeq H^2(S^2, \mathbb{Z})
$$

(up to a unique choice of sign, which determines the [[isomorphism]] on the right). Accordingly the 2-sphere has an essentially unique [[spin structure]] whose [[theta characteristic]] $\sqrt{\Omega^{1,0}}$ is the complex line bundle with unit [[first Chern class]]

$$
  c_1\left(\sqrt{\Omega^{1,0}\left(S^2\right)}\right)
  = 
  1
  \in 
  \mathbb{Z} \simeq H^2(S^2, \mathbb{Z})
  \,,
$$

the [[basic line bundle on the 2-sphere]].


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
$$

as in def. \ref{StandardCechCocycle}.

This has [[winding number]] $2$. Therefore the [[first Chern class]] of the holomorphic 1-form bundle $\Omega^{1,0}$ is $c_1(\Omega^{1,0}) =  \pm 2$ (the sign being an arbitrary convention, determined by the identification $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$).

And so it follows that there is a unique spin structure, namely given by choosing $\sqrt{\Omega^{1,0}}$ to be the line bundle on $S^2$ with first Chern class $\pm 1$.

=--

#### Prequantum bundle with connection
 {#PrequantumConnection}


We discuss equipping the above complex line bundles on $S^2$ with [[connection on a bundle|connections]]. 

+-- {: .num_defn #DeligneCocycle}
###### Definition

For $k \in  H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z} \hookrightarrow \mathbb{R}$, 
refine the [[Cech cohomology|Cech cocycle]] of def. \ref{StandardCechCocycle} to a Cech-[[Deligne cohomology|Deligne cocycle]] with [[curvature]] [[differential 2-form]] the [[Kähler form]] of prop. \ref{KaehlerStructure}

$$
  \omega = \partial \overline{\partial} K
$$


by taking the connection 1-form on $U_{\pm}$ to be 

$$  
  \begin{aligned}
    \theta
      & \coloneqq
    \exp\left(-K\right) 
     {\partial}
    \exp\left(K\right)
    \\
    & =
    {\partial} K
    \\
    & = k \frac{\overline{z} }{ 1 + {\vert z\vert}^2} d {z}
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #DeligneCocycleIsConsistent}
###### Proposition

The Cech-Deligne cocycle in def. \ref{DeligneCocycle} is indeed well defined.

=--

+-- {: .proof}
###### Proof

We need to check that the connection 1-form satisfies on $U_+ \cap U_- \simeq (S^2 - \{x_0, x_\infty\})$ the transition law

$$
  \theta_+ \;+\; z^{-k} d z^k \;=\; \theta_-
  \,.
$$

To see this first notice that on $U_+ \cap U_- \simeq (\mathbb{C} - \{0\})$ 

$$
  \begin{aligned}
   \theta_+ & = k\frac{\overline{z}_-^{-1}}{1 + {\vert z_-\vert^{-2}}} (-){z}_-^{-2} d {z}_-
   \\
   & = 
   -k \frac{{z}_-^{-1} d{z}_-}{1 + {\vert z_-\vert^2}}
   \\
   & = 
   -\frac{{z}_-^{-k} d {z}_-^k}{1  + {\vert z_-\vert}^2}
  \end{aligned}
  \,.
$$

With this it follows that on $U_+ \cap U_-$ indeed we have

$$
  \begin{aligned}
    z_-^{-k} d z_-^k + \theta_+ 
    & = 
    k
    \left(
      z_-^{-1} -\frac{z_-^{-1}}{1 + {\vert z_-\vert}^2}
    \right) d z_-
    \\
    & = 
    k \frac{\overline{z}_-}{1 + {\vert z_-\vert}^2}
    d z_-
    \\
    & = \theta_-
  \end{aligned}
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

Compare this invariance of the form of the connection to the invariance of the form of its [[curvature]] in remark \ref{KaehlerFormIsInvariant} above.

=--

+-- {: .num_remark}
###### Remark

For $\epsilon \in (0,1)$ let $D_{(\epsilon, \infty)}$ be the [[disk]] of [[radius]] $\epsilon$ around $x_\infty \in S^2$. Then by the [[Stokes theorem]] with def. \ref{DeligneCocycle} we have
the [[integral]] equality

$$
  \underset{S^2 - D_{(\epsilon,\infty)}}{\int} \omega
  \;=\; 
  \underset{\partial D_{(\epsilon, \infty)}}{\int} \theta
  \;=\; 
  \frac{k}{1 + \epsilon^2} 
  \,.
$$

In the [[limit of a sequence|limit]] that $\epsilon \to 0$ this shows that for integral $k$ as above, $\omega$ has integral [[periods]]

$$
  \begin{aligned}
  \int_{S^2} \omega
  = 
  \underset{\epsilon \to 0}{\lim}
  \underset{S^2 - D_{(\epsilon,\infty)}}{\int} \omega
  = 
  \underset{\epsilon \to 0}{\lim}
  \frac{k}{1 + \epsilon^2} 
  = 
  k
  \in \mathbb{Z}
  \end{aligned}
  \,.
$$

This is essentially the relation that historically was first recognized by [[Paul Dirac]] in the context of what today is known as the _[[Dirac charge quantization]]_ argument. In more modern language this expresses the defining [[homotopy pullback]] property of [[ordinary differential cohomology]].

=--







### The space of quantum states
 {#TheSpaceOfQuantumStates}


#### Kähler polarization

The [[Kähler manifold]] structure on $S^2$ of prop. \ref{KaehlerStructure} which lifts its [[symplectic structure]] given by the [[volume form]] canonically induces a [[polarization]] of the symplectic structure: the corresponding [[Kähler polarization]].

+-- {: .num_defn}
###### Definition

Given a [[prequantum line bundle]] $(L,\nabla)$ for $(S^2, \omega)$, a [[section]] $\Psi \in \Gamma(L)$ is polarized if for all $v \in \Gamma(T^{0,1}S^2)$ the [[covariant derivative]] of $\psi$ along $v$ vanishes

$$
  \nabla_v \Psi = 0
  \,.
$$

=--

By prop. \ref{DeligneCocycle} the connection $\nabla$ is what is called "well adapted" in that in the complex coordinate patch $U_\pm \simeq \mathbb{C}$ the covariant derivative along anti-holomorphic vector fields is given simply by the ordinary anti-holomorphic derivative:

$$
  \nabla_{\partial/\partial \overline{z}} \Psi = 
  \frac{\partial}{\partial \overline{z}} \Psi
  \,.
$$

This means that:

+-- {: .num_prop #KaehlerPolarizedIsHolomorphic}
###### Proposition

The Kähler-polarized sections are precisely the holomorphic sections. 

=--



#### Wavefunctions

+-- {: .num_defn}
###### Definition

Given a [[prequantum line bundle]] $(L,\omega)$ prequantizing $(S^2, \omega)$, the _[[space of quantum states]]_ is the [[vector space]] of [[polarization|polarized]] [[sections]] of $L \otimes \sqrt{\Omega^{1,0}}$, the _[[wave functions]]_:

$$
  \mathcal{H} \coloneqq \left\{ \Psi \in \Gamma\left(L\otimes \sqrt{\Omega^{1,0}}\right) | \overline{\partial} \Psi = 0 \right\}
$$

=--

+-- {: .num_remark #AppearanceOfTheMetaplecticCorrection}
###### Remark

Here the [[tensor product]] with $\sqrt{\Omega^{1,0}}$ is the [[metaplectic correction]], remark \ref{SpinStructureByThetaCharacteristic}, which by prop. \ref{CanonicalBundleAndSquareRoot} is the essentially unique line bundle of unit [[first Chern class]].

Since by prop. \ref{CanonicalBundleAndSquareRoot} this simply shifts the class of the prequantum bundle by one, and since in much of the traditional literature it is customary to ignore the metaplectic correction (which in the present case is indeed harmless), we will in the following regard $L \otimes \sqrt{\Omega^{1,0}}$ as the prequantum line bundle, by which we mean that we keep referring by "$k$" to the [[first Chern class]] of that line bundle on $S^2$ of which we consider sections etc. Strictly speaking the prequantum line bundle hence has class $k-1$ from now on, but this shift collides with all established literature and is not worth bothering with.

It is however maybe worth noticing that the shift of the class by +1 induced by the metaplectic correction can be regarded as lifting the possibly non-regular [[coadjoint orbits]] with $k \geq 0$ to the regular ones, with $k \geq 1$.

=--

+-- {: .num_prop #DimensionOfSpaceOfQuantumStates}
###### Proposition

The [[dimension]] of the [[space of quantum states]] on the 2-sphere is

$$
  dim(\mathcal{H})
  = 
  \left\{
   \array{
      k+1 & if \, k \geq 0;
      \\
      0 & otherwise
   }
  \right.
  \,,
$$

where $k \coloneqq c_1(L \otimes \sqrt{\Omega^{1,0}})$ is the [[first Chern class]] of the [[prequantum line bundle]] with [[metaplectic correction]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{KaehlerPolarizedIsHolomorphic} the polarized sections are precisely the holomorphic sections. By the construction in def. \ref{StandardCechCocycle} a holomorphic section of $L \otimes \sqrt{\Omega^{1,0}}$ is equivalently a pair of holomorphic functions $\Psi_\pm$ on $\mathbb{C}$ such that on $\mathbb{C} - \{0\}$ they are related by

$$
  \Psi_-(z_-) = \Psi_+(z_-^{-1}) z_-^{k}
  \,. 
$$

A linear [[basis]] for the space of unconstrained holomorphbic functions on $\mathbb{Z}$ is of course given by the monomials $\{z^n\}$. Therefore a [[basis]] for the admissible pairs as above is given by pairs $\Psi_\pm(z_-) = z_-^{n_\pm}$ such that

$$
  z_-^{n_-} = z_-^{-n_+} z_-^{k}
$$

hence such that

$$
  n_+ + n_- = k
  \,.
$$

If $k \geq 0$ then this equation has $(k+1)$ solutions. If $k \lt 0$ it has no solution.

=--


+-- {: .num_example}
###### Example

For $k = 2$ (by prop. \ref{CanonicalBundleAndSquareRoot} the class of the [[canonical line bundle]]) the [[space of quantum states]] is 3-dimensional and canonically identified with the [[vector space]] underlying the [[special unitary Lie algebra]] $\mathfrak{su}(2)$. 

=--

+-- {: .num_example}
###### Example

For $k = 1$ (by prop. \ref{CanonicalBundleAndSquareRoot} the class of the unique [[theta characteristic]]) it is 2-dimensional, being the space of states of a bare [[spinor]] in 3-dimensional Euclidean space. This is the standard model for a [[qbit]]. Below in example \ref{PauliMatrices} we see how the canonical [[quantum observables]] act on this space of states as the [[Pauli matrices]].

=--


### The quantum observables

#### The Hamiltonian $SU(2)$-action

We discuss the [[Hamiltonian action]] of the [[special unitary group]]/[[spin group]] $SU(2) \simeq Spin(3)$ on $(S^2, \omega)$.

First we state the abstract situation in terms of the [[orbit method]], then we unwind what this implies in detail.

+-- {: .num_prop}
###### Proposition

The [[Lie algebra]] $\mathfrak{su}(2)$ as a [[matrix Lie algebra]] is the sub Lie algebra on those matrices of the form

$$
  \left(
    \array{
      i z & x + i y
      \\
      - x + i y & - i z
    }
  \right)
  \;\;\;  
  with
  \;\;
  x,y,z \in \mathbb{R}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

The standard [[basis]] elements of $\mathfrak{su}(2)$ given by the above presentation are 

$$
  \sigma_1 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & 1
     \\
     -1 & 0
   }
  \right)
$$

$$
  \sigma_2 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & i
     \\
     i & 0
   }
  \right)
$$

$$
  \sigma_3
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     i & 0
     \\
     0 & -i
   }
  \right)
  \,.
$$

These are called the _[[Pauli matrices]]_.

=--

+-- {: .num_prop}
###### Proposition

The [[Pauli matrices]] satisfy the [[commutator]] relations

$$
  [\sigma_1, \sigma_2] = \sigma_3
$$

$$
  [\sigma_2, \sigma_3] = \sigma_1
$$

$$
  [\sigma_3, \sigma_1] = \sigma_2
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

The [[maximal torus]] of $SU(2)$ is the [[circle group]] $U(1)$. In the above [[matrix group]] presentation this is naturally identified with the subgroup of matrices of the form

$$
  \left(
    \array{
      t & 0 
      \\
      0 & t^{-1}
    }
  \right)
  \;\;
  with
  t \in U(1) \hookrightarrow \mathbb{C}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The [[coadjoint orbits]] of the [[coadjoint action]] of $SU(2)$ on $\mathfrak{su}(2)$ are equivalent to the subset of the above matrices with $x^2 + y^2 + z^2 = k^2$ for some $k \geq 0$. 

These are _regular_ coadjoint orbits for $k \gt 0$.


=--

By the discussion at _[orbit method -- The coadjoint orbit and the flag manifold](orbit%20method#TheCoadjointOrbitAndTheCosetSpaceAndFlagManifold)_ it follows that

+-- {: .num_prop}
###### Proposition

For $k \gt 0$ the corresponding coadjoint orbit and hence the symplectic 2-sphere is equivalent to the [[quotient]]/[[coset space]]

$$
  SU(2)/U(1) \stackrel{\simeq}{\to} \mathcal{O}_\lambda \simeq S^2
  \,,
$$

where the equivalence is induced by the map

$$
  g U(1) \mapsto Ad_g^\ast\langle \lambda, - \rangle
  \,.
$$

=--

#### The quantum operators

Recall the canonical [[coordinate]] functions $x_1, x_2, x_2 \colon S^2 \to \mathbb{R}$ from prop. \ref{TheThreeCanonicalFunctions}. 

+-- {: .num_prop }
###### Proposition

For $(L,\nabla)$ a [[prequantization]] of $(S,\omega)$ equipped with the above [[Kähler polarization]], the
[[prequantum operators]] associated to the canonical [[coordinate]] functions 

$$
  x_1, x_2, x_2 \colon S^2 \to \mathbb{R}
$$ 

from prop. \ref{TheThreeCanonicalFunctions} are [[quantum operators]] (respect the [[polarization]]) and in the canonical trivializaton of $L$ on $U_-$ their action on sections is that of the following [[vector fields]]:

$$
  Q(x_1 + i x_2) = z_-^2 \frac{\partial}{\partial z_-} - k z_-
$$

$$
  Q(x_1 - i x_2) = - \frac{\partial}{\partial z_-}
$$

$$
  Q(x_3) = z_- \frac{\partial}{\partial z_-} - k/2
  \,.
$$

=--


+-- {: .num_example #PauliMatrices}
###### Example

For $k = 1$ these act as the [[Pauli matrices]] on the [[space of quantum states]] $\mathcal{H} \simeq \mathbb{C}^2$. 

By the proof of prop. \ref{DimensionOfSpaceOfQuantumStates} the [[space of quantum states]] is spanned by those [[wavefunctions]] which on $U_-$ are of the form

$$
  \vert -\rangle \coloneqq z_-^0
$$

$$
  \vert +\rangle \coloneqq z_-^1
  \,.
$$

These are [[eigenvectors]] for $Q(x_3)$:

$$
  Q(x_3) \vert - \rangle = -\frac{1}{2} \vert - \rangle
$$

$$
  Q(x_3) \vert + \rangle = \frac{1}{2} \vert + \rangle
  \,.
$$

It is clear that $Q(x_1 - i x_2)$ acts as a lowering operator on these states. Notice that also $Q(x_1 + i x_2)$ indeed acts as a raising operator in that for the special value of $k = 1$ we have indeed

$$
  \begin{aligned}
    Q(x_1 + i x_2) \vert + \rangle 
    & = 
    z_-^2 \frac{\partial z_-}{\partial z_-} + z_- z_-
    \\
    & = 0
  \end{aligned}
  \,.
$$


=--
## Related concepts

* [[quantization of the 2-sphere]]

  * **geometric quantization of the 2-sphere**

  * [[deformation quantization of the 2-sphere]]


## References

For general references see at _[[orbit method]]_ and at _[[geometric quantization]]_. 

Reviews with an emphasis on the quantization of the 2-sphere include

section 3.1 of 

* [[Alexander Kirillov]], _[[Lectures on the Orbit Method]]_

section 7 of

* J. Maes, _An introduction to the orbit method_, Master thesis (2011) ([pdf](http://web.science.uu.nl/itf/Teaching/2011/JeroenMaes.pdf), [pdf slides](http://www.imus.us.es/FSMYT12/Talk_Jeroen_Maes.pdf), [web](https://dspace.library.uu.nl/handle/1874/205802))

Discussion in terms of [[Dirac induction]] is in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], part II, example 1.37 of _[[Loop Groups and Twisted K-Theory]]_
 {#FHT}


