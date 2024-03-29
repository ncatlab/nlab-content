
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


This page is meant to provide non-technical motivation for the notion of _[[cohesion]]_ as in formalized in the notions

* _[[cohesive topos]]_, 

* _[[cohesive (∞,1)-topos]]_, _[[cohesive homotopy type theory]]_ .


#Contents#
* table of contents
{:toc}

## Motivation

A notion of _[[cohesion]]_ on a collection $\mathbf{H}$ of [[spaces]] is supposed to be a means to specify how [[points]] in any space $X \in \mathbf{H}$ "hang together" or "cohere", analogous to how water molecules in a droplet of water are held together by [cohesion (in the sense of chemistry)](http://en.wikipedia.org/wiki/Cohesion_%28chemistry%29). (The inclined reader may, or may not, recognize this also in _[WdL, Form und Inhalt](Science+of+Logic#FormUndInhalt)_, see the discussion there.)

A basic example arises for [[topological spaces]] or [[manifolds]]: here the "droplet of water" is an _[[open ball]]_ of points. Indeed, one of the central examples of cohesive spaces is that of [[smooth spaces]] and these are spaces characterized by the fact that they can be _probed_ by smooth open balls (in the sense described at _[[motivation for sheaves, cohomology and higher stacks]]_), such that these smooth open balls are the _basic_ "cohesive droplets" out of which any smooth space is built (this roughly in the sense of [[topological base|basis of a topology]], but a bit more generally than that).

That intuition should be evident enough. The question is which formal axioms capture this droplet-intuition accurately and efficiently. The crucial insight of [[Bill Lawvere]] (see the references at _[[cohesive topos]]_) was that a rather minimalistic set of axioms already does the job:

1. there has to be an assignment $\Pi : \mathbf{H} \to Set$ that sends every cohesive space $X$ to its _set of cohesively [[connected components]]_. For instance a single open ball as above, a basic droplet, is sent to the set $\{*\}$ with a single element.

1. We should be entitled to regard every [[set]] $S \in Set$ trivially as a cohesive space in two ways: 

    * either we regard every element in $S$ as an atomic cohesive droplet itself, cohesively disconnected to any other point. Call the resulting cohesive space $Disc(X)$. For [[smooth space|smooth cohesion]], $Disc(X)$ is simply the [[discrete space|discrete manifold]] being the [[disjoint union]] of one point per element in $S$.

    * or, at the opposite extreme, we regard all the elements in $S$ as being cohesively connected, hence regard all of $S$ itself as one single big cohesive droplet. We write $coDisc(X)$ for $S$ regarded as a cohesive space this way, because in the context of [[Euclidean-topological infinity-groupoid|topological cohesion]] this is the [[codiscrete space]] on the given set.

1. The collection of discrete and codiscrete cohesive spaces should sit nicely inside the collection of all cohesive spaces, essentially in just the obvious way that one intuitively expects. For instance cohesive maps between two discretely cohesive spaces should be simply maps between the underlying sets, and so on.

   In particular the notion of "discrete" exhibited by the collection of discrete objects has indeed to be compatible with the notion of "cohesive" as seen by that map $\Pi$ above. This is just the evident consistency condition: for instance if $Disc(S)$ is a set regarded as a discrete cohesive space, then $\Pi(Disc(S))$, which is supposed to be its set of cohesively connected points, should be just $S$ itself, since no point in $Disc(S)$ is supposed to be cohesively connected to any other.  

   In particular $\Pi(Disc(*))$ should be the point again.

That's essentially it, already. It sounds very simple (hopefully) and indeed it is very simple. Once one knows the notion of an [[adjoint functor]] it is pretty straightforward to formalize the above text in terms of that notion, to arrive at the concept of _[[cohesive topos]]_. 

The interesting observation is that simple as this idea is, it has very powerful consequences ... once it is formalized not just with adjoint functors but with [[adjoint (∞,1)-functors]]. This is conceptually a very simple step. Moreover, in the [[foundations]] provided by [[homotopy type theory]] this is actually the simpler and more natural step. It leads to _[[cohesive (∞,1)-toposes]]_ and _[[cohesive homotopy type theory]]_.

## Special aspects

### Local contractibility / local $\infty$-connectedness
 {#LocalContractibility}

While cohesive spaces subsume several familiar notions of [[geometry]], there are some constraints.

In particular, a cohesive space is always _locally contractible_ or rather _locally $\infty$-connected_ in some sense. The local contractions are those of the "basic cohesive droplets", in the spirit of the above discussion. (In the [[(∞,1)-topos theory|(∞,1)-topos theoretic]] formalization this is reflected in the fact that every [[cohesive (∞,1)-topos]] is in particular a _[[locally ∞-connected (∞,1)-topos]]_.)

For instance [[locally contractible topological ∞-groupoids]] are cohesive, as are [[Euclidean-topological ∞-groupoids]].

But a geometry modeled on a [[small category|small]] [[full subcategory]] of [[Top]] that contains [[locally contractible topological space|locally non-contractible topological spaces]] will in general not be cohesive. In particular for instance general [[topological stacks]] do not live in a cohesive $(\infty,1)$-topos. But for instance [[differentiable stacks]] do, and generally [[smooth ∞-groupoids]], because every [[manifold]] and hence in particular every [[smooth manifold]] is locally contractible.


## Related entries

* [[geometry of physics]]

* [[fiber bundles in physics]]

* [[higher category theory and physics]]

* [[string theory FAQ]]

* [[twisted smooth cohomology in string theory]]

* [[motives in physics]]

* [[Hilbert's sixth problem]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[applications of (higher) category theory]]

* [[motivation for higher differential geometry]]



category: motivation

[[!redirects motivation for cohesion]]

