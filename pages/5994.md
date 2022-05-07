
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The [[path integral]] over the [[fermion]]ic variables of the standard kinetic [[action functional]] for [[fermion]]s (see for instance [[spinors in Yang-Mills theory]]) has a well-defined meaning as a [[section]] of the [[Pfaffian line bundle]] of the corresponding [[Dirac operator]].

## Setup

For definiteness, we consider a [[sigma model]] [[quantum field theory]] on a worldvolume $\Sigma$ and [[pseudo-Riemannian manifold|pseudo-Riemannian]] target [[spacetime]] $X$ with fields

* [[boson]]s: [[smooth function]]s $\phi : \Sigma \to X$

* [[fermion]]s ([[gravitino]]): $\psi \in \Gamma(S(\Sigma) \otimes \phi^* T M)$, [[section]]s of the [[tensor product]] of a [[spinor bundle]] on $\Sigma$ and the [[pullback]] of the [[cotangent bundle]] of $X$ along the given bosonic field $\phi$.

The [[action functional]]

$$
  S : (\phi, \psi) \mapsto S^{bos}(\phi) + S^{ferm}_{\phi}(\psi)
$$

is the sum of the 

* bosonic action 

  $$
    S^{bos})(\phi) 
     = 
    \int_\Sigma \langle d \phi \wedge \star d \phi\rangle
  $$

* fermionic action 

  $$
    S^{ferm}_\phi(\psi)
     = \int_\Sigma \langle \psi, D_\phi \psi\rangle 
  $$

  where $D_\phi$ is a [[Dirac operator]] on $S \otimes \phi^* T M$ (the Dirac operator on $S$ twisted by the pullback of the [[Levi-Civita connection]] on $T^* X$ ).

One imagines than that the hypothetical [[path integral]] symboilically written as

$$
  \int [d \phi] [d \psi] \exp(S(\psi)(\phi,\psi))
$$

can be computed in two steps 

$$
  \cdots = \int [d \phi] \exp(S^{bos}(\phi)) 
   \left(
     \int [d \psi]
     \exp(S^{ferm}_\phi(\psi))
   \right)
$$

by first computing the integral over the fermions

$$
  pfaff(\phi)
   := 
  \int [d \psi]
     \exp(S^{ferm}_\phi(\psi))
$$

and then inserting this into the remaining bosonic integral. Now, as opposed to the bosonic integral, this fermionic integral can be given well-defined sense by interpreting it as an infinite-dimensional [[Berezinian integral]].

However, while this makes the expression well defined, the result is not quite a function of $\phi$, but is instead a [[section]] $pfaff$ of a [[Pfaffian line bundle]]

$$
  \array{
    && Pfaff 
     \\
     {}^{pfaff := Z_{eff}^{ferm}}\nearrow & \downarrow 
    \\
   C^{\infty}(\Sigma, X)
 &= &  C^{\infty}(\Sigma, X)
  }
$$

over the space of bosonic field configurations. 

If $Pfaff$ is not isomorphic to the trivial line bundle, we say the system has a fermionic [[quantum anomaly]]. If instead $Pfaff$ is trivializable, any choice of trivialization

$$
  t : Paff \stackrel{\simeq}{\to} C^\infty(\Sigma, X) \times \mathbb{C}
$$

makes the fermionic path integral into a genuine function

$$
  Z_{eff}^{ferm}
   : = 
 (t \circ pfaff) :
  C^\infty(\Sigma, X) \to \mathbb{C}
  \,.
$$

Any such choice of $t$ is called a choice of [[quantum integrand]].

With this one can then try to enter the remaining bosonic path integral

$$
  \int [d \phi] \exp(S^{bos}(\phi)) Z_{eff}^{ferm}(\phi)
$$


## Pfaffian bundles

> We are implicitly assuming that $dim \Sigma = 2$ or maybe $8 n + 2$ in the following. Needs to be generalized.

For $n \in \mathbb{N}$, there the [[square root]] of the determinant of a skew symmetric $(n\times n)$-[[matrix]] $D$ -- the [[Pfaffian]] of the matrix -- can be understood as the [[Berezinian integral]]

