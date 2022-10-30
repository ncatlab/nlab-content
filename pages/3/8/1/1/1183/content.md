

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

A _$\sigma$-model_ is a [[quantum field theory]]  whose fields are maps from a _[[worldvolume]]_ $\Sigma$ into some _[[target space]]_ that carries some geometric structure -- usually a [[background gauge field]] given by a [[connection on an infinity-bundle]] generally or a cocycle in abelian [[differential cohomology]] more specifically.

One way to make this precise for _topological_ $\sigma$-models is to say that target space $X$, or possibly the gauge bundle $P \to X$ over it, [[representable functor|represents]] an functor that sends [[cobordism]] [[cospan]]s to [[span]]s which in turn are taken to act by pull-push on the quantum states, which are objects in [[geometric infinity-function theory]] living over the mapping spaces $[\Sigma, P]$. (...)

### Physical interpretation 

$\sigma$-model quantum field theories on [[worldvolume]] $\Sigma$ of top dimension $n+1$ are to be thought of as encoding the quantum mechanics of the propagation of an $n$-dimensional particle, called an _$(n-1)$-[[brane]]_, in [[target space]] $X$, subject to [[force]]s imposed on it by the [[background gauge field]], under which it is said to be _[[charge]]d_.

These cases describe non-topological quantum field theories. Here the formalization of the notion of $\sigma$-model is not entirely complete. Yet.

### Terminology and history
 {#TerminologyAndHistory}

In physics one tends to speak of a _model_ if one specifies a particular [[quantum field theory]] for describing a particular situation, for instance by specifying a [[Lagrangian]] or [[local action functional]] on some [[configuration space]]. This is traditionally not meant in the mathematical sense of _[[model]]_ of some [[theory]]. But in light of progress of mathematically formalizing [[quantum field theory]] (see [[FQFT]] and [[AQFT]]), it can with hindsight be interpreted in this way: 

a $\sigma$-model is supposed to be a type of [[model]] for the [[theory]] called [[quantum field theory]]. This sounds like a tautology, but much effort in mathematical physics is devoted to eventually making this a precise statement. In special cases and toy examples this has been achieved, but for the examples that seem to be directly relevant for the phenomenological description of the observed world, lots of clues still seem to be missing.

As to the "$\sigma$" in "$\sigma$-model": back in the 1960s people were interested in a hypothetical particle called the 
$\sigma$-particle.  [[Murray Gell-Mann]] came up with a theory of them.  It was called 'the $\sigma$-model'.  It was an old-fashioned field theory where the field took values in a vector space.   Then someone came up with a modified version of the &#963;-model where the field took values in some other [[manifold]] and this was called 'the nonlinear &#963;-model'.  

While the parameter space (the domain space of the fields) of the original $\sigma$-models was supposed to be our [[spacetime]] and the target space was some abstract space, with the advent of [[string theory]] the nonlinear $\sigma$-models gained importance as quantum field theories whose _target space_ is [[spacetime]] $X$ and whose parameter space is some low dimensional space, usually denoted $\Sigma$. A field configuration $\Sigma \to X$ is then interpreted as being the trajectory of an extended fundamental particle -- a fundamental [[brane]] -- in $X$, and the $\sigma$-model describes the quantum mechanics of that brane propagating in $X$.

In particular the [[quantum mechanics]] of a [[relativistic particle]] propagating on $X$ is described by a $\sigma$-model on the [[real line]] $\Sigma = \mathbb{R}$ -- the _worldline_ of the particle.

In [[string theory]] one considers 2-[[dimensional]] $\Sigma$ and thinks of maps $\Sigma \to X$ as being the _worldsheets_ of the trajectory of a string propagating in spacetime.

In the context of [[11-dimensional supergravity]] there is a $\sigma$-model with 3-dimensional $\Sigma$, describing the propagation of a [[membrane]] in [[spacetime]].

## Examples 

### Non-topological $\sigma$-models 

* The canonical textbook example of a quantum mechanical system is of this form for $n=1$: A line [[vector bundle|bundle]] with [[connection on a bundle|connection]] $E \to X$ on a ([[pseudo-Riemannian manifold|pseudo-]])[[Riemannian manifold]] $X$ induces the 1-dimensional [[quantum field theory]] which is the quantum mechanics of a point particle which propagates on $X$, subject to the forces of [[gravity]] (given by the [[pseudo-Riemannian metric]] on $X$) and [[electromagnetism]] (given by the line bundle with connection). The [[Hamilton operator]] encoding this quantum dynamics in this case is the Laplace-operator of $T X$ twisted by the line bundle $E$.

  For $X$ a [[spacetime]] this is called the [[relativistic particle]].

  For $\Sigma$ or $X$ a [[supermanifold]] this is the [[superparticle]].

* Generalizing in the above example the line bundle $E$ by an abelian [[bundle gerbe]] with a connection yields a background for a 2-dimensional $\sigma$-model which mayb be thought of as describing the propgation of a [[string theory|string]].  The best-studied version of this is the case where $X = G$ is a [[Lie group]], in which case this $\sigma$-model is known as the _[[WZW model|Wess--Zumino--Witten model]]_.



### Topological $\sigma$-models 


* [[Dijkgraaf-Witten theory]] is the (2+1)-dimensioanl $\sigma$-model induced from an abelian 2-gerbe on $\mathbf{B} G$, for $G$ a finite group.

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

## References 

First indications on how to formalize $\sigma$-models in a [[higher category theory|higher categorical]] context were given in

* [[Dan Freed]], _Higher algebraic structures and quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

A grand picture developing this approach further is sketched in 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_  ([arXiv](http://arxiv.org/abs/0905.0731))

A discussion of 2 or 2+1-dimensional $\Sigma$-models whose target is an [[derived stack]]/[[infinity-stack]] is in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral transforms and Drinfeld centers in derived geometry_ ([arXiv](http://arxiv.org/abs/0805.0157)) .

More discussion of the latter is at [[geometric infinity-function theory]].

[[!redirects sigma-models]]
[[!redirects sigma model]]
[[!redirects ∞-model]]
[[!redirects ∞-models]]