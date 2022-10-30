
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

The notion was suggested in ([Lawvere 91, p. 7](#Lawvere91), [Lawvere 94, p. 11](#Lawvere94)) to capture the phenomena of "Unity and Identity of Opposites" as they appear informally in [[Georg Hegel]]'s _[[Science of Logic]]_. 

(One might therefore say the notion is meant to capture the idea of "dialectic", though there is some debate as to wether Hegel's  somewhat mythical "creation out of [[paradox]]" should really go by this term, see [this Wikipeda entry](#Wikipedia) ).

## Definition

In ([Lawvere 94](#Lawvere94)) an _adjoint cylinder_ is defined to be an [[adjoint triple]] such that the induced [[adjoint pair]] on one of the two sides consists of [[identity]] functors.

This means equivalently that the other [[adjoint pair]] consists of an [[idempotent monad|idempotent]] [[monad]] and [[comonad]], either of the form

$$
  U \;\colon\; modality \dashv comodality
  \,,
$$

or in the form

$$
  U \;\colon\; comodality \dashv modality
  \,,
$$

hence is an [[adjoint pair]] of [[modal operators]] (as in _[[modal type theory]]_). A category equipped with an adjoint modality of the second form is called a _[[category of being]]_ in ([Lawver 91](#Lawvere91)).

Given any such, we may say that the "unity" expressed by the two opposites is exhibited by the canonical [[natural transformation]]

$$
  U X 
  \;\colon\;
  \array{
    comodal X &\longrightarrow& X &\longrightarrow& modal X
    \\
    opposite\;1 && unity && opposite\;2
  }
$$

which is the composite of the [[counit of a comonad|counit of the comodality]] and the [[unit of a monad|unit of the modality]].

One can consider longer sequences of such adjoints of co/modalities, but the longer they get, the less likely they are to be non-trivial. The longest that still has good nontrivial models seems to be [[adjoint triples]] of modalities. Of these there is then similarly either the form

$$
  modality \dashv comodality \dashv modality
$$

(the "Yin triple") as for instance in the definition of _[[cohesion]]_ and

$$
  comodality \dashv modality \dashv comodality
$$

(the "Yang triple") as for instance in the definition of _[[differential cohesion]]_.

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


Looking through ([Hegel 1812, vol 1, book 1, section 1, chapter 1](#Hegel1812)) one might call $\emptyset$ "nothing", call $\ast$ "being" and then call this unity of opposites "becoming". In particular in &#167;174 of _[[Science of Logic]]_ it says

> there is nothing which is not an intermediate state between being and nothing

which seems to be well-captured by the above unity transformation.

### Quantity : discreteness $\dashv$ continuity
 {#Mengen}

The adjoint modality in a [[local topos]] is that given by
[[flat modality]] $\dashv$ [[sharp modality]]

$$
  \flat \dashv \sharp
  \,.
$$

Capturing [[discrete objects]]/[[codiscrete objects]].

The corresponding unity transformation is

$$
    \flat X \longrightarrow X \longrightarrow \sharp X
$$

According to ([Lawvere 94, p. 6](#Lawvere94)) this unity captures the duality that in a [[set]] all [[elements]] are distinct and yet indistinguishable, an apparent [[paradox]] that may be traced back to [[Georg Cantor]].  

Looking through Hegel's [[Science of Logic]] at _[On discreteness and repulsion](#Science+of+Logic#OnDiscretenessAndRepulsion)_ one can see that matches with what Hegel calls

> (par 398) Quantity is the unity of these moments of continuity and discreteness

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \sharp X
    \\
    {moment\;of \atop discreteness} && && {moment\;of \atop continuity}
  }
$$


### Continuuum : repulsion $\dashv$ cohesion
 {#ContinuumRepulsionCohesion}

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

### Infinitesimal Continuuum : infin. repulsion $\dashv$ infinit. cohesion
 {#ContinuumRepulsionCohesion}

For $\mathbf{H}$ equipped moreover with [[differential cohesion]],
there is the [[infinitesimal object|infinitesimal]] version of 
[[shape modality]] $\dashv$ [[flat modality]]  namely the adjoint modality

[[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]


$$
  \int^{inf} \dashv \flat^{inf}
  \,.
$$

The corresponding unity-transformation is the 

$$
  \array{
    \flat^{inf} X \longrightarrow X \longrightarrow \int^{inf} X
  }
$$

maps from the [[coefficients]] for [[crystalline cohomology]] to the [[de Rham space]] of types $X$, where all infinitesimal neighbour points are identified. 

In view of the above the unity exhibited here is clearly to be called the "infinitesimal continuum".



### Cohesive sets

The combination of the above two examples of [Continuum](#ContinuumRepulsionCohesion) and [Quantity](#Mengen) is an [[adjoint triple]] of [[modalities]]

$$
  \int \;\dashv\; \flat \;\dashv\; \sharp
$$

[[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

characteristic of a [[cohesive topos]].

### Totally distributive categories

For $\mathcal{K}$ a [[totally distributive category]]
it induces on its [[category of presheaves]] an adjoint modality whose [[right adjoint]] is the [[Yoneda embedding]] $Y$ postcomposed with its [[left adjoint]] $X$.

## Related concepts

* [[modal type theory]]

* [[category of being]]

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
[[!redirects unity and identity of opposites]]

[[!redirects dialectic]]
[[!redirects dialectics]]

[[!redirects duality of opposites]]
[[!redirects dualities of opposites]]