$$
  pfaff(D) 
    =  
   \int [d \vec \theta]
   \exp( \langle \theta , D \theta\rangle)
  \in
  det \mathbb{R}^n
$$

over the [[Grassmann algebra]] elements $\theta_i$. Written this way this is an element of the [[determinant line]] of $\mathbb{R}^n$: its identification with a number depends on the choice of basis for $\mathbb{R}^n$. For this case this is unproblematic, since there is a canonical choice of basis for the single vector space $\mathbb{R}^n$, but when $D$ instead depends on a parameter $\phi$, then in general its Pfaffian can at best be a section of a [[determinant line bundle]].

We now generalize this to the case that $D$ is not a finite-dimensional matrix, but a [[Dirac operator]] acting on spaces of sections of a [[spinor bundle]]. We discuss that we can reduce this "infinite-dimensional matrix" in a sense _locally_ to a finite dimensional one in a consistent way, such that the above ordinary construction of Pfaffians applies.

In the above setup, write 

$$
  \mathcal{H}_\phi^{\pm} := \Gamma(S^{\pm} \otimes \phi^* T^* X)
$$

for the space of spinor sections for given $\phi : \Sigma \to X$. Then the choral [[Dirac operator]]s a maps

$$
  D_\phi^{\pm} : \mathcal{H}_\phi^{\pm} \to \mathcal{H}^{\mp}_\phi
  \,.
$$

We also have a "quaternionic structure"

$$
  J_\phi^{\pm} : \mathcal{H}_\phi^{\pm} \to \mathcal{H}^{\mp}_\phi
$$

Define then an [[open cover]] of the space $C^\infty(\Sigma,X)$
of the space of bosonic fields with [[open set]]s  $U_\mu$ for $(0 \leq \mu)$ given by

$$
  U_\mu := \{ \phi \in C^\infty(\Sigma,X)  | \mu \nin Spec D_\phi^2\}
  \,,
$$

hence the collection of bosonic field configurations such that $\mu$ is not in the [[operator spectrum]] of the squared [[Dirac operator]].

Over these open subsets we have the _finite_ [[rank]] [[vector bundle]]s

$$
  \mathcal{H}_\phi^{\mu \pm} 
  :=
   \oplus_{0 \leq \epsilon \leq \mu}
  Eig(D_\phi^2, \epsilon)
$$ 

of [[eigenspace]]s of $D_\phi^2$ for [[eigenvalue]]s bounded by $\mu$.

The Dirac operator that we are interested in is

$$
  D_\phi^\mu
  :=
  J_\phi^- \circ D_\phi^+ : \mathcal{H}_\phi^{\mu,+} \to \mathcal{H}_\phi^{\mu,+}
 \,.
$$


This defines now a finite-dimensional [[matrix]]

$$
  \langle -, D_\phi^\mu -\rangle
$$

whose [[Berezinian integral]] is the [[Pfaffian]]

$$
  \int [d \psi] \exp(\langle \psi , D^\mu_\phi \phi \rangle )
  =
  pfaff(D^\mu_\phi) \in det \mathcal{H}^{\mu \pi}_\phi
  \,.
$$

One shows that these constructions for each $\mu$ glue together to define

* a smooth [[line bundle]] $Pfaff \to C^\infty(\Sigma, X)$

* with a smooth [[section]] $pfaff(D)$.

Moreover, there is canonically a [[hermitean metric]] and a  canonical unitary [[connection on a bundle]] (the [[Freed-Bismut connection]]) on this bundle.




## Examples

For the [[sigma model]] describing the [[brane|heterotic superstring]] propagating on a [[pseudo-Riemannian manifold]] $X$, the trivialization of the Pfaffian line bundle, hence the cancellation of its fermionic [[quantum anomaly]] is related to the existence of a (twisted) [[differential string structure]] on $X$. See there for more details.

## Related entries

* [[path integral]]

* [[spinors in Yang-Mills theory]]

[[!redirects fermionic path integrals]]
