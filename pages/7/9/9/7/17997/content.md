
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

For $X$ a [[compact Hausdorff space]], the _fundamental product theorem in topological K-theory_ identifies 

1. the [[topological K-theory]]-[[commutative ring|ring]] $K(X \times S^2)$ of the [[product topological space]] $X \times S^2$ with the [[2-sphere]] $S^2 $;

1. the K-theory ring $K(X)$ of the original space $X$ with a generator $H$ for the [[basic line bundle on the 2-sphere]] adjoined:

$$
  K(X) \otimes_{\mathbb{Z}} \mathbb{Z}[H]/(H-1)^2
    \overset{\simeq}{\longrightarrow}
  K(X \times S^2) 
  \,.
$$

This theorem in particular serves as a substantial step in a [[proof]] of [[Bott periodicity]] for [[topological K-theory]] (cor. \ref{BottPeriodicity} below).

The usual [[proof]] proceeds by 

1.  realizing all [[vector bundles]] on $X \times S^2$ via an $X$-parameterized [[clutching construction]];

1. showing that all the clutching functions are [[homotopy|homotopic]] to those that are Laurent polynomials as functions on $S^1$, hence products of a polynomial clutching $p$ functions with a monomial $z^{-n}$ of negative power;

1. observing that the bundle corresponding to a clutching function of the form $f z^n$ is equivalent to the bundle corresponding to $f$ and tensored with the $n$th [[tensor product of vector bundles]]-power of the [[basic complex line bundle on the 2-sphere]];

1. showing that some [[direct sum of vector bundles]] of the vector bundle corresponding to a polynomial clutching function with one coming from a trivial clutching function is given by a linear clutching function;

1. showing that bundles coming from linear clutching functions are [[direct sums of vector bundles|direct sums]] of one coming from a trivial clutching function with the one coming from the homogeneously linear part;

Applying these steps to a vector bundle on $X \times S^2$ yields a virtual sum of [[external tensor products of vector bundles]] of bundles on $X$ with powers of the [[basic complex line bundle on the 2-sphere]]. This means that the function in the fundamental product theorem is surjective.
By similar means one shows that it is also injective.


## Statement

For $S^2 \subset \mathbb{R}^3$ the [[2-sphere]] with its [[Euclidean space|Euclidean]] [[subspace topology]], 
write $h$ for the [[basic line bundle on the 2-sphere]]. Its image in the [[topological K-theory]] ring $K(S^2)$ satisfies the relation

$$
  2 h = h^2 + 1
  \;\;\Leftrightarrow\;\;
  (h-1)^2 = 0 
$$

