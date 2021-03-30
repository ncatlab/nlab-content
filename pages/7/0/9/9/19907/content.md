


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Statement 

The [[little n-disk operad]] is [[formal dg-algebra|formal]] in the sense that for each of its component [[topological spaces]] there is a [[zig-zag]] of [[quasi-isomorphisms]] between their [[de Rham cohomology]] and their [[de Rham complex]], and such that these morphisms are compatible with the induced [[cooperad]]-[[structure]] on both sides.

Concretely, the [[zig-zags]] may be taken to consist of one [[span]] of [[quasi-isomorphisms]] out of a suitable [[graph complex]] to the [[de Rham cohomology]]/[[de Rham complex]] of the [[Fulton-MacPherson operad]], which in turn is [[weak equivalence|weakly equivalent]] to the [[little n-disk operad]] ([this Prop.](Fulton-MacPherson+operad#WeakEquivalenceToLittleNDiskOperad)).

Here the morphism from the [[graph complex]] to the [[de Rham complex]] of the [[Fulton-MacPherson operad]] regards the latter as the [[compactification]] of a [[configuration space of points]], regards [[functions]]/[[differential forms]] on [[configuration spaces of points]] as [[n-point functions]] of a [[topological quantum field theory|topological]] [[quantum field theory]], regards suitable [[graphs]] as [[Feynman diagrams]] and proceeds by sending each such graph/Feynman diagram to a corresponding [[Feynman amplitude]].

This idea of a proof was sketched in [Kontsevich 99](#Kontsevich99), a full account is due to [Lambrechts-Volic 14](#LambrechtsVolic14).


## Related concepts

* [[Kontsevich formality]]


## References

The special case of formality of $E_2$ (see also _[[Kontsevich formality]]_) was finally proven in

* [[Dmitry Tamarkin]], _Another proof of M. Kontsevich formality theorem_ ([arXiv:math/9803025](https://arxiv.org/abs/math/9803025))

* [[Dmitry Tamarkin]], _Formality of Chain Operad of Small Squares_

See [Kontsevich 99, p. 15](#Kontsevich99) for the history of this result.

A general proof of formality of $E_n$ for all $n$ was sketched in

* {#Kontsevich99} [[Maxim Kontsevich]], section 3, around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

and fully spelled out in

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society ; no. 1079, 2014  ([arXiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

Further discussion of the graph complex as a model for the [[de Rham cohomology]] of  [[configuration spaces of points]] is in

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))

* [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))

* [[Ricardo Campos]], Julien Ducoulombier, Najib Idrissi, [[Thomas Willwacher]], _A model for framed configuration spaces of points_ ([arXiv:1807.08319](https://arxiv.org/abs/1807.08319))

The following paper constructs a canonical chain of formality quasiisomorphisms for the operad of chains on framed little disks and the operad of chains on little disks. The construction is done in terms of logarithmic algebraic geometry and is
remarkable for being rational (and indeed definable integrally) in de Rham
cohomology:

* [[Dmitry Vaintrob]], _Formality of little disks and algebraic geometry_, [arXiv:2103.15054](https://arxiv.org/abs/2103.15054).

[[!redirects formality of the little n-disk operad]]

[[!redirects the Fulton-MacPherson operad is formal]]
[[!redirects formality of the Fulton-MacPherson operad]]