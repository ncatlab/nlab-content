
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For classes of [[gauge theories]], such as ([[super Yang-Mills theory|super]]) [[Yang-Mills theory]] or [[Chern-Simons theory]] or various [[matrix models]],  whose [[gauge groups]] may be $N \times N$ [[square matrices]] for any [[natural number]] $N$, notably in the [[special unitary group]] $SU(N)$, the [[special orthogonal group]] $SO(N)$ or the [[quaternionic unitary group]] ("symplectic group") $Sp(N)$, one may consider the [[limit of a sequence|limit]] of the theory's [[scattering amplitudes]] and other [[quantum observables]] as $N\to \infty$ ("large [[number of colours]]-limit"). In good cases the values close to but away from this _large $N$ limit_ scale with $1/N$ and allow a [[perturbation series]] around the large $N$ limit called the _$1/N$ expansion_.

This _large $N$ limit_ often has remarkable properties, often revealing an otherwise hidden relation to [[perturbative string theories]] with the parameter $1/N$ proportional to the [[string coupling constant]].

Notably for [[Yang-Mills theory]] and in particular for [[QCD]], the large $N$-behaviour is exhibited by rewriting the [[Feynman amplitudes]] in [['t Hooft double line notation]]. If the [['t Hooft coupling]] $g^2 N$  is held fixed as $N\to \infty$, this turns out to organize the gauge theory's [[Feynman perturbation series]] by the [[Euler characteristic]]/[[genus of a surface|genus]] of emerging [[string theory|string]] [[worldsheet]] [[surfaces]], with genus 0 ([[planar graphs]]) dominating in the large $N$ limit, whence also called the _[[planar limit]]_.