(by [this prop.](basic+complex+line+bundle+on+the+2-sphere#TensorRelationForBasicLineBundleOn2Sphere)).

Notice that $h-1$ is the image of $h$ in the [[reduced K-theory]] $\tilde K(X)$ of $S^2$ under the splitting $K(X) \simeq \tilde K(X) \oplus \mathbb{Z}$ (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)). This element 

$$
  h - 1 \in \tilde K_{\mathbb{C}}(S^2)
$$

is called the _[[Bott element]]_ of complex [[topological K-theory]].

It follows that there is a [[ring homomorphism]] of the form

$$
  \array{
    \mathbb{Z}[h]/\left( (h-1)^2 \right)
      &\overset{}{\longrightarrow}&
    K(S^2)
    \\
    h &\overset{\phantom{AAA}}{\mapsto}& h
  }
$$

from the [[polynomial ring]] in one abstract generator, [[quotient ring|quotiented]] by this relation, to the [[topological K-theory]] ring.

More generally, for $X$ a [[topological space]] this induces the composite ring homomorphism

$$
  \array{
    \Phi \colon
    &
    K(X) \otimes \mathbb{Z}[h]/((h-1)^2)
      & \longrightarrow & 
    K(X) \otimes K(S^2)
      & \overset{\boxtimes}{\longrightarrow} &
    K(X \times S^2)
    \\
    &
    (E, h)
      &\overset{\phantom{AAA} }{\mapsto}&
    (E,H)
      &\overset{\phantom{AAA}}{\mapsto}&
    (\pi_{X}^\ast E) \cdot (\pi_{S^2}^\ast H) 
  }
$$

to the topological K-theory ring of the [[product topological space]] $X \times S^2$, where the second map $\boxtimes$ is the [[external tensor product of vector bundles]]. 

+-- {: .num_prop #FundamentalProductTheorem}
###### Proposition
**(fundamental product theorem in topological K-theory)**

For $X$ a [[compact Hausdorff space]], then ring homomorphism $\Phi \colon     K(X) \otimes \mathbb{Z}[h]/((h-1)^2) \longrightarrow K(X \times S^2)$ is an [[isomorphism]].

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

For $X$ a [[compact Hausdorff space]] we have that the [[external tensor product of vector bundles]] with vector bundles on the [[2-sphere]]

$$
  \boxtimes
    \;\colon\;
  K(X) \otimes K(S^2) \overset{\simeq}{\longrightarrow} K(X \times S^2)
$$

is an [[isomorphism]] in [[topological K-theory]].

=--

## Bott periodicity

When restricted to [[reduced K-theory]] then the external product theorem (cor. \ref{ExternalProductTheorem}) yields the statement of [[Bott periodicity]] of topological K-theory:

+-- {: .num_cor #BottPeriodicity}
###### Corollary
**([[Bott periodicity]])

Let $X$ be a  [[pointed topological space|pointed]] [[compact Hausdorff space]]. 

Then there is an [[isomorphism]] of [[reduced K-theory]] 

$$
  (h-1)
    \widetilde \boxtimes
  (-)  
    \;\colon\; 
  \tilde K(X) \overset{\simeq}{\longrightarrow} \tilde K(\Sigma^2 X)
$$

from that of $X$ to that of its double [[suspension]] $\Sigma^2 X$.

=--

+-- {: .proof}
###### Proof

By [this example](topological+K-theory#ReducedKTheoryOfProductSpace)
there is for any two pointed compact Hausdorff spaces $X$ and $Y$ an [[isomorphism]]

$$
  \tilde K(Y \times X) 
    \simeq
  \tilde K(Y \wedge X)
    \oplus
  \tilde K(Y)
    \oplus 
  \tilde K(X)
$$

relating the reduced K-theory of the [[product topological space]]
with that of the [[smash product]].

Using this and the fact that for any pointed compact Hausdorff space $Z$ we have 
$K(Z) \simeq \tilde K(Z) \oplus \mathbb{Z}$ ([this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)) the isomorphism of the external product theorem (cor. \ref{ExternalProductTheorem}) 

$$
  K(S^2) \otimes K(X)  
   \underoverset{\simeq}{\boxtimes}{\longrightarrow}
  K(S^2 \times X)
$$

becomes

$$ 
  \left(
    \tilde K(S^2) \oplus \mathbb{Z}
  \right)
    \otimes
  \left(
     \tilde K(X) \oplus \mathbb{Z}
  \right)
   \;\simeq\;
  \left(
    \tilde K(S^2 \times X)
     \oplus
     \mathbb{Z}    
  \right)
   \simeq
  \left(
    \tilde K(S^2 \wedge X)
      \oplus 
    \tilde K(S^2)
      \oplus
    \tilde K(X)
      \oplus
    \mathbb{Z} 
  \right)
  \,.
$$

Multiplying out and chasing through the constructions to see that this reduces to an isomorphism on the common summand $\tilde K(S^2) \oplus \tilde K(X) \oplus \mathbb{Z}$, this yields an isomorphism of the form

$$
  \tilde K(S^2) \otimes \tilde K(X)
    \underoverset{\simeq}{\widetilde \boxtimes}{\longrightarrow}
  \tilde K(S^2 \wedge X)
    =
  \tilde K(\Sigma^2 X)
  \,,
$$

where on the right we used that [[smash product]] with the 2-sphere is the same as double [[suspension]]. 

Finally there is an [[isomorphism]]

$$
  \array{
    \mathbb{Z} 
      &\underoverset{\simeq}{ \beta }{\longrightarrow}&
    \tilde K_{\mathbb{C}}(S^2)
    \\
    1 &\overset{\phantom{AAA}}{\mapsto}& (h-1)
  }
$$

(example \ref{TopologicalKTheoryRingOfThe2Sphere}). The composite

$$
  \array{
    \tilde K_{\mathbb{C}}(X)
      &
      \simeq
    \mathbb{Z} \otimes \tilde K_{\mathbb{C}}(X)
      \overset{ \beta \otimes id }{\longrightarrow}
    \tilde K_{\mathbb{C}}(S^2) \otimes \tilde K_{\mathbb{C}}(X)
      \underoverset{\simeq}{\widetilde \boxtimes}{\longrightarrow}
      &
    \tilde K_{\mathbb{C}}(S^2 \wedge X)
      =
    \tilde K_{\mathbb{C}}(\Sigma^2 X)
    \\
    E - rk_x(E) &\overset{\phantom{AAAA}}{\mapsto}& (h-1) \widetilde \boxtimes (E - rk_x(E))
  }
$$

is the isomorphism to be established.

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


## Related concepts

* [[equivariant K-theory of projective G-space]]



## References

Review:

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 6 (from p. 19 on) in: _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))

* {#Hatcher} [[Allen Hatcher]], section 2.1 (from p. 45 on) in: _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* [[Varvara Karpova]], Section 5.2 in: _Complex Topological K-Theory_, 2009 ([pdf](http://infoscience.epfl.ch/record/162450/files/karpova.semestre.hess2.pdf), [[KarpovaTopologicalKTheory.pdf:file]])


[[!redirects external product theorem]]
[[!redirects external product theorem in topological K-theory]]

[[!redirects fundamental product theorem in K-theory]]


