
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _diffeomorphism group_ $Diff(X)$ of a [[smooth manifold]] $X$ is the [[group]] of its [[diffeomorphism]]s: the [[automorphism group]] of $X$ as an [[object]] of the [[category]] [[SmoothMfd]].

## Examples

### Of the 3-sphere

+-- {: .num_theorem #SmaleConjecture}
###### Theorem

The diffemorphism group of the 3-sphere is [[homotopy equivalence|homotopy equivalent]] to the [[orthogonal group]] $O(4)$, the equivalence being exhibited by the canonical inclusion

$$
  O(4) \hookrightarrow Diff(S^3)
  \,.
$$

=--

After being conjectured by Smale, this was proven in ([Hatcher 1983](#Hatcher)).

### Of general 3-manifolds

+-- {: .num_theorem}
###### Theorem

For every [[smooth manifold]] $X$ of [[dimension]] 3 the canonical map

$$
  Diff(X) \to Homeo(X)
$$

sending [[diffeomorphisms]] to their underlying [[homeomorphisms]] of [[topological spaces]] is a [[weak homotopy equivalence]]. 

=--

That this follows from the Smale cojecture, theorem \ref{SmaleConjecture}, was shown in [Cerf](#Cerf). For discussion see [Hatcher, 1978](#Hatcher78).


## References

### For 3-manifolds

* J. Cerf, _Sur les diff&#233;omorphismes de la sph&#232;re de dimension trois ($\Gamma_4 = 0$)_, Lecture Notes in Math., vol. 53, Springer-Verlag, Berlin and New York, 1968_
 {#Cerf}

* [[Allen Hatcher]], _Linearization in 3-dimensional topology_, Proceedings of the international congress of Mathematicians, Helsinki (1978)
 {#Hatcher78}

* [[Allen Hatcher]], _A proof of the Smale conjecture, $Diff(S^3) \simeq O(4)$, Annals of Mathematics 117 (1983) ([jstor](http://www.jstor.org/pss/2007035))
 {#Hatcher}

[[!redirects diffeomorphism groups]]
[[!redirects Smale conjecture]]
