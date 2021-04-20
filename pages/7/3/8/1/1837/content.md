
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A _gauge theory_ may denote either a [[classical field theory]] or a [[quantum field theory]] whose [[space of trajectories|field configurations]] are [[cocycles]] in [[differential cohomology]] ([[ordinary differential cohomology|abelian]] or [[Chern-Weil theory|nonabelian]]).

### Ordinary gauge theories

An _ordinary gauge theory_ is a [[quantum field theory]] whose field configurations are [[vector bundles]] 
[[connection on a bundle|with connection]].

This includes notably the [[field (physics)|fields]] that carry the three fundamental forces of the [[standard model of particle physics]]:

* Ordinary [[electromagnetism]] in the absence of magnetic charges is a gauge theory of $U(1)$-[[principal bundle]]s with [[connection on a bundle|connection]]. 

* Fields in [[Yang-Mills theory]] (such as appearing in the [[standard model of particle physics]] and in [[GUT]]s) are [[vector bundle]]s [[connection on a bundle|with connection]].

Other examples include formal physical models.

* [[Dijkgraaf-Witten theory]] is a gauge theory whose field configurations are $G$-[[principal bundle]]s for $G$ a finite group (these come with a unique [[connection on a bundle|connection]], so that in this simple case the connection is no extra datum).

The group $G$ in these examples is called the [[gauge group]] of the theory.

### Higher and generalized gauge theories 

The above examples of gauge fields consisted of cocycles in degree-$1$ [[differential cohomology]].

More generally, a _[[higher gauge theory]]_ is a [[quantum field 
theory]] whose field configurations are cocycles in more general [[differential cohomology]], for instance higher degree [[Deligne cohomology|Deligne cocycles]] or more generally cocycles in other differential refinements, such as in differential [[K-theory]].

This generalization does contain experimentally visible physics such as

* The [[magnetic current]] in [[electromagnetism]] is a [[bundle gerbe|bundle gerbe with connection]], a [[Deligne cohomology|Deligne cocycle]] refining a cocycle in degree-$3$ [[Eilenberg-MacLane spectrum|Eilenberg-MacLane cohomology]]: the _magnetic charge_ .

But a whole tower of higher and generalized gauge theories became visible with the study of higher [[supergravity]] theories,

* The [[Kalb-Ramond field]] is a [[bundle gerbe|bundle gerbe with connection]], a [[Deligne cohomology|Deligne cocycle]] with curvature 3-form.

* The [[supergravity C-field]] is a [[Deligne cohomology|Deligne cocycle]] with curvature 4-form.

* The [[RR-field]] is a cocycle in [[differential K-theory]].


### Gravity as a (non-)gauge theory

In the [[first order formulation of gravity]] also the theory of [[gravity]] looks a little like a gauge theory. However, there is a crucial difference. What really happens here is _[[Cartan geometry]]_: the field of gravity may be encoded in a [[vielbein]] field, namelely an [[orthogonal structure]] on the [[tangent bundle]], hence as an example of a [[G-structure]], and the [[torsion of a G-structure|torsion freedom]] of this G-structure may be encoded by an auxiliary [[connection on a bundle|connection]], namely a [[Cartan connection]], often called the "[[spin connection]]" in this context. Hence while in the formulation of [[Cartan geometry]] gravity is described by many of the ingredients from [[differential geometry]] that also govern pure gauge theory, it's not quite the same. In particular there is a constraint on a [[Cartan connection]], which in terms of [[vielbein]] fields is the constraint that the vielbein (which is part of the Cartan connection) is non-degenerate, and hence really a "[[soldering form]]". Such a constraint is absent in a "genuine" gauge theory such as [[Yang-Mills theory]] or [[Chern-Simons theory]].

## Properties

### Non-redundancy and locality

Sometimes one see the view expressed that [[gauge symmetry]] is "just a redundancy" in the description of a [[theory (physics)|theory of physics]], for instance in that among [[observables]] it is only the [[gauge invariance|gauge invariant]] ones which are physically meaningful.

