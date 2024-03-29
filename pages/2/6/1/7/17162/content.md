[[!redirects homology of MU]]

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

The ([[generalized homology|generalised]]) [[homology]] of [[Thom spectra]] $M G$, such as [[MO]] and [[MU]].

In the presence of a [[Thom isomorphism]] (e.g. for [[complex oriented cohomology]] of [[MU]]) this identifies with the homology of the [[classifying spaces]] $B G$, such as [[BO|$B O$]] and [[BU|$B U$]].

Feeding the homology of $M G$ into an [[Adams spectral sequence]] gives a way to compute its [[homotopy groups]].

This is for instance a key ingredient in [[Quillen's theorem on MU]] giving the [[homotopy groups of a spectrum|homotopy groups]] of $MU$.

## Statement

+-- {: .num_prop}
###### Proposition

For $E$ a [[complex oriented cohomology theory]], there is an [[isomorphism]] of [[graded rings]]

$$
  E_\bullet(M U) \simeq (\pi_\bullet E)[b_1, b_2, \cdots]
  \,,
$$

where the $\{b_i \in E_\bullet(M U(1))\}$ are a [[dual basis]] to the basis $\{t^{i+1} \in E^\bullet(M U) \simeq t (\pi_\bullet E)[ [ t ] ]\}$ that is induced by the [[complex oriented cohomology theory|complex orientation]].

=--

([Lurie 10, lecture 7, prop. 2](#Lurie10))

## Related concepts

* [[Boardman homomorphism]]

* [[homology of MO]]

## References

* [[Frank Adams]], part II.6 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Kochmann96} [[Stanley Kochmann]], section 2.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], lecture 7 of _[[Chromatic Homotopy Theory]]_, 2010, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf))


