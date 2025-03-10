+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[compact Lie group]] and $\Sigma$ a [[surface]], the _Hitchin connection_ ([Hitchin 90](#Hitchin90)) is a [[projectively flat connection]] over the [[moduli space of Riemann surfaces]] $\mathcal{M}_\Sigma$ whose [[fiber]] over a [[complex structure]] on $\Sigma$ is a [[space of quantum states]] which [[quantization of Chern-Simons theory]] for [[gauge group]] $G$ assigns to the induced [[Kähler polarization]] on the [[moduli space of flat connection]] $Loc_G(\Sigma)$ (the [[phase space]] of [[Chern-Simons theory]]), hence whose fiber is the space of [[holomorphic sections]] of the [[prequantum line bundle]] of the CS theory with respect to the induced K&#228;hler structure on $Loc_G(\Sigma)$ (induced, for abelian $G$, via the [Weil complex structure](intermediate+Jacobian#WeilIntermediateJacobian) and in the general nonabelian case via the [[Narasimhan-Seshadri theorem]]/[[Donaldson-Uhlenbeck-Yau theorem]]).

Therefore the existence and (projective) flatness of the Hitchin connection exhibits the relative independence of the [[geometric quantization]] of [[Chern-Simons theory]] from the choice of [[polarization]]. 

The Hitchin connection is akin to the _[[Knizhnik-Zamolodchikov connection]]_, which is built by thinking [[AdS3-CFT2 and CS-WZW correspondence|holographic dually]] of the vector bundle of [[conformal blocks]] of the corresponding $G$-[[Wess-Zumino-Witten model]] [[2d CFT]] on $\Sigma$. 

A more axiomatic characterization of such projectively flat connections in terms of [[modular functors]] is due to [Segal 88, prop. 5.4](#Segal88). See [Segal 88, around (5.9)](#Segal88) for discussion of how to turn these projectively flat connections into genuine [[flat connections]].

Reviews of the Hitchin connection include [Lauridsen 10, section 2](#Lauridsen10).

## Related concepts

* [[quantization of Chern-Simons theory]]

* [[AdS3-CFT2 and CS-WZW correspondence]]

* [[modular functor]]


## References


The original article is 

* {#Hitchin90} [[Nigel Hitchin]], _Flat connections and geometric quantization_, : Comm. Math. Phys. Volume 131, Number 2 (1990), 347-380. ([Euclid](http://projecteuclid.org/euclid.cmp/1104200841))
 
(What is now called the Hitchin connection appears in theorem 3.6 there, its expression in local coordinates is around (3.15). That for abelian gauge group $U(1)$ the classical [[Riemann theta functions]] constitute the covariantly constant sections of the Hitchin connection in these coordinates is remark 4.12.)

More axiomatic/abstract discussion of these projectively flat connections in terms of [[modular functors]] is in 

* {#Segal88} [[Graeme Segal]], section 5 of _The definition of conformal field theory_ , preprint, 1988; also in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ , London Math. Soc. Lect. Note Ser., Vol. 308. Cambridge University Press, Cambridge (2004) 421-577. ([pdf](https://people.maths.ox.ac.uk/segalg/0521540496txt.pdf)) 


More explicit expressions are discussed in 

* Bert van Geemen, [[Aise Johan de Jong]], _On Hitchin's Connection_ ([arXiv:alg--geom/9701007](http://arxiv.org/abs/alg--geom/9701007))

A nice review and new concise account is in 

* {#Looijenga10} [[Eduard Looijenga]], _From WZW models to Modular Functors_ ([arXiv:1009.2245](http://arxiv.org/abs/1009.2245))

* {#Andersen11} Johan Martens [[Jørgen Andersen]], notes by S&#248;ren J&#248;rgensen, section 1.2.1 and 4 of _Topological quantum field theories and moduli spaces_, 2011 ([pdf](http://maths.fuglede.dk/noter/tqftms.pdf))

Discussion for [[deformation quantization]] instead of [[geometric quantization]] is in 

* [[Jørgen Andersen]], _Hitchin's connection, Toeplitz operators and symmetry invariant deformation quantization_ ([arXiv:math/0611126](http://arxiv.org/abs/math/0611126))

This also reproduces the original construciton in the context of [[Chern-Simons theory]] in 

* {#AxelrodPietraWitten91} [[Scott Axelrod]], S. Della Pietra, [[Edward Witten]], _Geometric quantization of Chern-Simons gauge theory_, Jour. Diff. Geom. 33 (1991), 787-902.  ([EUCLID](http://projecteuclid.org/euclid.jdg/1214446565))
 

More details (on [[metaplectic correction]]) and generalization to connections over more general manifolds are in 

* {#ScheinostSchottenloher96} Peter Scheinost, [[Martin Schottenloher]], _Metaplectic quantization of the moduli spaces of flat and parabolic bundles_, J. reine angew. Mathematik, 466 (1996) ([web](https://eudml.org/doc/153753))
 

Similar generalization away from [[moduli spaces of flat connections]] to general [[symplectic manifolds]] with [[Kähler structure]] on them is also in

* {#Lauridsen10} Lauridsen, _Aspects of quantum mathematics  -- Hitchin connections and the AJ conjecture_, PhD thesis Aarhus 2010 ([pdf](http://pure.au.dk/portal/files/41741925/imf_phd_2010_mrl.pdf))

Relation between the Hitchin connection and bundles of [[conformal blocks]] is discussed in 

* {#Laszlo98} [[Yves Laszlo]] _Hitchin's and WZW connection are the same_, J. Differential Geom. 49 (1998), no. 3, 547&#8211;576 ([pdf](http://www.emis.de/journals/NYJM/JDG/archive/vol.49/3_5.pdf))

For more on this see at _[[quantization of 3d Chern-Simons theory]]_.
 

[[!redirects Hitchin connections]]
