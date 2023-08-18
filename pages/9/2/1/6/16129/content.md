
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

is, on the level of the underlying [[topological spaces]], a [[homotopy equivalence]], indeed it preserves the [[maximal compact subgroup]], which is the [[special orthogonal group]] $SO(n)$ on both sides 

(see [Kolář, Michor & Slovák 1993, §13.1 & Prop. on p. 131](#KolářMichorSlovák93); [Dartnell 1994, section 1](#Dartnell94), also [Grasseau 2006, pp. 14](#Grasseau06)).



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

Original discussion in the context of [[integrability of G-structures]]

* {#Guillemin65} [[Victor Guillemin]], section 3 of: *The integrability problem for $G$-structures*, Trans. Amer. Math. Soc. **116** (1965), 544-560 &lbrack;[jstor:1994134](http://www.jstor.org/stable/1994134)&rbrack;

and in the context of [[natural vector bundles]]:

* {#Terng78} [[Chuu-Lian Terng]], p. 779 of: *Natural vector bundles and natural differential operators*, Amer. J. Math. **100** (1978) 775-828 &lbrack;[doi:10.2307/2373910](https://doi.org/10.2307/2373910), [jstor:2373910](https://www.jstor.org/stable/2373910)&rbrack;

Textbook accounts and lecture notes:

* [[Demeter Krupka]], [[Josef Janyška]], §2.2 in: _Lectures on differential invariants_, Univerzita J. E. Purkyně, Brno (1990) &lbrack;ISBN:80-210-165-8, [researchgate](https://www.researchgate.net/publication/36792711_Lectures_on_Differential_Invariants)&rbrack;

  > (there jet groups are called "differential groups")

* {#KolářMichorSlovák93} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], section 13 of: *[[Natural operators in differential geometry]]*, Springer (1993)  &lbrack;[doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [book webpage](https://www.emis.de/monographs/KSM/), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;

See also

* Wikipedia, _[Jet group](https://en.wikipedia.org/wiki/Jet_group)_

* [MO discussion](http://mathoverflow.net/a/55322/381)

Discussion of the [[group cohomology|group]] [[homology]] of jet groups:

* {#Dartnell94} [[Pablo Dartnell]], *On the homology of groups of jets*, Journal of Pure and Applied Algebra **92** 2 (1994) 109-121 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90017-5">doi:10.1016/0022-4049(94)90017-5</a>&rbrack;

* [[Emmanuel Dror Farjoun]], Jekel, Suciu, _Homology of jet groups_ ([pdf](http://www.northeastern.edu/suciu/papers/jets.pdf))

Discussion of jet-[[frame bundles]] and their [[Cartan geometry]]:

* {#Grasseau06} Michael Grasseau, *Jets, frames, and their Cartan geometry* &lbrack;[arXiv:math-ph/0603063](https://arxiv.org/abs/math-ph/0603063), [hal:00021276](https://hal.science/hal-00021276)&rbrack;






[[!redirects jet groups]]

[[!redirects group of jets]]
[[!redirects groups of jets]]