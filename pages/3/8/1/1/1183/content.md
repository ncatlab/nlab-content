

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}


## Idea
 {#Idea}

A _$\sigma$-model_ is a particular kind of [[classical field theory]], which induces its quantization to a [[quantum field theory]].  The basic data describing a specific $\sigma$-model is some kind of "[[space]]" $X$, in a [[category]] of "[[spaces]]" which includes [[smooth manifolds]].  We call $X$ the [[target space]], and we define the "[[configuration space]] of fields" $Conf_\Sigma$  over a manifold $\Sigma$ to be the [[mapping space]] $Map(\Sigma, X)$.  That is, a "configuration of fields" over a manifold $\Sigma$ is like an an $X$-valued [[function]] on $\Sigma$.

We assign a [[dimension]] $n \in \mathbb{N}$ to our $\sigma$-model, take $dim \Sigma \leq n$ and assume that [[target space]] $X$ is equipped with a "[[circle n-bundle with connection]]".  

For $n = 1$ this is an ordinary [[circle bundle]] [[connection on a bundle|with connection]] and models a configuration of the [[electromagnetic field]] on $X$. To distinguish this "field" on $X$ from the fields on $\Sigma$ we speak of a _[[background gauge field]]_. (This remains fixed background data unless and until we pass to _[[second quantization]]_ .) A field configuration $\Sigma \to X$ on $\Sigma$ models a trajectory of a [[charge]]d particle subject to the [[force]]s exerted by this background field.

For $n = 2$, a circle $n$-bundle with connection is a [[circle n-group|circle 2-group]] [[principal 2-bundle]] or equivalently a [[bundle gerbe]] with connection. This models a "higher electromagnetic field", called a [[Kalb-Ramond field]]. Now $\Sigma$ is taken to be 2-dimensional and a map $\Sigma \to X$ models the trajectory of a [[string]] on $X$, subject to forces exerted on it by this higher order field.

This pattern continues. In the next dimension a [[membrane]] with 3-dimensional [[worldvolume]] is charged under a [[circle n-bundle with connection|circle 3-bundle]] with connection, for instance something called the [[supergravity C-field]].

While one can speak of [[principal ∞-bundles|higher bundles]] in full generality and full analogy to ordinary [[principal bundle]]s, it is useful to observe that any circle $n$-bundle is characterized by a classifying map $\alpha : X \to \mathbf{B}^n U(1)$ in our category of [[space]]s, so we can just think about classifying maps instead.  Here $U(1)$ is the [[circle group]], and $\mathbf{B}^n$ denotes its $n$th _[[delooping]]_ ; thus such a map is also a sort of [[cocycle]] in "[[smooth infinity-groupoid|smooth]] $n$th [[cohomology]] of $X$ with coefficients in $U(1)$". The additional data of a _connection_ refines this to a cocycle in _[[ordinary differential cohomology|differential cohomology]]_ of $X$.

Such connection data $\nabla$ on a circle $n$-bundle defines -- and is defined by -- a notion of [[higher parallel transport]] over $n$-dimensional trajectories: for closed $n$-dimensional $\Sigma$ it defines a map $hol : (\gamma : \Sigma \to X) \mapsto \exp(i \int_\Sigma \gamma^*\nabla) \in U(1)$ that sends trajectories to elements in $U(1)$: the [[holonomy]] of $\nabla$ over $\Sigma$, given by [[integration]] of local data over $\Sigma$. The local data being integrated is called the _[[Lagrangian]]_ of the $\sigma$-model. Its integral is called the [[action functional]]. 

In the _[[QFT|quantum]]_ $\sigma$-model one considers in turn the integral of the [[action functional]] over all of [[configuration space]]: the "[[path integral]]". In the _classical $\sigma$-model_ one considers only the [[critical locus]] of the action functional (where the rough idea is that the path integral to some approximation localizes around the critical locus). Points in this critical locus are said to be configurations that satisfy the "[[Euler-Lagrange equations]] of motion". These are supposed to be the physically realized trajectories among all of them, in the classical approximation.

Finally, just like an ordinary [[circle group]]-[[principal bundle]] has an [[associated bundle|associated]] [[vector bundle]] once we fix a [[representation]] of $U(1)$ to be the [[fiber]]s, any "[[circle n-bundle]]" has an associated "[[n-vector bundle]]" once we fix a "[[∞-representation]]" $\rho : \mathbf{B}^n U(1) \to n Vect$ on "[[n-vector spaces]]".  Just as for the ordinary $U(1)$, here we usually pick the canonical 1-dimensional such "representation".  Finally, we define bundles $V_\Sigma : Conf_\Sigma \to \mathcal{C}$ of "internal states" by [[transgression]] of these associated bundles.

The passage from [[principal ∞-bundle]]s to [[associated ∞-bundle]]s is necessary for the description of the quantum $\sigma$-model: it assigns in positive codimension spaces of [[section]]s of these associated bundles. For a 1-categorical description of the resulting [[QFT]] ordinary vector bundles (assigned in codimension 1) would suffice, but the $\sigma$-model should determine much more: an [[extended quantum field theory]]. This requires sections of higher vector bundles. For instance for $n = 2$ some boundary conditions of the $\sigma$-model are given by sections of the background [[n-vector bundle|2-vector bundle]]: these are the [[twisted bundle|twisted vector bundles]] known as the [[Chan-Paton bundles]] on the [[boundary]]-[[D-brane]]s of the [[string]]. (...)

We now try to fill this with life by spelling out some standard examples. Further [below](#Exposition) we look at precise formalizations of the situation.


## Terminology and history
 {#TerminologyAndHistory}

In physics one tends to speak of a _model_ if one specifies a particular [[quantum field theory]] for describing a particular situation, for instance by specifying a [[Lagrangian]] or [[local action functional]] on some [[configuration space]]. This is traditionally not meant in the mathematical sense of _[[model]]_ of some [[theory]]. But in light of progress of mathematically formalizing [[quantum field theory]] (see [[FQFT]] and [[AQFT]]), it can with hindsight be interpreted in this way: 

a $\sigma$-model is supposed to be a type of [[model]] for the [[theory]] called [[quantum field theory]]. This sounds like a tautology, but much effort in mathematical physics is devoted to eventually making this a precise statement. In special cases and toy examples this has been achieved, but for the examples that seem to be directly relevant for the phenomenological description of the observed world, lots of clues still seem to be missing.

As to the "$\sigma$" in "$\sigma$-model": back in the 1960s people were interested in a hypothetical particle called the 
$\sigma$-particle.  [[Murray Gell-Mann]] came up with a theory of them.  It was called 'the $\sigma$-model'.  It was an old-fashioned field theory where the field took values in a vector space.   Then someone came up with a modified version of the &#963;-model where the field took values in some other [[manifold]] and this was called 'the nonlinear &#963;-model'.  

While the parameter space (the domain space of the fields) of the original $\sigma$-models was supposed to be our [[spacetime]] and the target space was some abstract space, with the advent of [[string theory]] the nonlinear $\sigma$-models gained importance as quantum field theories whose _target space_ is [[spacetime]] $X$ and whose parameter space is some low dimensional space, usually denoted $\Sigma$. A field configuration $\Sigma \to X$ is then interpreted as being the trajectory of an extended fundamental particle -- a fundamental [[brane]] -- in $X$, and the $\sigma$-model describes the quantum mechanics of that brane propagating in $X$.

In particular the [[quantum mechanics]] of a [[relativistic particle]] propagating on $X$ is described by a $\sigma$-model on the [[real line]] $\Sigma = \mathbb{R}$ -- the _worldline_ of the particle.

In [[string theory]] one considers 2-[[dimension]]al $\Sigma$ and thinks of maps $\Sigma \to X$ as being the _worldsheets_ of the trajectory of a string propagating in spacetime.

In the context of [[11-dimensional supergravity]] there is a $\sigma$-model with 3-dimensional $\Sigma$, describing the propagation of a [[membrane]] in [[spacetime]].


## Exposition of classical sigma-models
 {#ExpositionClassical}

We survey, starting from the very basics, [[classical field theory]] aspects of $\sigma$-models that describe dynamics of [[particle]]s, [[strings]]s and [[brane]]s on geometric [[target space]]s.

The content of this section is at

* [[sigma-model -- exposition of classical sigma-models]]



## Exposition of higher gauge theories as $\sigma$-models
 {#GaugeTheoryAsSigmaModel}

We discuss how [[gauge theories]] and their higher analogs are 
naturally regarded as $\sigma$-models.

The content of this section is at

* [[sigma-model -- exposition of higher gauge theories as sigma-models]].

## Exposition of quantum $\sigma$-models
 {#ExpositionQuantumSigmaModel} 
 {#StringTopology}

Above we have discussed some standard [classical sigma-models](#ExpositionClassical) and [higher gauge theories as sigma-models](#GaugeTheoryAsSigmaModel), also mostly classically. Here we talk about the [[quantization]] of these models (or some of them) to [[QFT]]s: _quantum $\sigma$-models_ .

The content of this section is at

* [[sigma-model -- exposition of quantum sigma-models]].

See there for discussion of [[string topology]], [[Gromov-Witten theory]], [[Chern-Simons theory]].

## Exposition of a general abstract formulation
 {#Exposition}

We give a leisurely exposition of a general abstract formulation $\sigma$-models, aimed at readers with a background in [[category theory]] but trying to assume no other prerequisites.

What is called an _$n$-dimensional $\sigma$-model_ is first of all an instance of an $n$-dimensional [[quantum field theory]] (to be explained). The distinctive feature of those quantum field theories that are $\sigma$-models is that 

1. these arise from a simpler kind of field theory -- called a [[classical field theory]] -- by a process called [[quantization]] 

1. moreover, this simpler kind of field theory encoded by[[geometry|geometric data]] in a nice way: it describes physical [[configuration space]]s that are [[mapping space]]s into a [[geometry|geometric]] [[space]] equipped with some [[synthetic differential geometry|differential geometric]] [[structure]].

We give expositions of these items step-by-step:

1. [Quantum field theory](#ExpositionQuantumFieldTheory)

1. [Classical field theory](#ExpositionClassicalFieldTheory)

1. [Quantization](#ExpositionQuantization)

1. [Classical sigma-models](#ExpositionClassicalSigmaModels)

1. [Quantum sigma-models](#ExpositionQuantumSigmaModels)

We draw from ([FHLT, section 3](#FHLT)).

The content of this section is at 

* [[sigma-model -- exposition of a general abstract formulation]].

## Exposition of second quantization of $\sigma$-models
 {#SecondQuantization}

We discuss [[second quantization]] in the context of $\sigma$-models.

The content of this section is at

* [[sigma-model -- exposition of second quantization of sigma-models]]

## Examples 

### Non-topological $\sigma$-models 

* The canonical textbook example of a quantum mechanical system is of this form for $n=1$: A line [[vector bundle|bundle]] with [[connection on a bundle|connection]] $E \to X$ on a ([[pseudo-Riemannian manifold|pseudo-]])[[Riemannian manifold]] $X$ induces the 1-dimensional [[quantum field theory]] which is the quantum mechanics of a point particle which propagates on $X$, subject to the forces of [[gravity]] (given by the [[pseudo-Riemannian metric]] on $X$) and [[electromagnetism]] (given by the line bundle with connection). The [[Hamilton operator]] encoding this quantum dynamics in this case is the Laplace-operator of $T X$ twisted by the line bundle $E$.

  For $X$ a [[spacetime]] this is called the [[relativistic particle]].

  For $\Sigma$ or $X$ a [[supermanifold]] this is the [[superparticle]].

* Generalizing in the above example the line bundle $E$ by an abelian [[bundle gerbe]] with a connection yields a background for a 2-dimensional $\sigma$-model which mayb be thought of as describing the propgation of a [[string theory|string]].  The best-studied version of this is the case where $X = G$ is a [[Lie group]], in which case this $\sigma$-model is known as the _[[WZW model|Wess--Zumino--Witten model]]_.



### Topological $\sigma$-models 


* [[Dijkgraaf-Witten theory]] is the (2+1)-dimensional $\sigma$-model induced from an abelian 2-gerbe on $\mathbf{B} G$, for $G$ a finite group.

* [[Chern-Simons theory]] is supposed to be analogously the $\sigma$-model induced from an abelian 2-gerbe with connection on $\mathbf{B}G$, but now for $G$ a Lie group.

* the [[Poisson sigma-model]] is a model whose target is a [[Poisson Lie algebroid]].

* in [[AKSZ theory]] this is generalized to a large class of sigma models with [[symplectic Lie n-algebroid]]s as target.

* Rozansky--Witten theory is essentially the $\sigma$-model for $X$ a smooth projective variety.

* generally [[schreiber:∞-Chern-Simons theory]] is a $\sigma$-model with a [[smooth ∞-groupoid]] of [[connection on an ∞-bundle|∞-connections]].


## Related concepts

* **sigma model**

  * [[worldvolume]]

  * [[target space]]

  * [[background gauge field]]

* [[brane]]

  * [[particle]], [[superparticle]]
 
  * [[string]]

  * [[membrane]]

* [[homological mirror symmetry]]

  * [[A-model]], [[B-model]]

  * [[Landau-Ginzburg model]]

## References 

A standard reference on 2-dimensional [[string]] $\sigma$-models is 


* [[Pierre Deligne]], [[Dan Freed]], _Classical field theory_ , chapter 5, page 211 in...

  and

  [[Krzysztof Gawedzki]], _Lectures on conformal field theory_ , part 3, lecture 3 in

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


First indications on how to formalize $\sigma$-models in a [[higher category theory|higher categorical]] context were given in

* [[Dan Freed]], _Higher algebraic structures and quantization_, ([arXiv](http://arxiv.org/abs/hep-th/9212115))

A grand picture developing this approach further is sketched in 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_,  ([arXiv](http://arxiv.org/abs/0905.0731))
 {#FHLT}

A discussion of 2- or (2+1)-dimensional $\Sigma$-models whose target is an [[derived stack]]/[[infinity-stack]] is in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral transforms and Drinfeld centers in derived geometry_, ([arXiv](http://arxiv.org/abs/0805.0157)) .

More discussion of the latter is at [[geometric infinity-function theory]].

A discussion of $\sigma$-models of higher gauge theory type is at

* [[Urs Schreiber]], _[[schreiber:infinity-Chern-Simons theory]]_ .

Concrete applications of $\sigma$-models with target [[stack]]s (typically smooth ones, hence [[smooth infinity-groupoid|smooth groupoid]]s) in [[string theory]] and [[supergravity]] are discussed for instance in

* [[Tony Pantev]], [[Eric Sharpe]], _Gauged linear sigma-models for gerbes (and other toric stacks)_, ([arXiv:hep-th/0502053](http://arxiv.org/abs/hep-th/0502053))
 {#PantevSharpe}

* S. Hellerman, [[Eric Sharpe]], _Sums over topological sectors and quantization of Fayet-Iliopoulos parameters_, ([arXiv:1012.5999](http://arxiv.org/abs/1012.5999))
 {#HellermanSharpe}


[[!redirects sigma-models]]
[[!redirects sigma model]]
[[!redirects ∞-model]]
[[!redirects ∞-models]]