([[open/closed string duality|Open/closed string duality]] plays a subtle role in interpreting the [['t Hooft double line notation]] of [[gauge theory]] [[Feynman diagrams]] in the [[large N limit]] alternatively as [[open string]] or as [[closed string]] [[worldsheets]], see [Gopakumar-Vafa 98](#GopakumarVafa98), [Gaiotto-Rastelli 05](#GaiottiRastelli05), [Gopakumar 04](#Gopakumar04) and notably
[Marino 04, Section III, p. 14](#Marino04)).

At least for the case of [[super Yang-Mills theories]] the full statement of the relation of large-$N$ gauge theory to a [[perturbative string theory]] is the content of the _[[AdS/CFT correspondence]]_, which explains that the effective [[string]] [[worldsheets]] emerging from the [[gauge theory]] propagate in a higher-dimensional asymptotically [[anti-de Sitter spacetime]] (the [[near horizon geometry]] of a [[black brane]]) whose [[asymptotic boundary]] (the [[worldvolume]] of the [[black brane]] itself) is identified with the [[spacetime]] of the original [[gauge theory]].

An extreme case of this large $N$-limit is that of the [[BFSS matrix model]] in [[AdS2/CFT1 duality]] where _all_ spatial dependence of [[field (physics)|fields]] in the higher dimensional spacetime is supposedly encoded in the [[quantum mechanics]] of $N\times N$ [[matrix model|matrices]] as $N\to \infty$. And for the [[IKKT matrix model]] this includes also the temporal dependence.

For non-[[supersymmetry|supersymmetric]] [[gauge theories]] such as [[QCD]] this [[duality in string theory|duality]] still holds in suitably adjusted form such as in the _[[AdS/QCD correspondence]]_. Here the $1/N$-expansion serves to provide a computational tool for describing [[confinement|confined]] [[hadron]] states ([[mesons]] and [[baryons]], hence in particular [[nucleons]] and hence ordinary room-temperature [[matter]]) which are not seen by ordinary [[perturbative quantum field theory|perturbation theory]] in the gauge theory [[coupling constant]] (the [[confinement]]/[[mass gap problem]]).


## Related concepts

* [[planar limit]]

* [[large 1/N limit]]

* [['t Hooft coupling]]

* [[light-cone gauge quantization]]

* [[AdS-CFT duality]]

* [[BFSS matrix model]]

* [[volume conjecture]]



## References

### General


The original article observing the large $N$-behaviour and the [[planar limit]] of [[Yang-Mills theory]] in [['t Hooft double line notation]] is:

* {#tHooft74} [[Gerard 't Hooft]], _A Planar Diagram Theory for Strong Interactions_, Nucl. Phys. B72 (1974) 461 ([spire:80491](http://inspirehep.net/record/80491), <a href="https://doi.org/10.1016/0550-3213(74)90154-0">doi:10.1016/0550-3213(74)90154-0</a>)

First inkling of [[holographic QCD]] and [[matrix models]]:

* {#EguchiKawai82} [[Tohru Eguchi]], [[Hikaru Kawai]], _Reduction of dynamical degrees of freedom in the large-$N$ gauge theory_, Phys. Rev. Lett. 48, 1063 (1982) ([spire:176459](http://inspirehep.net/record/176459), [doi:10.1103/PhysRevLett.48.1063](https://doi.org/10.1103/PhysRevLett.48.1063))


* A. Gonzalez-Arroyo, M. Okawa, _A twisted model for large $N$ lattice gauge theory_, Physics Letters B120:1--3 (1983) 174--178 (<a href="https://doi.org/10.1016/0370-2693(83)90647-0">doi:10.1016/0370-2693(83)90647-0</a>)

* A. Gonzalez-Arroyo, M. Okawa, _Twisted-Eguchi-Kawai model: A reduced model for large-
$N$ lattice gauge theory_, Phys. Rev. D 27, 2397 (1983) ([doi:10.1103/PhysRevD.27.2397](https://doi.org/10.1103/PhysRevD.27.2397))

First observation that various observables in [[QCD]] for $N=3$ are actually well-approximated by the large $N$-limit:

* {#LuciniTeper01} B. Lucini, M. Teper, *SU(N)* gauge theories in four dimensions: exploring the approach to $N = \infty$, JHEP 0106 050 (2001) &lbrack;[doi:10.1088/1126-6708/2001/06/050](https://doi.org/10.1088/1126-6708/2001/06/050)&rbrack;

See:


* [[Edward Witten]], *Some Milestones in the Study of Confinement*, talk at *[[Prospects in Theoretical Physics 2023 -- Understanding Confinement]]*, IAS (2023) &lbrack;[web](https://www.ias.edu/video/some-milestones-study-confinement), [YT](https://youtu.be/TvIz-6YOdKs)&rbrack;

  > [26:26](https://youtu.be/TvIz-6YOdKs?t=1586): "by now it's clear &lbrack;[Lucini & Teper 2001](large+N+limit#LuciniTeper01)&rbrack; that [[lattice gauge theory]], at least for the [[glueball]] sector, has made it clear that the [[large N limit|$1/N$-expansion]] is a good approximation to the real world, especially if you include a leading correction to the [[large N limit|large $N$ limit]]. Now unfortunately this is best established in the [[glueball]] sector, which is not very accessible experimentally."
  
  > [28:56](https://youtu.be/TvIz-6YOdKs?t=1736): "but the $1/N$ expansion doesn't explain everything. In fact, it's not hard to find phenomena in meson physics where the $1/N$-expansion does *not* work well."

  > [36:15](https://youtu.be/TvIz-6YOdKs?t=2175): "I suspect the [[large N limit|$1/N$-expansion]] works reasonably well for many aspects of [[baryons]]. However, as for [[mesons]], it is easy to point to things that won't work well for baryons. In particular, among other things, I don't think the [[large N limit|$1/N$ expansion]] will be successful for [[nuclei]] as opposed to individual [[nucleons]]."

  > [37:12](https://youtu.be/TvIz-6YOdKs?t=2232): "I don' t think the phenomenological models used by nuclear physicists would have any success at of if the [[large N limit]] was a good description of [[nuclei]]."



Lecture notes and other reviews:

* [[Sidney Coleman]], _$1/N$_, 

  in: A. Zichichi  (ed.) _Pointlike Structures Inside and Outside Hadrons_. The Subnuclear Series, vol 17. Springer 1982 ([doi:10.1007/978-1-4684-1065-5_2](https://doi.org/10.1007/978-1-4684-1065-5_2))

  and Chapter 8 in: [[Sidney Coleman]], _Aspects of Symmetry_, Cambridge University Press 1985 ([doi:10.1017/CBO9780511565045.009](https://doi.org/10.1017/CBO9780511565045.009))

* [[Gerard 't Hooft]], _Large $N$_, workshop lecture ([hep-th/0204069](http://arxiv.org/abs/hep-th/0204069))

* A. V. Manohar, _Large $N$ QCD_, Les Houches Lecture 2004, (arXiv:[hep-ph/9802419](https://arxiv.org/abs/hep-ph/9802419), [pdf](http://einstein.ucsd.edu/manohar/pdf/LesHouches.pdf))

* Markus Gross, _Large $N$_ (2006) &lbrack:[[GrossLargeN.pdf:file]]&rbrack;

* {#McGreevySwingle08} McGreevy, Swingle, _Large $N$ counting_ (2008) &lbrack;[[GreevySwingle.pdf:file]]&rbrack;

* [[Paul Romatschke]], *Quantum Field Theory in Large $N$ Wonderland: Three Lectures* &lbrack;[arXiv:2310.00048](https://arxiv.org/abs/2310.00048)&rbrack;

* Francesco Giacosa, *Introductory visual lecture on QCD at large-$N_c$: bound states, chiral models, and phase diagram* &lbrack;[arXiv:2402.14097](https://arxiv.org/abs/2402.14097)&rbrack;

* Leonardo Santilli: *Large $N$ limits of supersymmetric quantum field theories: A pedagogical overview* &lbrack;[arXiv:2501.05794](https://arxiv.org/abs/2501.05794)&rbrack;





See also:

* Wikipedia, _[1/N expansion](http://en.wikipedia.org/wiki/1/N_expansion)_

* E. Br&#233;zin, S.R. Wadia, eds. _The Large $N$ Expansion in Quantum Field Theory and Statistical Physics_, a book collection of reprinted historical articles, [gBooks](http://books.google.com/books?id=4TbOUqWBf-IC)

Application of [[WKB method]]:

* [[V. P. Maslov]], O. Yu. Shvedov, _Large-N expansion as a semiclassical approximation to the third-quantized theory_, Physical Review D60(10) 105012 [doi](https://doi.org/10.1103/PhysRevD.60.105012)

The refinement for [[super Yang-Mills theory]] to the [[AdS/CFT correspondence]] (see there for more) originates with

* [[Juan Maldacena]], _The large $N$ limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys.2:231-252, 1998 [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); _Wilson loops in large N field theories_, hep-th/9803002. 

reviewed for instance in 

* {#Maldacena97a} [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998 ([hep-th/9711200](http://arxiv.org/abs/hep-th/9711200))

But see at _[[AdS/CFT correspondence]]_ for a more comprehensive list of references.

Further discussion:

* {#Witten79} [[Edward Witten]], _Baryons in the $1/n$ Expansion_, Nucl. Phys. B160 (1979) 57--115 ([spire:140391](http://inspirehep.net/record/140391), <a href="https://doi.org/10.1016/0550-3213(79)90232-3">doi:10.1016/0550-3213(79)90232-3</a>)

  (on [[mesons]] and [[baryons]] in the [[large N limit]])



* A. Jevicki, _Instantons and the $1/N$ expansion in nonlinear $\sigma$ models_, Phys. Rev. D 20, 3331--3335 (1979) [pdf](http://prd.aps.org/pdf/PRD/v20/i12/p3331_1)

* Laurence G. Yaffe, _Large $N$ limits as classical mechanics_, Rev. Mod. Phys. __54__, 407--435 (1982) ([pdf](http://rmp.aps.org/pdf/RMP/v54/i2/p407_1))

* [[Alexander A. Migdal]], _Loop equations and $1/N$ expansion_, Physics Reports **102** (4) 199-290 (1983) &lbrack;<a href="https://doi.org/10.1016%2F0370-1573%2883%2990076-5">doi</a>&rbrack;


* M. Bershadsky, Z. Kakushadze, [[Cumrun Vafa]], _String expansion as large $N$ expansion of gauge theories_, Nucl.Phys. B523 (1998) 59--72 ([hep-th/9803076](http://arxiv.org/abs/hep-th/9803076), <a href="http://dx.doi.org/10.1016/S0550-3213(98)00272-7">doi</a>)

* [[Gary Horowitz]], [[Hirosi Ooguri]], _Spectrum of large $N$ gauge theory from supergravity_, hep-th/9802116

* S. Sinha, [[Cumrun Vafa]], _$SO$ and $Sp$ Chern-Simons at Large $N$_ ([arXiv:hep-th/0012136](https://arxiv.org/abs/hep-th/0012136))

  (for [[Chern-Simons theory as a topological string theory]])

* Hiroyuki Fuji, Yutaka Ookouchi, _Confining Phase Superpotentials for $SO/Sp$ Gauge Theories via Geometric Transition_, JHEP 0302:028, 2003 ([arXiv:hep-th/0205301](https://arxiv.org/abs/hep-th/0205301))

* {#OoguriVafa02} [[Hirosi Ooguri]], [[Cumrun Vafa]], _Worldsheet derivation of a large $N$ duality_, Nucl. Phys. B641:3--34, 2002 ([arXiv:hep-th/0205297](https://arxiv.org/abs/hep-th/0205297))

* Semyon Klevtsov, _Random normal matrices, Bergman kernel and projective embeddings_,  J. High Energ. Phys. 2014, 133 (2014) <a href="https://doi.org/10.1007JHEP01(2014)133">doi</a> [arXiv:1309.7333](https://arxiv.org/abs/1309.7333)

* Jan Albert, Johan Henriksson, [[Leonardo Rastelli]], Alessandro Vichi, *Bootstrapping mesons at large $N$: Regge trajectory from spin-two maximization* &lbrack;[arXiv:2312.15013](https://arxiv.org/abs/2312.15013)&rbrack;


On a kind of [[BV-quantization]] of the [[Loday-Quillen-Tsygan theorem]] and relating to the [[large N limit|large $N$-limit]] of [[Chern-Simons theory]]:

* [[Grégory Ginot]], [[Owen Gwilliam]], [[Alastair Hamilton]], [[Mahmoud Zeinalian]], _Large $N$ phenomena and quantization of the Loday-Quillen-Tsygan theorem_, Adv. Math. __409A__ (2022) 108631 &lbrack;[arXiv:2108.12109](https://arxiv.org/abs/2108.12109), [doi:10.1016/j.aim.2022.108631](https://doi.org/10.1016/j.aim.2022.108631)&rbrack;
* [[Owen Gwilliam]], [[Alastair Hamilton]], [[Mahmoud Zeinalian]], _A homological approach to the Gaussian Unitary Ensemble_, [arXiv:2206.04256](https://arxiv.org/abs/2206.04256)

On the [[logical equivalence]] between the [[four-colour theorem]] and a statement about transition from the [[small N limit]] to the [[large N limit]] for [[Lie algebra weight systems]] on [[Jacobi diagrams]] via the [['t Hooft double line construction]]:

* [[Dror Bar-Natan]], _Lie Algebras and the Four Color Theorem_, Combinatorica 17-1(1997) 43--52  ([arXiv:q-alg/9606016](https://arxiv.org/abs/q-alg/9606016), [doi:10.1007/BF01196130](https://doi.org/10.1007/BF01196130))

On the [[large N limit]] in [[lattice gauge theory]]:

* Margarita Garcia Perez, _Prospects for large $N$ gauge theories on the lattice_ ([arXiv:2001.10859](https://arxiv.org/abs/2001.10859))

See also:

* Marco Bochicchio, Mauro Papinutto, Francesco Scardino, *On the structure of the large-$N$ expansion in $SU(N)$ Yang-Mills theory* &lbrack;[arXiv:2401.09312](https://arxiv.org/abs/2401.09312)&rbrack;



### Open/closed string duality

On the role of [[open/closed string duality]] in interpreting the [[large N limit]]:

* {#GopakumarVafa98} [[Rajesh Gopakumar]], [[Cumrun Vafa]], _On the Gauge Theory/Geometry Correspondence_, Adv. Theor. Math. Phys. 3 (1999) 1415--1443 ([arXiv:hep-th/9811131](https://arxiv.org/abs/hep-th/9811131))


* {#GaiottiRastelli05} [[Davide Gaiotto]], [[Leonardo Rastelli]], _A paradigm of open/closed duality: Liouville D-branes and the Kontsevich model_, JHEP 0507:053,2005 ([hep-th/0312196](https://arxiv.org/abs/hep-th/0312196))

> Nowadays we interpret $[$ the [['t Hooft double line notation]] $]$ quite literally as the perturbative expansion of an open string theory, either because the full open string theory is just equal to the gauge
theory (as e.g. for Chern-Simons theory [27]), or because we take an appropriate
low-energy limit (as e.g. for N = 4 SYM [31]).

> The general speculation [1] is that upon summing over the number of holes, (1.1) can be recast as the genus expansion for some closed string theory of coupling $g_s = g_{YM}^2$. This speculation is sometimes justified by appealing to the intuition that diagrams with
a larger and larger number of holes look more and more like smooth closed Riemann surfaces. This intuition is perfectly appropriate for the double-scaled matrix models, where the finite N theory is interpreted as a discretization of the closed Riemann surface; to recover the continuum limit, one must send $N\to \infty$ and tune $t$ to the
critical point $t_c$ where diagrams with a diverging number of holes dominate.

>  However, in AdS/CFT, or in the Gopakumar-Vafa duality [2], $t$ is a free parameter, corresponding on the closed string theory side to a geometric modulus. The intuition described above clearly goes wrong here. 

> A much more fitting way in which the open/closed duality may come about in these cases is for each fatgraph of genus g and
with h holes to be replaced by a closed Riemann surface of the same genus g and with h punctures: each hole is filled and replaced by a single closed string insertion.

* {#Gopakumar04} [[Rajesh Gopakumar]], _Free Field Theory as a String Theory?_, Comptes Rendus Physique 5 (2004) 1111-1119 ([hep-th/0409233](https://arxiv.org/abs/hep-th/0409233))

* {#Marino04} [[Marcos Marino]], _Chern-Simons Theory and Topological Strings_, Rev. Mod. Phys. 77:675-720, 2005 ([arXiv:hep-th/0406005](https://arxiv.org/abs/hep-th/0406005))

In relation to [[quantum error correction]]:

* Alexey Milekhin, *Quantum error correction and large $N$* ([arXiv:2008.12869](https://arxiv.org/abs/2008.12869))






category: physics

[[!redirects large N limit]]
[[!redirects large N limits]]
[[!redirects large-N limit]]
[[!redirects large-N limits]]
[[!redirects large n limit]]
[[!redirects large n limits]]
[[!redirects large-n limit]]
[[!redirects large-n limits]]
[[!redirects large N expansion]]
[[!redirects large N expansions]]
[[!redirects large-N expansion]]
[[!redirects large-N expansions]]
[[!redirects large n expansion]]
[[!redirects large n expansions]]
[[!redirects large-n expansion]]
[[!redirects large-n expansions]]

[[!redirects 1/N expansion]]
[[!redirects 1/N expansions]]

[[!redirects 't Hooft limit]]
[[!redirects 't Hooft limits]]



