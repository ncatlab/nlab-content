

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

_Orbifold K-theory_ is [[K-theory]] (typically: [[topological K-theory]]) of [[orbifolds]], usually meant to reduce to $G$-[[equivariant K-theory]] on $G$-[[global quotient orbifolds]].

## Definition

In general it is subtle to decide whether a given [[orbifold cohomology]]-theory $E^\bullet(\mathcal{X})$ is equivalently the $G$-[[equivariant cohomology]] of a [[topological G-space]] $X$ for any realization of $\mathcal{X}$ as a [[global quotient orbifold]] of $X$ by $G$ (as highlighted by [Pronk & Scull 2007](#PronkScull07)). But for [[topological K-theory|topological]] [[equivariant K-theory]] this is the case, by [Pronk & Scull 07, Prop. 4.1](#PronkScull07).

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

This is the approach taken in [Adem & Ruan 01, Def. 3.4](#AdemRuan01).


## Related concepts

* [[equivariant K-theory]]

* [[twisted equivariant K-theory]]

* [[orbifold differential K-theory]]

* [[twisted ad-equivariant Tate K-theory]]

  * [[equivariant elliptic cohomology]]

## References

### General

The definition originates, via [[bundle gerbes]] and [[bundle gerbe modules]] on [[Lie groupoids]], in: 

* {#LupercioUribe01} [[Ernesto Lupercio]], [[Bernardo Uribe]], *Gerbes over Orbifolds and Twisted K-theory*, Comm. Math. Phys. **245** (2004) 449-489.  ([arXiv:math/0105039](http://arxiv.org/abs/math/0105039), [doi:10.1007/s00220-003-1035-x](https://doi.org/10.1007/s00220-003-1035-x))

The definition of the K-theory of [[global quotient orbifolds]] as the [[twisted equivariant K-theory]] of the [[universal covering space]] appears in

* {#AdemRuan01} [[Alejandro Adem]], [[Yongbin Ruan]]: *Twisted Orbifold K-Theory*, Commun. Math. Phys. **237** (2003) 533-556 &lbrack;[arXiv:math/0107168](https://arxiv.org/abs/math/0107168), [doi:10.1007/s00220-003-0849-x](https://doi.org/10.1007/s00220-003-0849-x)&rbrack;

Review:

* {#ALR07} [[Alejandro Adem]], [[Johann Leida]], [[Yongbin Ruan]], Section 3 of: _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) &lbrack;[doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf)&rbrack;

The general [[proof]] that this is well-defined (independent of the realization of the orbifold as a [[global quotient orbifold|global quotient]]) is due to

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], Section 4 of: _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

A more geometric model of orbifold K-theory in terms of [[bundles]] of [[Fredholm operators]] over [[Lie groupoids]]/[[differentiable stacks]]:

* {#FreedHopkinsTeleman07} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Loop groups and twisted K-theory I_, Journal of Topology, **4** 4 (2016) &lbrack;[arXiv:0711.1906](https://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019)&rbrack;

Review in:

* {#Freed12} [[Daniel Freed]], Lecture 1 of: _Lectures on twisted K-theory and orientifolds_, lecures at _[K-Theory and Quantum Fields](http://www.esi.ac.at/activities/events/2012/k-theory-and-quantum-fields)_, ESI (2012) &lbrack;[[FreedESI2012.pdf:file]]&rbrack;

* [[Joost Nuiten]], Section 3.2.2 of: _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_ MSc thesis, Utrecht (August 2013) &lbrack;[pdf](http://ncatlab.org/schreiber/files/thesisNuiten.pdf)&rbrack;

* [[Valentin Zakharevich]], Sections 2.2, 2.3 of: _K-Theoretic Computation of the Verlinde Ring_, PhD thesis (2018) &lbrack;[hdl:2152/67663](http://hdl.handle.net/2152/67663), [pdf](http://www.math.jhu.edu/~vzakharevich/research/Dissertation.pdf), [[ZakharevichKTheoryAndVerlindeRing.pdf:file]]&rbrack;


The claim that these two definitions are equivalent, in that this groupoid K-theory reduces to [[equivariant K-theory]] on [[global quotient orbifolds]], is Prop. 3.5 in [Freed, Hopkins & Teleman 2007](#FreedHopkinsTeleman07).


Another definition of K-theory of orbifolds ("full orbifold K-theory") is due to

* Tyler J. Jarvis, [[Ralph Kaufmann]], Takashi Kimura: _Stringy K-theory and the Chern character_, Invent. math. **168** (2007) 23–81 &lbrack;[arXiv:math/0502280](https://arxiv.org/abs/math/0502280), [doi:10.1007/s00222-006-0026-x](https://doi.org/10.1007/s00222-006-0026-x)&rbrack;

proven there to coincide with [Adem & Ruan 2001](#AdemRuan01) on global quotients.

More on this in:

* Rebecca Goldin, Megumi Harada, Tara S. Holm, [[Takashi Kimura]], _The full orbifold K-theory of abelian symplectic quotients_, Journal of K-theory **8** 2 (2011) 339-362 &lbrack;[arXiv:0812.4964](https://arxiv.org/abs/0812.4964), [doi:10.1017/is010005021jkt118](https://doi.org/10.1017/is010005021jkt118)&rbrack;



### Via global equivariant homotopy theory

The suggestion ([Schwede 17, Intro](orbifold+cohomology#Schwede17), [Schwede 18, p. ix-x](orbifold+cohomology#Schwede18)) that [[orbifolds]] should be regarded as [[orbispaces]] in [[global equivariant homotopy theory]] and then their [[orbifold cohomology]] be given by [[equivariant cohomology]] with [[coefficients]] in [[global equivariant spectra]] is worked out for ([[Bredon cohomology]] and) [[orbifold K-theory]] in:

* Branko Juran: _Orbifolds, Orbispaces and Global Homotopy Theory_ &lbrack;[arXiv:2006.12374](https://arxiv.org/abs/2006.12374)&rbrack;

Example 5.31 there shows that on [[global quotient orbifolds]] this is again equivalent to the previous definitions.


### Stringy product

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

* {#BecerraUribe09} [[Edward Becerra]], [[Bernardo Uribe]], _Stringy product on twisted orbifold K-theory for abelian quotients_, Trans. Amer. Math. Soc. 361 (2009), 5781-5803  ([arXiv:0706.3229](https://arxiv.org/abs/0706.3229), [doi:10.1090/S0002-9947-09-04760-6](https://doi.org/10.1090/S0002-9947-09-04760-6))

* Jianxun Hu, [[Bai-Ling Wang]], _Delocalized Chern character for stringy orbifold K-theory_, Trans. Amer. Math. Soc. 365 (2013), 6309-6341  ([arXiv:1110.0953](https://arxiv.org/abs/1110.0953), [doi:10.1090/S0002-9947-2013-05834-5](https://doi.org/10.1090/S0002-9947-2013-05834-5))


[[!redirects orbifold K-theories]]

