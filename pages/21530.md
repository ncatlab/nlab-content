

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Orbifold K-theory_ is [[K-theory]] (typically: [[topological K-theory]]) of [[orbifolds]].

## Definition

In general it is subtle to decide whether a given [[orbifold cohomology]]-theory $E^\bullet(\mathcal{X})$ is equivalently the $G$-[[equivariant cohomology]] of a [[topological G-space]] $X$ for any realization of $\mathcal{X}$ as a [[global quotient orbifold]] of $X$ by $G$ (as highlighted in[Pronk-Scull 07](#PronkScull07)). But for [[topological K-theory|topological]] [[equivariant K-theory]] this is the case, by [Pronk-Scull 07, Prop. 4.1](#PronkScull07).

Therefore it makes sense to _define_ the K-theory of an [[orbifold]] $\mathcal{X}$ which is equivalent to a [[global quotient orbifold]] 

$$
  \mathcal{X} \simeq \prec(X \!\sslash\! G)
$$

to be the $G$-[[equivariant K-theory]] of $X$:

$$
  K^\bullet(\mathcal{X})
  \;\coloneqq\;
  K_G^\bullet(X)
  \,.
$$

This is the approach taken in [AdemRuan 01, Def. 3.4](#AdemRuan01)

## References

The definition of the K-theory of [[global quotient orbifolds]] as the [[equivariant K-theory]] of the universal covering space appears in

* {#AdemRuan01} [[Alejandro Adem]], [[Yongbin Ruan]], _Twisted Orbifold K-Theory_, Commun. Math. Phys. 237 (2003) 533-556 ([arXiv:math/0107168](https://arxiv.org/abs/math/0107168))

Review in

* {#ALR07} [[Alejandro Adem]], [[Johann Leida]], [[Yongbin Ruan]], Section 3 of: _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

The general [[proof]] that this is well-defined (independent of the realization of the orbifold as a [[global quotient orbifold|global quotient]]) is due to

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], Section 4 of: _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

A more geometric model of orbifold K-theory in terms of [[bundles]] of [[Fredholm operators]] over [[Lie groupoids]]/[[differentiable stacks]]:

* {#FreedHopkinsTeleman07} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Loop groups and twisted K-theory I_, Journal of Topology, Volume4, Issue 4 ([arXiv:0711.1906](https://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019))

Review in:

* {#Freed12} [[Daniel Freed]], Lecture 1 of: _Lectures on twisted K-theory and orientifolds_, lecures at _[K-Theory and Quantum Fields](http://www.esi.ac.at/activities/events/2012/k-theory-and-quantum-fields)_, ESI 2012 ([[FreedESI2012.pdf:file]])

* [[Joost Nuiten]], Section 3.2.2 of: _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_ MSc thesis, Utrecht, August 2013 ([pdf](http://ncatlab.org/schreiber/files/thesisNuiten.pdf))

The claim that these two definitions are equivalent, in that this groupoid K-theory reduces to [[equivariant K-theory]] on [[global quotient orbifolds]], is [Freed-Hopkins-Teleman 07, Prop. 3.5](#FreedHopkinsTeleman07).

The suggestion ([Schwede 17, Intro](orbifold+cohomology#Schwede17), [Schwede 18, p. ix-x](orbifold+cohomology#Schwede18)) that [[orbifolds]] should be regarded as [[orbispaces]] in [[global equivariant homotopy theory]] and then their [[orbifold cohomology]] be given by [[equivariant cohomology]] with [[coefficients]] in [[global equivariant spectra]] is worked out for ([[Bredon cohomology]] and) [[orbifold K-theory]] in:

* Branko Juran, _Orbifolds, Orbispaces and Global Homotopy Theory_ ([arXiv:2006.12374](https://arxiv.org/abs/2006.12374))

Example 5.31 there shows that on [[global quotient orbifolds]] this is again equivalent to the previous definitions.

