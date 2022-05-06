## Internal Links

* [with single brackets](base+change)
* [[base change|with double brackets (to existant page)]]
* [[foo bar|with double brackets (to new page)]]
* [[pullback#PullbackFunctor|with double brackets to fragment]]


### Traditional notions of orbifold cohomology

Traditionally, the [[cohomology]] of [[orbifolds]]  has, by and large, been taken to be simply the cohomology of (the plain [[homotopy type]] of) the [[geometric realization of simplicial topological spaces|geometric realization]] of the [[Lie groupoid]] (or [[topological groupoid]]) corresponding to the orbifold. 

For global quotient orbifolds of a [[topological G-space|G-space]] $X$, this is the cohomology of (the bare [[homotopy type]] of) the  [[Borel construction]] $X \!\sslash\! G \;\simeq\; X \times_G E G $, hence is _[[Borel cohomology]]_ (as opposed to finer versions of [[equivariant cohomology]] such as [[Bredon cohomology]]). 

A dedicated account of this Borel cohomology of orbifolds, in the generality of [[twisted cohomology]] (i.e. with [[local coefficients]]) is in:

* {#MoerdijkPronk99} [[Ieke Moerdijk]], [[Dorette Pronk]], _Simplicial cohomology of orbifolds_, Indagationes Mathematicae Volume 10, Issue 2, 1999, Pages 269-293 (<a href="https://doi.org/10.1016/S0019-3577(99)80021-4">doi:10.1016/S0019-3577(99)80021-4</a>)

Moreover, since the orbifold's [[isotropy groups]] $G_x$ are, by definition, [[finite groups]], their [[classifying spaces]] $\ast \!\sslash\! G \simeq G B G$ have purely [[torsion subgroup|torsion]] [[integral cohomology]] in positive degrees, and hence become indistinguishable from the [[point]] in [[rational cohomology]] (and more generally whenever their [[order of a group]] is [[unit|invertible]] in the [[coefficient]] [[ring]]).

Therefore in the special case of [[rational cohomology|rational]] or [[real cohomology|real]] [[coefficient]], the traditional orbifold Borel cohomology reduces further to an invariant of just (the [[homotopy type]] of) of the naive quotient underlying an orbifold. For global quotient orbifolds  this is the [[topological quotient space]] $X/G$.

In this form, as an invariant of $X/G$, the [[real cohomology|real]]/[[de Rham cohomology]] of orbifolds was originally introduced in 

* {#Satake56} [[Ichiro Satake]], _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363 ([doi:10.1073/pnas.42.6.359]( https://doi.org/10.1073/pnas.42.6.359))

Since this traditional [[rational cohomology]] of orbifolds does, hence, not actually reflect the specific nature of orbifolds, a proposal for a finer notion of orbifold cohomology was famously introduced (motivated from orbifolds as [[target spaces]] in [[string theory]], hence from orbifolding of [[2d CFTs]]) in 

* {#ChenRuan00} [[Weimin Chen]], [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](https://arxiv.org/abs/math/0004129))

However, [[Chen-Ruan cohomology]] of an orbifold $\mathcal{X}$ turns out to be just Bredon cohomology with rational coefficients, hence is just Satake's coarse cohomology, but applied to the [[inertia orbifold]] of $\mathcal{X}$. A review that makes this explicit is (see p. 4 and 7):

* {#Clader14} Emily Clader, _Orbifolds and orbifold cohomology_, 2014 ([pdf](http://www-personal.umich.edu/~eclader/OctLect1.pdf))

Hence Chen-Ruan cohomology of a global quotient orbifold is equivalently the [[rational cohomology]] (or [[real cohomology|real]] or complex cohomology) for the [[topological quotient space]] $Aut(X\!\sslash\!G)/G$ of the space of [[automorphisms]] in the [[action groupoid]] by the $G$-[[conjugation]] [[action]].

However it was observed in (see p. 18)

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, [[Alejandro Adem]], [[Jack Morava]], Yongbin Ruan (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

that for global quotient orbifolds Chen-Ruan cohomology indeed is equivalent, to a $G$-equivariant [[Bredon cohomology]] of $X$ -- for one specific choice of [[equivariant cohomology|equivariant]] [[coefficient]] system ([[abelian sheaf]] on the [[orbit category]] of $G$), namely for $G/H \mapsto ClassFunction(H)$.

More in detail, [Moerdijk 02, p. 18](#Moerdijk02) really observes that the Chen-Ruan cohomology of a global quotient orbifold is equivalently the [[abelian sheaf cohomology]] of the naive quotient space $X/G$ with [[coefficients]] in the [[abelian sheaf]] whose [[stalk]] at $[x] \in X/G$ is the [[ring]] of [[class functions]] of the [[isotropy group]] at $x$; and then appeals to Theorem 5.5 in

* {#Honkasalu90} Honkasalo, _Equivariant Alexander-Spanier cohomology for actions of compact Lie groups_, Mathematica Scandinavica Vol. 67, No. 1 (1990), pp. 23-34 ([jstor:24492569](https://www.jstor.org/stable/24492569))

for the followup statement that the [[abelian sheaf cohomology]] of $X/G$ with coefficient sheaf $\underline{A}$ being "[[locally constant sheaf|locally constant]] except for dependence on [[isotropy groups]]" is equivalently [[Bredon cohomology]] of $X$ with coefficients in $G/H \mapsto \underline{A}_x$. This identification of the coefficient systems is Prop. 6.5 b) in:

* {#Honkasalo88} Honkasalo, _Equivariant Alexander-Spanier cohomology_,  Mathematica Scandinavia,  63, 179-195, 1988 ([doi:10.7146/math.scand.a-12232](https://doi.org/10.7146/math.scand.a-12232))

In summary: Traditional orbifold cohomology theory is [[Borel cohomology]] of underlying [[Borel construction]]-spaces, and reduces [[rational cohomology|rationally]] further to the [[rational cohomology]] of undelrying naive [[quotient spaces]]. [[Chen-Ruan cohomology]] is just the latter naive cohomology but applied after passing to [[inertia orbolds]], which is equivalent to the [[Bredon cohomology]] of the original orbifold, for one specific [[equivariant cohomology|equivariant coefficient]]-system.




Let 

$$
  \mathcal{X}
  \;\coloneqq\;
  OrbSnglr\big(  X \!\sslash\! G \big)
$$ 

be the global quotient [[orbifold]] supposed to correspond to a [[smooth manifold]] $X$ equipped with the [[action]] of a [[finite group]] $G$ (for definiteness, and to avoid inessential technical fine-print).

Write

* $Snglr(\mathcal{X}) = X/G$ for its naive quotient space, 

  traditionally regarded as [[topological space]] 

  (namely the [[quotient topological space]] of the [[topological G-space]] underlying $X$),

  though this quotient does exist also in [[diffeological spaces]], which would be the more appropriate [[category]] to regard it in ([IKZ 10](#IKZ10));

* $Smth(\mathcal{X}) = X \sslash G$ for its [[homotopy quotient]] space,

  traditionally regarded as a [[topological space]] (namely the [[Borel construction]] on the [[topological G-space]] underlying X),

  though this homotopy quotient does exists also in [[differentiable stacks]]/[[smooth groupoids]], which is the more appropriate [[(2,1)-category]] to regard it in ([MP97](#MoerdijkPronk97)).

Most notions of [[cohomology]] of the orbifold $\mathcal{X}$ considered in existing literature are actually invariants just of $Snglr(\mathcal{X})$ or just of $Smth(\mathcal{X})$, and mostly just of their underlying topological spaces -- the closest to an exception to this rule is Chen-Ruan cohomology, which however is also just the cohomology of a naive quotient, just of a different orbifold (the [[inertia orbifold]]):

| **cohomology of $Snglr(\mathcal{X})$** | 
|-----------------------|
| [Satake 56, Thm 1](#Satake56): $H_{Sa}^\bullet(\mathcal{X}) = H^\bullet\big(Shp \circ Snglr(\mathcal{X}),\mathbb{R}\big)$ | 
|  **cohomology of $Smth(\mathcal{X})$**   |
| [Moerdijk-Pronk 99](#MoerdijkPronk99), [ALR 07  Def. 1.56](#ALR07): $H^\bullet_{MP}\big( \mathcal{X}, \mathcal{A} \big) = H^\bullet\big( Shp\circ Smth(\mathcal{X}), A \big)$ <br/>    |
| **cohomology of $Snglr\big( [\mathcal{B}\mathbb{Z}, \mathcal{X}] \big)$** |
| [Chen-Ruan 00](#ChenRuan00): $H^\bullet_{CR}(\mathcal{X}) \coloneqq H^\bullet\Big( Shp \circ Snglr\big( [\mathcal{B}\mathbb{Z}, \mathcal{X}] \big)  ,\mathbb{K}\Big)$ <br/> (see [Clader 14, p. 4, p.7](#Clader14)) <br/> [Moe 02, p. 18](#Moerdijk02):  $H^\bullet_{CR}(\mathcal{X}) = H^\bullet\big( Shp \circ Snglr(\mathcal{X}), R_{\mathbb{K}}(Isotr(-))  \big)$  <br/> [Honkasalo 88, Thm. 6.4](#Honkasalo88), [Honkasalo 90, Thm. 5.5](#Honkasalu90): $\cdots = H^\bullet_G\big(X, something \big) $ |  



## References

* {#Satake56} [[Ichiro Satake]], _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363 ([doi:10.1073/pnas.42.6.359]( https://doi.org/10.1073/pnas.42.6.359))


* {#Honkasalo88} Honkasalo, _Equivariant Alexander-Spanier cohomology_,  Mathematica Scandinavia,  63, 179-195, 1988 ([doi:10.7146/math.scand.a-12232](https://doi.org/10.7146/math.scand.a-12232))


* {#Honkasalu90} Honkasalo, _Equivariant Alexander-Spanier cohomology for actions of compact Lie groups_, Mathematica Scandinavica Vol. 67, No. 1 (1990), pp. 23-34 ([jstor:24492569](https://www.jstor.org/stable/24492569))

* {#MoerdijkPronk97} [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf), [doi:10.4171/LEM/56-3-4](http://dx.doi.org/10.4171/LEM/56-3-4))

* {#MoerdijkPronk99} [[Ieke Moerdijk]], [[Dorette Pronk]], _Simplicial cohomology of orbifolds_, Indagationes Mathematicae Volume 10, Issue 2, 1999, Pages 269-293 (<a href="https://doi.org/10.1016/S0019-3577(99)80021-4">doi:10.1016/S0019-3577(99)80021-4</a>)

* {#ChenRuan00} [[Weimin Chen]], [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](https://arxiv.org/abs/math/0004129))

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, [[Alejandro Adem]], [[Jack Morava]], Yongbin Ruan (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

* {#ALR07} A. Adem, J. Leida, [[Yongbin Ruan]], _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))


* {#IKZ10} [[Patrick Iglesias-Zemmour]], [[Yael Karshon]], Moshe Zadka, _Orbifolds as diffeologies_, Transactions of the American Mathematical Society 362 (2010), 2811-2831 ([arXiv:math/0501093](https://arxiv.org/abs/math/0501093)) 

* {#Clader14} Emily Clader, _Orbifolds and orbifold cohomology_, 2014 ([pdf](http://www-personal.umich.edu/~eclader/OctLect1.pdf))

 * The signature for the theory of the _standard induction algebra_ has one sort symbol $N$, one function symbol $s:N\to N$ and one constant $O:N$. The theory axiomaticizes [[natural number object|natural number objects]] and the third axiom makes crucial use of the infinitary disjunction of geometric logic in order to state that every natural number is standard i.e. either 0 or obtained from 0 by repeated application of the successor function:

  - $0 = s(n) \vdash_{n} \bot$
  - $s(n) = s(n') \vdash_{n n'} n=n'$
   - $\top \vdash_{n} \bigvee_{i} n=\underset{i}{\underbrace{s \dots s}}(0)$

The [[classifying topos]] is $Set$. But due to the trivial subtopos lattice, theories classified by Set admit no quotient theories whence the geometric theory of natural numbers is complete in striking contrast with classical finitary first order logic! Furthermore, since $Set$ is the terminal topos classifying also the [[empty theory]], one sees that the object/type $\mathbb{N}$ of natural numbers "comes for free" in geometric logic. This observation underlies the ideas for a [[geometric type theory]] (for more on this see there!).
