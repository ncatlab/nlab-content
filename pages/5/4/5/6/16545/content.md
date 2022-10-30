
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[variational calculus]] an _evolutionary vector_ field is a particular type of vertical [[vector field]] on the infinite-order [[jet bundle]] $J^\infty_\Sigma(E)$ of a [[fiber bundle]] $E \overset{fb}{\to} \Sigma$, which may be interpreted as the generator of a transformation of the [[space of sections]] $\Gamma_\Sigma(E)$ of $E$. 

Evolutionary vector fields describe [[infinitesimal]] [[symmetries]] of [[Lagrangian field theories]] in the formulation of the [[variational bicomplex]], and as such form an ingredient of [[Noether's theorem]].

## Definition

There are (at least) two different definitions, def. \ref{EvolutionaryVectorFieldPerceivedOnJetBundle} and def. \ref{AsGeneralizedVectorFieldOnE} below, which are equivalent (prop. \ref{EquivalenceOfDefinitions} below).


### As a vector field on the jet bundle

+-- {: .num_defn #EvolutionaryVectorFieldPerceivedOnJetBundle}
###### Definition
**(as a vector field on the [[jet bundle]])**

An **evolutionary vector field** is a [[vector field]] $v$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ which is [[vertical vector field|vertical]] with respect to the [[projection]] $\pi_\infty: J^\infty_\Sigma E \to \Sigma$ such that the following equivalent conditions hold:

1. The [[Lie derivative]] $\mathcal{L}_v$ satisfies 

   1. $\mathcal{L}_v d = d \mathcal{L}_v$,

   1. $\mathcal{L}_v = \iota_v \delta + \delta \iota_v$,

   where $d$ is the [[horizontal derivative]] on differential forms on $J^\infty E$, while $\delta$ is the [[vertical derivative]]. 

1. $v$ preserves the [[contact ideal]], i.e., for which $\mathcal{L}_v\theta$ is a [[contact form]] whenever $\theta$ is a [[contact form]].

We denote the subspace of evolutionary vector fields as $\mathfrak{X}_{ev}(J^\infty_\Sigma(E)) \subset \mathfrak{X}_V(J^\infty_\Sigma(E))$.

=--


Note that every evolutionary vector field is uniquely defined by its action on the [[pullbacks of functions]] on $E$ to $J^\infty_\Sigma(E)$. To formalize this, one may use the following notion.

+-- {: .num_defn #Characteristic}
###### Definition

Let $v \in \mathfrak{X}_{ev}(J^\infty E)$ be an evolutionary vector field. Its **characteristic** is the map $\pi_{\infty,0*} \circ v: J^\infty E \to V E$.

=--

### As a generalized vector field on the fiber bundle

Alternatively, a generalized vector field on the [[fiber bundle]] $E$ may be seen as a vector field on $E$ whose coefficients are functions on the [[jet bundle]] $J^\infty E$. More formally, it is a particular map from $J^\infty E$ to $T E$. Here we are interested only in a particular class of vertical vector fields.

+-- {: .num_defn #AsGeneralizedVectorFieldOnE}
###### Definition

An **evolutionary vector field** is a map $w \colon J^\infty_\Sigma(E) \to V_\Sigma E$ from the [[jet bundle]] $J^\infty E$ to the [[vertical tangent bundle]] $V_\Sigma E$, such that 

$$
  \nu \circ w = \pi_{\infty,0}
  \phantom{AAAAAAA}
  \array{
    J^\infty_\Sigma(E)
    && \overset{w}{\longrightarrow} &&
    V_\Sigma E
    \\
    & {}_{\mathllap{\pi_{\infty,0}}}\searrow && \swarrow_{\mathllap{\nu}}
    \\
    && \E
  }
  \,,
$$ 

where $\nu: V_\Sigma E \to E$ is the bundle map of $V_\Sigma E$ and $\pi_{\infty,0}: J^\infty_\Sigma(E) \to E$ is the target map of the jet bundle.

=--

Every evolutionary vector field can unique be prolonged to a vector field on $J^\infty_\Sigma(E)$.

+-- {: .num_defn #Prolongation}
###### Definition

Let $w$ be an evolutionary vector field in the sense of def. \ref{AsGeneralizedVectorFieldOnE}. Its **prolongation** to $J^\infty_\Sigma E$ is the unique vertical vector field $pr w$ on $J^\infty_\Sigma E$ such that 

1. $w$ and $pr w$ agree on functions on $E$ 

1. $pr w$ preserves the contact ideal, i.e., $\mathcal{L}_v\theta$ is a [[contact form]] whenever $\theta$ is a [[contact form]].

=--

### Equivalence of the definitions

+-- {: .num_prop #EquivalenceOfDefinitions}
###### Proposition
**(equivalence of the two definitions)**

If $v$ is an evolutionary vector field in the sense of def. \ref{EvolutionaryVectorFieldPerceivedOnJetBundle}, then its characteristic $\pi_{\infty,0*} \circ v$ (def. \ref{Characteristic}) is an evolutionary vector field in the sense of def. \ref{AsGeneralizedVectorFieldOnE}. 

Conversely, if $w$ is an evolutionary vector field in the sense of def. \ref{AsGeneralizedVectorFieldOnE}, then its prolongation $pr w$ (def. \ref{Prolongation}) is an evolutionary vector field in the sense of def. \ref{EvolutionaryVectorFieldPerceivedOnJetBundle}. 

Furthermore, $pr (\pi_{\infty,0*} \circ v) = v$ and $\pi_{\infty,0*} \circ (pr w) = w$, so that this establishes a [[bijection]] between both definitions.

=--

## Related concepts

* [[point symmetry]]

* [[conserved current]]


## References

See also

* [[Joseph Krasil'shchik]], Alexander Verbovetsky, section 1.4 of _Geometry of jet spaces and integrable systems_, J.Geom.Phys.61:1633-1674, 2011 ([arXiv:1002.0077](https://arxiv.org/abs/1002.0077))

