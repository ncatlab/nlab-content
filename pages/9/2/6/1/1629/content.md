
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **homeomorphism** (also spelt 'homoeomorphism' and 'hom&#339;omorphism' but *not* '[[homomorphism]]') is an [[isomorphism]] in the [[category]] [[Top]] of [[topological spaces]].

That is, a homeomorphism $f : X \to Y$ is a [[continuous map]] of [[topological spaces]] such that there is an [[inverse]] $f^{-1}: Y \to X $ that is also a continuous map of topological spaces.  Equivalently, $f$ is a [[bijection]] between the underlying sets such that both $f$ and its inverse are continuous.

For more see at _[[Introduction to Topology -- 1]]_ the section _[Homeomorphisms](Introduction+to+Topology -- 1#Homeomorphisms)_.


The term 'homeomorphism' is also applied to isomorphisms in categories that generalise $Top$, such as the category of [[convergence spaces]] and the category of [[locales]].

## Counter-examples

Beware that a continous [[bijection]] is not necessarily a homeomorphism; that is, $Top$ is not a [[balanced category]].

For example $\exp(2\pi i(-)) [0,1) \to S^1$ is continuous and the underlying function of sets is a [[bijection]], but the inverse function at the level of sets is not continuous.

But see prop. \ref{HomeoContinuousOpenBijection}.

## Properties

+-- {: .num_prop #HomeoContinuousOpenBijection}
###### Proposition
**([[homeomorphisms]] are the [[continuous function|continuous]] and [[open map|open]] [[bijections]])

Let $f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)$ be a [[continuous function]]
between [[topological spaces]]. Then the following are equivalence:

1. $f$ is a [[homeomorphism]];

1. $f$ is a [[bijection]] and an [[open map]];

1. $f$ is a [[bijection]] and a [[closed map]].

=--

+-- {: .proof}
###### Proof

It is clear from the definition that a homeomorphism in particular has to be a bijection.
The condition that the [[inverse function]] $Y \leftarrow X \colon g$ be continuous means
that the [[pre-image]] function of $g$ sends open subsets to open subsets. But by $g$ being the inverse to
$f$, that pre-image function is equal to $f$, regarded as a function on subsets:

$$
  g^{-1} = f \;\colon\; P(X) \to P(Y)
  \,.
$$

Hence $g^{-1}$ sends opens to opens precisely if $f$ does, which is the case precisely if $f$ is an open map,
by definition.
This shows the equivalence of the first two items. The equivalence between the first and the third follows
similarly via prop. \ref{ClosedSubsetContinuity}.

=--



## Related concepts

* [[homeomorphism invariant]]

* [[homotopy equivalence]]

* [[weak homotopy equivalence]]

## References

The terminology "homeomorphism" is due to:

* [[Henri Poincaré]], *[[Analysis Situs]]*, Journal de l'École Polytechnique. (2). 1: 1–123 (1895) ([gallica:12148/bpt6k4337198/f7](https://gallica.bnf.fr/ark:/12148/bpt6k4337198/f7), Engl: [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/poincare2009.pdf), [[Stillwell_AnalysisSitus.pdf:file]])



[[!redirects homeomorphisms]]
[[!redirects homœomorphism]]
[[!redirects homœomorphisms]]
[[!redirects homoeomorphism]]
[[!redirects homoeomorphisms]]

[[!redirects homeomorphic]]
[[!redirects homœomorphic]]
[[!redirects homoeomorphic]]