This statement however

### Anomalies 

In the presence of [[magnetic charge]] (and then even in the absence of [[chiral fermion anomaly|chiral fermion anomalies]]) the standard would-be action functional for higher gauge theories may be ill-defined. The [[Green-Schwarz mechanism]] is a famous phenomenon in [[differential cohomology]] by which such a [[quantum anomaly]] cancels against that given by chiral fermions.

## List of gauge fields and their models

The following tries to give an overview of some collection of gauge fields in physics, their models by [[differential cohomology]] and further details.

* [[Yang-Mills field]]

  * cocycle in lowest degree [[schreiber:Differential Nonabelian Cohomology|nonabelian differential cohomology]]  

    * originally realized in terms of differential [[Čech cohomology|Čech cocycle]]s
      $$
        \hat F \in \mathbf{H}(X, \bar \mathbf{B} G)
      $$
      with coefficients in the [[groupoid of Lie-algebra valued forms]],
       
      then traditionally in terms of [[vector bundle]]s [[connection on a bundle|with connection]]

  * [[field strength]] depending on the [[group]] $G$ we have
  
    * $G = U(1)$ - [[electromagnetism]] (see below)

    * $G = SU(2)\times U(1)$ - electroweak force field strength

    * $G = SU(3)$ - strong nuclear force field

  * [[parallel transport]]: [[Wilson line]]s

