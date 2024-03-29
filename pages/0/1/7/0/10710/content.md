[[!redirects phantom maps]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

## Definition

In [[stable homotopy theory]]/[[cohomology theory]] a [[homomorphism]] of [[spectra]] $E \longrightarrow F$ is called a _phantom map_ if it induces (up to [[homotopy]]) the [[zero morphism]] on [[generalized homology theories]]
$E_\bullet \longrightarrow F_\bullet$, hence if for every [[topological space]]/[[homotopy type]] $X$ the induced map of [[homology groups]]

$$
  E_\bullet(X) \longrightarrow F_\bullet(X)
$$

is the [[zero morphism]].

The existence of phantom maps implies that despite the [[Brown representability theorem]], there is a subtle difference between generalized (Eilenberg-Steenrod) homology theories and the [[spectra]] which represent them: the latter contain in general more information. (Note that this issue is not present when working with cohomology theories instead of homology theories).

In even more classical context, a continuous map $f$ from a [[CW-complex]] $X$ to a topological space $Y$ is a phantom map if it is not homotopic to a constant but for every finite CW-subcomplex $Z\subset X$ the restriction $f|_Z:Z\to Y$ is homotopic to a constant.

## Properties

### Between Landweber-exact spectra

Between [[Landweber exact spectra]], every phantom map is already null-homotopic. (e.g. [Lurie, 10, corollary 7](#Lurie)).

## References

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 17 _Phantom maps_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture17.pdf)) 
 {#Lurie}

[[!redirects phantom morphism]]
[[!redirects phantom morphisms]]

[[!redirects phantom homomorphism]]
[[!redirects phantom homomorphisms]]