
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

A **Green-Schwarz mechanism** is a modification of an [[action functional]] of a [[quantum field theory]] involving higher [[gauge field]]s that makes a [[quantum anomaly]] of the original action functional disappear.

More in detail:

* An [[action functional]] in [[path integral|path integral quantization]] is said to be [[quantum anomaly|anomalous]] if it is only locally identified with a function on the configuration space of fields, but is globally instead a section of a line [[bundle]] (usually equipped with [[connection on a bundle|connection]]).

* Given two anomalous action functionals in this sense, it may happen that while the two corresponding line bundles on configuration space are each nontrivial, their [[tensor product]] becomes trivializable. In this case one can consider the non-anomalous action function given by the sum of the two anomalous action functionals. This is what is called **anomaly cancellation** of one piece of an action functional against another. 

* The two main sources of examples for action functionals that are anomalous are

  * the standard action functional for chiral fermions 

    * this is a section of the [[Pfaffian line bundle]] for the 
      [[Dirac operator]]

  * the action functional for [[differential cohomology|differential cocycles]] (higher connection, higher [[gauge theory]]) in the presence of [[electric charge|electric]] and [[magnetic charge]]s: 

    * this is a [[section]] of the [[transgression]] of the 
      [[line bundle]] arising as the [[cup product]] of 
      the [[electric charge|electric]] and 
      [[magnetic charge|magnetic differential cocycles]].


A **Green--Schwarz mechanism** is the addition of an action functional for higher differential cocycles with [[magnetic charge]]s such that their [[quantum anomaly]] cancels a given [[Pfaffian line bundle]]: so it is a choice of by itself ill-defined action functional for higher gauge theory that cancels the ill-definedness of an action functional for chiral fermions.

In the more strict and original sense of the word, _the_ Green--Schwarz mechanism is the application of this procedure in the theory called [[heterotic string theory|heterotic supergravity]]: there it so happens that the Pfaffian line bundle of the fermionic action has as [[Chern class]] the [[transgression]] of a degree-12 class in [[ordinary differential cohomology]] that factorizes as $I_8 \wedge I_4$. Since heterotic supergravity contains a higher gauge field that couples to [[string theory|strings]], this is precisely of the form $J_{electric} \wedge J_{magnetic}$ that the anomaly for the corresponding higher gauge theory in the presence of magnetic charges gives rise to. So the original Green--Schwarz anomaly cancellation mechanism consist of modifying the "naive" action functional for heterotic supergravity by adding the contribution that corresponds to adding a magnetic current of the form

$$
  j_B := I_4
  \,.
$$

Further discussion for the moment at

