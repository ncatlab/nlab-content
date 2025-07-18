
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **standard [[model (in particle physics)|model]] of [[particle physics]]** is a [[model (in particle physics)]]: a [[quantum field theory]] that describes the _[[fundamental particles]]_ currently experimentally known, containing 

* **[[matter]]**: [[electrons]], [[neutrinos]], [[quarks]] and other [[fermions]], 

as well as three of the four _fundamental [[forces]]_ as currently known, which, somewhat roughly, are

* **[[force]]**:  the [[electroweak field|electroweak force]] (including [[electromagnetism]]) and the [[strong nuclear force]].

It is defined as a [[local Lagrangian]] [[field (physics)|field]] [[theory (physics)|theory]] which is an  [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]].

The main ingredient missing from the standard model is the [[quantum physics|quantum]] version of the field of [[gravity]]. For decades, a large part of theoretical physics has been absorbed with attempts to understand how this last of the known fundamental forces might fit into the picture.

As a [[quantum field theory]], the standard model is in particular a [[Yang-Mills theory|Yang–Mills]] [[gauge theory]] with [[spinors in Yang-Mills theory|spinors in Yang–Mills theory]]. 

Although there are several approaches to formulate a mathematically precise definition of what a [[quantum field theory]] is, there is no rigorous formulation (yet) that comprises the whole standard model. 

## Properties

