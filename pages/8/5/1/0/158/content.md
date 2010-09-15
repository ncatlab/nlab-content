
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of $\infty$-groupoid is the generalization of that of [[group]] and [[groupoid]]s to [[higher category theory]]:

an $\infty$-groupoid -- equivalently an [[(∞,0)-category]] -- is an [[∞-category]] in which all [[k-morphism]]s for all $k$ are [[equivalences]]. 

The collection of all $\infty$-groupoids forms the [[(∞,1)-category]] [[∞Grpd]].

Special cases of $\infty$-groupoids include [[groupoid]]s, [[2-groupoid]]s, [[3-groupoid]]s, [[n-groupoid]]s, [[delooping]]s of [[group]]s, [[2-group]]s, [[∞-group]]s.


## Realizations

A simple and very useful incarnation of $\infty$-groupoids is available using a [[geometric definition of higher categories]] in the form of [[simplicial set]]s that are [[Kan complex]]es: the $k$-cells of the underlying simplicial set are the [[k-morphism]]s of the $\infty$-groupoid, and the Kan [[horn]]-filler conditions encode the fact that adjacent $k$-morphisms have a (non-unique) composite $k$-morphism and that every $k$-morphism is invertible with respect to this composition.
See [[Kan complex]] for a detailed discussion of how these incarnate $\infty$-groupoids. 

The [[(∞,1)-category]] of all $\infty$-groupoids is [[presentable (∞,1)-category|presented]] along these lines by the Quillen [[model structure on simplicial sets]], whose fibrant-cofibrant objects are precisely the Kan complexes:

$$
  \infty Grpd \simeq (sSet_{Quillen})^\circ
  \,.
$$

 One may turn this geometric definition into an [[algebraic definition of higher category|algebraic definition of ∞-groupoids]] by _choosing [[horn]]-fillers_ . The resulting notion is that of an [[algebraic Kan complex]] that has been shown by [[Thomas Nikolaus]] to yield an equivalent [[(∞,1)-category]] of $\infty$-groupoids.

Every other algebraic definition of [[omega-categories]] is supposed to yield an equivalent notion of $\infty$-groupoid when restricted to $\omega$-categories all whose [[k-morphism]]s are invertible. This is the statement of the [[homotopy hypothesis]], which is for Kan complexes and algebraic Kan complexes a theorem and for other definitions regarded as a consistency condition.

 
Notably in [[Pursuing Stacks]] and the earlier letter to Larry Breen, [[Alexander Grothendieck]] initiated the study of $\infty$-groupoids and the homotopy hypothesis with his original definition of [[Grothendieck weak infinity-groupoid]]s, that has recently attracted renewed attention.

One may also consider entirely strict $\infty$-groupoids, usually called $\omega$-groupoids or [[strict ∞-groupoids]]. These are equivalent to [[crossed complexes]] of [[group]]s and [[groupoid]]s. 

$\infty$-groupoids with a single object are the [[delooping]] $\mathbf{B}G$ of [[∞-group]]s. These are equivalently modeled by [[simplicial group]]s. Notably abelian simplicial groups are therefore a model for abelian $\infty$-groupoids. Under the [[Dold-Kan correspondence]] these are equivalent to non-negatively graded [[chain complex]]es, which therefore also are a model for abelian $\infty$-groupoids. This way much of [[homological algebra]] is secretly the study of special $\infty$-groupoids.


[[!redirects ∞-groupoid]]
[[!redirects ∞-groupoids]]
[[!redirects infinity groupoid]]
[[!redirects infinity-groupoids]]
[[!redirects ∞-groupoid]]