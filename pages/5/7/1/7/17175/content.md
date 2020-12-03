
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of [[Chern classes]] of [[complex vector bundles]], as [[universal characteristic classes]] in [[ordinary cohomology]], generalizes to any [[complex oriented cohomology|complex oriented]] [[generalized cohomology theory]]: the _Conner-Floyd Chern classes_ ([Conner-Floyd 66](#ConnerFloyd66), [Adams 74](#Adams74)), review includes ([Kochmann 96, section 4.3](#Kochmann96), [Lurie 10, lectures 4 and 5](#Lurie10)):

for $E$ a [[generalized cohomology theory]], the analog of the [[first Chern class]] in $E$-cohomology is what appears in the very definition of [[complex oriented cohomology]]. The higher generalized Chern classes are induced from this by the [[splitting principle]]. See at _[complex oriented cohomology -- the cohomology ring of BU(n)](complex+oriented+cohomology+theory#TheCohomologyRingOfBUn)_.

The generalized Chern classes serve as the generalized [[Thom classes]] that make every [[complex vector bundle]] have [[orientation in generalized cohomology]] with respect to any [[complex oriented cohomology theory]] ([Lurie 10, lecture 5, prop. 6](#Lurie10)).

## Properties

### Existence

+-- {: .num_prop #ConnerFloyedClasses}
###### Proposition

Given a [[complex oriented cohomology theory]] $E$ with complex orientation $c_1^E$, then the $E$-[[generalized cohomology]] of the [[classifying space]] $B U(n)$ is freely generated over the [[graded commutative ring]] $\pi_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) by classes $c_k^E$ for $0 \leq k \leq n$ of degree $2k$, these are called the **[[Conner-Floyd-Chern classes]]**

$$
  E^\bullet(B U(n))
    \;\simeq\;
  \pi_\bullet(E)[ [ c_1^E, c_2^E, \cdots, c_n^E ] ]
  \,.
$$

Moreover, pullback along the canonical inclusion $B U(n) \to B U(n+1)$ is the [[identity]] on $c_k^E$ for $k \leq n$ and sends $c_{n+1}^E$ to zero.

For $E = $ [[HA|HZ]] this reduces to the standard [[Chern classes]].

=--

for details see ([Pedrotti 16, prop. 3.1.14](#Pedrotti16))



## References

The concept for [[MU]]-theory was introduced in

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

An early account in a broader context of [[complex oriented cohomology theory]]:

* {#Adams74} [[Frank Adams]], part I.4, part II.2, part III.10 of _[[Stable homotopy and generalised homology]]_, 1974

More recent textbook and lecture notes include

* {#Kochmann96} [[Stanley Kochmann]], section 4.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010, lecture 4 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf)) and lecture 5 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))

Some more details are spelled out in 

* {#Pedrotti16} [[Riccardo Pedrotti]], _Complex oriented cohomology, generalized orientation and Thom isomorphism_, 2016, 2018 ([[PedrotticECohomology2018.pdf:file]])



[[!redirects Conner-Floyd Chern classes]]

[[!redirects Conner-Floyd class]]
[[!redirects Conner-Floyd classes]]


[[!redirects Conner-Floyd-Chern class]]
[[!redirects Conner-Floyd-Chern classes]]


[[!redirects generalized Chern class]]
[[!redirects generalized Chern classes]]

[[!redirects generalised Chern class]]
[[!redirects generalised Chern classes]]