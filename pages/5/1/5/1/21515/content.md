
### Traditional orbifold cohomology

Traditionally, the [[cohomology]] of [[orbifolds]]  has, by and large, been taken to be simply the [[ordinary cohomology]] of (the plain [[homotopy type]] of) the [[geometric realization of simplicial topological spaces|geometric realization]] of the [[topological groupoid|topological]]/[[Lie groupoid]]  corresponding to the orbifold. 

For the [[global quotient orbifold]] of a [[topological G-space|G-space]] $X$, this is the [[ordinary cohomology]] of (the bare [[homotopy type]] of) the  [[Borel construction]] $X \!\sslash\! G \;\simeq\; X \times_G E G $, hence is _[[Borel cohomology]]_ (as opposed to finer versions of [[equivariant cohomology]] such as [[Bredon cohomology]]). 

A dedicated account of this Borel cohomology of orbifolds, in the generality of [[twisted cohomology]] (i.e. with [[local coefficients]]) is in:

* {#MoerdijkPronk99} [[Ieke Moerdijk]], [[Dorette Pronk]], _Simplicial cohomology of orbifolds_, Indagationes Mathematicae Volume 10, Issue 2, 1999, Pages 269-293 (<a href="https://doi.org/10.1016/S0019-3577(99)80021-4">doi:10.1016/S0019-3577(99)80021-4</a>)

Moreover, since the orbifold's [[isotropy groups]] $G_x$ are, by definition, [[finite groups]], their [[classifying spaces]] $\ast \!\sslash\! G \simeq B G$ have purely [[torsion subgroup|torsion]] [[integral cohomology]] in [[positive number|positive]] degrees, and hence become indistinguishable from the [[point]] in [[rational cohomology]] (and more generally whenever their [[order of a group|order]] is [[unit|invertible]] in the [[coefficient]] [[ring]]).

Therefore, in the special case of [[rational cohomology|rational]]/[[real cohomology|real]]/[[complex cohomology|complex]] [[coefficients]], the traditional orbifold Borel cohomology reduces further to an invariant of just (the [[homotopy type]] of) the naive quotient underlying an orbifold. For global quotient orbifolds  this is the [[topological quotient space]] $X/G$.

In this form, as an invariant of just $X/G$, the [[real cohomology|real]]/[[complex cohomology|complex]]/[[de Rham cohomology]] of orbifolds was originally introduced in 

* {#Satake56} [[Ichiro Satake]], _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363 ([doi:10.1073/pnas.42.6.359](https://doi.org/10.1073/pnas.42.6.359))

following analogous constructions in

* [[Walter Lewis Baily]], _On the quotient of an analytic manifold by a group of analytic homeomorphisms_, PNAS 40 (9) 804-808 (1954) ([doi:10.1073/pnas.40.9.804](https://doi.org/10.1073/pnas.40.9.804))


Since this traditional [[rational cohomology]] of orbifolds does, hence, not actually reflect the specific nature of orbifolds, a proposal for a finer notion of orbifold cohomology was famously introduced (motivated from orbifolds as [[target spaces]] in [[string theory]], hence from orbifolding of [[2d CFTs]]) in 

* {#ChenRuan00} [[Weimin Chen]], [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](https://arxiv.org/abs/math/0004129))

However, [[Chen-Ruan cohomology]] of an orbifold $\mathcal{X}$ turns out to be just Borel cohomology with rational coefficients, hence is just Satake's coarse cohomology -- but applied to the [[inertia orbifold]] of $\mathcal{X}$. A review that makes this nicely explicit is (see p. 4 and 7):

* {#Clader14} Emily Clader, _Orbifolds and orbifold cohomology_, 2014 ([pdf](http://www-personal.umich.edu/~eclader/OctLect1.pdf))

Hence [[Chen-Ruan cohomology]] of a global quotient orbifold is equivalently the [[rational cohomology]] ([[real cohomology]],  [[complex cohomology]]) for the [[topological quotient space]] $AutMor(X\!\sslash\!G)/G$ of the space of [[automorphisms]] in the [[action groupoid]] by the $G$-[[conjugation]] [[action]].

On the other hand, it was observed in (see p. 18)

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

that for global quotient orbifolds Chen-Ruan cohomology indeed is equivalent to a $G$-equivariant [[Bredon cohomology]] of $X$ -- for one specific choice of [[equivariant cohomology|equivariant]] [[coefficient]] system ([[abelian sheaf]] on the [[orbit category]] of $G$), namely for $G/H \mapsto ClassFunctions(H)$.

Or rather, [Moerdijk 02, p. 18](#Moerdijk02) observes that the Chen-Ruan cohomology of a global quotient orbifold is equivalently the [[abelian sheaf cohomology]] of the naive quotient space $X/G$ with [[coefficients]] in the [[abelian sheaf]] whose [[stalk]] at $[x] \in X/G$ is the [[ring]] of [[class functions]] of the [[isotropy group]] at $x$; and then appeals to Theorem 5.5 in

* {#Honkasalu90} [[Hannu Honkasalo]], _Equivariant Alexander-Spanier cohomology for actions of compact Lie groups_, Mathematica Scandinavica Vol. 67, No. 1 (1990), pp. 23-34 ([jstor:24492569](https://www.jstor.org/stable/24492569))

for the followup statement that the [[abelian sheaf cohomology]] of $X/G$ with coefficient sheaf $\underline{A}$ being "[[locally constant sheaf|locally constant]] except for dependence on [[isotropy groups]]" is equivalently [[Bredon cohomology]] of $X$ with coefficients in $G/H \mapsto \underline{A}_x$ for $Isotr_x = H$. This identification of the coefficient systems is Prop. 6.5 b) in:

* {#Honkasalo88} [[Hannu Honkasalo]], _Equivariant Alexander-Spanier cohomology_,  Mathematica Scandinavia,  63, 179-195, 1988 ([doi:10.7146/math.scand.a-12232](https://doi.org/10.7146/math.scand.a-12232))

See also Section 4.3 of

* {#SzaboValentino07} [[Richard Szabo]], [[Alessandro Valentino]], _Ramond-Ramond Fields, Fractional Branes and Orbifold Differential K-Theory_, Commun. Math. Phys. 294:647-702, 2010 ([arXiv:0710.2773](https://arxiv.org/abs/0710.2773))



In summary: 

* Traditional orbifold cohomology theory is [[Borel cohomology]] of underlying [[Borel construction]]-spaces, and reduces [[rational cohomology|rationally]] further to the [[rational cohomology]] of underlying naive [[quotient spaces]]. 

* [[Chen-Ruan cohomology]] is just the latter rational cohomology but applied after passage to the [[inertia orbifold]]. This is equivalent to the [[Bredon cohomology]] of the original orbifold, for one specific [[equivariant cohomology|equivariant coefficient]]-system.

This suggests, of course, that more of [[proper equivariant homotopy theory|proper]] [[equivariant cohomology]] should be brought to bear on a theory of orbifold cohomology. A partial way to achieve this is to prove for  a given [[equivariant cohomology]]-theory that it descends from an invariant of [[topological G-spaces]] to one of the associated [[global quotient orbifolds]].

For [[topological K-theory|topological]] [[equivariant K-theory]] this is the case, by

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], Prop. 4.1 in: _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

Therefore it makes sense to _define_ [[orbifold K-theory]] for [[orbifolds]] $\mathcal{X}$ which are equivalent to a [[global quotient orbifold]] 
$
  \mathcal{X} \simeq \prec(X \!\sslash\! G)
$
to be the $G$-[[equivariant K-theory]] of $X$:
$
  K^\bullet(\mathcal{X})
  \;\coloneqq\;
  K_G^\bullet(X)
  \,.
$

This is the approach taken in 

* {#AdemRuan01} [[Alejandro Adem]], [[Yongbin Ruan]], Section 3 of: _Twisted Orbifold K-Theory_, Commun. Math. Phys. 237 (2003) 533-556 ([arXiv:math/0107168](https://arxiv.org/abs/math/0107168))


Exposition and review of traditional orbifold cohomology, with an emphasis on [[Chen-Ruan cohomology]] and [[orbifold K-theory]], is in:

* {#ALR07} [[Alejandro Adem]], [[Johann Leida]], [[Yongbin Ruan]], _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))



