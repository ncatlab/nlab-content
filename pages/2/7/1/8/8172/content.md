
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

The _Adams spectral sequence_ is a type of [[spectral sequences]] used for computations  in [[stable homotopy theory]]. It is a variant of the [[Serre spectral sequence]] obtained by restricting attention to the stable range of [[cohomology]] with [[coefficients]] in $\mathbb{Z}/p\mathbb{Z}$.

The Adams spectral sequence is further refined by the _[[Adams-Novikov spectral sequence]]_ by replacing [[ordinary cohomology]] modulo $p$ by [[complex cobordism cohomology theory]].

## Definition

### Traditional

Given a [[connective spectrum]] $X$ such that $H^\bullet(X)$
has finite type, then for each [[prime number]] $p$ there exists a [[spectral sequence]] which converges to the [[homotopy groups]] of $X$ modulo $p$ $\pi_ast(X) \otimes \mathbb{Z}_p$ and whose $E^2$-page is

$$
  E_2^{s,t} \simeq  Ext_A^{s,t}(H^\bullet(X), \mathbb{Z}/(p) )
$$

where $A$ is the [[Steenrod algebra]]. 

This is due to ([Adams 58](#Adams58)). A review is around ([Ravenel, theorem, 2.1.1](#Ravenel)).

### Via cosimplicial spectra 

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

## Properties

### Relation to Steenrod algebra

The $E_2$-page of the Adams spectral sequence for the $p$-component of 
$\pi_{n+k}(S^n)$  is the [[Steenrod algebra]] (for given prime $p$).

## Related concepts

* [[Adams-Novikov spectral sequence]]

* [[Steenrod algebra]]

## References

The original article is

* [[John Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958),
180&#8211;214.
 {#Adams58}


Reviews are in

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, page 8 of chapter I _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf)) and section 1 of chapter 2
 {#Ravenel}


* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* Nerses Aramian, _The Adams spectral sequence_ ([pdf](http://www.math.uiuc.edu/~bertg/Aramian_ASS.pdf))

* [[Alexander Kupers]], _An introduction to the Adams spectral sequence_ ([pdf](http://math.stanford.edu/~kupers/adamsss.pdf))

* R. Bruner, _An Adams spectral sequence primer_ ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* [[Jacob Lurie]], _The Adams Spectral Sequence_, 2010 ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  {#Lurie10}

* [[Jacob Lurie]], _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

[[!redirects Adams spectral sequences]]