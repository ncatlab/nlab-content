
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In joint generalization of the [[cobordism cohomology theories]] [[MSU]] and [[MFr]] of [[closed manifold|closed]] $SU$-manifolds and of $Fr$-manifolds, respectively, an _$(SU,fr)$-manifold_ ([Conner-Floyd 66, Section 16, p. 103 onwards](#ConnerFloyd66)) is a [[compact topological space|compact]] [[manifold with boundary]] equipped with [[special unitary group]]-[[tangential structure]] on its [[stable tangent bundle]] and equipped with a [[trivial vector bundle|trivialization]] (stable [[framed manifold|framing]]) of that over the [[boundary]].

The corresponding [[bordism classes]] form a [[bordism ring]] denoted $\Omega^{SU,fr}_\bullet$.

## Properties

### Representing spectrum

In generalization to how $\Omega^{SU}_{2k}$ is represented by [[homotopy classes]] of [[maps]] into the [[Thom spectrum]] [[MSU]], so $\Omega^{SU,fr}_{2k}$ is represented by maps into the [[quotient spaces]] $MSU_{2k}/S^{2k}$ (for $S^{2k} = Th(\mathbb{C}^{k}) \to Th( \mathbb{C}^k \times_{U(k)} E U(k) ) = MU_{2k}$ the canonical inclusion):

\[
  \label{InTermsOfHomotopyGroupsOfQuotientedThomSpace}
  \Omega^{(SU,fr)}_\bullet
  \;=\;
  \pi_{\bullet + 2k}
  \big(
    MSU_{2k}/S^{2k}
  \big)
  \,,
  \;\;\;\;\;
  \text{for any}
  \;
  2k \geq \bullet + 2
  \,.
\]

([Conner-Floyd 66, p. 103](#ConnerFloyd66))

### Relation to $MSU$ and $MFr$

In every eighth degree, the [[bordism rings]] for [[MSU]], $MSUFr$ and [[MFr]] sit in a [[short exact sequence]] of the form ([Conner-Floyd 66, p. 104](#ConnerFloyd66)):


\[
  \label{ShortExactSequenceOfUFrBordismRings}
  0 
  \to
  \Omega^{SU}_{8\bullet+4}
  \overset{i}{
    \longrightarrow
  }
  \Omega^{SU,fr}_{8\bullet+4}
  \overset{\partial}{
    \longrightarrow
  }
  \Omega^{fr}_{8\bullet + 3}
  \to
  0
  \,,
\]

where $i$ is the evident inclusion, while $\partial$ is restriction to the [[boundary]].


In particular, this means that $\partial$ is [[surjective function|surjective]], hence that every $Fr$-manifold of dimension $8k + 3$ is the boundary of a $(U,fr)$-manifold.


### Relation to Todd classes and the $e_{\mathbb{R}}$-invariant

In refinement of how the complex [[e-invariant is the Todd class of cobounding (U,fr)-manifolds]] we have for [[special unitary group]]-structure instead of [[unitary group]]-structure and in dimensions $8\bullet + 4$: 

Since on $(8 \bullet + 4)$-dimensional $SU$-manifolds the [[Todd class]] is divisible by 2 [Conner-Floyd 66, Prop. 16.4](#ConnerFloyd66), we have ([Conner-Floyd 66, p. 104](#ConnerFloyd66)) the following [[short exact sequence]] of [[MSUFr]]-[[bordism rings]]:

\[
  \label{HalfToddClassesOnShortExactSequenceOfSUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^{SU}_{8\bullet+4}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{SU,fr}_{8\bullet+4}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_{8\bullet + 3}
  &
  \simeq
  &
  \pi^s_{8\bullet+3}
  \\
  & 
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e_{\mathbb{R}}}
  \\
  0 
  \to
  & 
  \mathbb{Z}
  &\overset{\;\;\;\;\;}{\hookrightarrow}&
  \mathbb{Q}  
  &\overset{\;\;\;\;}{\longrightarrow}&
  \mathbb{Q}/\mathbb{Z}
  &=&
  \mathbb{Q}/\mathbb{Z}
  }
  \,.
\]

This produces $e_{\mathbb{R}}$, the [[Adams e-invariant]] with respect to [[KO]]-theory instead of [[KU]] ([Adams 66, p. 39](e-invariant#Adams66)), which, in degrees $8k + 3$, is indeed half of the e-invariant $e_{\mathbb{C}}$ for $KU$ (by [Adams 66, Prop. 7.14](e-invariant#Adams66)). 

In fact, for $k = 0$ we have:

+-- {: .num_prop #AdamseRInvariantDetectsThirdStableHomotopyGroupOfSpheres} 
###### Proposition
**([Adams 66, Example 7.17  and p. 46](e-invariant#Adams66))**

In degree 3, the [[KO]]-theoretic [[e-invariant]] $e_{\mathbb{R}}$ takes the value $\left[\tfrac{1}{24}\right] \in \mathbb{Q}/\mathbb{Z}$ on the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$  and hence reflects the full [[third stable homotopy group of spheres]]:

$$
  \array{
    \pi^s_3 
      &
      \underoverset{
        \simeq
      }{
        e_{\mathbb{R}}
      }{
        \;\;\longrightarrow\;\;
      } 
      &
    \mathbb{Z}/24 
    & 
    \subset 
    &  
    \mathbb{Q}/\mathbb{Z}
    \\
    [h_{\mathbb{H}}]
    &&\mapsto&&
    \left[\tfrac{1}{24}\right]    
  }
$$

while $e_{\mathbb{C}}$ sees only "half" of it (by [Adams 66, Prop. 7.14](e-invariant#Adams66)).

=--

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

The concept of $(SU,fr)$-bordism theory and its relation to the [[e-invariant]] originates with:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 16 from p. 103 onwards, in: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))
