

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The  _De Donder-Weyl-Hamilton equation_ is a refinement of [[Hamilton's equation]] from a single [[variational derivative|variational]] direction to many. 

Where [[Hamilton's equation]] appears as a natural condition in [[symplectic geometry]], so the De Donder-Weyl-Hamilton equation appears as the analogous condition in [[multisymplectic geometry]]/[[n-plectic geometry]].

Where [[Hamilton's equation]] appears as the [[equations of motion]] of a [[mechanical system]] whose [[dynamics]] is described by evolution along a single parameter ([[time]]), so the _De Donder-Weyl Hamilton equation_ appears as the [[equations of motion]] of a higher dimensional [[field theory]] given by a [[local Lagrangian]] where "evolution" is along more parameters ([[spacetime]]).

## Definition

Let $\Sigma$ be a [[smooth manifold]] to be regarded as [[worldvolume]]/[[spacetime]] and let $F \to \Sigma$ be a smooth [[bundle]] to be thought of as the [[field bundle]].

For simplicity of exposition we first consider local patches and take without essential restriction $\Sigma$ to be a [[Cartesian space]] and the [[field bundle]] to be a trivial [[vector bundle]] $X \times \Sigma$. In all of the following the [[summation convention]] for summation over repeated induces is understood.

We then denote the canonical [[coordinates]] on $\Sigma$ by $\{\sigma^\mu\}$ and those on $X$ by $\{\phi^i\}$.

Write $(J^1 E^)^\ast$ for the dualized first [[jet bundle]] of $E$. Under the above assumptions this has canonical local coordinates $\{\sigma^\mu, \phi^i, \pi_i^\mu\}$. Here we call $\pi^\mu_i$ the "$\mu$-th [[momentum]] of the $i$-th field".


Consider a [[local Lagrangian]] $L$ which is _of first order_, hence which is a function on the first [[jet bundle]] $J^1 E$ of the [[field bundle]].

+-- {: .num_defn #ELEquations}
###### Definition

Its [[Euler-Lagrange equations]] are

$$
  \partial_\mu
  \frac{\delta L }{\delta (\partial_\mu \phi^i)} 
   = 
  \frac{\delta L}{ \delta \phi^i}
  \,.
$$

=--

+-- {: .num_defn #dWHamiltonianByLegendre}
###### Definition

The _De Donder-Weyl-Hamiltonian_ of $L$ is its generalized [[Legendre transform]] (if it exists), the function

$$
  H \coloneqq \pi^\mu_i \partial_\mu \phi^i - L
$$

on the dual jet bundle.

=--

+-- {: .num_prop #DWHEquations}
###### Proposition/Definition

In terms of the De Donder-Weyl Hamiltonian $H$, def. \ref{dWHamiltonianByLegendre},  the [[Euler-Lagrange equations of motion]], def. \ref{ELEquations}, are equivalent to the [[differential equations]]

$$
  \partial_\mu \phi^i
    =
   \frac{\partial H}{\partial \pi_i^\mu} 
  \;\;\,,
  \;\;\;\;
  \partial_\mu \pi^\mu_i
   =
  -
  \frac{\partial H}{ \partial \phi^i} 
  \,.
$$

These are called the **De Donder-Weyl-Hamilton equations**.

=--


## Properties

### As a multisymplectic/$n$-plectic Hamiltonian equation 
 {#AsnplecticHamiltonEquation}

For $(X,\omega)$ a [[symplectic manifold]] and $H \in C^\infty(X)$ a [[smooth function]] regarded as a [[Hamiltonian]], then [[Hamilton's equations]] are equivalent to

$$
  \iota_v \omega = \mathbf{d}H
$$

for $v$ a [[tangent vector]] to a [[trajectory]] in [[phase space]]. This may be referred to as the "non-relativistic" form of the symplectic version of Hamilton's equations, as the "[[time]]"-parameter is not part of the [[phase space]].

By passing from plain phase space to the corresponding [[multisymplectic geometry|dual jet bundle]], hence by adjoining a [[worldline]] coordinate $t$, this is equivalent to

$$
  \iota_v \Omega = 0
$$

where now

$$
  \Omega = \omega + \mathbf{d}H \wedge \mathbf{d}t
  \,.
$$

This may accordingly be thought of as the [[relativity|relativistic]] version of Hamilton's equations.

We now discuss the analog of both the "non-relativistic" and of this "[[relativity|relativistic]] version" of [[Hamilton's equation]] for the de Donder-Weyl-Hamilton equation. 

In both cases, the $n$-tuple of [[tangent vectors]] to a [[section]] which satisfies the [[equations of motion]] is characterized as a _[[Hamiltonian n-vector field]]_. See there for more discussion.

#### Relativistic form

+-- {: .num_defn #PrePlecticForm}
###### Definition

Given a De Donder-Weyl-Hamiltonian $H$, def. \ref{dWHamiltonianByLegendre}, define a [[differential form]] 

$$
  \Omega \in \Omega^{n+1}_{cl}((J^1 E)^\ast)
$$

on the dual jet bundle (the _[[multisymplectic form]]_ or _[[n-plectic form|pre-(n+1)-plectic form]]_) by

$$
  \Omega 
   \;\coloneqq \;
    \mathbf{d} \phi^i \wedge \mathbf{d} \pi^\mu_i  
   \wedge (\iota_{\partial_\mu} vol_\Sigma) 
    + 
    \mathbf{d} H \wedge vol_\Sigma
  \,.
$$

=--

+-- {: .num_prop  #DWHInRelativisticPlecticForm}
###### Proposition

A [[section]] $(\phi^i, \pi^\mu_i) \colon \Sigma \to J^1 E^\ast$ of the dualized first [[jet bundle]]  satisfies the [[equations of motion]], prop. \ref{DWHEquations}, precisely if its [[tangent vectors]] 

$$
  v_\mu 
    \coloneqq \partial_{\mu} 
  + 
    \frac{\partial \phi^i}{\partial \sigma^\mu} \partial_{\phi^i}
  + 
  \frac{\partial \pi_i^\nu}{\partial \sigma^\mu} \partial_{p^\nu_i}
$$

jointly annihilate the pre-$(n+1)$-plectic form of def. \ref{PrePlecticForm} in that the [[equation]]:

$$
  (\iota_{v_1} \cdots \iota_{v_n}) \Omega
  = 0
$$

holds.

=--

+-- {: .proof}
###### Proof 

First, the component of this equation which does not contain any $\mathbf{d}\sigma^\mu$ is 

$$
  \iota_{v_i}
  \;
  \mathbf{d}\phi^i \wedge \mathbf{d}\pi^i_\mu
  = 
  \mathbf{d}H
  \,.
$$

This is already equivalent to the DWH equation, prop. \ref{DWHEquations}.

Second, this already implies that the components of the equation that are proportional to $\mathbf{d}\sigma^\mu$ are automatically satisfied; because these components are

$$
  \frac{\partial \phi^i}{\partial \sigma^\mu}
  \frac{\partial \pi_i^\mu}{\partial \sigma^\nu}
  \mathbf{d}\sigma^\nu
  -
  \frac{\partial \phi^i}{\partial \sigma^\nu}
  \frac{\partial \pi_i^\mu}{\partial \sigma^\mu}
  \mathbf{d}\sigma^\nu
  =
  \frac{\partial H}{\partial \phi^i}\frac{\partial \phi^i}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
  + 
  \frac{\partial H}{\partial \pi_i^\mu}\frac{\partial \pi_i^\mu}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
$$

and inserting the DWH equations on the left makes the left side identically equal to the right hand side.

=--

+-- {: .num_remark}
###### Remark

Proposition \ref{DWHInRelativisticPlecticForm} is indeed true in the general case where $H$ may be [[spacetime]] dependent (depend nontrivially on the $\sigma^\mu$).

=--


#### Non-relativistic form

To obtain the "non-relativistic" form of the $(n+1)$-plectic
form of the DWH equation, consider the _affine_ dual first jet bundle with canonical coordinates $\{\sigma^a , \phi^i, \pi^a_i, e \}$.

+-- {: .num_remark}
###### Remark

The canonical [[n-plectic form|pre-(n+1)-plectic form]] on
the affine dual first jet bundle is

$$
  \omega 
   \coloneqq 
  \mathbf{d}\phi^i \wedge \mathbf{d}\phi^\mu_a
  \iota_{\partial_{\sigma^\mu}} vol_\Sigma
  + 
  \mathbf{d}e \wedge vol_\Sigma 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


Vector fields tangent to a [[section]] of the affine dual first jet bundle are of the form

$$
  v_\mu 
  \coloneqq 
    \partial_{\mu} 
  + 
    \frac{\partial \phi^i}{\partial \sigma^\mu} \partial_{\phi^i}
  + 
    \frac{\partial \pi_i^\nu}{\partial \sigma^\mu} \partial_{p^\nu_i}
  +
    \frac{\partial e}{\partial \sigma^\mu} \partial_e
  \,.
$$

=--

+-- {: .num_prop #DWHInNonRelativisticPlecticForm}
###### Proposition

On the affine dual first jet bundle the de Donder-Weyl-Hamilton equation characterizes those [[sections]] whose [[tangent vectors]] as above satisfy

$$
  (\iota_{v_1} \cdots \iota_{v_n})
  \omega
  = 
  \mathbf{d}(H + e)
$$

=--

This has been pointed out in ([H&#233;lein 02, around equation (4)](#Helein02)).

+-- {: .proof}
###### Proof 

This is a slight variant of the proof of prop. \ref{DWHInRelativisticPlecticForm}.
First, the component of the equation independend of $\mathbf{d}\sigma^\nu$ is 

$$
  \iota_{v_i}
  \;
  \mathbf{d}\pi^i_\mu \wedge \mathbf{d}\phi^i 
  +
  \mathbf{d}e
  = 
  \mathbf{d}H
  +
  \mathbf{d}e
  \,.
$$

Here the term $\mathbf{d}e$ cancels on both sides and leaves the equation equivalent to the DWH equation as in the first step of the proof of prop. \ref{DWHInRelativisticPlecticForm}.

Second, the component of the claimed equation proportional to $\mathbf{d}\sigma^\mu$ is now

$$
  \frac{\partial \phi^i}{\partial \sigma^\mu}
  \frac{\partial \pi_i^\mu}{\partial \sigma^\nu}
  \mathbf{d}\sigma^\nu
  -
  \frac{\partial \phi^i}{\partial \sigma^\nu}
  \frac{\partial \pi_i^\mu}{\partial \sigma^\mu}
  \mathbf{d}\sigma^\nu
  + 
  \frac{\partial e}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
  = 0
  \,.
$$

Inserting into this the DWH equation makes it equivalent to

$$
  \frac{\partial H}{\partial \phi^i}\frac{\partial \phi^i}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
  + 
  \frac{\partial H}{\partial \pi_i^\mu}\frac{\partial \pi_i^\mu}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
  +   
  \frac{\partial e}{\partial \sigma^\nu} \mathbf{d}\sigma^\nu
  = 0
$$

This has a unique solution, up to a global constant, given by

$$
  e(\{ \sigma^\nu \}) 
   = 
  - H(
    \{
      \phi^i(\{ \sigma^\nu \}), 
      \pi^\mu_i (\{ \sigma^\nu \})
    \}
    )
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

By the proof of prop. \ref{DWHInNonRelativisticPlecticForm} we have _on shell_ that $H + e = 0$ and that $\omega = \Omega$.

=--


## Related concepts

* [[Hamiltonian n-vector field]]


## References

Maybe the first example of what is now called De Donder-Weyl theory appeared in 

* [[Constantin Carathéodory]], _&#220;ber die Extremalen und geod&#228;tischen Felder in der Variationsrechnung der mehrfachen Integrale_, Acta Sci. Math. (Szeged) 4 (1929) 193-216

Then Weyl and de Donder independently published 

* [[Hermann Weyl]], _Geodesic fields in the calculus of variations_, Ann. Math. (2) 36 (1935) 607-629.

* [[Théophile De Donder]], _Th&#233;orie invariante du calcul des variations_, Nuov. &#233;d, Gauthiers&#8211;Villars, Paris 1935

Reviews:

* Wikipedia, _[De Donder-Weyl theory](http://en.wikipedia.org/wiki/De_Donder%E2%80%93Weyl_theory)_

* [[Narciso Román-Roy]], _Multisymplectic Lagrangian and Hamiltonian Formalisms of Classical Field Theories_, SIGMA 5 (2009), 100 ([journal](http://www.emis.de/journals/SIGMA/2009/100/), [arXiv:math-ph/0506022](http://arxiv.org/abs/math-ph/0506022)) 

* [[Frédéric Hélein]], _Hamiltonian formalisms for
multidimensional calculus of variations and perturbation theory_, ([arXiv:math-ph/0212036](http://arxiv.org/abs/math-ph/0212036))
 {#Helein02}

See also

* I.V. Kanatchikov, _De Donder-Weyl theory and a hypercomplex extension of quantum mechanics to field theory_ , ([arXiv:hep-th/9810165](http://arxiv.org/abs/hep-th/9810165))


For more see the references at _[[multisymplectic geometry]]_, at _[[n-plectic geometry]]_ and at _[[Hamiltonian n-vector field]]_.

[[!redirects de Donder-Weyl-Hamilton equation]]


[[!redirects De Donder-Weyl hamiltonian]]
[[!redirects de Donder-Weyl Hamiltonian]]

[[!redirects Hamilton-De Donder-Weyl equation]]
[[!redirects Hamilton-de Donder-Weyl equations]]
[[!redirects Hamiltoni-De Donder-Weyl equations]]

[[!redirects De Donder-Weyl equation]]
[[!redirects de Donder-Weyl equations]]

[[!redirects De Donder-Weyl formalism]]

[[!redirects Hamilton-De Donder-Weyl equations of motion]]
[[!redirects Hamilton-De Donder-Weyl equations of motion]]

[[!redirects de Donder-Weyl theory]]

[[!redirects De Donder-Weyl field theory]]
