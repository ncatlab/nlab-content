[[!redirects fundamental product theorem in K-theory]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[compact Hausdorff space]] The _fundamental product theorem in topological K-theory_ identifies 

1. the [[topological K-theory]]-[[commutative ring|ring]] $K(X \times S^2)$ of the [[product topological space]] $X \times S^2$ with the [[2-sphere]] $S^2 $;

1. the K-theory ring $K(X)$ of the original space $X$ with a generator $H$ for the [[basic line bundle on the 2-sphere]] adjoined:

$$
  K(X \times S^2) \simeq K(X) \otimes_{\mathbb{Z}} \mathbb{Z}[H]/(H-1)^2
  \,.
$$

This theorem in particular serves as a substantial step in a [[proof]] of [[Bott periodicity]] for [[topological K-theory]].

The usual [[proof]] proceeds by first realizing all [[vector bundles]] on $X \times S^2$ via an $X$-parameterized [[clutching construction]], then showing that all the clutching functions are [[homotopy|homotopic]] to those that are [[Laurent series]] as functions on $S^1$, and then analyzing these.




## Statement

For $S^2 \subset \mathbb{R}^3$ the [[2-sphere]] with its [[Euclidean space|Euclidean]] [[subspace topology]], 
write $h$ for the [[basic line bundle on the 2-sphere]]. Its image in the [[topological K-theory]] ring $K(S^2)$ satisfies the relation

$$
  2 h = h^2 + 1
  \;\;\Leftrightarrow\;\;
  (h-1)^2 = 0 
$$

(by [this prop.](basic+complex+line+bundle+on+the+2-sphere#TensorRelationForBasicLineBundleOn2Sphere)).

(Notice that $h-1$ is the image of $h$ in the [[reduced K-theory]] $\tilde K(X)$ of $S^2$ under the splitting $K(X) \simeq \tilde K(X) \oplus \mathbb{Z}$ (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)).)

It follows that there is a [[ring homomorphism]] of the form

$$
  \array{
    \mathbb{Z}[h]/\left( (h-1)^2 \right)
      &\overset{}{\longrightarrow}&
    K(S^2)
    \\
    h &\overset{\phantom{AAA}}{\mapsto}& H
  }
$$

from the [[polynomial ring]] in one abstract generator, [[quotient ring|quotiented]] by this relation, to the [[topological K-theory]] ring.

More generally, for $X$ a [[topological space]], then this induces the composite ring homomorphism

$$
  \array{
    K(X) \otimes \mathbb{Z}[h]/((h-1)^2)
      & \longrightarrow & 
    K(X) \times K(S^2)
      & \longrightarrow &
    K(X \times S^2)
    \\
    (E, h)
      &\overset{\phantom{AAA} }{\mapsto}&
    (E,H)
      &\overset{\phantom{AAA}}{\mapsto}&
    (\pi_{X}^\ast E) \cdot (\pi_{S^2}^\ast H) 
  }
$$

to the topological K-theory ring of the [[product topological space]] $X \times S^^2$, where the second map is the [[external tensor product of vector bundles]].

+-- {: .num_prop #FundamentalProductTheorem}
###### Proposition
**(fundamental product theorem in topological K-theory)**

For $X$ a [[compact Hausdorff space]], then this ring homomorphism is an [[isomorphism]].

=--

(e.g. [Hatcher, theorem 2.2](#Hatcher))

+-- {: .num_remark}
###### Remark

More generally, for $L\to X$ a [[complex line bundle]] with class $l \in K(X)$ and with $P(1 \oplus L)$ denoting its [[projective bundle]] then 

$$
  K(X)[h]/((h-1)(l \cdot h -1))
   \simeq
  K(P(1 \oplus L))
$$

=--

(e.g. [Wirthmuller 12, p. 17](#Wirthmuller12))

As a special case this implies the first statement above:


For $X = \ast$ the product theorem prop. \ref{FundamentalProductTheorem} says in particular that the first of the two morphisms in the composite is an [[isomorphism]] (example \ref{TopologicalKTheoryRingOfThe2Sphere} below)  and hence by the [[two-out-of-three]]-property for [[isomorphisms]] it follows that

+-- {: .num_cor #ExternalProductTheorem}
###### Corollary
**(external product theorem)**

For $X$ a [[compact Hausdorff space]] we have that the [[external tensor product of vector bundles]] 

$$
  K(X) \otimes K(S^2) \overset{\simeq}{\longrightarrow} K(X \times S^2)
$$

is an [[isomorphism]] in [[topological K-theory]].

=--

## Examples

+-- {: .num_example #TopologicalKTheoryRingOfThe2Sphere}
###### Example
**([[topological K-theory]] ring of the [[2-sphere]])

For $X = \ast$ the [[point space]], the fundamental product theorem \ref{FundamentalProductTheorem} states that the homomorphism

$$
  \array{
    \mathbb{Z}[h]/((h-1)^2)
      &\longrightarrow&
    K(S^2)
    \\
    h &\mapsto& h
  }
$$

is an [[isomorphism]]. 

This means that the relation $(h-1)^2 = 0$ satisfied by the [[basic line bundle on the 2-sphere]] ([this prop.](basic+complex+line+bundle+on+the+2-sphere#TensorRelationForBasicLineBundleOn2Sphere)) is the _only_ relation is satisfies in topological K-theory.

Notice that the underlying [[abelian group]] of $\mathbb{Z}[h]/((h-1)^2)$ is two [[direct sum]] copies of the [[integers]],

$$
  K(S^2) \simeq \mathbb{Z} \oplus \mathbb{Z} = \langle 1, h\rangle
$$

one copy spanned by the [[trivial vector bundle|trivial]] [[complex line bundle]] on the 2-sphere, the other spanned by the [[basic complex line bundle on the 2-sphere]]. (In contrast, the underlying abelian group of the [[polynomial ring]] $\mathbb{R}[h]$ has infinitely many copies of $\mathbb{Z}$, one for each $h^n$, for $n \in \mathbb{N}$).

It follows (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)) that the [[reduced K-theory]] group of the 2-sphere is

$$
  \tilde K(S^2) \simeq \mathbb{Z}
  \,.
$$

=--





## References

* {#Hatcher} [[Allen Hatcher]], section 2.1 (from p. 45 on) in _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 6 (from p. 19 on) in _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


[[!redirects external product theorem]]
