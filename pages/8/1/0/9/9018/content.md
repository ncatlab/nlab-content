
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

The [[Kaluza-Klein reduction]] of [[11-dimensional supergravity]] on [[G2 manifolds]] (notably [[Freund-Rubin compactifications]] and variants) yields an [[effective field theory|effective]] $N=1$ [[4-dimensional supergravity]]. This construction is the lift to [[M-theory]] of the KK-compactification of [[string theory]] on [[Calabi-Yau manifolds]] (see at _[[string phenomenology]]_).

In order for this to yield [[phenomenology|phenomenologically]] interesting effective physics the compactification space must be an [[orbifold]] (hence an orbifold of [[special holonomy]]), its [[stabilizer groups]] will encode the [[nonabelian group|nonabelian]] [[gauge group]] of the effective theory by "[[geometric engineering of quantum field theory]]" ([Acharya 98](#Acharya98), [Atiyah-Witten 01, section 6](#AtiyahWitten01)). Specifically for discussion of [[string phenomenology]] obtaining or approximating the [[standard model of particle physics]] by this procedure see at _[[G2-MSSM]]_.

## Details
 {#G2Manifolds}

### Vacuum solutions
 {#VacuumSolutionsAndTorsion}

Genuine [[G2-manifold]]/[[orbifold]] fibers, these having vanishing [[Ricci curvature]], correspond to [[vacuum]] solutions of the [[Einstein equations]] of [[11d supergravity]], i.e. with vanishing [[field strength]] of the [[gravitino]] and the [[supergravity C-field]] (see e.g. [Acharya 02, p. 9](#Acharya02)).
(If one includes non-vanishing $C$-field strength one finds "weak $G_2$-holonomy" instead, see [below](#TheCField)).

Notice that vanishing [[gravitino]] [[field strength]] (i.e. [[covariant derivative]]) means that the [[torsion of a Cartan connection|torsion]] of the super-[[vielbein]] is in each [[tangent space]] the canonical torsion of the [[super Minkowski spacetime]]. This [[supergravity torsion constraint|torsion constraint]] already just for the bosonic part $(E^a)$ of the super-vielbein $(E^a, E^\alpha)$ implies (together with the [[Bianchi identities]]) the [[equations of motion]] of supergravity, hence here the vacuum [[Einstein equations]] in the 11d [[spacetime]]. 

### Complexified moduli space
{#ComplexifiedModuli} 

For vanishing [[field strength]] of the [[supergravity C-field]], the formal linear combination 

$$
  \tau \coloneqq C_3 + i \phi_3
$$

of the (flat) supergravity $C$-field $C_3$ and the the 3-form $\phi_3$ of the $G_2$-structure is the natural [[holomorphic function|holomorphic coordinate]] on the [[moduli space]] of the [[KK-compactification]] of a $G_2$-manifold, in M-theoretic higher analogy of the complexified K&#228;hler classes of CY compactifications of 10d string theory ([Harvey-Moore 99, (2.7)](#HarveyMoore99), [Acharya 02, (32) (59) (74)](#Acharya02), [Grigorian-Yau 08, (4.57)](#GrigorianYau08), [Acharya-Bobkov 08, (4)](#AcharyaBobkov08))

### Nonabelian gauge groups and chiral fermions at orbifold singularities
 {#EnhancedGaugeGroups}

The [[KK-compactification]] of vaccuum [[11-dimensional supergravity]] on a _[[smooth manifold|smooth]]_ [[G2-manifold]] $Y$ results in a [[effective field theory|effective]] [[N=1 D=4 super Yang-Mills theory]] with [[abelian group|abelian]] [[gauge group]] $U(1)^{b_2(Y)}$ and with $b_3(Y)$ [[complex scalar fields]] which are neutral (not charged) under this gauge group (with $b_\bullet(Y)$ the [[Betti numbers]] of $Y$) (e.g. [Acharya 02, section 2.3](#Acharya02)). This is of course unsuitable for [[phenomenology]].

But when $Y$ is a $G_2$-[[orbifold]] then:

1. at an [[ADE classification|ADE orbifold]] singularity the gauge group becomes nonabelian ([Acharya 98](#Acharya98), [Acharya 00](#Acharya00), review includes [Acharya 02, section 3](#Acharya02), [BBS 07, p. 422, 436](#BBS07));

1. at a [[conifold singularity]] [[chiral fermions]] appear ([Atiyah-Witten 01](#AtiyahWitten01), [Acharya-Witten 01](#AcharyaWitten01)).

The first point is argued from the [[duality in string theory|duality]] between M-theory compactified on [[K3]] and [[heterotic string theory]] on a 3-torus. Here it is fairly well understood that at the degenertion points of the K3-[[moduli space]] enhanced nonabelian gauge symmetry appears. The degeneration points correspond to vanishing 2-[[cycles]] and the ideas is that therefore the [[M2-brane]] [[BPS charges]] corresponding to these cycles become massless and hence contribute further states of the 4d effective field theory. See at _[[enhanced gauge symmetry]]_.




### Solutions with non-vanishing $C$-field strength
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

For realistic [[field (physics)|field]] content after [[Kaluza-Klein compactification]] one needs to consider not smooth (weak) [[G2-manifolds]] but [[conical singularities]] and [[orbifolds]] of these. see the first page of ([Acharya-Denef-Hofman-Lambert](#AcharyaDenefHofmanLambert)) for discussion of [[phenomenology]] for such orbifold $G_2$ models and further pointers and see ([Acharya 98](#Acharya98)) for general discussion of orbifolds with $G_2$-structure.

## Related concepts

* [[G2]]

* [[G2 manifold]], [[generalized G2-manifold]]

* [[G2-MSSM]]

* [[Freund-Rubin compactification]]

* [[exceptional generalized geometry]]

* [[topological M-theory]], [[Hitchin functional]]

* [[7d Chern-Simons theory]]

## References

The [[KK-compactification]] of [[11d supergravity]] of [[fibers]] of [[special holonomy]] was originally considered in

* {#DauriaFreCastellani91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter V.6 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[George Papadopoulos]], [[Paul Townsend]], _Compactification of D=11 supergravity on spaces of exceptional holonomy_, Phys.Lett.B357:300-306,1995 ([arXiv:hep-th/9506150](http://arxiv.org/abs/hep-th/9506150))

Specifically [[string phenomenology]] for the case of compactification on [[G2-manifolds]] (or rather [[orbifolds]] ) goes back to

* {#Acharya98} [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_, Adv.Theor.Math.Phys. 3 (1999) 227-248 ([arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205))

* {#Acharya00} [[Bobby Acharya]], _On Realising $N=1$ Super Yang-Mills in M theory_ ([arXiv:hep-th/0011089](http://arxiv.org/abs/hep-th/0011089))

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

* {#AcharyaWitten01} [[Bobby Acharya]], [[Edward Witten]], _Chiral Fermions from Manifolds of G2 Holonomy_ ([arXiv:hep-th/0109152](http://arxiv.org/abs/hep-th/0109152))

See also

* [[Mirjam Cvetic]], [[Gary Gibbons]], H. L&#252;  and C.N. Pope, _Supersymmetric M3-branes and G2 Manifolds_ ([pdf](http://cdsweb.cern.ch/record/503160/files/0106026.pdf))

* {#AcharyaDenefHofmanLambert03} [[Bobby Acharya]], F. Denef, C. Hofman, [[Neil Lambert]], _Freund-Rubin Revisited_ ([arXiv:hep-th/0308046](http://arxiv.org/abs/hep-th/0308046))


Discussion of [[Freund-Rubin compactification]] on $\mathbb{R}^4 \times X_7$ "with flux", hence non-vanishing [[supergravity C-field]] and how they preserve one supersymmetry if $X_7$ is of [[weak G2 holonomy]] with $\lambda$ = [[cosmological constant]] = C-[[field strength]] on $\mathbb{R}^4$ is in

* {#BilalDerendingerSfetos} [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 
* {#HouseMicu04} Thomas House, Andrei Micu, _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))


Survey and further discussion includes

* [[Michael Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))


* [[Sergei Gukov]], _M-theory on manifolds with exceptional holonomy_, Fortschr. Phys. 51 (2003), 719&#8211;731 ([pdf](http://research.physics.unc.edu/string/gukov.pdf))


* {#Acharya02} [[Bobby Acharya]], _M Theory, $G_2$-manifolds and Four Dimensional Physics_,  Classical and Quantum Gravity Volume 19 Number 22, 2002  ([pdf](http://users.ictp.it/~pub_off/lectures/lns013/Acharya/Acharya_Final.pdf))


* Adil Belhaj, _M-theory on G2 manifolds and the method of (p, q) brane webs_ (2004) ([web](http://iopscience.iop.org/0305-4470/37/18/011))

* Adam B. Barrett, _M-Theory on Manifolds with $G_2$ Holonomy_ ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))

 

 * [[James Halverson]], David Morrison, _The Landscape of M-theory Compactifications on Seven-Manifolds with $G_2$ Holonomy_ ([arXiv:1412.4123](http://arxiv.org/abs/1412.4123))

The corresponding [[membrane]] [[instanton]] corrections to the [[superpotential]] are discussed in 

* {#HarveyMoore99} [[Jeffrey Harvey]], [[Greg Moore]], _Superpotentials and Membrane Instantons_ ([arXiv:hep-th/9907026](http://arxiv.org/abs/hep-th/9907026))

* {#BBS07} [[Katrin Becker]], [[Melanie Becker]], [[John Schwarz]], p. 333 of _String Theory and M-Theory: A Modern Introduction_, 2007

A survey of the corresponding [[string phenomenology]] is in

* [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

the [[hierarchy problem]] is discussed in

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], Piyush Kumar, Diana Vaman, _An M theory Solution to the Hierarchy Problem_, Phys.Rev.Lett.97:191601,2006 ([arXiv:hep-th/0606262](http://arxiv.org/abs/hep-th/0606262))

the [[moduli space]] and [[moduli stabilization]] is discussed in

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _Explaining the Electroweak Scale and Stabilizing Moduli in M Theory_, Phys.Rev.D76:126010,2007 ([arXiv:hep-th/0701034](http://arxiv.org/abs/hep-th/0701034))

* {#GrigorianYau08} [[Sergey Grigorian]], [[Shing-Tung Yau]], _Local geometry of the $G_2$ moduli space_, Commun.Math.Phys.287:459-488,2009 ([arXiv:0802.0723](http://arxiv.org/abs/0802.0723))

* {#AcharyaBobkov08} [[Bobby Acharya]], Konstantin Bobkov, _K&#228;hler Independence of the G2-MSSM_, HEP 1009:001,2010 ([arXiv:0810.3285](http://arxiv.org/abs/0810.3285))

* [[Spiro Karigiannis]], [[Naichung Conan Leung]]_, _Hodge Theory for G2-manifolds: Intermediate Jacobians and Abel-Jacobi maps_, Proceedings of the London Mathematical Society (3) 99, 297-325 (2009) ([arXiv:0709.2987](http://arxiv.org/abs/0709.2987) [talk slides pdf](http://www.math.uwaterloo.ca/~karigian/talks/g2modulispace.pdf)


the [[strong CP problem]] is discussed in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], section 6 of _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))


* [[Bobby Acharya]], Konstantin Bobkov, [[Piyush Kumar]], _An M Theory Solution to the Strong CP Problem and Constraints on the Axiverse_, JHEP 1011:105,2010 ([arXiv:1004.5138](http://arxiv.org/abs/1004.5138))

and realization of [[GUTs]] in

* {#Witten02} [[Edward Witten]], _Deconstruction, $G_2$ Holonomy, and Doublet-Triplet Splitting_, ([arXiv:hep-ph/0201018](http://arxiv.org/abs/hep-ph/0201018))

* [[Bobby Acharya]], Krzysztof Bozek, Miguel Crispim Romao, Stephen F. King, Chakrit Pongkitivanichkul, _$SO(10)$ Grand Unification in M theory on a $G_2$ manifold_ ([arXiv:1502.01727](http://arxiv.org/abs/1502.01727))

[[!redirects G2 compactifications of M-theory]]