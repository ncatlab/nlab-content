
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Geometric quantization
+-- {: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _polarization_ on an [[algebraic variety]] is a choice of [[line bundle]] on it whose [[Chern class]] is analogous to the class represented by a [[Kähler form]] in [[complex analytic geometry]].

In other words, the concept of polarized algebraic variety is the generalization of that of _[[Kähler polarization]]_ from [[symplectic geometry]]/[[complex geometry]] to more general [[algebraic geometry]]. In fact it is the generalization of the concept of a [[holomorphic line bundle|holomorphic]] [[prequantum line bundle]] compatible with a [[Kähler polarization]]. 

(Notice however the reversion of the logic: in [[symplectic geometry]] the symplectic form is given and then a [[complex structure]] is chosen to match it, whereas here in [[algebraic geometry]] the analog of the complex structure exists beforehand, given by the algebraic structure, and now a polarization conversely asks for the analog of a compatible symplectic form (and for its [[prequantization]])).

Therefore a polarized variety together with a choice of [[Theta characteristic]] on it is the algebraic geometry version of a polarized [[phase space]] with [[metaplectic correction]]. See at _[[geometric quantization]]_ for more on this.

## Definition

A _polarization_ of an [[algebraic variety]] $X$ over an [[algebraically closed field]] $k$ is a choice of [[ample sheaf|ample]] element in its [[Néron-Severi group]] $Pic_X/Pic_X^0$. In other words, a polarization is the choice of an [[equivalence class]] of an [[ample sheaf|ample]] algebraic [[line bundle]] over $X$ (e.g. [[holomorphic line bundles]] if $k$ is the [[complex numbers]]) where two such are regarded as equivalent if they differ by tensoring with one whose underlying topological [[Chern class]] is trivial.

The polarization is called _principal_ if it is of [[degree of a coherent sheaf|degree]] 1.

## Examples

### Jacobians and higher Jacobians

The [[Jacobian variety]] of an algebraic variety is principally polarized by the [[theta divisor]].

See also [this MO discussion](http://mathoverflow.net/q/95288/381).

More generally the higher [[intermediate Jacobians]] with their Weil complex structure are polarized. On the other hand, when equipped with the  Griffith complex structure they carry a [[p-convex polarization]] which is [[symplectomorphism|symplectomorphic]] but not [[biholomorphism|biholomorphic]] to the Weil polarization.

## Related concepts

* [[p-convex polarization]]

* [[Prym-Tyurin variety]]

## References

* {#Voisin02} [[Claire Voisin]], section 7 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3


* [[eom]], _[Polarized algebraic variety](http://www.encyclopediaofmath.org/index.php/Polarized_algebraic_variety)_

* Jeroen Sijsling, _What is... a polarization?_ [pdf](http://pub.math.leidenuniv.nl/~strengtc/cm/polariz.pdf)

Polarization specifically of [[Jacobian varieties]] is discussed for instance in 

* {#Polsihchuk03} [[Alexander Polishchuk]], section 17 of _Abelian varieties, Theta functions and the Fourier transform_, Cambridge University Press (2003) ([pdf](http://math1.unice.fr/~beauvill/pubs/poli.pdf))


[[!redirects polarized algebraic varieties]]

[[!redirects polarized variety]]
[[!redirects polarized varieties]]

[[!redirects principally polarized algebraic variety]]
[[!redirects principally polarized algebraic varieties]]
[[!redirects principally polarized variety]]
[[!redirects principally polarized varieties]]