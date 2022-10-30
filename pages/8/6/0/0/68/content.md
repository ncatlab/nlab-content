+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _differentiable stack_ is a [[geometric stack]] on the [[site]] [[SmoothMfd]] of [[smooth manifold]]s: a stack which is represented by a [[Lie groupoid]].

This means that a differentiable stack is in a way _nothing else_ but a Lie groupoid: but the point is that equivalence of stacks captures the notion of [[Morita equivalence]] of their presenting (Lie) groupoids.

This means that looking at a Lie groupoid in terms of the stack it presents provides a direct way to recognizing the right notion of equivalence of these objects. The notion of Morita equivalence, on the other hand, proceeds via the reasoning of [[homotopy theory]].

Notice that the stack [[presented stack|presented]] by a (Lie) groupoid $G$ is really the stack which sends every test manifold to the category of $G$-principal bundles over that manifold. Such a $G$-principal bundle, also known as a [[torsor]], is analogous to a [[module]] for an algebra. This explains the terminology of "Morita morphisms", which originates in algebra: 

Just as two algebras are Morita equivalent if their categories of modules are equivalent, two groupoids are Morita equivalent if their stacks of torsors are equivalent.

## Properties

### Characterization by Lie groupoids
 {#CharacterizatiobByLieGroupoids}

Sending a [[Lie groupoid]] to the [[smooth stack]] it represents constitutes an [[equivalence of (infinity,1)-categories]] between [[Lie groupoids]] with Morita morphisms/[[bibundles]] between them and differentiable stacks.

(e.g. [Blohmann 07](#Blohmann), [Carchedi 11](#Carchedi11)). For review in a broader context see also [Nuiten 13, around prop. 2.2.34](#Nuiten13)

### Other descriptions

A differentible stack is in particular an object in the [[cohesive (∞,1)-topos]] [[Smooth∞Grpd]] that is 

* [[1-truncated]] 

* <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ConcreteObjects">concrete</a>.

It is however more special than that. The general 1-truncated concrete [[smooth ∞-groupoids]] are [[internal groupoids]] in [[diffeological spaces]].

### Mapping stacks

For $X$, $Y$ two differentiable stacks, there is the [[mapping stack]] $[X,Y]$, which a priory is only a [[smooth stack]]. It should be true that a sufficient condition for this itself to be a [[Frechet manifold|Frechet]]-differentiable stack is that $X$ has an [[atlas]] by a [[compact topological space|compact]] [[smooth manifold]]. 

(See also [[manifold structure of mapping spaces]].)


## Related concept

* [[geometric stack]]

  * [[algebraic stack]]

  * [[topological stack]]

  * **differentiable stack**

    * [[groupoid K-theory]]

* [[geometric ∞-stack]]

* [[cohesive ∞-groupoid]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * [[synthetic differential ∞-groupoid]]

## References

* {#Blohmann} [[Christian Blohmann]], _Stacky Lie groups_, Int. Mat. Res. Not. (2008) Vol. 2008: article ID rnn082 ([arXiv:math/0702399](http://arxiv.org/abs/math/0702399))
 

* [[Kai Behrend]], [[Ping Xu]], _Differentiable Stacks and Gerbes_ J. Symplectic Geom. Volume 9, Number 3 (2011), 285-341. ([arXiv:math/0605694](http://arxiv.org/abs/arXiv:math/0605694))

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~mat903/preprints/heinloth.pdf))

* [[Richard Hepworth]], _Vector fields and flows on differentiable stacks_ ([arXiv](http://arxiv.org/abs/0810.0979)).

* {#Carchedi11} [[David Carchedi]], _Categorical Properties of Topological and Diffentiable Stacks_, PhD thesis, Universiteit Utrecht, 2011

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, MSc thesis, Utrecht, August 2013

See also the references at [[geometric stack]] and [[topological stack]].

[[!redirects differentiable stacks]]