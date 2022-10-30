
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

A _gauge theory_ may denote either a [[classical field theory]] or a [[quantum field theory]] whose [[field configurations]] are [[cocycles]] in [[differential cohomology]] ([[ordinary differential cohomology|abelian]] or [[Chern-Weil theory|nonabelian]]).

### Ordinary gauge theories

An _ordinary gauge theory_ is a [[quantum field theory]] whose field configurations are [[vector bundle]]s 
[[connection on a bundle|with connection]].

This includes notable the fields that carry the three fundamental forces of the [[standard model of particle physics]]:

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

But a whoe tower of higher and generalized gauge theories became visible with the study of higher [[supergravity]] theories,

* The [[Kalb-Ramond field]] is a [[bundle gerbe|bundle gerbe with connection]], a [[Deligne cohomology|Deligne cocycle]] with curvature 3-form.

* The [[supergravity C-field]] is a [[Deligne cohomology|Deligne cocycle]] with curvature 4-form.

* The [[RR-field]] is a cocycle in [[differential K-theory]].


### Gravity as a gauge theory

There are various models that realize gravity also as a gauge theory.

* [Chern-Simons Actions for (Super)-Gravities](http://golem.ph.utexas.edu/category/2008/03/chernsimons_actions_for_superg.html)

In particular [[supergravity]] theories have interpretations as higher gauge theories as described at [[D'Auria-Fre formulation of supergravity]].

## Anomalies 

In the presence of [[magnetic charge]] (and then even in the absence of [[chiral fermion anomaly|chiral fermion anomalies]]) the standard would-be action functional for higher gauge theories may be ill-defined. The [[Green-Schwarz mechanism]] is a famous phenomenon in [[differential cohomology]] by which such a [[quantum anomaly]] cancels against that given by chiral fermions.

## List of gauge fields and their models

The following tries to give an overview of some collection of gauge fields in physics, their models by [[differential cohomology]] and further details.

* [[Yang-Mills field]]

  * cocycle in lowest degree [[schreiber:Differential Nonabelian Cohomology|nonabelian differential cohomology]]  

    * originally realized in terms of differential [[?ech cohomology|?ech cocycle]]s
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

    * naturally/historically realized in terms of Maxwell-Dirac presentation as a cocycle in [[?ech cohomology|?ech]]--[[Deligne cohomology|Deligne]] cocycle
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

      * a cocycle in [[?ech cohomology|?ech]]--[[Deligne cohomology|Deligne]] cocycle
        $$
          \hat H \in \mathbf{H}(X,\bar \mathbf{B}^2 U(1))
        $$

      * a [[bundle gerbe]] with connection

  * [[field strength]]: $H \in \Omega^3(X)$ the "$H$-field" -- on a D-[[brane]] this is the [[magnetic current]] for the  [[Yang-Mills field]] on the [[brane]]

  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 2-particle (the [[string theory|string]]).


* [[supergravity C-field]]

  * cocycle in degree-$4$ [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of as a cocycle in [[?ech cohomology|?ech]]--[[Deligne cohomology|Deligne]] cocycle
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


* [[gauge group]]

* [[gauge transformation]], [[higher gauge transformation]]

* [[BRST complex]], [[BV-BRST formalism]]

* [[ghost field]], [[ghost-of-ghost field]]

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

An introduction to concepts in the [[quantization]] of gauge theories is in

* [[Nicolai Reshitikhin]], _Lectures on quantization of gauge systems_ ([pdf](http://staff.science.uva.nl/~nresheti/Holb-Quant-Gauge.pdf))

A standard textbook on the [[BV-BRST formalism]] for the quantization of gauge systems is in

* [[Marc Henneaux]], [[Claudio Teitelboim]], _Quantization of gauge systems_ Princeton University Press

Discussion of abelian higher gauge theory in terms of [[differential cohomology]] is in

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_

* [[Alessandro Valentino]], _Differential cohomology and quantum gauge fields_ ([pdf](http://www.uni-math.gwdg.de/sandro/seminarGoett.pdf))
* [[José Figueroa-O'Farrill]], _Gauge theory_ ([web page](http://empg.maths.ed.ac.uk/Activities/GT/index.html)) 
* Tohru Eguchi, Peter Gilkey, Andrew Hanson, _Gravitation, gauge theories and differential geometry_, Physics Reports __66__:6 (1980) 213&#8212;393 [pdf](http://empg.maths.ed.ac.uk/Activities/GT/EGH.pdf)

### History

* [[Lochlainn O'Raifeartaigh]], _The Dawning of Gauge Theory_, Princeton University Press (1997)

* [[Lochlainn O'Raifeartaigh]], Norbert Straumann, _Gauge Theory: Historical Origins and
Some Modern Developments_ Rev. Mod. Phys. 72, 1-23 (2000).


* Norbert Straumann, _Gauge principle and QED_, talk at PHOTON2005, Warsaw (2005) ([arXiv:hep-ph/0509116](http://arxiv.org/abs/hep-ph/0509116)) 


[[!redirects gauge theories]]

[[!redirects gauge field theory]]
[[!redirects gauge field theories]]

[[!redirects higher gauge theory]]
[[!redirects higher gauge theories]]

[[!redirects gauge principle]]
