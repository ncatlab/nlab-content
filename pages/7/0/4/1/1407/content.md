
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

_Perturbative string theory_ is something at least close to a [[vertical categorification|categorification]] of the following description of _perturbative quantum field theory_ in terms of sums over Feynman diagrams.

Recall that in [[quantum field theory]] one approach to make sense of the [[path integral]] is the _perturbation series expansion_,  which interprets the path integral as a certain sum over graphs of certain numbers assigned to each graph.

The graphs are called _Feynman graphs_, the numbers assigned to them are called _([[renormalization|renormalized]]) amplitudes_ and the sum over graphs of (renormalized) amplitudes is the _perturbation series_.

The amplitude assigned to a single graph with $n$ external edges is interpreted as the amplitude for $n$ "quanta" or "particles" of the fields in question to interact in the way indicated by the graph. 

Crucial for the motivation of the idea of string theory is the observation that this (renormalized) amplitude assigned to a graph is itself the _correlator_ of a 1-dimensional quantum field theory on that graph: the "worldline quantum field theory" describing the (relativistic) quantum mechanics of these particles. This is usually a [[sigma-model]] with parameter space the given graph and target space the spacetime on which the fields live for which the perturbation series computes the path integral.

When made explicit this is called the [worldline formalism](http://www.physics.thetangentbundle.net/wiki/Quantum_field_theory/worldline_formalism) for computing the quantum field perturbation series. A useful discussion is for instance in

* M. G. Schmidt, C. Schubert, _The Worldline Path Integral Approach to Feynman Graphs_ ([arXiv](http://arxiv.org/abs/hep-ph/9412358))


The premise of perturbative string theory is to replace the perturbation series over correlators of a 1-d QFT over graphs by a sum of correlators of a 2-dQFT over 2-dimensional surfaces -- called worldsheets. Again in simple cases this 2d QFT is a [[sigma-model]] whose target is the spacetime in which one computes interactions. 

In analogy to the previous case, one thinks of the amplitude assigned this way to a surface as the amplitude for the boundary arcs -- the _string_s -- to interact in the way given by the surface.

Some of the motivations for considering this replacement of  graphs by surfaces have been the following:

* the 2-d correlators are better behaved in that they don't have to be renormalized. The "counterterms" appearing in renormalization of ordinary QFT can be identified with contributions to the correlators that come from the linear extension of the strings (see the above reference for more on this);

* there are less choices involved: a Feynman graph is really a decorated graph with the decoration from some more or less arbitrary index set, describing the nature of the particles associated with a given edge and the nature of the interaction associated with a given vertex. In the sum over surfaces there is no extra decoration (except on the boundary of the surfaces) and one finds that instead a single string diagram (a 2d QFT correlator for a given surface) encodes already a sum over (infinitely) many particle species decorations and all possible interaction decorations for them;

* while there are less choices to be made by hand, it turns out that the effective particle content that does arise automatically from this prescription happens to be structurally of the kind one would hope for: the massless effective particles described by the string perturbation series happen to be _gauge bosons_, _fermions_ charged under them, and, notably, _graviton_s. This is structurally exactly the [[Yang-Mills theory]] input of the [[standard model of particle physics]] combined with perturbative [[quantum gravity]] that one would hope to see.

These aspects have motivated the impression that the string perturbation series might be considerably closer to the true formalism of fundamental physics than ordinary perturbative quantum field theory. This impression is however offset by the following problems:

* while the worldsheet 2-d QFT whose correlators are summed over surfaces are themselves much easier to handle than the full target space quantum physics they are used to encode, a fully complete and rigorous theory of 2d QFT is available only in simple special cases. 

* In particular, even though there are fewer arbitrary choices involved in the string perturbation series as compared to the ordinary Feynman perturbation series, one crucial choice still present is that of this worldsheet 2d QFT. By the above, every choice of worldsheet QFT (called a choice of "vacuum") corresponds to a choice of effective target space geometry (to be thought of as the one that the perturbation series computes the quantum perturbations about) and particle content (see [[2-spectral triple]] for more on that). One would therefore like to understand the space of all worldsheet QFTs whose effective target space geometry and particle content is close to the one experimentally observed. After many years of rather na&#239;ve approaches to handle or not to handle this, it has more recently at least come to the general attention that there is something to be better understood here.

* More fundamentally, already the role of the original perturbation series in quantum field theory is actually not fully understood. Its main success is the observation that truncating or resumming the perturbation series in a more or less ad hoc way, it does yield values that very well describe a plethora of real world measurements.  One imagines that there is a _non-perturbative_ definition of [[quantum field theory]] such that in certain well-defined circumstances the perturbation series does yield an approximation to it and is _a posteriori_ justified. If so, there should be an analogous nonperturbative definition of string theory. There is a large ratio of speculations as to what that might be over solid results about it.

## Subtopics

* [[landscape of string theory vacua]]

...

## References

For a list of literature see

* [[books about string theory]].


String theory leads a life somewhere in between the usual physics literature and the usual math literature. Large parts of it are still lacking a satisfactory mathematical formulation. But every now and then one aspect of the huge edifice of string theory finds a well defined formalization and branches off as a branch of pure mathematics. Famous examples are

* [[FQFT|topological field theory]]

  * [[CFT]]

    * [[flop transition]]

  * [[TCFT]]

    * [[homological mirror symmetry]]

      * [[A-infinity category|A-infinity categories]]


* [[T-duality]]

  * [[topological T-duality]]

  * [[generalized complex geometry]]

* [[quantum anomaly]] canellation [[Green-Schwarz mechanism]] 

  * [[Spin structure]]

  * [[String structure]]

  * [[Fivebrane structure]]

* etc.

The question is what the formalism might be that unifies all this into one coherent theory of higher quantum field theory.

An article summarizing information about [[cohomology|cohomological]] models for aspects of string theory and listing plenty of useful further references is

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_

A book trying to summarize the state of the art of capturing mathematical structures fundamental to the definition of perturbative string theory is

* [[Branislav Jurco]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_


[[!redirects superstring theory]]