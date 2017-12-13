

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[variational calculus]], the _[[variational bicomplex]]_ of a [[fiber bundle]] serves to give a local description of the [[variational derivative]] $\delta$. In applications one is typically interested in 1) specifying a [[differential equation]] which carves out its [[solution]] locus ([[diffiety]]) inside the [[jet bundle]] and 2) forming the [[quotient]] by [[infinitesimal symmetries]] of the [[PDE]]. Moreover, it is usually useful to perform both these operations in [[homotopy theory]]/[[higher differential geometry]]. Using tools from [[homological algebra]], under suitable conditions the resulting combined [[homotopy intersection]] in and [[homotopy quotient]] is modeled by a combination of the [[variational bicomplex]] with a _[[local BV-BRST complex]]_.

## Definition


+-- {: .num_defn #BVVariationalBicomplex}
###### Definition
**([[variational BV-bicomplex]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] ([this def.](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime))
equipped with a [[gauge parameter bundle]]   $\mathcal{G}$ ([this def.\](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#GaugeParametrizedInfinitesimalGaugeTransformation)) which is closed ([this def..](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#GaugeParametrizedInfinitesimalGaugeTransformation#GaugeParametersClosed)).
Consider the [[Lie algebroid]] $E/(\mathcal{G} \times_\Sigma T \Sigma)$ from [this example](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#GaugeParametrizedInfinitesimalGaugeTransformation#GaugeParametersClosed#LocalOffShellBRSTComplex),
whose [[Chevalley-Eilenberg algebra]] is the [[local BRST complex]] of the theory.

Then its [[Weil algebra]] $W(E/(\mathcal{G} \times_\Sigma T \Sigma))$
has as differential the [[variational derivative]] ([this def.](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime))
plus the [[BRST differential]]

$$
  \begin{aligned}
    d_{W}
    & = \mathbf{d} - (d - s_{BRST})
    \\
    & =
    \delta + s_{BRST}
  \end{aligned}
  \,.
$$

Therefore we speak of the _[[variational BRST-bicomplex]]_ and write

$$
  \Omega^\bullet_\Sigma( E/(\mathcal{G} \times_\Sigma T \Sigma) )
  \,.
$$

Similarly, the Weil algebra of the derived prolonged shell $\mathcal{E}^\infty_{BV}$ ([this def.](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#DerivedProlongedShell)) has differential

$$
  \begin{aligned}
    d_W
      & =  \mathbf{d} - (d - s)
    \\
    & = \delta + s
  \end{aligned}
  \,.
$$

Since $s$ is the [[BV-BRST differential]] this defines the "BV-BRST [[variational bicomplex]]".

=--

[[!redirects variational BV-bicomplex]]
[[!redirects variational BRST-bicomplex]]
[[!redirects variational BV-BRST-bicomplex]]


[[!redirects variational BV bicomplex]]
[[!redirects variational BRST bicomplex]]
[[!redirects variational BV-BRST bicomplex]]

