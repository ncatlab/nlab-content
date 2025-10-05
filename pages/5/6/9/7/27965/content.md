


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


For $\mathfrak{g}$ a [[Lie algebra]], its [[automorphism group]] $Aut(\mathfrak{g}) \subset GL(\mathfrak{g})$ (in the [[category]] [[LieAlg]]) is the [[subgroup]] of the [[general linear group]] of invertible [[linear maps]] $\alpha \colon \mathfrak{g} \xrightarrow{\sim} \mathfrak{g}$  which preserve the [[Lie bracket]], in that for $\alpha \in Aut(\mathfrak{g})$ and $x,y\in \mathfrak{g}$ we have

$$
  \alpha\big(
    [x,y]
  \big) 
  = 
  \big[
    \alpha(x), \alpha(y)
  \big]
  \,.
$$

The group operation is the [[composition]] of linear maps.

This group canonically carries the [[structure]] of a [[Lie group]]. The corresponding [[Lie algebra]] is the *[[derivation Lie algebra]]* of $\mathfrak{g}$.


## Properties

There is a [[normal subgroup]] $Aut(\mathfrak{g})_0$ of automorphisms, the _[[inner automorphisms]]_, obtained via the [[adjoint action]] as

$$
  exp\big(ad(x)\big) 
    \colon 
  \mathfrak{g} \longrightarrow \mathfrak{g}
  \,,
$$

for $x\in \mathfrak{g}$, giving rise to the [[exact sequence]]

$$
  1 
    \to 
  Aut(\mathfrak{g})_0 
    \longrightarrow 
  Aut(\mathfrak{g}) 
    \longrightarrow 
  \pi_0\big( Aut(\mathfrak{g}) \big) 
    \to 
  1
  \mathrlap{\,.}
$$

The [[quotient group]] $\pi_0\big(Aut(\mathfrak{g})\big)$ of _[[outer automorphisms]]_ is [[discrete group|discrete]].

This sequence is known to be a [[group extension|split extension]] for $\mathfrak{g}$ a [[simple algebra|simple]] Lie algebra of finite dimension over the [[real number|reals]] or over the [[complex number|complex numbers]] ([Gündogan 2010](#Gund10)).


## References

* {#Gund10} Hasan Gündogan: *The component group of the automorphism group of a simple Lie algebra and the splitting of the corresponding short exact sequence*, J. Lie Theory **20** 4 (2010) 709-737 &lbrack;[jlt:20035](https://www.heldermann.de/JLT/JLT20/JLT204/jlt20035.htm), [pdf](https://www.heldermann-verlag.de/jlt/jlt20/guendola2e.pdf)&rbrack;


## Related concepts

* [[endomorphism Lie algebra]]

* [[automorphism Lie algebra]]

* [[automorphism of a vertex operator algebra]]

* [[automorphism infinity-Lie algebra]]

[[!redirects automorphism groups of Lie algebras]]


