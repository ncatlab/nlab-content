<div class="rightHandSide toc">
[[!include physicscontents]]
</div>



# Idea #

A _gauge theory_ is a [[quantum field theory]] whose field configurations are cocycles in [[differential cohomology]].

## ordinary gauge theories

An _ordinary gauge theory_ is a [[quantum field theory]] whose field configurations are [[vector bundle]]s 
[[connection on a bundle|with connection]].

This includes notable the fields that carry the three fundamental forces of the [[standard model of particle physics]]:

* Ordinary [[electromagnetism]] in the absence of magnetic charges is a gauge theory of $U(1)$-[[principal bundle]]s with [[connection on a bundle|connection]]. 

* Fields in [[Yang-Mills theory]] (such as appearing in the [[standard model of particle physics]] and in [[GUT]]s) are [[vector bundle]]s [[connection on a bundle|with connection]].

Other examples include formal physical models.

* [[Dijkgraaf-Witten theory]] is a gauge theory whose field configurations are $G$-[[principal bundle]]s for $G$ a finite group (these come with a unique [[connection on a bundle|connection]], so that in this simple case the connection is no extra datum).

## higher and generalized gauge theories ##

The above examples of gauge fields consisted of cocycles in degree 1 [[differential cohomology]].

More generally, a _higher gauge theory_ is a [[quantum field 
theory]] whose field configurations are cocycles in more general [[differential cohomology]], for instance higher degree [[Deligne cohomology|Deligne cocycles]] or more generally cocycles in other differential refinements, such as in differential [[K-theory]].

This generalization does contain experimentally visible physics such as

* The [[magnetic current]] in [[electromagnetism]] is a [[bundle gerbe|bundle gerbe with connection]], a [[Deligne cohomology|Deligne cocycle]] refining a cocycle in degree 3 [[Eilenberg-MacLane spectrum|Eilenberg-MacLane cohomology]]: the _magnetic charge_ .

But a whoe tower of higher and generalized gauge theories became visible with the study of higher [[supergravity]] theories,

* The [[Kalb-Ramond field]] is a [[bundle gerbe|bundle gerbe with connection]], a [[Deligne cohomology|Deligne cocycle]] with curvature 3-form.

* The [[supergravity C-field]] is a [[Deligne cohomology|Deligne cocycle]] with curvature 4-form.

* The [[RR-field]] is a cocycle in [[differential K-theory]].


## gravity as a gauge theory ##

There are various models that realize gravity also as a gauge theory.

* [Chern-Simons Actions for (Super)-Gravities](http://golem.ph.utexas.edu/category/2008/03/chernsimons_actions_for_superg.html)


# Anomalies #

In the presence of [[magnetic charge]] (and then even in the absence of [[chiral fermion anomaly|chiral fermion anomalies]]) the standard would-be action functional for higher gauge theories may be ill-defined. The [[Green-Schwarz mechanism]] is a famous phenomenon in [[differential cohomology]] by which such a [[quantum anomaly]] cancels against that given by chiral fermions.

# list of gauge fields and their models #

The following tries to give an overview of some collection of gauge fields in physics, their models by [[differential cohomology]] and further details.

* [[Yang-Mills field]]

  * cocycle in lowest degree [[schreiber:Differential Nonabelian Cohomology|nonabelian differential cohomology]]  

    * originally realized in terms of differential [[Cech cohomology|Cech cocycle]]s
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

  * cocycle in degree 2 [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of Maxwell-Dirac presentation as a cocycle in [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne cocycle]]
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

  * cocycle in degree 3 [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of 

      * a cocycle in [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne cocycle]]
        $$
          \hat H \in \mathbf{H}(X,\bar \mathbf{B}^2 U(1))
        $$

      * a [[bundle gerbe]] with connection

  * [[field strength]]: $H \in \Omega^3(X)$ the "$H$-field" -- on a D-[[brane]] this is the [[magnetic current]] for the  [[Yang-Mills field]] on the [[brane]]

  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 2-particle (the [[string theory|string]]).


* [[supergravity C-field]]

  * cocycle in degree 4 [[Eilenberg-MacLane spectrum|ordinary]] [[differential cohomology]]

    * naturally/historically realized in terms of as a cocycle in [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne cocycle]]
      $$
        \hat H \in \mathbf{H}(X,\bar \mathbf{B}^3 U(1))
      $$

  * [[field strength]]: $H \in \Omega^4(X)$ the "$G$-field" -- in heterotic [[supergravity]] this is the 5-brane [[magnetic current]] for the  [[twisted cohomology|twisted]] [[Kalb-Ramond field]]
 
  * [[parallel transport]]: gauge interaction piece of [[path integral|action functional]] of the electrically charged quantum 3-particle (the [[membrane]]).


* [[RR field]]

  * cocycle in [[differential K-theory]]

    * in presence of nontrivial [[Kalb-Ramond field]]: cocycle in differential [[twisted K-theory]]

  * [[field strength]]: RR-forms

[[!redirects gauge field]]