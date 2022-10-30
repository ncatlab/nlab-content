
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Any pretriangulated [[dg-category]] $\mathcal{C}$ presents a [[stable (infinity,1)-category]]. A plain dg-category only presents a spectrally enriched (infinity,1)-category. One way to construct this is to apply the [[Dold-Kan correspondence]] on each [[hom-object]] to produce a fibrant [[sSet-enriched category]] and then, if desired, form the [[homotopy coherent nerve]] of that to obtain a [[quasi-category]]. 

On the other hand, the _dg-nerve_ of $\mathcal{C}$ is a more direct construction that directly sends the dg-category to a [[simplicial set]] which is the [[quasi-category]] incarnation of the corresponding [[stable (∞,1)-category]].

To the extent that one may think of $\mathcal{C}$ as analogous to a [[category of chain complexes]], the dg-nerve may be thought of producing the [[simplicial set]] whose $k$-[[simplices]] are the [[local systems]] on $\Delta^k$ with [[coefficients]] in $\mathcal{C}$ ([[flat ∞-connections]] with coefficients in $\mathcal{C}$).

## References

Definition 2.2 in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_ ([arXiv:0908.2843](http://arxiv.org/abs/0908.2843))

Construction 1.3.1.6 in 

* [[Jacob Lurie]], _[[Higher Algebra]]_

In the following paper, the definition of the dg-nerve is extended to [[A-infinity categories]], and it is proved that the dg-nerve maps [[pretriangulated dg-categories]] to [[stable (∞,1)-categories]].

* Giovanni Faonte, _Simplicial nerve of an A-infinity category_, [arXiv:1312.2127](http://arxiv.org/abs/1312.2127v1).

[[!redirects dg-nerves]]
[[!redirects nerve of a dg-category]]
[[!redirects nerves of dg-categories]]