### Gauge group
  {#GaugeGroup}

The _exact_ [[gauge group]] of the standard model is not quite the [[product group]]

$$
  U(1) \times SU(2) \times SU(3)
$$

of the [[circle group]] with [[special unitary groups]], but is the [[quotient group]] 

\[
  \label{ExactGSM}
  G_{SM} 
  \;=\;
  \big(
    U(1) \times SU(2) \times SU(3)
  \big)
  / \mathbb{Z}_6
\]

of that by a [[cyclic group]] $\mathbb{Z}_6 \subset U(1) \times SU(2) \times SU(3)$ which is the [[subgroup]] [[generators and relations|generated]] from an element of the form

$$
  (q_6, q_2 \mathbf{1}_2, q_3 \mathbf{1}_3) \;\in\;
  U(1) \times SU(2) \times SU(3)
  \,,
$$

where $q_n \in U(1)$ denotes an $n$th [[primitive root of unity]], i.e. 

$$
  \left(
    e^{2 \pi i \tfrac{1}{6}}
    \;,\; 
    e^{2 \pi i \tfrac{1}{2}} \mathbf{1}_2\;,\; 
    e^{2 \pi i \tfrac{1}{3}} \mathbf{1}_3
  \right) 
  \;\in\;
  U(1) \times SU(2) \times SU(3)
  \,.
$$

(See [Baez-Huerta 09, p. 33-36](#BaezHuerta09) for a fairly comprehensive discussion; also e.g. [HMY 13, p. 2](#HMY13).

This is in the sense that all *known* [[elementary particles]] in the standard model are [[invariant]] under this $\mathbb{Z}/6$ subgroup. In principle it could be that as yet undetected heavy particles break this invariance after all, cf. [Li & Xu 2024](#LiXu24).)



Strikingly, this  exact gauge group (eq:ExactGSM) of the standard model of particle physics happens to coincide with... 

1. ...the group

   $$
      G_{SM} 
       \;\simeq\; 
      S\big(U(2) \times U(3)\big) 
       \;\subset\; 
      SU(5)
   $$ 

   of [[determinant]]-1 elements in the [[direct product group]] $U(2) \times U(3)$, which makes manifest that the standard model gauge group is a [[subgroup]] of the [[simple Lie group]] [[special unitary group|SU(5)]].

   This is the basis of "[[grand unified theories]]" ([[GUT]]), speculative extensions of the standard model trying to understand its gauge group as being a [[spontaneously broken symmetry|spontaneously broken]] _[[simple Lie group]]_-[[symmetry]].

1. ...the [[subgroup]] of the [[Jordan algebra]] [[automorphism group]] of the [[octonions|octonionic]] [[Albert algebra]] that "[[stabilizer subgroup|stabilizes]] a 4d sub-[[Minkowski spacetime]]" (see [there](Albert+algebra#StabilizerOf4dMinkowskiInsideOctonionicAlbertAlgebra) for details).

   More concretely, it is identified with the [[subgroup]] of [[Spin(9)]] which respects a splitting $\mathbb{H} \oplus \mathbb{H} \simeq_{\mathbb{R}} \mathbb{C} \oplus \mathbb{C}^3$ ([Krasnov 19](Spin%289%29#Krasnov19), see also at [SO(10)-GUT](GUT#TheGUTKnownAsSO10))



  This is part of ongoing speculation that  [[octonion|octonionic]] [[exceptional structures]] might be behind the standard model.

### Fermion content

[[!include flavors of fundamental particles -- table]]


## Tension with experiment and Incompleteness
 {#TensionWithExperiment}

The standard model of particle physics is supported by a tremendous level of confirmation by [[experiment]], lately by the [[LHC]] experiment. But there are indictations of discrepancies, pointing to "new physics". See at 

* [[flavour anomaly]]

* [[anomalous magnetic moment]] -- [anomalies](anomalous+magnetic+moment#Anomalies).

Not quite in tension with the standard model, but still possibly pointing to unaccounted effects is the 

* [[Higgs field]]-[metastability](Higgs+field#MassAndVacuumInstability).

Then there are experimental phenomena which are known to be implied by the standard model by way of computer simulation ([[lattice QCD]]), but which are not conceptually understood:

* [[confinement]] ([[mass gap problem]])

Finally there is the evident and notorious fact that the standard model simply does not include any [[quantum field theory]] of the fourth known fundamental [[force]], [[gravity]]. See at

* [[quantum gravity]]

for more on this.

<br/>

## Variations and generalizations

There is a plethora of attempts and suggestions for variations and generalizations of the standard model into models that may resolve the tension with experiment mentioned [above](#TensionWithExperiment) and which may be conceptually more satisfying from the point of view of models in theoretical physics. 

### Kaluza--Klein theory

Shortly after the conception of [[general relativity]], it was observed by Kaluza and Klein that the force of [[gravity]] alone may effectively appear -- if considered on a [[spacetime]] that is a [[bundle]] whose [[fiber]] has a tiny volume (as meaured by the [[Riemannian metric]]) -- as the field of gravity coupled to [[gauge field]]s on the base of the bundle. For details on this see [[Kaluza-Klein mechanism]].

The huge conceptual simplification that this observation suggested had excited theoreticians early on, but a problem of Kaluza--Klein models is that not only does the "compactified" theory of gravity as if by magic emulate [[gauge field]]s, but it also always contains further scalar fields that are _not_ experimentally observed. 

For that reason interest in Kaluza--Klein theories had decreased in the middle of the last century. Physics departments saw a major revival of the idea when [[string theory]] (see below) gained interest, since that theory necessarily exhibits a Kaluza--Klein mechanism. Incidentally, the problem of the spurious fields -- the moduli -- was still present in this approach. For more on this see the entry [[landscape of string theory vacua]].


### GUTs

One of the oldest studies of variations of the standard model is the investigation of [[GUT|grand unified theories]] (GUTs), which are [[Yang-Mills theory|Yang–Mills theories]] that instead of the standard model gauge group have a bigger gauge group which is however a [[simple group]].


### Noncommutative geometry
 {#NCGeometry}

A widespread perception is that some of the conceptual problems with the standard model point to the fact that some basic assumption of 20th century physics on the nature of reality is oversimplified. According to the approach of [[noncommutative geometry]], modeling [[spacetime]] as a smooth [[manifold]] is an oversimplification that makes itself felt when the quantization of the force of [[gravity]] becomes relevant.

In a class of "noncommutative" generalizations of the standard model, spacetime is therefore replaced more generally by a [[spectral triple]] that models a possibly "noncommutative space". One of the more successful approaches in this direction is the [[Connes-Lott-Chamseddine model]]. This effectively is a [[Kaluza-Klein theory]] (see above), but with the crucial difference that the fiber in the KK-picture is a highly non-classical non-commutative space, whose classical dimension is that of a point, but whose intrinsic dimension is 6. (This is incidentally the same value of the internal dimension as suggest by [[string theory]].)

For more on this see

* [[Urs Schreiber]], _Connes on Spectral Geometry of the Standard Model_ ([part I](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of.html), [part II](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_1.html) [part III](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_2.html), [part IV](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_3.html)) 



### String theory

A more drastic theoretical modifications to the standard model is proposed in the context of [[string theory]], where the entire concept of [[quantum field theory]] is proposed to be refined by something else. As opposed to [[GUTs]], this approach at least suggests a way in which also the fourth remaining force field of [[gravity]] could be incorporated into the picture.

See

* [[intersecting D-brane models]]

* [[G₂-MSSM]]




## Related concepts

* [[quantum field theory]]

  * [[perturbative quantum field theory]]

  * [[non-perturbative quantum field theory]]

* [[forces]]

  * [[electromagnetism]]

  * [[strong nuclear force]]

  * [[weak nuclear force]]

    * [[CKM matrix]]

* [[chiral fermions]]

* [[chiral perturbation theory]], [[quantum hadrodynamics]]

* [[flavor (particle physics)|flavoru]] [[generation of fundamental particles]]

* [[Yang-Mills theory]]

  * [[QCD]], [[electroweak field]], [[electromagnetism]]

* [[technicolor]], [[supersymmetry]]

* [[Grand Unified Theory]], [[theory of everything]]

* [[gauge coupling unification]]

* relevant [[experiments]]

  * [[LHC experiment]]

  * [[LHCb experiment]]

  * [[Belle collaboration]]

* anomalies

  * [anomalous magnetic moment of the muon](anomalous magnetic moment#Anomalies)

  * [[flavour anomaly]]

  * [[V_cb puzzle]]

* [[phenomenology]], [[hierarchy problem]]


* [[MSSM]]

  * [[G₂-MSSM]]

* [[intersecting D-brane model]]

* [[standard model of cosmology]]

* [string theory FAQ -- Did string theory provide any insight relevant in experimental particle physics?](string+theory+FAQ#InsightInParticlePhysics)

[[!include standard model of fundamental physics - table]]



## References


### General

The first actual statement of what came to be called the standard model is (cf. [Bjorken 1985](#Bjorken85)):

* [[John Iliopoulos]]: *Progress in Gauge Theories*, in: *High energy physics*, Proceedings, 17th International Conference, ICHEP 1974, London, England, July 01-July 10 (1974) III.89-116  &lbrack;[spire:3000](https://inspirehep.net/literature/3000), [pdf](https://inspirehep.net/files/a995da1bd7c951e14421df33810a9c43)&rbrack;

Early lecture notes in the broader context of [[gauge theories]]:

* [[John Iliopoulos]]: *An introduction to gauge theories*, Academic Training Lectures, Geneva (1975) &lbrack;[cds:185945](https://cds.cern.ch/record/185945?ln=en), [pdf](https://cds.cern.ch/record/185945/files/CERN-76-11.pdf)&rbrack;


Monographs:

* W. Noel Cottingham, Derek A. Greenwood: _An introduction to the standard model of particle physics_, Cambridge University Press (2012) &lbrack;[doi:10.1017/CBO9780511791406 ](https://doi.org/10.1017/CBO9780511791406 ), [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1126.81002&format=complete)&rbrack;

*  [[Paul Langacker]]: _The Standard Model and Beyond_, CRC Press (2009, 2012, second edition 2017) &lbrack;[spire:846915](http://inspirehep.net/record/846915/), [publisher webpage](https://www.crcpress.com/The-Standard-Model-and-Beyond/Langacker/p/book/9781498763219), [author webpage](http://www.sns.ias.edu/~pgl/SMB/)&rbrack;

* J. D. Vergados: *The Standard Model and Beyond*, World Scientific (2017) &lbrack;[doi:10.1142/10669](https://www.worldscientific.com/worldscibooks/10.1142/10669)&rbrack;

* [[John F. Donoghue]], Eugene Golowich, Barry R. Holstein: *Dynamics of the Standard Model*, Cambridge University Press (2022) &lbrack;[doi:10.1017/9781009291033](https://doi.org/10.1017/9781009291033), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/FF8A95F0F22A67FABA729DBB39BA2816/9781009291002AR.pdf)&rbrack;

* Wolfgang Bietenholz, Uwe-Jens Wiese: *Uncovering Quantum Field Theory and the Standard Model*, Cambridge University Press (2025) &lbrack;[ISBN:9781108472333](https://www.cambridge.org/highereducation/books/uncovering-quantum-field-theory-and-the-standard-model/D68C7687188CBD9111503A348A5E09FA)&rbrack;

Further review and introduction:

* [[Cliff Burgess]], Guy Moore: *The Standard Model -- A Primer*, Cambridge University Press (2011) &lbrack;[doi:10.1017/CBO9780511819698](https://doi.org/10.1017/CBO9780511819698), [pdf](https://physics.mcmaster.ca/~cburgess/Book/Ch1-6SnippetSM.pdf)&rbrack;

* [[Matthew Schwartz]], *Quantum Field Theory and the Standard Model*, Cambridge University Press (2014) &lbrack;[ISBN:9781107034730](https://www.cambridge.org/de/universitypress/subjects/physics/theoretical-physics-and-mathematical-physics/quantum-field-theory-and-standard-model?format=HB&isbn=9781107034730), [doi:10.1017/9781139540940](https://doi.org/10.1017/9781139540940), [pdf](https://indico.ihep.ac.cn/event/11134/attachments/3783/4308/QFT-Schwartz.pdf)&rbrack;


* [[Gerd Rudolph]], [[Matthias Schmidt]], Section 7.7 of: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

* Ben Gripaios, _Lectures: From quantum mechanics to the Standard Model_ ([arXiv:2005.06355](https://arxiv.org/abs/2005.06355))

* [[Tristan Hübsch]]: *The Standard Model*, chapter II of: *Advanced Concepts in Particle and Field Theory*, Cambridge University Press (2022) &lbrack;[doi:10.1017/9781009291507](https://doi.org/10.1017/9781009291507)&rbrack;

* [[Fernando Quevedo]], Andreas Schachner: *Cambridge Lectures on The Standard Model* &lbrack;[arXiv:2409.09211](https://arxiv.org/abs/2409.09211)&rbrack;


Mathematical ([[representation theory|representation theoretic]]) review with an eye towards [[grand unified theory]]:

* [[Howard Georgi]], *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

* {#BaezHuerta09} [[John Baez]], [[John Huerta]], _The Algebra of Grand Unified Theories_, Bull. Am. Math. Soc. 47:483-552, 2010 ([arXiv:0904.1556](http://arxiv.org/abs/0904.1556))

and with an eye towards [[intersecting D-brane models]]L

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 1 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press (2012)

and with emphasis of the [[effective field theories]] involved ([[chiral perturbation theory]], [Fermi's theory](effective+quantum+field+theory#FermiTheoryOfWeakInteractions)):

* [[Luis Alvarez-Gaumé]], [[Miguel A. Vázquez-Mozo]], *Lectures on Field Theory and the Standard Model: A Symmetry-Oriented Approach* &lbrack;[arXiv:2306.08097](https://arxiv.org/abs/2306.08097)&rbrack;

More on the issue of the exact gauge group:

* {#LiXu24} Hao-Lin Li, Ling-Xiao Xu, *Understanding the SM gauge group from SMEFT* &lbrack;[arXiv:2404.04229](https://arxiv.org/abs/2404.04229)&rbrack;



On [[subgroups]] of Clifford algebras reminiscent of [[gauge groups]] of relevance in the [[standard model of particle physics]] and [[grand unified theories]] thereof:

* {#Wilson20} [[Robert A. Wilson]], *A group-theorist's perspective on symmetry groups in physics* ([arXiv:2009.14613](https://arxiv.org/abs/2009.14613))

* {#Wilson21} [[Robert A. Wilson]], *On the Problem of Choosing Subgroups of Clifford Algebras for Applications in Fundamental Physics*, Adv. Appl. Clifford Algebras 31, 59 (2021) ([doi:10.1007/s00006-021-01160-5]( https://doi.org/10.1007/s00006-021-01160-5))

See also:

* [Albert algebra -- possible relation to color gauge structure](Albert+algebra#ReferencesRelationStandardModel)

* [[Alain Connes]], [[Matilde Marcolli]], chapter I, section 12 of _[[Noncommutative Geometry, Quantum Fields and Motives]]_


Review with outlook "beyond the standard model":

* [[Paul Langacker]], _The standard model and beyond_, talk at TPFNP 2005 ([pdf](http://www.sns.ias.edu/~pgl/talks/neutron.pdf), [[Langacker05.pdf:file]])

* Dmitry Kazakov, _Beyond the Standard Model' 17_ ([arXiv:1807.00148](https://arxiv.org/abs/1807.00148))

* {#Wulzer19} Andrea Wulzer, _Behind the Standard Model_ ([arXiv:1901.01017](https://arxiv.org/abs/1901.01017))

* [[James Wells]], _The Once and Present Standard Model of Elementary Particle Physics_ ([arxiv:1911.04604](https://arxiv.org/abs/1911.04604))



### Anomaly cancellation
 {#ReferencesAnomalyCancellation}

Discussion of [[anomaly cancellation]] on the [[standard model of particle physics]]:

* {#HMY13} Takaaki Hashimoto, Mamoru Matsunaga, Kenta Yamamoto, _Quantization of hypercharge in gauge groups locally isomorphic but globally nonisomorphic to $SU(3)_c \times SU(2)_L \times U(1)_Y$_ ([arXiv:1302.0669](https://arxiv.org/abs/1302.0669))


* Nakarin Lohitsiri, [[David Tong]], _Hypercharge Quantisation and Fermat's Last Theorem_ ([arXiv:1907.00514](https://arxiv.org/abs/1907.00514))

  (relating to [[Fermat's last theorem]])

### History
 {#ReferencesHistory}

* {#Bjorken85} [[James Bjorken]], _The November Revolution: A Theorist Reminisces_ (1985) &lbrack;[spire:214067](http://inspirehep.net/record/214067)&rbrack;

> "The big international conference of $[$1974$]$ in 
London was a turning point $[$...$]$ Ellis' catalog well reflected the state  of theoretical confusion and general disarray in trying to  interpret the $e^+ e^-$ data. But in the midst of all of this was a  talk by [[John Iliopoulos]] (I think I was there too). With  passionate zealotry, he laid out with great accuracy what we call the [[standard model of particle physics|standard model]]. Everything was there: [[proton decay]], [[charm quark|charm]],  the GIM mechanism of course, [[QCD]], the $SU(2)\times U(1)$ [[electroweak  theory]], $SU(5)$ [[GUT|grand unification]], [[Higgs field|Higgs]], etc. It was all presented with absolute conviction and sounded at the time just a little mad, at least to me (I am a conservative)."

* [[John Iliopoulos]]: *The rise of the Standard Model*, section 6 of: *Physics in the CERN theory division*, CHS-39, Geneva (1993) &lbrack;[cds:261679](https://cds.cern.ch/record/261679?ln=en), [pdf](https://cds.cern.ch/record/261679/files/CERN-CH-39.pdf)&rbrack;

* [[Tom Kibble]], _The Standard Model of Particle Physics_ &lbrack;[arXiv:1412.4094](http://arxiv.org/abs/1412.4094)&rbrack;

* {#Iliopoulos16} [[John Iliopoulos]]: _The making of the standard theory_, Adv. Ser. Direct. High Energy Phys. **26** (2016) 29-59 &lbrack;[spire:1497884](http://inspirehep.net/record/1497884), [pdf](http://cds.cern.ch/record/2217096/files/9789814733519_0002.pdf)&rbrack;

* [[Steven Weinberg]]: *The Conceptual Basis of the Standard Model: Steven Weinberg*, concluding talk at: *[The Standard Model at 50](https://artsci.case.edu/smat50/)*, 1-4 June 2018, Cleveland &lbrack;video:[YT](https://youtu.be/nydSHnv1ABI?list=PLBELrG1nZ2U6H3I1il4NhNVNcdUVUE5Ye)&rbrack;

* [[John Iliopoulos]]: *From Many Models to ONE THEORY*, talk at Plectics Labs Perspectives In Theoretical Physics Series (July 2024)  &lbrack;[arXiv:2501.10233](https://arxiv.org/abs/2501.10233), video:[YT](https://youtu.be/ECUBXySE0pI)&rbrack;






