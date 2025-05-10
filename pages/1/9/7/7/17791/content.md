
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[tensor product]] of [[linear representations]].

## Definition

Let $G$ be a [[group]] and let

$$
  \rho_i \;\colon\; G \times V_i \longrightarrow V_i
$$

be two [[linear representations]] of $G$ on [[vector spaces]] $V_i$, for $i \in \{1,2\}$. Then the _tensor product of representations_ of these is the linear representation whose underlying vector space is the [[tensor product of vector spaces]] $V_1 \otimes_k V_2$ equipped with the $G$-action induced by the [[diagonal action]]

$$
  G \times V_1 \times V_2
     \overset{\Delta_G \times id}{\longrightarrow}
  G \times G \times V_1 \times V_2
     \simeq
   G \times V_1 \times G \times V_1
     \overset{\rho_1 \times \rho_2}{\longrightarrow}
   V_1 \times V_2
  \,.
$$

## Related concepts

* [[category of representations]]

* [[Clebsch-Gordan coefficient]]

* [[Wigner 3j symbol]], [[Wigner 6j symbol]], [[Wigner 9j symbol]]

* [[McKay quiver]]

[[!redirects tensor products of representations]]

[[!redirects tensor product of representations]]



