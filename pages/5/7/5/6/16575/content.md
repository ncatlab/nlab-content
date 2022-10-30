

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Generally, an _enhanced gauge symmetry_ referes to the appearance of [[gauge theory]] with a larger [[gauge group]] than may be suprficially apparent.



### On coincident D-branes

A famous case is the enhance gauge symmetry in the [[Chan-Paton gauge fields]] of coincident [[D-branes]]. A priori each D-brane carries a [[complex line bundle]]/[[circle principal bundle]], but as $n$ of them coincide the [[gauge group]] is expected to enhance from $(U(1))^n$ to the [[unitary group]] $U(n)$ (or the [[special unitary group]] $SU(n)$). 

Mathematically this gauge enhancement on D-branes is modeled by the [[Baum-Douglas geometric cycle]] model for [[K-homology]] ([Reis-Szabo 05, def. 1.5 and p. 16](#ReisSzabo05), [Szabo 08, p. 4](#Szabo08)): One such cycle is given by a submanifold $W \overset{\phi}{\hookrightarrow} X$ of [[spacetime]] $X$ equipped with [[spin^c structure]] and with a [[complex vector bundle]] $E \to X$, and given two such cycles $(W,\phi,E_1)$ and $(W,\phi,E_2)$ with the same underlying manifold ("coincident D-brane [[worldvolume]]") then their formal [[direct sum]] is identified with the single cycle carrying the [[direct sum of vector bundles]] 

$$
  (W,\phi, E_1) + (W, \phi, E_2)
  \;\sim\;
  (W, \phi, E_1 \oplus E_2)
  \,.
$$

If here $E_i$ has [[rank]] $n_i$ and hence [[structure group]] $U(n_i)$, then the [[direct sum of vector bundles]] $E_1 \oplus E_2$ has [[structure group]] the [[product group]] $U(n_1) \times U(n_2)$. 

In particular the sum of $n$ coincidnt cycles each carrying a line bundle yields a rank-$n$ vector bundle with structure group $(U(1))^n$. In this sense then a cycle carrying a general rank $n$-vector bundle, hence with structure group $U(n)$, may be thought of as a "gauge enhancement" of making $n$ D-branes coincide.


### From massless BPS states

In the context of the realization of [[super Yang-Mills theories]] as [[effective field theories]] of [[superstring theory]], [[BPS branes]] in the string background becomes BPS states of the SYM theory. These become massless as the [[cycles]] on the which BPS charge is supported shrink away (at boundary points of the given [[moduli space]]). In this case these additional massless states may appear as additional gauge bosons in the compactified gauge theory which thereby develops a bigger gauge group. Typically a previously abelian gauge group becomes non-abelian this way.

Examples include [[KK-compactification]] of [[M-theory]] on [[K3]] fibers and on [[G2-manifolds]] with [[ADE singularities]], corresponding to [[F-theory]] on [[elliptic fibrations]] making [[K3]]-fibrations with singular fibers, corresponding to [[heterotic string theory]] on singular elliptic fibrations. See at 

* [[M-theory lift of gauge enhancement on D6-branes]]

* _[[M-theory on G2-manifolds]]_ the section _[Nonabelian gauge groups and chiral fermions at orbifold singularities](M-theory+on+G2-manifolds#EnhancedGaugeGroups)_;

* _[[F-theory]]_ the section _[F-brane scan](F-theory#Fbranescan)_

* _[[duality between F-theory and heterotic string theory]]_.

### On M9-Branes

In [[Horava-Witten theory]] there is supposed to be gauge enhancement over the [[M9-branes]] such as to identify their [[worldvolume]] theory with [[E8]]-[[heterotic string theory]]. 


Under the [[duality in string theory|duality]] between [[M-theory]] and [[type IIA string theory]] the M9-brane may be identified with the [[O8-plane]]:

<img src="https://ncatlab.org/nlab/files/O8DualToM9.jpg" width="600"/>

> from [GKSTY 02, section 3](#GKSTY02)

This may be used to understand the [[gauge enhancement]] to [[E8]]-[[gauge groups]] at the [[heterotic string theory|heterotic]] boundary of [[Horava-Witten theory]]:


<img src="https://ncatlab.org/nlab/files/ViaO8GaugeEnhancementOnM9.jpg" width="600"/>

> from [GKSTY 02, section 3](#GKSTY02)


## Related concepts

* [[spontaneously broken symmetry]]


## References

### On coincident D-branes
  {#ReferencesOnCoincidentDBranes}

The idea that on $N$ coincident D-branes there is gauge enhancement to $U(N)$-gauge field theory is due to 

* {#Witten95} [[Edward Witten]], section 3 of _Bound States Of Strings And $p$-Branes_, Nucl.Phys.B460:335-350, 1996 ([arXiv:hep-th/9510135](https://arxiv.org/abs/hep-th/9510135))

There, this is called an "obvious guess" (first line on p. 8). Subsequently,  most authors cite this obvious guess as a fact; for instance the review 

* {#Myers03} [[Robert Myers]], section 3 of _Nonabelian Phenomena on D-branes_, Class.Quant.Grav. 20 (2003) ([arXiv:hep-th/0303072](https://arxiv.org/abs/hep-th/0303072))

By actual computation in [[open string field theory]] "convincing evidence" (see bottom of p. 22) was found in

* {#ColettiSigalovTaylor03} Erasmo Coletti, Ilya Sigalov, [[Washington Taylor]], _Abelian and nonabelian vector field effective actions from string field theory_, JHEP 0309 (2003) 050 ([arXiv:hep-th/0306041](https://arxiv.org/abs/hep-th/0306041))

while the first actual derivation seems to be due to

* {#Lee16} [[Taejin Lee]], _Covariant open bosonic string field theory on multiple D-branes in the proper-time gauge_, Journal of the Korean Physical Society December 2017, Volume 71, Issue 12, pp 886–903 ([arXiv:1609.01473](https://arxiv.org/abs/1609.01473))

which is surveyed in

* {#Lee17} [[Taejin Lee]], _Deformation of the Cubic Open String Field Theory_, Phys. Lett. B 768 (2017) 248 ([arXiv:1701.06154](https://arxiv.org/abs/1701.06154))

That on [[D0-branes]] this reproduces the [[BFSS matrix model]] and on [[D(-1)-branes]] the [[IKKT matrix model]] is shown in

* [[Taejin Lee]], _Covariant Open String Field Theory on Multiple D$p$-Branes_ ([arXiv:1703.06402](https://arxiv.org/abs/1703.06402))

Discussion of gauge enhancement on coincident D-branes in terms of [[Baum-Douglas geometric cycles]] for [[K-homology]] is in 

* {#ReisSzabo05} Rui Reis, [[Richard Szabo]], _Geometric K-Homology of Flat D-Branes_ ,Commun.Math.Phys. 266 (2006) 71-122, Journal of the Korean Physical Society December 2017, Volume 71, Issue 12, pp 886–903 ([arXiv:hep-th/0507043](https://arxiv.org/abs/hep-th/0507043))

reviewed in

* {#Szabo08} [[Richard Szabo]], _D-branes and bivariant K-theory_, Noncommutative Geometry and Physics 3 1 (2013): 131. ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))


### On M-branes at ADE-singularities

The picture of [[M-theory lift of gauge enhancement on D6-branes]] is due to

* {#Sen97} [[Ashoke Sen]], Section 2, _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

Review of the standard lore of gauge enhancement in M-theory includes

* {#Barrett06} Adam B. Barrett, section 2.3 (following [Acharya-Gukov 04](#AcharyaGukov04)) of _M-Theory on Manifolds with $G_2$ Holonomy_, 2006 ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))

(...)

### General

Original articles include

* [[Edward Witten]], section 4.6 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126,1995 ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

* {#HullTownsend95} [[Chris Hull]], [[Paul Townsend]], _Enhanced Gauge Symmetries in Superstring Theories_, Nucl.Phys. B451 (1995) 525-546 ([arXiv:hep-th/9505073](http://arxiv.org/abs/hep-th/9505073))

* [[Paul Aspinwall]], _Enhanced Gauge Symmetries and K3 Surfaces_, Phys.Lett. B357 (1995) 329-334 ([arXiv:hep-th/9507012](http://arxiv.org/abs/hep-th/9507012))

* [[Chris Hull]], _Duality, Enhanced Symmetry and Massless Black Holes_, in Proceedings of Strings'95: Future Perspectives in String Theory (World Scientific, 1996, I. Bars et al. eds.), p. 230 ([pdf](http://physics.usc.edu/Strings95/Proceedings/pdf/hull.pdf))

* M. Bershadsky, [[Ken Intriligator]], [[Shamit Kachru]], [[David Morrison]], V. Sadov, [[Cumrun Vafa]], _Geometric Singularities and Enhanced Gauge Symmetries_, Nucl.Phys.B481:215-252,1996 ([arXiv:hep-th/9605200](http://arxiv.org/abs/hep-th/9605200))

* [[Philip Candelas]], Eugene Perevalov, Govindan Rajesh, _Toric Geometry and Enhanced Gauge Symmetry of F-Theory/Heterotic Vacua_, Nucl.Phys. B507 (1997) 445-474 ([arXiv:hep-th/9704097](http://arxiv.org/abs/hep-th/9704097))


* [[Mirjam Cvetic]], [[Chris Hull]], _Wrapped Branes and Supersymmetry_, Nucl.Phys.B519:141-158,1998 ([arXiv:hep-th/9709033](http://arxiv.org/abs/hep-th/9709033))

* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](http://arxiv.org/abs/hep-th/0409191))

* {#HalvorsonMorrison15} [[James Halverson]], [[David Morrison]], _On Gauge Enhancement and Singular Limits in $G_2$ Compactifications of M-theory_ ([arXiv:1507.05965](http://arxiv.org/abs/1507.05965))

* [[Neil Lambert]], Miles Owen, _Charged Chiral Fermions from M5-Branes_ ([arXiv:1802.07766](https://arxiv.org/abs/1802.07766))

Discussion via duality of [[M9-branes]] to [[O-planes]] is in

* {#GKSTY02} E. Gorbatov, V.S. Kaplunovsky, J. Sonnenschein, [[Stefan Theisen]], S. Yankielowicz, section 3 of _On Heterotic Orbifolds, M Theory and Type I' Brane Engineering_, JHEP 0205:015, 2002 ([arXiv:hep-th/0108135](https://arxiv.org/abs/hep-th/0108135))


[[!redirects enhanced gauge symmetries]]

[[!redirects gauge enhancement]]
[[!redirects gauge enhancements]]