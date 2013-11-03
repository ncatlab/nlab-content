
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of [[adjunction]] as such expresses a [[duality]]. The stronger notion of an _adjoint cyclinder_ or _adjoint modality_ is meant to express specifically a _duality between opposites_. 

The notion was suggested in ([Lawvere 94, p. 11](#Lawvere94)) (and in view of [Lawvere 91](#Lawvere91)) to capture the phenomena of "Unity and Identity of Opposites" as they appear informally in [[Georg Hegel]]'s _[[Science of Logic]]_. 

(One might therefore say the notion was suggested to capture the idea of "dialectic", though there is some debate as to wether Hegel's  somewhat mythical "creation out of [[paradox]]" should really go by this term, see [this Wikipeda entry](#Wikipedia) ).

## Definition

In ([Lawvere 94](#Lawvere94)) an _adjoint cylinder_ is defined to be an [[adjoint triple]] such that the induced [[adjoint pair]] on one of the two sides consists of [[identity]] functors.

This means equivalently that the other [[adjoint pair]] consists of an [[idempotent monad|idempotent]] [[monad]]/[[comonad]]

$$
  U \;\colon\; \mathbf{L} \dashv \mathbf{R}
  \,,
$$

hence is an [[adjoint pair]] of [[modal operators]] (as in _[[modal type theory]]_).

Given any such, we may say that that the "unity" expressed by the two opposites is exhibited by the canonical [[natural transformation]]

$$
  U X 
  \;\colon\;
  \array{
    \mathbf{L} X &\longrightarrow& X &\longrightarrow& \mathbf{R}X
    \\
    opposite\;1 && unity && opposite\;2
  }
$$

which is the composite of the $\mathbf{L}$-[[counit of a comonad|counit]] and the $\mathbf{R}$-[[unit of a monad|monad]] (or the other way around).

## Examples

### Werden : Sein $\dashv$ Nichts

For $\mathbf{H}$ a [[topos]]/[[(∞,1)-topos]] consider the "initial topos", the [[terminal category]] $\ast \simeq Sh(\emptyset)$ ([[category of sheaves]] on the empty site).

There is then an [[adjoint triple]]

$$
  \mathbf{H}
   \stackrel{\overset{\vdash \ast}{\longleftarrow}}{\stackrel{\overset{}{\longrightarrow}}{\underset{\vdash \emptyset}{\longleftarrow}}}
  \ast
$$

given by including the [[initial object]] $\emptyset$ and the [[terminal object]] $\ast$ into $\mathbf{H}$.

In the [[type theory]] of $\mathbf{H}$ this corresponds to the [[adjoint pair]] of [[modalities]]

$$
  \emptyset \dashv \ast
$$

which are constant on the [[initial object]]/[[terminal object]], respectively.

The induced unity transformation is

$$
  \array{
    \emptyset \longrightarrow X \longrightarrow \ast
  }
$$

hence the unique factorization of the unique function $\emptyset \longrightarrow \ast$ through any other [[type]].


Looking through ([Hegel 1812, vol 1, book 1, section 1, chapter 1](#Hegel1812)) one might call $\emptyset$ "nothing", call $\ast$ "being" and then call this unity of opposites "becoming". In particular in &#167;174 it says

> there is nothing which is not an intermediate state between being and nothing

which seems to be well-captured by the above unity transformation.


### Continuuum : repulsion $\dashv$ cohesion

For $\mathbf{H}$ a [[cohesive topos]]/[[cohesive (∞,1)-topos]]
the [[shape modality]] $\dashv$ [[flat modality]] constitute an adjoint cylinder

$$
  \int \dashv \flat
  \,.
$$

The corresponding unity-transformation is the [points-to-pieces transform](cohesive%20topos#CanonicalComparison)

$$
  \array{
    \flat X \longrightarrow X \longrightarrow \int X
  }
$$

Looking through ([Hegel 1812, vol 1, book 1, section 2, chapter 1](#Hegel1812)) one might call $\flat$ "repulsion", call $\int$ "attraction"/"[[cohesion]]" and then call this unity of opposites "[[continuum]]". Indeed, by the discussion at _[[cohesive topos]]_, this does quite well capture the geometric notion of continuum geometry.


### Menge : discreteness $\dashv$ codiscreteness

The other adjoint cylinder in a [[cohesive topos]] is that given by
[[flat modality]] $\dashv$ [[sharp modality]]

$$
  \flat \dashv \sharp
  \,.
$$

Capturing [[discrete objects]]/[[codiscrete objects]].

The corresponding unity transformation

$$
  \flat X \longrightarrow X \longrightarrow \sharp X
$$

According to ([Lawvere 94, p. 6](#Lawvere94)) this unity captures the duality that in a [[set]] all [[elements]] are distinct and yet indistinguishable, an apparent [[paradox]] that may be traced back to [[Georg Cantor]].  (Which is also somewhere in Hegel, need to find the paragraph number...)


## References

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ in A. Carboni, M. Pedicchio, G. Rosolini, _Category Theory_  , [[Como|Proceedings of the International Conference held in Como]], Lecture Notes in Mathematics 1488, Springer (1991)
 {#Lawvere91}


* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_, Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([[LawvereCohesiveToposes.pdf:file]])
  {#Lawvere94}

* [[Georg Hegel]], _[[Science of Logic]]_, 1812
 {#Hegel1812}

* Wikipedia, _[Hegelian dialectic](http://en.wikipedia.org/wiki/Hegelian_dialectic)_
  {#Wikipedia}



[[!redirects adjoint cylinders]]

[[!redirects adjoint modality]]
[[!redirects adjoint modalities]]

[[!redirects opposite]]
[[!redirects opposites]]

[[!redirects unity of opposites]]