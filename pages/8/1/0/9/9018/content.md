
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[Kaluza-Klein reduction]] of [[11-dimensional supergravity]] on [[G2 manifolds]] yields an [[effective field theory|effective]] $N=1$ [[4-dimensional supergravity]]. This construction is the lift to [[M-theory]] of the KK-compactification of [[string theory]] on [[Calabi-Yau manifolds]].

Specifically for discussion of obtaining or approximating the [[standard model of particle physics]] by this procedure see at _[[G2-MSSM]]_.

## Details
 {#G2Manifolds}

### The C-field
 {#TheCField}

In compactifications with [[weak G2 holonomy]] it is the defining 4-form $\phi_4$ (the one which for strict [[G2 manifolds]] is the [[Hodge star operator|Hodge dual]] of the [[associative 3-form]]) which is the [[flux]]/[[field strength]] of the [[supergravity C-field]]. See for instance ([Bilal-Serendinger-Sfetos 02, section 6](#BilalDerendingerSfetos)):

Consider a [[KK-compactification]]-Ansatz $X_{11} = (X_4,g_4) \times (X_7,g_7)$ and

* $F_4 = f vol_{X_4}$;

* $F_7 = \tilde g e_7^\ast \phi_4$

where $e_4$, $e_7$ are given [[vielbein]] fields on $X_4$ and $X_7$ and $\phi_4$ is the [[Hodge star operator|Hodge dual]] of the [[associative 3-form]]. Then the [[Einstein equations]] of [[11-dimensional supergravity]] give

$$
  R_4 = - \frac{1}{3}\left(f^2 + \frac{7}{2} \tilde g^2\right) g_4
$$

$$
  R_7 = \frac{1}{6}\left(f^2 + 5 \tilde g^2\right) g_7
$$

(where $g_4$, $g_7$ is the [[pseudo-Riemannian metric|metric tensor]]) saying that both spaces are [[Einstein manifolds]] ([BSS 02, (5.4)](#BilalDerendingerSfetos)). The [[equations of motion]] for the [[supergravity C-field]] is

$$
  \tilde g\left(
     d \phi - f \star\phi
  \right)
$$

for $\phi = e_7^\ast \phi_3$ the pullback of the [[associative 3-form]] ([BSS 02, (5.5)](#BilalDerendingerSfetos)), saying that $\phi \propto \star F_7$ exhibits [weak G2-holonomy](G2+manifold#WeakG2Holonomy) with weakness parameter given by the component of the  [[C-field]] on $X_4$.

### Singularities

For realistic [[field (physics)|field]] content after [[Kaluza-Klein compactification]] one needs to consider not smooth (weak) [[G2-manifolds]] but [[orbifolds]] of these. see the first page of ([Acharya-Denef-Hofman-Lambert](#AcharyaDenefHofmanLambert)) for discussion of [[phenomenology]] for such orbifold $G_2$ models and further pointers and see ([Achary 98](#Acharya98)) for general discussion of orbifolds with $G_2$-structure.

## Related concepts

* [[G2]]

* [[G2 manifold]], [[generalized G2-manifold]]

* [[G2-MSSM]]

* [[Freund-Rubin compactification]]

* [[exceptional generalized geometry]]

* [[topological M-theory]], [[Hitchin functional]]

* [[7d Chern-Simons theory]]

## References


* [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([pdf](http://www.intlpress.com/journals/ATMP/archive/2002/6-1-1.pdf))

* [[Mirjam Cvetic]], [[Gary Gibbons]], H. L&#252;  and C.N. Pope, _Supersymmetric M3-branes and G2 Manifolds_ ([pdf](http://cdsweb.cern.ch/record/503160/files/0106026.pdf))

Discussion of [[Freund-Rubin compactification]] on $\mathbb{R}^4 \times X_7$ "with flux", hence non-vanishing [[supergravity C-field]] and how they preserve one supersymmetry if $X_7$ is of [[weak G2 holonomy]] with $\lambda$ = [[cosmological constant]] = C-[[field strength]] on $\mathbb{R}^4$ is in

* {#BilalDerendingerSfetos} [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 
* {#HouseMicu04} Thomas House, Andrei Micu, _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))


Surveys include

* [[Mike Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))


* [[Sergei Gukov]], _M-theory on manifolds with exceptional holonomy_, Fortschr. Phys. 51 (2003), 719&#8211;731 ([pdf](http://research.physics.unc.edu/string/gukov.pdf))


* [[Bobby Acharya]], _M Theory, $G_2$-manifolds and Four Dimensional Physics_,  Classical and Quantum Gravity Volume 19 Number 22  ([pdf](http://users.ictp.it/~pub_off/lectures/lns013/Acharya/Acharya_Final.pdf))



* Adil Belhaj, _M-theory on G2 manifolds and the method of (p, q) brane webs_ (2004) ([web](http://iopscience.iop.org/0305-4470/37/18/011))

* Adam B. Barrett, _M-Theory on Manifolds with $G_2$ Holonomy_ ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))

Compactificaton on [[orbifolds]] of $G_2$-manifolds, introducing ([[orbifold]]-) singularities necessary for realistic [[effective QFTs]] is discussed in 

* [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_ ([arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205))
 {#Achary98}

* [[Bobby Acharya]], F. Denef, C. Hofman, N. Lambert, _Freund-Rubin Revisited_ ([arXiv:hep-th/0308046](http://arxiv.org/abs/hep-th/0308046))
 {#AcharyaDenefHofmanLambert03}


The corresponding [[membrane]] [[instanton]] corrections to the [[superpotential]] are discussed in 

* [[Jeffrey Harvey]], [[Greg Moore]], _Superpotentials and Membrane Instantons_ ([arXiv:hep-th/9907026](http://arxiv.org/abs/hep-th/9907026))


The [[hierarchy problem]] in the context of $G_2$-compactifications is discussed in

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], Piyush Kumar, Diana Vaman, _An M theory Solution to the Hierarchy Problem_, Phys.Rev.Lett.97:191601,2006 ([arXiv:hep-th/0606262](http://arxiv.org/abs/hep-th/0606262))

A survey of the corresponding [[string phenomenology]] is in

* [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

[[!redirects G2 compactifications of M-theory]]