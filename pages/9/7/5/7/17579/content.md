
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

+-- {: .num_defn}
###### Definition

A [[site]] is called **atomic** if the [[covering sieve|covering]] [[sieves]] are exactly the [[inhabited set|inhabited]] sieves.
=--

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ be a [[category]]. Then $\mathcal{C}$ can be made into an atomic site if and only if for any diagram
$$
\array{
  & & A \\
  & & \downarrow\\
  B & \to & C
}
$$
there is an object $D$ and arrows $D \to A, B$ such that the following diagram commutes:
$$
\array{
  D & \to & A \\
  \downarrow & & \downarrow\\
  B & \to & C
}
$$
=--

+-- {: .proof}
###### Proof
This is exactly what is needed for the pullback stability axiom to hold, and the other axioms are immediate.
=--