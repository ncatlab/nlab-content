
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

In the course of providing a [[geometry|geometric]] [[proof]] of the [[spin-statistics theorem]], [Berry & Robbins 1997](#BerryRobbins97) asked, at each [[natural number]] $n \in \mathbb{N}$, for a [[continuous function|continuous]] and [[symmetric group|$Sym(n)$]]-[[equivariant function]]

\[
  \label{TheBerryRobbinsMap}
  \underset{ {}^{\{1,\cdots, n\}}  }{Conf}\big(\mathbb{R}^3\big)
  \xrightarrow{\phantom{AAA}}
  \mathrm{U}(n)/\big(\mathrm{U}(1)\big)^n
\]

* from the [[configuration space of points|configuration space of $n$ points]] (ordered and unlabeled) in [[Euclidean space]] $\mathbb{R}^3$

* to the [[coset space]] of the [[unitary group]] $\mathrm{U}(n)$ by its [[maximal torus]], hence the complete [[flag manifold]] of flags in $\mathbb{C}^n$, 

both equipped with the evident [[group action]] by the [[symmetric group]] $Sym(n)$.

For the first non-empty case $n = 2$ this readily reduces to asking for a [[continuous map]] of the form $\mathbb{R}^3 \setminus \{0\} \xrightarrow{\;\;} \mathbb{C}P^1 \simeq S^2$ which is [[equivariant function|equivariant]] with respect to passage to antipodal points. This is immediately seen to be given by the radial projection.
But this special case turns out not to be representative of the general case, as this simple construction idea does not generalize to $n \gt 2$.

That a continuous and $Sym(n)$-equivariant Berry-Robbins map (eq:TheBerryRobbinsMap) indeed exists for all $n$ was proven in [Atiyah 2000](#Atiyah00). 

In this article, [[Michael Atiyah|Atiyah]] turned attention to the stronger question asking for a function (eq:TheBerryRobbinsMap) which is [[smooth function|smooth]] and $Sym(n) \times $[[SO(3)|$SO(3)$]]-[[equivariant]] and provided an elegant proof strategy for this stronger statement, which however hinges on some [[conjecture|conjectural]] positivity properties of a certain [[determinant]] (discussed in more detail and with first numerical evidence in [Atiyah 2001](#Atiyah01)), interpreted as the [[electromagnetism|electrostatic]] [[energy]] of $n$-[[particles]] in $\mathbb{R}^3$.

Extensive numerical checks of this stronger but conjectural construction was recorded, up to $n \lt 30$ , in [Atiyah & Sutcliffe 2002](#AtiyahSutcliffe02), together with a refined formulation of the [[conjecture]], whence it came to be known as the *Atiyah-Sutcliffe conjecture*.

The Atiyah-Sutcliffe conjecture has been [[proof|proven]] for $n = 3$ in [Atiyah 2000](#Atiyah00)/[01](#Atiyah01) and for $n = 4$ by [Eastwood & Norbury 01](#EastwoodNorbury01). 

## References

The origin of the question in investigation of the [[spin-statistics theorem]]:

* {#BerryRobbins97} [[Michael V. Berry]], [[Jonathan M. Robbins]], *Indistinguishability for quantum particles: spin, statistics and the geometric phase*, Proceedings of the Royal Society A **453** 1963 (1997) 1771-1790 ([doi:10.1098/rspa.1997.0096](https://doi.org/10.1098/rspa.1997.0096))

First form and first checks of the conjecture:

* {#Atiyah00} [[Michael F. Atiyah]], _The geometry of classical particles_, in Surveys in Differential Geometry, Surv. Differ. Geom. __7__, Int. Press 2000, 1–15 ([doi:10.4310/SDG.2002.v7.n1.a1](https://doi.org/10.4310/SDG.2002.v7.n1.a1))

* {#Atiyah01} [[Michael F. Atiyah]], _Configurations of points_, R. Soc. Lond. Philos. Trans. Ser. A, Math. Phys. Eng. Sci. 359 (2001) 1375–1387 ([doi:10.1098/rsta.2001.0840](https://doi.org/10.1098/rsta.2001.0840))

Generalization of the [[codomain]] to [[flag manifolds]] of other [[compact Lie groups]]:

* [[Michael F. Atiyah]], [[Roger Bielawski]], _Nahm’s equations, configuration spaces and flag manifolds_, Bull. Braz. Math. Soc. (N.S.) 33 (2002), 157–176 ([math.RT/0110112](https://arxiv.org/abs/math.RT/0110112), [doi:10.1007/s005740200007](https://doi.org/10.1007/s005740200007))


  > (using [[Nahm's equation]])

Full formulation of the Atiyah-Sutcliffe conjecture:

* {#AtiyahSutcliffe02} [[Michael F. Atiyah]], [[Paul M. Sutcliffe]], _The geometry of point particles_, Proc. Roy. Soc. London Ser. A 458 (2002), 1089–1115 ([hep-th/0105179](https://arxiv.org/abs/hep-th/0105179), [doi:10.1098/rspa.2001.0913](https://doi.org/10.1098/rspa.2001.0913))

Proof for $n = 4$:

* {#EastwoodNorbury01} [[Michael Eastwood]], [[Paul Norbury]], _A proof of Atiyah’s conjecture of four points in Euclidean three-space_, Geom. Topol. 5 (2001) 885–893 ([arXiv:math/0109161](https://arxiv.org/abs/math/0109161), [doi:10.2140/gt.2001.5.88510.2140/gt.2001.5.885](https://msp.org/gt/2001/5-2/p12.xhtml))

Further discussion:

* Dragutin Svrtan, Igor Urbiha, _Atiyah-Sutcliffe conjectures for almost collinear configurations and some new conjectures for symmetric functions_, ([math.AG/0406386](https://arxiv.org/abs/math/0406386)) 

* Dragutin Svrtan, Igor Urbiha, _Verification and strengthening of the Atiyah--Sutcliffe conjectures for several types of configurations_ ([math.MG/0609174](https://arxiv.org/abs/math/0609174))

* Marcin Mazur, Bogdan V. Petrenko, _On the conjectures of Atiyah and Sutcliffe_, Geom Dedicata **158**  (2012) 329–342
([doi:10.1007/s10711-011-9636-6](https://doi.org/10.1007/s10711-011-9636-6), [arxiv:1102.4662](https://arxiv.org/abs/1102.4662))

* [[Joseph Malkoun]], *Root Systems and the Atiyah-Sutcliffe Problem*, Journal of Mathematical Physics 60, 101702 (2019) ([arXiv:1903.00325](https://arxiv.org/abs/1903.00325))

* [[Joseph Malkoun]], _The Atiyah-Sutcliffe determinant_ ([arXiv:1903.05957](https://arxiv.org/abs/1903.05957))




