


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[local field theory]] with [[field (physics)|fields]] on a given [[spacetime]] $X$, the _spacetime support_ of an [[observable]] $A$ is the maximal region in spacetime such that $A$ depends on ("observes") the values of fields at the points in this region.

In a [[local field theory]] spacetime support of observables is typically required to be a [[compact subset]] of spacetime, which, under the [[Heine-Borel theorem]], reflects the intuition that every [[experiment]] (every "observation" of [[physics]]) is necessarily [[bounded subset|bounded]] in [[spacetime]].

For more see at _[[geometry of physics -- perturbative quantum field theory]]_ the chapter _[7. Observables](geometry+of+physics+--+perturbative+quantum+field+theory#Observables)_

## Definition

+-- {: .num_defn #SpacetimeSupport}
###### Definition
**([[spacetime support]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{FieldsAndFieldBundles}),
with induced [[jet bundle]] $J^\infty_\Sigma(E)$

For every [[subset]] $S \subset \Sigma$ let

$$
  \array{
    J^\infty_\Sigma(E)\vert_S
      &\overset{\iota_S}{\hookrightarrow}&
    J^\infty_\Sigma(E)
    \\
    \downarrow &(pb)& \downarrow
    \\
    S &\hookrightarrow& \Sigma
  }
$$

be the corresponding restriction of the [[jet bundle]] of $E$.

The _spacetime support  _ $supp_\Sigma(A)$ of a [[differential form]] $A \in \Omega^\bullet(J^\infty_\Sigma(E))$
on the [[jet bundle]] of $E$ is the [[topological closure]] of the maximal subset $S \subset \Sigma$
such that the restriction of $A$ to the jet bundle restrited to this subset does not vanishes:

$$
  supp_\Sigma(A) \coloneqq Cl( \{ x \in \Sigma |  \iota_{\{x\}}^\ast A \neq 0 \} )
$$

We write

$$
  \Omega^{r,s}_{\Sigma,cp}(E)
  \coloneqq
  \left\{
    A \in \Omega^{r,s}_\Sigma(E)
    \;\vert\;
    supp_\Sigma(A) \, \text{is compact}
  \right\}
    \;\hookrightarrow\;
  \Omega^{r,s}_\Sigma(E)
$$

for the subspace of differential forms on the jet bundle whose spacetime support is a [[compact subspace]].

=--

## Related concepts

* [[support]], [[support of a distribution]]

* [[compact support]]

* [[local observable]]

## References

* _[[geometry of physics -- perturbative quantum field theory]]_ the chapter _[7. Observables](geometry+of+physics+--+perturbative+quantum+field+theory#Observables)_


[[!redirects spacetime supports]]
