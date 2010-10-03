
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
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

A [[connection on a bundle]] induces a notion of [[parallel transport]] over _paths_ . A [[connection on a 2-bundle]] induces a generalization of this to a notion of parallel transport over _surfaces_ . Similarly a [[connection on a 3-bundle]] induces a notion of parallel transport over 3-dimensional volumes.

Generally, a [[connection on an ∞-bundle]] induces a notion of parallel transport in arbitrary dimension.

## Definition


Let $A$ be an [[∞-Lie groupoid]] such that morphisms $X \to A$ in [[?LieGrpd]] classify the $A$-[[principal ∞-bundle]]s under consideration. Write $A_{conn}$ for the differential refinement described at [[∞-Lie algebra valued form]], such that lifts

$$
  \array{
     && A_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     X &\stackrel{g}{\to}& A
  }
$$

describe [[connections on ∞-bundles]].

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ say that $\nabla$ **admits parallel $n$-transport** if for all [[smooth manifold]]s $\Sigma$ of [[dimension]] $n$ and all morphisms 

$$
  \phi : \Sigma \to X
$$

we have that the pullback of $\nabla$ to $\Sigma$

$$
  \phi^* \nabla : \Sigma \stackrel{\phi}{\to} X \stackrel{\nabla}{\to} A_{conn}
$$

**flat** in that it factors through the canonical inclusion $\mathbf{\flat}A \to A_{conn}$.

In other words: if all the lower [[curvature]] $k$-forms, $1 \leq k \leq n$ of $\phi^* \nabla$ vanish (the higher ones vanish automatically for dimensional reasons).

=--

Here $\mathbf{\flat}A = [\mathbf{\Pi}(-),A]$ is the coefficient for [[schreiber:path ∞-groupoid|flat differential A-cohomology]].


+-- {: .un_defn}
###### Remark

This condition is automatically satisfied for ordinary [[connections on bundles]], hence for $A = \mathbf{B}G$ with $G$ an ordinary [[Lie group]]: because in that case there is only a single curvature form, namely the ordinary [[curvature]] 2-form.

But for a [[principal 2-bundle]] with connection there is in general a 2-form curvature and a 3-form curvature. A 2-connection therefore admits parallel transport only if its 2-form curvature is constrained to vanish. 

Notice however that if the coefficient object $A$ happens to be $(n-1)$-[[connected]] -- for instance if it is an [[Eilenberg-MacLane object]] in degree $n$, then there is no extra condition and _every_ connection admits parallel transport. This is notably the case for [[circle n-bundles with connection]].
 
=--


+-- {: .un_defn}
###### Definition

For $\nabla : X \to A_{conn}$ an $\infty$-connection that admits parallel $n$-transport, this is for each $\phi : \Sigma \to X$ the morphism

$$
  \mathbf{\Pi}(\Sigma) \to A
$$

that corresponds to $\phi^* \nabla$ under the equivalence

$$
  \mathbf{H}(\Sigma, \mathbf{\flat}A ) \simeq \mathbf{H}(\mathbf{\Pi}(\Sigma), A)
  \,.
$$

=--

+-- {: .un_defn}
###### Remark


The objects of the [[schreiber:path ∞-groupoid]] $\mathbf{\Pi}(\Sigma)$ are points in $\Sigma$, the morphisms are paths in there, the 2-morphisms surves between these paths, and so on. Hence a morphism $\mathbf{\Pi}(\Sigma) \to A$ assigns fibers in $A$ to points in $X$, and equivalences between these fibers to paths in $\Sigma$, and so on.

=--


## Higher holonomy

We now define thee higher analog of [[holonomy]] for the case that $\Sigma$ is closed.

+-- {: .un_defn}
###### Definition

Let $\nabla : X \to A_{conn}$ be a connection with parallel $n$-transport and $\phi : \Sigma \to X$ a morphism from a _closed_ $n$-[[manifold]].

Then the **$n$-holonomy** of $\nabla$ over $\Sigma$ is the image $[\phi^* \nabla]$ of

$$
  \phi^* \nabla : \Pi(\Sigma) \to \Gamma(A)
$$

in the [[homotpy category]]

$$
  [\phi^* \nabla] \in [\Pi(\Sigma), \Gamma(A)] 
$$

=--


## Examples

### For trivial circle $n$-bundles / for $n$-forms

The simplest example is the parallel transport in a [[circle n-bundle with connection]] over a [[smooth manifold]] $X$ whose underlying $\mathbf{B}^{n-1}U(1)$-bundle is trivial. This is equivalently given by a degree $n$-[[differential form]] $A \in \Omega^n(X)$. For $\phi : \Sigma_n \to X$ any [[smooth function]] from an $n$-dimensional manifold $\Sigma$, the corresponding parallel transport is simply the [[integral]] of $A$ over $\Sigma$:

$$
  \tra_A(\Sigma) = \exp(i \int_\Sigma \phi^* A)
  \;\;\; \in \;\; U(1)
  \,.
$$

One can understand higher parallel transport therefore as a generalization of integration of diifferential $n$-forms to the case where

* the $n$-form is not globally defined;

