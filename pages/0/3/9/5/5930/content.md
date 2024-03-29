
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _local algebra over an algebraic theory_ is to an [[algebra over an algebraic theory]] as a [[local ring]] is to a [[ring]]:

a local algebra in a [[sheaf topos]] is an algebra object / [[sheaf]] of [[algebra over an algebraic theory|algebras]], which is determined by its local restrictions, for a sense of _local_ determined both by the [[Grothendieck topology]] of any [[site]] of definition of the topos, as well as by a [[coverage]] on the category of finitely presented algebras.

## Definition

Let $\mathbb{T}$ be an [[essentially algebraic theory]] and write $\mathcal{C}_{\mathbb{T}}$ for its [[syntactic category]]: the category of [[finitely presented object|finitely presented]] $\mathbb{T}$-algebras

$$
  \mathcal{C}_{\mathbb{T}} 
    \simeq
  \mathbb{T}Alg^{fp}
  \,.
$$

Let $J$ be a [[coverage]] on $\mathcal{C}_{\mathbb{T}}$. 

+-- {: .num_defn}
###### Definition


For $\mathcal{E}$ a [[topos]], a **$J$-local $\mathbb{T}$-algebra** in $\mathcal{E}$ is a [[functor]]

$$
  A : \mathcal{C}_{\mathbb{T}} \to \mathcal{E}
$$

that 

1. preserves [[finite limit]]; 

1. sends $J$-[[covering]]s in $\mathcal{C}_{\mathbb{T}}$ to [[epimorphism]]s in $\mathcal{E}$.


A topos equipped with a local algebra object is a [[locally algebra-ed topos]].

=--

## Properties

+-- {: .num_prop #EveryToposIsAClassifyingToposForLocalAlgebras}
###### Proposition

A [[theory]] of local algebras is a [[geometric theory]] and every geometric theory is the theory of some local algebras.

=--

For the moment see [[classifying topos]] for details.

## Examples

* A [[local ring]] is a local algebra for the theory of rings.

  A topos equipped with a local ring is a [[locally ringed topos]].

## Related concepts

* [[algebraic theory]], [[essentially algebraic theory]]

* [[algebra over an algebraic theory]]

The [[(∞,1)-category theory]]-analog of a theory of local algebras is (except for the additional choice of "admissible morphisms") a

* [[geometry (for structured (∞,1)-toposes)]]

[[!redirects local algebras]]
