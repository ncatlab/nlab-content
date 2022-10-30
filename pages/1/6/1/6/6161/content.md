
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _K&#252;nneth theorem_ is a statement relating the [[homology]] or [[cohomology]] of two objects $X$ and $Y$ with that of their [[product]] $X \times Y$. 

In good situations it identifies the (co)homology of a product with the tesor product of the (co)homologies: $H^\bullet(X \times Y, E) \simeq H^\bullet(X,E) \otimes H^\bullet(Y,E)$. But in general this simple relation receives corrections by [[Tor]]-groups.

## In ordinary cohomology

(..)

## In Generalised Cohomology Theories ##

The K&#252;nneth theorem for [[generalised cohomology theories]] is a special case of the [[universal coefficient theorem]].  Let $E$ be a [[ring spectrum]], $X$ and $Y$ two [[spectra]].  Then we define a new [[cohomology theory]] as the $E$-[[module spectrum]] $G \coloneqq F(Y, E)$ where $F(-,-)$ is the [[function spectrum]] (that is, the [[internal hom]] in the category of [[spectra]]).  The ([[reduced cohomology|reduced]]) cohomology of $X$ in this cohomology theory is thus given by:

$$
G^*(X) = [X,F(Y,E)] = [X \wedge Y,E] = E^*(X \wedge Y)
$$

A [[universal coefficient theorem]] gives a way of computing $G^*(X)$ from knowledge of $E^*(X)$ and $G^*(pt)$.  In this case, $G^*(pt) = E^*(Y)$ so our initial data is $E^*(X)$ and $E^*(Y)$.

For more details, see the page on the _[[universal coefficient theorem]]_.

## References

### In ordinary (co)homology

* Rob Thompson, _Products and the K&#252;nneth theorem_ ([pdf](http://math.hunter.cuny.edu/~rthompso/topology_notes/chapter%20nine.pdf))

Section [3.B](http://www.math.cornell.edu/~hatcher/AT/ATch3.4.pdf) of 

* [[Alan Hatcher]], _[Algebraic topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_


### In generalized (co)homology

See the corresponding references at _[[universal coefficient theorem]]_,


[[!redirects Künneth formula]]

[[!redirects Kuenneth theorem]]
[[!redirects Kuenneth formula]]
[[!redirects Kunneth theorem]]
[[!redirects Kunneth formula]]
[[!redirects Künneth isomorphism]]

[[!redirects Künneth theorem for complexes]]