* [[electromagnetic field]]

  * cocycle in degree-$2$ [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of Maxwell-Dirac presentation as a cocycle in [[Čech cohomology|Čech]]--[[Deligne cohomology|Deligne]] cocycle
      $$
        \hat F \in \mathbf{H}(X,\bar \mathbf{B} U(1))
      $$

  * [[field strength]]: the electric field $E$ and magnetic field $B$, locally at a point $x \in X$
    $$
      F = E \wedge d t + \star_3 B 
    $$

  * on $X = \mathbb{R}^3\backslash \{0\}$: underlying class in integral cohomology $cl(\hat F) \in H(X,\mathbf{B} U(1)) \simeq H^2(X,\mathbb{Z})$ is the [[magnetic charge]]

  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 1-particle


* [[Kalb-Ramond field]]

  * cocycle in degree-$3$ [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of 

      * a cocycle in [[Čech cohomology|Čech]]--[[Deligne cohomology|Deligne]] cocycle

        $$
          \hat H \in \mathbf{H}(X,\bar \mathbf{B}^2 U(1))
        $$

      * a [[bundle gerbe]] with connection

  * [[field strength]]: $H \in \Omega^3(X)$ the "$H$-field" -- on a D-[[brane]] this is the [[magnetic current]] for the  [[Yang-Mills field]] on the [[brane]]

  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 2-particle (the [[string theory|string]]).


* [[supergravity C-field]]

  * cocycle in degree-$4$ [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of as a cocycle in [[Čech cohomology|Čech]]--[[Deligne cohomology|Deligne]] cocycle
      $$
        \hat H \in \mathbf{H}(X,\bar \mathbf{B}^3 U(1))
      $$

      using the [[D'Auria-Fre formulation of supergravity]] it may also be thought of as a [[schreiber:theory of differential nonabelian cohomology|nonabelian differential cocycle]] given by a [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]

  * [[field strength]]: $H \in \Omega^4(X)$ the "$G$-field" -- in heterotic [[supergravity]] this is the 5-brane [[magnetic current]] for the  [[twisted cohomology|twisted]] [[Kalb-Ramond field]]
 
  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 3-particle (the [[brane|membrane]]).


* [[RR field]]

  * cocycle in [[differential K-theory]]

    * in presence of nontrivial [[Kalb-Ramond field]]: cocycle in differential [[twisted K-theory]]

  * [[field strength]]: RR-forms

## Related concepts

* [[fiber bundles in physics]]

* [[gauge]]

* [[gauge group]]

* [[gauge transformation]], [[higher gauge transformation]]

* [[BRST complex]], [[BV-BRST formalism]]

* [[ghost field]], [[ghost-of-ghost field]]

* [[gauge fixing]], [[gauge fixing fermion]], [[gauge invariant]]

* [[lattice gauge theory]]

* [[Gribov ambiguity]]

* [[quiver gauge theory]]

[[!include gauge field - table]]


* [[higher U(1)-gauge theory]]

  * [[higher electric background charge coupling]]

* [[self-dual higher gauge theory]]
 

* [[higher spin gauge theory]]


* [[quantum anomaly]]

  * [[Green-Schwarz mechanism]]

* [[schreiber:infinity-Chern-Simons theory]]

* [[free field theory]]

## References

### General

General textbook accounts:

* Mike Guidry, _Gauge Field Theories: An Introduction with Applications_, Wiley 2008 ([ISBN:978-3-527-61736-4](https://www.wiley.com/en-us/Gauge+Field+Theories%3A+An+Introduction+with+Applications-p-9783527617364))

* [[Mikio Nakahara]], Section 10.5 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


Basics on [[fiber bundles in physics]] are recalled in

* Adam Marsh, _Gauge Theories and Fiber Bundles: Definitions, Pictures, and Results_ ([arXiv:1607.03089](https://arxiv.org/abs/1607.03089))


An introduction to concepts in the [[quantization]] of gauge theories is in

* [[Nicolai Reshitikhin]], _Lectures on quantization of gauge systems_ ([pdf](http://staff.science.uva.nl/~nresheti/Holb-Quant-Gauge.pdf))

A standard textbook on the [[BV-BRST formalism]] for the quantization of gauge systems is in

* [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_ Princeton University Press, 1992

Comprehensive lecture notes on this are at 

* _[[geometry of physics -- perturbative quantum field theory]]_.


Discussion of abelian higher gauge theory in terms of [[differential cohomology]] is in

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_

* [[Alessandro Valentino]], _Differential cohomology and quantum gauge fields_ ([pdf](http://www.uni-math.gwdg.de/sandro/seminarGoett.pdf))

* [[José Figueroa-O'Farrill]], _Gauge theory_ ([web page](http://empg.maths.ed.ac.uk/Activities/GT/index.html)) 

* [[Tohru Eguchi]], Peter Gilkey, Andrew Hanson, _Gravitation, gauge theories and differential geometry_, Physics Reports __66__:6 (1980) 213&#8212;393 ([pdf](http://empg.maths.ed.ac.uk/Activities/GT/EGH.pdf))

For discussion in the context of [[gravity]] see also

* {#Witten17} [[Edward Witten]], _Symmetry and Emergence_ ([arXiv:1710.01791](https://arxiv.org/abs/1710.01791))


### In AQFT
 {#ReferencesInAQFT}

Standard discussion of gauge theory in the context of [[algebraic quantum field theory]] ([[AQFT]]) includes

* [[Franco Strocchi]], section 4 of _Relativistic Quantum Mechanics and Field Theory_, Found.Phys. 34 (2004) 501-527 ([arXiv:hep-th/0401143](http://arxiv.org/abs/hep-th/0401143))

For [[AQFT on curved spacetimes]] the axioms of AQFT need to be promoted to a context of [[higher geometry]] unless [locality](field+%28physics%29#IdeaLocality) is broken, see the expositions at 

* _[[schreiber:Higher field bundles for gauge fields]]_

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories
in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([web](field+bundle#Schenkel14)) 

This was established in

* {#BDS} Marco Benini, [[Claudio Dappiaggi]], [[Alexander Schenkel]], _Quantized Abelian principal connections on Lorentzian manifolds_, Communications in Mathematical Physics 2013 ([arXiv:1303.2515](http://arxiv.org/abs/1303.2515))

and the program of improving the axioms of [[AQFT on curved spacetimes]] to the [[stack|stacky]] context in order to accomodate gauge theory includes the following articles:

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))

* [[Marco Benini]], [[Alexander Schenkel]], _Quantum field theories on categories fibered in groupoids_ ([arXiv:1610.06071](https://arxiv.org/abs/1610.06071))

* [[Marco Benini]], [[Alexander Schenkel]], [[Urs Schreiber]], _The stack of Yang-Mills fields on Lorentzian manifolds_ ([arXiv:1704.01378](https://arxiv.org/abs/1704.01378))

 

### Dualities

An exposition of the relation to [[geometric Langlands duality]] is in

* [[Edward Frenkel]], _Gauge theory and Langlands duality_ ([pdf](http://math.berkeley.edu/~frenkel/bourbaki-gauge.pdf))


### History
 {#History}

A discussion of "[[gauge]]" and [[gauge transformation]] in [[metaphysics]] is in

* [[Georg Hegel]], [&#167;714](Science+of+Logic#714) of _[[Science of Logic]]_, 1812

[[Hermann Weyl]]'s historical argument motivating gauge theory in [[physics]] from rescaling of units of length was given in 1918 in

* [[Hermann Weyl]], _Raum, Zeit, Materie: Vorlesungen &#252;ber die Allgemeine Relativit&#228;tstheorie_, Springer Berlin Heidelberg 1923 

  > The manuscript of Weyl's first book on mathematical physics, Space &#8211; Time &#8211; Matter (STM) (Raum &#8211; Zeit &#8211; Materie), delivered to the publishing house (Springer) Easter 1918, did not contain Weyl's new geometry and proposal for a UFT. It was prepared from the lecture notes of a course given in the Summer semester of 1917 at the Polytechnical Institute (ETH) Z&#252;rich. Weyl included his recent findings only in the 3rd edition (1919) of the book. The English and French versions (Weyl 1922b, Weyl 1922a), translated from the fourth revised edition (1921), contained a short exposition of Weyl's generalized metric and the idea for a scale gauge theory of electromagnetism. ([Scholz](#Scholz))

See

* {#Scholz} Erhard Scholz, _H. Weyl's and E. Cartan's proposals for infinitesimal geometry in the early 1920s_ ([pdf](http://www2.math.uni-wuppertal.de/~scholz/preprints/weyl_cartan.pdf))

Early surveys include

* {#Iliopoulos75} [[John Iliopoulos]], _Progress in Gauge Theories_, 1975 ([spire:3000](http://inspirehep.net/record/3000))

Quick reviews include

* Quigley, _On the origins of gauge theory_ ([pdf](http://www.math.toronto.edu/~colliand/426_03/Papers03/C_Quigley.pdf))

* Afriat, _Weyl's gauge argument_ ([pdf](http://hal.inria.fr/docs/00/76/96/90/PDF/WGA.pdf))

More comprehensive historical accounts include

* [[Lochlainn O'Raifeartaigh]], _The Dawning of Gauge Theory_, Princeton University Press (1997)

* [[Lochlainn O'Raifeartaigh]], Norbert Straumann, _Gauge Theory: Historical Origins and Some Modern Developments_ Rev. Mod. Phys. 72, 1-23 (2000).

* [[Norbert Straumann]], _Early History of Gauge Theories and Weak Interactions_ ([arXiv:hep-ph/9609230](http://arxiv.org/abs/hep-ph/9609230))

* [[Norbert Straumann]], _Gauge principle and QED_, talk at PHOTON2005, Warsaw (2005) ([arXiv:hep-ph/0509116](http://arxiv.org/abs/hep-ph/0509116)) 


[[!redirects gauge theories]]

[[!redirects gauge field theory]]
[[!redirects gauge field theories]]


[[!redirects gauge principle]]

[[!redirects gauge field]]
[[!redirects gauge fields]]
