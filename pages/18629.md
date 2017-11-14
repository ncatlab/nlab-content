
#Contents#
* table of contents
{:toc}

## Definition

Throughout, let 

1. $\Sigma$ be a [[smooth manifold]] of [[dimension]] $p+1$, thought of as [[spacetime]];

1. $E \overset{fb}{\longrightarrow} \Sigma$ a [[fiber bundle]] thought of as a _[[field bundle]]_

1. $\mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)$ a [[Lagrangian density]].


+-- {: .num_defn #Variation}
###### Definition
**(variation)**

A _variation_ is a vertical [[vector field]] $v$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ which
vanishes when evaluated in the [[horizontal differential forms]];

hence for the [[field bundle]] a [[trivial vector bundle]] over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle},
a variation is of the form

$$
  v = v^a \partial_{\Phi^a} + v^a_{,\mu} \partial_{\phi^a_{,\mu}} + v^a_{\mu_1 \mu_2} \partial_{\phi^a_{\mu_1 \mu_2}} + \cdots
$$

=--



+-- {: .num_defn #SymmetriesAndConservedCurrents}
###### Definition
**(infinitesimal symmetries of the Lagrangian and [[conserved currents]])

Given a [[Lagrangian density]] $\mathbf{L}$ as above, then

1. an _infinitesimal symmetry of the Lagrangian_ is a variation $v$ (def. \ref{Variation}) such that the [[Lie derivative]] $\mathcal{L}_v$ of the 
   Lagrangian density is a [[total derivative|total spacetime derivative]]
   
   $$
     \mathcal{L}_v \mathbf{L} = d \tilde J
   $$
   

1. an _[[on-shell]] [[conserved current]]_ is a horizontal $p$-form $J \in \Omega^{p,0}_\Sigma(E)$ whose [[total derivative|total spacetime derivative]] vanishes on the [[shell]] 
   
   $$
     d J\vert_{\mathcal{E}} = 0
     \,.
   $$

=--

## Properties

### Noether's theorem

+-- {: .num_prop #NoethersFirstTheorem}
###### Proposition
**([[Noether's theorem]] I)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If $v$ is an infinitesimal symmetry of the Lagrangian (def. \ref{SymmetriesAndConservedCurrents}) 
with $\mathcal{L}_v \mathbf{L} = d \tilde J_v$, then

$$
  J_v \coloneqq \tilde J_v - \iota_v \Theta
$$

is an [[on-shell]] [[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}), for $\Theta$
any choice of potential for the [[presymplectic current]] from def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

By [[Cartan's magic formula]] for the [[Lie derivative]] and using and the fact that the variation vector field $v$ vanishes on horizontal differential forms
we may re-express the defining equation for the symmetry as

$$
  d \tilde J
  =
  \mathcal{L}_v \mathbf{L}
  =
  \iota_v \underset{= \delta_{EL}\mathbf{L} + d \Theta}{\underbrace{\mathbf{d} \mathbf{L}}}
  +
  \mathbf{d} \underset{= 0}{\underbrace{\iota_v \mathbf{L}}} 
  =
  \frac{\delta_{EL}\mathbf{L}}{\delta v}
  - d \iota_v \Theta
$$

which is equivalent to

$$
  d(\underset{= J_v}{\underbrace{\tilde J - \iota_v \Theta}}) = \frac{\delta_{EL}\mathbf{L}}{\delta v}
$$

Since by definition of $\mathcal{E}$ the form $\frac{\delta_{EL} \mathbf{L}}{\delta v}$ vanishes on $\mathcal{E}$
this yield the claim.

=--


[[!redirects symmetries of a Lagrangian density]]


[[!redirects symmetry of the Lagrangian density]]
[[!redirects symmetries of the Lagrangian density]]

[[!redirects symmetry of a Lagrangian]]
[[!redirects symmetries of a Lagrangian]]

[[!redirects symmetry of the Lagrangian]]
[[!redirects symmetries of the Lagrangian]]



[[!redirects infinitesimal symmetry of a Lagrangian density]]
[[!redirects infinitesimal symmetries of a Lagrangian density]]


[[!redirects infinitesimal symmetry of the Lagrangian density]]
[[!redirects infinitesimal symmetries of the Lagrangian density]]

[[!redirects infinitesimal symmetry of a Lagrangian]]
[[!redirects infinitesimal symmetries of a Lagrangian]]

[[!redirects infinitesimal symmetry of the Lagrangian]]
[[!redirects infinitesimal symmetries of the Lagrangian]]

[[!redirects infinitesimal symmetries of Lagrangians]]