* the $n$-form takes values not in $\mathbb{R}$ but more generally is an [[∞-Lie algebroid valued differential form]].

### For circle $n$-bundles with connection

We show how the $n$-holonomy of [[circle n-bundles with connection]] is reproduced from the above.

Let $\phi^* \nabla : \mathbf{\Pi}(\Sigma) \to \mathbf{B}^n U(1)$ be the parallel transport for a [[circle n-bundle with connection]] over a $\phi : \Sigma \to X$.

This is equivalent to a morphism

$$
  \Pi(\Sigma) \to \mathcal{B}^n U(1)
  ,.
$$

We may map this further to its $(n-dim \Sigma)$-[[nLab:truncated|truncation]]

$$
  :\infty Grpd(\Pi(\Sigma), \mathcal{B}^n U(1)) 
  \to
  \tau_{n-dim \Sigma} \infty Grpd(\Pi(X), \mathcal{B}^n U(1))
  \,.
$$

+-- {: .un_theorem}
###### Theorem

We have

$$
  \tau_{n-dim\Sigma} \infty Grpd(\Pi(\Sigma), \mathcal{B}^n U(1))
  \simeq
  \mathbf{B}^{n-dim \Sigma} U(1)
  \,.
$$

=--

(This is due to an observation by [[nLab:Domenico Fiorenza]].)

+-- {: .proof}
###### Proof

By general abstract reasoning (recalled at [[nLab:cohomology]] and [[nLab:fiber sequence]]) we have for the [[nLab:homotopy group]]s that

\[
  \pi_i \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))
  \simeq 
  H^{n-i}(\Sigma, U(1))
  \,.
\]

Now use the [[nLab:universal coefficient theorem]], which asserts that we have an [[nLab:exact sequence]]

\[
  0
  \to 
  Ext^1(H_{n-i-1}(\Sigma,\mathbb{Z}),U(1))
  \to 
  H^{n-i}(\Sigma,U(1))
  \to 
  Hom(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
  \to 0
  \,.
\]

Since $U(1)$ is an [[nLab:injective object|injective]] $\mathbb{Z}$-[[nLab:module]] we have 

$$
  Ext^1(-,U(1))=0
  \,.
$$  

This means that we have an [[nLab:isomorphism]]

\[
  H^{n-i}(\Sigma,U(1))
  \simeq 
  Hom_{Ab}(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
\]

that identifies the [[nLab:cohomology group]] in question with the [[nLab:internal hom]] in [[nLab:Ab]] from the integral [[nLab:homology]] group of $\Sigma$ to $U(1)$.

For $i\lt (n-dim \Sigma)$, the right hand is zero, so that 

$$
  \pi_i \infty Grpd(\Pi(\Sigma),\mathbf{B}^n U(1)) =0 \;\;\;\;
  for i\lt (n-dim \Sigma)
  \,. 
$$ 

For $i=(n-dim \Sigma)$, instead, $H_{n-i}(\Sigma,\mathbb{Z})\simeq \mathbb{Z}$, since $\Sigma$ is a closed $dim \Sigma$-manifold and so 

$$
  \pi_{(n-dim\Sigma)} \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))\simeq U(1)
  \,.
$$


=--


+-- {: .un_def}
###### Definition 

The resulting morphism

$$
  \mathbf{H}(\Sigma, A_{conn})
  \stackrel{\exp(i S(-))}{\to}
  \mathbf{B}^{n-dim\Sigma} U(1)
$$

in [[nLab:∞Grpd]] we call the **$\infty$-Chern-Simons action** on $\Sigma$.

=--

Here in the language of [[nLab:quantum field theory]]

* the [[nLab:object]]s of $\mathbf{H}(\Sigma,A_{conn})$ are the [[nLab:gauge field]] on $\Sigma$;

* the [[nLab:morphism]]s in $\mathbf{H}(\Sigma, A_{conn})$ are the [[nLab:gauge transformation]]s;.








## Applications

### In physics

In [[physics]] various [[action functional]]s for [[quantum field theories]] are nothing but higher parallel transport.

* The gauge interaction part of the action functional for the particle charged under a background [[electromagnetic field]], which is a [[circle n-bundle with connection|circle bundle with connection]] $\nabla$, is the parallel 1-transport of $\nabla$.

* The gauge interaction part of the action functional for the string charged under a background [[Kalb-Ramond field]], which is a [[circle n-bundle with connection|circle 2-bundle with connection]] $\nabla$, is the parallel 2-transport of $\nabla$.

* The gauge interaction part of the action functional for the membrane charged under a background [[supergravity C-field]], which is a [[circle n-bundle with connection|circle 3-bundle with connection]] $\nabla$, is the parallel 3-transport of $\nabla$.

* The action functional of [[Chern-Simons theory]] is the parallel 3-transport of a [[Chern-Simons circle 3-bundle]].



## References

For references on parallel 2-transport in bundle gerbes see [[connection on a bundle gerbe]].

The generalization of this to parallel 2-transport of [[connections on a 2-bundle]] as described above is in 

* SWIII (<a href="SchrWalII+III">web</a>)
{#SWIII}
