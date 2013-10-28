
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A class of [[spectral sequences]] in [[stable homotopy theory]].

## Definition

Let $p$ be a [[prime number]]. Write

$$
  R \coloneqq H \mathbb{F}_p
$$

for the [[Eilenberg-MacLane spectrum]] of the [[field]] $\mathbb{F}_p$. The [[A-infinity algebra]] structure on this induced an [[augmentation|augmented]] [[cosimplicial object|cosimplicial]] [[spectrum]]

$$
  \overline{R}^\bullet \;\colon\; k \mapsto R^{\otimes k}
  \,.
$$

Write $R^\bullet$ for the underlying [[cosimplicial object]] (here and in the following the overline indicates [[augmentation]]).

For $X$ any other [[spectrum]], [[tensor product|tensoring]] induces the (augmented) cosimplicial spectrum

$$
  \overline{X}^\bullet \coloneqq X \otimes \overline{R}^\bullet
  \,.
$$

Now the [[augmentation]] morphism induces a canonical map from $\overline{X}^{-1}$ into the [[totalization]] of $X^\bullet$

$$
  \overline{X}^{-1} \longrightarrow Tot X^\bullet
  \,.
$$

The Adams spectral sequence computes the [[kernels]] of the morphisms on [[homotopy groups]] of this map. ([Lurie 10, theorem 2](#Lurie10))

## Related concepts

* [[Steenrod algebra]]

## References

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* [[Jacob Lurie]], _The Adams Spectral Sequence_, 2010 ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  {#Lurie10}

* [[Jacob Lurie]], _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

[[!redirects Adams spectral sequences]]