
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

\tableofcontents

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

An **extended natural numbers object** (extended NNO) in a topos is an [[object]] that behaves [[internalization|internal to]] that topos like the set $\overline{\mathbb{N}}$ of [[extended natural number|extended natural numbers]] does in [[Set]].

## Definition

### In a topos or cartesian closed distributive category

An **extended natural numbers object** in any [[topos]] (or any [[cartesian closed category|cartesian closed]] [[distributive category]]) $E$ with [[terminal object]] $1$ and [[coproduct]] $A + B$ is 

* an object $\overline{\mathbb{N}}$ in $E$ 

* equipped with a morphism $p:\overline{\mathbb{N}} \to (1 + \overline{\mathbb{N}})$

* such that for every other object $A$ with morphism $q:A \to (1 + A)$, there is a unique morphism $\mu_A:A \to \overline{\mathbb{N}}$ such that this diagram commutes:

$$\array{& A & \overset{q}\rightarrow & 1 + A & \\
          \mu_A & \downarrow &&\downarrow & \mu_A\\
          &\overline{\mathbb{N}} & \underset{p}\rightarrow& 1 + \overline{\mathbb{N}} & \\
}$$

Thus, the extended NNO is the [[terminal coalgebra]] for the [[endofunctor]] $A \mapsto 1 + A$ on $E$. 

### In a symmetric closed distributive monoidal category

The above definition makes sense in any [[symmetric monoidal category|symmetric]] [[closed monoidal category|closed]] [[distributive monoidal category]] $C$, provided that we use the [[tensor unit]] and [[tensor product]] instead of the [[terminal object]] and [[cartesian product]]. 

An **extended natural numbers object** in a symmetric closed distributive monoidal category $C$ with [[tensor unit]] $I$ and [[coproduct]] $A \oplus B$ is 

* an object $\overline{N}$ in $C$ 

* equipped with a morphism $p:\overline{N} \to (I \oplus \overline{N})$

* such that for every other object $A$ with morphism $q:A \to (I \oplus A)$, there is a unique morphism $\mu_A:A \to \overline{N}$ such that this diagram commutes:

$$\array{& A & \overset{q}\rightarrow & I \oplus A & \\
          \mu_A & \downarrow &&\downarrow & \mu_A\\
          &\overline{N} & \underset{p}\rightarrow& I \oplus \overline{N} & \\
}$$

## Examples

* The set of [[extended natural numbers]] is the extended natural numbers object in [[Set]]

* Given a [[field]] $K$, the underlying [[vector space]] of the [[sequence algebra]] $K^\mathbb{N}$ is the extended natural numbers object in [[Vect|$\mathrm{Vect}_K$]]. 

## Properties

If the topos is a [[Boolean topos]] with a [[natural numbers object]], then the extended natural numbers object  $\overline{\mathbb{N}}$ is isomorphic to the object $\mathbb{N} + 1$.

## Related concepts

* [[extended natural numbers]]
* [[natural numbers object]]

[[!redirects conatural numbers object]]
[[!redirects conatural numbers objects]]
[[!redirects conatural number object]]
[[!redirects conatural number objects]]
[[!redirects conatural-numbers object]]
[[!redirects conatural-numbers objects]]
[[!redirects conatural-number object]]
[[!redirects conatural-number objects]]

[[!redirects co-natural numbers object]]
[[!redirects co-natural numbers objects]]
[[!redirects co-natural number object]]
[[!redirects co-natural number objects]]
[[!redirects co-natural-numbers object]]
[[!redirects co-natural-numbers objects]]
[[!redirects co-natural-number object]]
[[!redirects co-natural-number objects]]

[[!redirects extended natural numbers object]]
[[!redirects extended natural numbers objects]]
[[!redirects extended natural number object]]
[[!redirects extended natural number objects]]
[[!redirects extended natural-numbers object]]
[[!redirects extended natural-numbers objects]]
[[!redirects extended natural-number object]]
[[!redirects extended natural-number objects]]
[[!redirects extended NNO]]
[[!redirects extended NNOs]]