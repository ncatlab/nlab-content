
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

(See [Baez-Huerta 09, p. 33-36](#BaezHuerta09) for a fairly comprehensive discussion. See also e.g. [HMY 13, p. 2](#HMY13).)

The exact gauge group (eq:ExactGSM) happens to coincide with 

1. $S\big(U(2) \times U(3)\big) \subset SU(5)$ -- this is the basis of "[[grand unified theories]]" ([[GUT]]), speculative extensions of the standard model trying to understand its gauge group as being a [[spontaneously broken symmetry|spontaneously broken]] _[[simple Lie group]]_-[[symmetry]].

1. the [[subgroup]] of the [[Jordan algebra]] [[automorphism group]] of the [[octonions|octonionic]] [[Albert algebra]] that "[[stabilizer subgroup|stabilizes]] a 4d sub-[[Minkowski spacetime]]" (see [there](Albert+algebra#StabilizerOf4dMinkowskiInsideOctonionicAlbertAlgebra) for details) -- this is part of ongoing speculation that exceptional [[octonion|octonionic]] structures might be behind the standard model.

## Variations and generalizations

There is a plethora of attempts and suggestions for variations and generalizations of the standard model into models that are conceptually more satisfying from the point of view of models in theoretical physics. 

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

* [[G2-MSSM]]




## Related concepts

* [[generation of fundamental particles]]

* [[Yang-Mills theory]]

  * [[QCD]], [[electroweak field]], [[electromagnetism]]

* [[technicolor]], [[supersymmetry]]

* [[Grand Unified Theory]], [[theory of everything]]

* [[gauge coupling unification]]

* [[LHC]]

* [[phenomenology]], [[hierarchy problem]]

* [[MSSM]]

  * [[G2-MSSM]]

* [[intersecting D-brane model]]

* [[standard model of cosmology]]


* [string theory FAQ -- Did string theory provide any insight relevant in experimental particle physics?](string+theory+FAQ#InsightInParticlePhysics)

[[!include standard model of fundamental physics - table]]

## References

A clean survey and gentle introduction is given in

* {#BaezHuerta09} [[John Baez]], [[John Huerta]], _The Algebra of Grand Unified Theories_, Bull.Am.Math.Soc.47:483-552,2010 ([arXiv:0904.1556](http://arxiv.org/abs/0904.1556))

Textbook accounts include

*  [[Paul Langacker]], _The Standard Model and Beyond_, CRC Press 2009 ([webpage](http://www.sns.ias.edu/~pgl/SMB/))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 1 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

See also

* [[Alain Connes]], [[Matilde Marcolli]], chapter I, section 12 _[[Noncommutative Geometry, Quantum Fields and Motives]]_

Review combined with outlook is provided in 

* Dmitry Kazakov, _Beyond the Standard Model' 17_ ([arXiv:1807.00148](https://arxiv.org/abs/1807.00148))

A historical account is in 

* [[Tom Kibble]], _The Standard Model of Particle Physics_ ([arXiv:1412.4094](http://arxiv.org/abs/1412.4094))

There are tons of textbooks about the standard model, so any recommendation is hopelessly biased. The following textbook is a short and relativly easy introduction that nevertheless covers a lot of ground:

* Cottingham, W. Noel; Greenwood, Derek A.: _An introduction to the standard model of particle physics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1126.81002&format=complete))

See also

* {#HMY13} Takaaki Hashimoto, Mamoru Matsunaga, Kenta Yamamoto, _Quantization of hypercharge in gauge groups locally isomorphic but globally nonisomorphic to $SU(3)_c \times SU(2)_L \times U(1)_Y$_ ([arXiv:1302.0669](https://arxiv.org/abs/1302.0669))

For further references see [[quantum field theory]] and the Wikipedia entry

* Wikipedia, _[standard model] (http://en.wikipedia.org/wiki/Standard_Model)_