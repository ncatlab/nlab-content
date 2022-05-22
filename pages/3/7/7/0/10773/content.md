
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[(∞,1)-category theory]] the typical notion of [[filtered object]] in [[category theory]] simplifies: instead of a [[sequential diagram]] of [[monomorphisms]], it is just any [[tower diagram]].

## Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]].

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _filtering_ on an [[object]] $X \in \mathcal{C}$ is a [[sequential diagram]] $X_\bullet \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n-1} \to X_n \to X_{n+1} \to \cdots
$$

such that 

$$
  X \simeq \underset{\rightarrow}{\lim} X_\bullet
$$

is the [[sequential colimit|sequential]] [[homotopy colimit]] of the tower.

Dually a _cofiltering_ of $X$ is a tower $X_\bullet$ such that 

$$
  X \simeq \underset{\leftarrow}{\lim} X_\bullet
$$

is the [[homotopy limit]].

=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).


## Applications

### Spectral sequence

If $\mathcal{C}$ is a [[stable (∞,1)-category]] with [[sequential limits]]/[[sequential colimits]] and with a [[t-structure]], then every filtering/cofiltering on $X$ induces a [[spectral sequence of a filtered stable homotopy type]] which converges to the [[homotopy groups]] of $X$.

The [[spectral sequence of a filtered stable homotopy type]] associated with the chromatic tower (regarded as a [[filtered object in an (infinity,1)-category]]) is the _[[chromatic spectral sequence]]_ ([Wilson 13, section 2.1.2](#Wilson13))

## Related concepts

* [[filtered chain complex]]

* [[filtered spectrum]]

* [[tower of homotopy fibers]]

* [[persistent homotopy theory]]

[[!include Lurie spectral sequences -- table]]

\linebreak

[[!redirects filtered objects in an (∞,1)-category]]

\linebreak

[[!include filtered objects -- contents]]


[[!redirects filtered objects in an (∞,1)-category]]


[[!redirects filtered object in an (infinity,1)-category]]
[[!redirects filtered objects in an (infinity,1)-category]]

[[!redirects filtered object of an (∞,1)-category]]
[[!redirects filtered objects of an (∞,1)-category]]

[[!redirects filtered object of an (infinity,1)-category]]
[[!redirects filtered objects of an (infinity,1)-category]]


