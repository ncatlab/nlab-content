
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _jet group_ is the generalization of [[general linear group]] from first order to higher order [[jets]].

In terms of [[synthetic differential geometry]]/[[differential cohesion]] a [[general linear group]] is the [[automorphism group]] of a first-order [[infinitesimal disk]], while a jet group is the automorphism group of a higher order infinitesimal disk. See also at _[differential cohesion -- Frame bundles](differential+cohesive+%28infinity%2C1%29-topos#GLnTangentBundles)_.

## Properties

### Homotopy type
 {#HomotopyType}

For all $k \in \mathbb{N}$, the [[homotopy type]] of the orientation preserving jet group $GL^k_p(n)$ is that of the ordinary orientation-preserving [[general linear group]] $GL(n)$, and the canonical projection

$$
  GL^k_+(n) \longrightarrow GL_+(n)
$$

is, on the level of the underlying [[topological spaces]], a [[homotopy equivalence]], indeed it preserves the [[maximal compact subgroup]], which is the [[special orthogonal group]] $SO(n)$ on both sides (recalled e.g. in [Dartnell 94, section 1](#Dartnell94)).

### Group homology

The canonical projection $GL^k_+(n) \longrightarrow GL_+(n)$ also induces an [[isomorphism]] on  [[group homology]] with constant [[integer]] coefficients

$$
  H_\bullet^{grp}(GL^k_+(n), \mathbb{Z})
  \stackrel{\simeq}{\longrightarrow}
  H_\bullet^{grp}(GL_+(n),\mathbb{Z})
  \,.
$$

([Dartnell 94, theorem 1.1](#Dartnell94))

## Related concepts

* [[higher order frame bundle]]

* [[jet groupoid]]

## References

Original discussion (in the context of [[integrability of G-structures]]) is due to

* {#Guillemin65} [[Victor Guillemin]], section 3 of _The integrability problem for $G$-structures_, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

Textbook accounts and lecture notes include

* {#Terng78} C.L. Terng, _Natural vector bundles and natural differential operators_, Amer. J. Math. 100 (1978) 775-828.

* [[Demeter Krupka]], Josef Jany&#353;ka,  _Lectures on differential invariants_, Univerzita JEP, Brno, 1990.

* [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], section 13 of _[[Natural operators in differential geometry]]_ ([pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf))

See also

* Wikipedia, _[Jet group](https://en.wikipedia.org/wiki/Jet_group)_

* [MO discussion](http://mathoverflow.net/a/55322/381)

Discussion of the [[group cohomology|group]] [[homology]] of jet groups includes

* {#Dartnell94} [[Pablo Dartnell]], _On the homology of groups of jets_, Journal of Pure and Applied Algebra Volume 92, Issue 2, 7 March 1994, Pages 109&#8211;121 ([publisher](http://www.sciencedirect.com/science/article/pii/0022404994900175))

* Dror Farjoun, Jekel, Suciu, _Homology of jet groups_ ([pdf](http://www.northeastern.edu/suciu/papers/jets.pdf))


[[!redirects jet groups]]

[[!redirects group of jets]]
[[!redirects groups of jets]]