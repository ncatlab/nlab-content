
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

To the extent that one may think of $\mathcal{C}$ as analogous to a [[category of chain complexes]], the dg-nerve may be thought of producing the [[simplicial set]] whose $k$-[[simplices]] are the [[local systems]] on $\Delta^k$ with [[coefficients]] in $\mathcal{C}$ ([[flat ∞-connections]] with coefficients in $\mathcal{C}$). The formula is just as for [[Lie integration]] of [[L-infinity algebroids]]. 

## References

The definition originates with:

* {#BlockSmith14} [[Jonathan Block]], [[Aaron M. Smith]], Def. 2.3 (2.4 in the preprint) of: *The higher Riemann--Hilbert correspondence*, Advances in Mathematics **252** (2014) 382-405 &lbrack;[arXiv:0908.2843](https://arxiv.org/abs/0908.2843), [doi:10.1016/j.aim.2013.11.001](https://doi.org/10.1016/j.aim.2013.11.001)&rbrack;
 
* [[Jacob Lurie]], Construction 1.3.1.6 in: *[[Higher Algebra]]*

Extension to [[A-infinity categories|$A_\infty$-categories]], proof that the dg-nerve maps [[pretriangulated dg-categories]] to [[stable (∞,1)-categories]].

* {#Faonte13} [[Giovanni Faonte]], _Simplicial nerve of an A-infinity category_, [arXiv:1312.2127](http://arxiv.org/abs/1312.2127).

[[!redirects dg-nerves]]
[[!redirects nerve of a dg-category]]
[[!redirects nerves of dg-categories]]
