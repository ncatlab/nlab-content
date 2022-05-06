
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given a [[group]] $G$ and two [[subgroups]] $H$ and $K$, then the set of **double cosets**, $H \backslash G/K$, is composed of [[equivalence classes]] of elements of $G$, where two elements are regarded as equivalent if they differ by left multiplication with an element in $H$ and right multiplication with an element of $K$.

This construction generalises to [[topological groups]] and [[Lie groups]], where it is called a **double coset space**. The double coset space for $G$ a [[compact Lie group]] and $H$ and $K$ [[closed subspace|closed]] [[connected topological space|connected]] [[subgroups]], with $H$ [[action|acting]] [[free action|freely]] on the singe [[coset space]] $G/K$, is also known as a _[[biquotient space]]_.

From the [[nPOV]], a weak form of the double coset construction is often more natural, $H \backslash \backslash G//K$, and can be defined as the [[homotopy pullback]] of maps of [[looping and delooping|delooped]] groups, $\mathbf{B} H \to \mathbf{B} G$ and $\mathbf{B} K \to \mathbf{B} G$. This holds more generally for any three [[∞-groups]], with any homomorphisms $H \to G$ and $K \to G$.

## Properties

### Mackey's formula
 {#MackeyFormula}

> the following needs to state the assumpotion on the kind of group, e.g. [[finite group]], [[compact Lie groups]], ...

Double coset decompositions are useful in [[representation theory]], for example in [[George Mackey]]'s formula for the [[restricted representation|restriction]] back to $H$ of a module [[induced representation|induced]] from $K$. Let $W$ be a [[linear representation]] of $K$. Then

$$
  Res^G_H Ind^G_K W 
   \cong 
  \underset{[g] \in H \backslash G/K} \bigoplus Ind^H_{K_g} W_g
  \,,
$$

where $K_g \coloneqq H \intersection g K g^{-1}$, and $W_g$ is the representation of $K_g$ which is $W$ as a vector space, but with action $x \cdot w = (g^{-1} x g) w$ where now $g^{-1} x g \in K$. This formula, sometimes called _Mackey's decomposition theorem_, amounts to the [[Beck-Chevalley condition]] for the homotopy pullback square. It appears, as the _Mackey axiom_, in one of the original definitions of [[Mackey functor]] ([Bouc 02](#Bouc02)).

## Examples

### Gromoll-Meyer sphere

The [[Gromoll-Meyer sphere]] -- an [[exotic 7-sphere]] -- arises as the [[biquotient]] of [[Sp(2)]] by two copies of [[Sp(1)]].

## Related concepts

* [[biquotient space]]

* [[Clifford-Klein form]]

* [[locally Klein geometry]]

* [[Hecke algebra]]

* [[Bruhat decomposition]]

##References

* {#Bouc02} Serge Bouc, _Mackey functors_, ([pdf](http://www.lamfa.u-picardie.fr/bouc/mackey.pdf))

* Burt Totaro, _Cheeger manifolds and the classification of biquotients_ ([arXiv:math/0210247](https://arxiv.org/abs/math/0210247))

[[!redirects double cosets]]

[[!redirects double coset space]]
[[!redirects double coset spaces]]