* [Charges and Twisted Bundles, IV: Anomaly Cancellation](http://golem.ph.utexas.edu/category/2008/04/charges_and_twisted_bundles_iv.html)


## The higher magnetic charge anomaly


### The higher abelian Yang-Mills action functional 
  {#YMactionfunctional}

Consider on some [[spacetime]] $X$ a [[gauge field]] $[\nabla] \in H_{diff}^{n+1}(X)$ modeled in [[ordinary differential cohomology]] in degree $n+1$: a [[circle n-bundle with connection]]. For instance

* in degree $n=1$ this is an [[electromagnetic field]];

* in degree $n=2$ this is a [[Kalb-Ramond field]];

* in degree $n = 3$ a [[supergravity C-field]].

Canonically associated to the [[gauge field]] is its [[field strength]]: the [[curvature]] [[differential form]]

$$
  F_\nabla \in \Omega^{n+1}_{cl}(X)
  \,.
$$

The abelian [[Yang-Mills action functional]] for our gauge field (the [[action functional]] of higher order [[electromagnetism]]) is the [[function]]

$$
  \exp(i S_{YM}(-)) : H_{diff}^{n+1}(X) \to \mathbb{C}
$$

that sends the field $\nabla$

$$
  \exp(i S_{YM}(-))
    : 
  [\nabla] 
   \mapsto 
  \exp(-i \int_X F_\nabla \wedge \star F_\nabla)
$$

to the [[exponential]] of the [[integral]] over the [[spacetime]] $X$ of the  [[differential form]] obtained as the [[wedge product]] of the [[curvature form]] with its image under the [[Hodge star operator]] correspondonding to the [[pseudo-Riemannian manifold|pseudo-Riemannian metric]] on $X$.

The fact that this map [[function]] defined in terms of [[cocycle]]s is a well defined function on [[cohomology]] means that the [[action functional]] is [[gauge transformation|gauge invariant]]. At this point this is just the trivial statement that under a [[gauge transformation]]

$$
  \nabla \stackrel{g}{\to} \nabla'
$$

the [[curvature]] invariant: $F_\nabla = F_{\nabla'}$.



### ... with electric charge ...
  {#WithElectricCharge}

The [above](#YMactionfunctional) [[action functional]] describes the dynamics of the [[gauge field]] all by itself, with no interactions with other fields or with [[relativistic particle|fundamental particle]]s/[[brane|fundamental brane]]s.

A distribution of  $n$-[[electric charge]] on $X$ is modeled itself by a [[cocycle]] $\hat j_E$ in [[ordinary differential cohomology]] in degree $dim X - n$

$$
  [\hat j_E] \in H_{diff}^{dim X - d}(X)
  \,.
$$

The [[curvature]] $j_E$ of $\hat j_E$ is the [[electric current]] form. The [[action functional]] that encodes the [[force]] of the [[gauge field]] exerted on this electric charge distribution is locally on [[coordinate chart]]s $U \subset X$ given by the [[integral]] $\int_X A_U \wedge j_E$, where $A_U$ is the local [[connection on an infinity-bundle|connection]] $n$-form of the gauge fiedl $\nabla$.

Globally, this contribution is given by the push-forward 

$$
  2 \pi i\int_X (-) : H_{diff}^{dim X}(X) \to H_{diff}^0(*) = U(1)
$$ 

of the [[cup product]] $\hat j_E \cdot \nabla$ in [[ordinary differential cohomology]].

In total the [[action functional]] of higher abelian [[Yang-Mills theory]] in the presence of [[electric charge]] is the [[function]]

$$
  \exp(i S_{YM}(-) + i S_{el}(-)) 
    :
  H^{n+1}_{diff}(X) 
   \times
  H^{dim X - n}_{diff}(X)
   \to
  \mathbb{C}
$$

given by

$$
  ([\nabla], [\hat j_E]) 
     \mapsto
  \exp(i \int(\int_X F_\nabla \wedge \star F_\nabla))
  \exp(2 \pi i \int_X \hat j_E \cdot \nabla)
  \,.
$$


### ... and with magnetic charge.

We now consider one more additional term in the [[action functional]], one that desribes moreovr the interaction of our [[gauge field]] with a distribution of $n$-[[magnetic charge]] on $X$, in addition to the interaction with the distribution of [[electric charge]] described 
[above](#WithElectricCharge).

The [[magnetic charge]] distribution itself is also modeled as a  [[cocycle]] $\hat j_B$ in [[ordiary differential cohomology]]. As opposed to the [[electric charge]] it is however not part of the dynamics but of the kinemtics of the system: it does not manifestly show up in the integral expression for the [[action functional]], but does modify the nature of the configuration space that this action functional is defined on.

In order to formalize this we have to refine the formalization of the structure of the configuration space. So far we had regarded the [[set]] $H^{dim X - n}_{diff}(X) \times H_{diff}^n(X)$ of gauge equivalence classes of 


(...)



## References

A clear and precise account of what anomalies are and what the Green-Schwarz mechanism is to cancel them is given in

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))








[[!redirects Green Schwarz mechanism]]
[[!redirects Green-Schwarz mechanism]]
[[!redirects Green–Schwarz mechanism]]
[[!redirects Green--Schwarz mechanism]]
[[!redirects Green Schwartz mechanism]]
[[!redirects Green-Schwartz mechanism]]
[[!redirects Green–Schwartz mechanism]]
[[!redirects Green--Schwartz mechanism]]
