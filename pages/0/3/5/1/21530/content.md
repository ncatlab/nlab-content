

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


The general [[proof]] that this is well-defined is due to

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], Section 4 of: _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

