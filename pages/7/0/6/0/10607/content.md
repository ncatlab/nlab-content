

## Idea

The notion of [[adjunction]] as such expresses a [[duality]]. The stronger notion of an "adjoint cyclinder" is meant to express specifically a _duality between opposites_. 

The notion was suggested in ([Lawvere 94, p. 11](#Lawvere94)) (and in view of [Lawvere 91](#Lawvere91)) to capture the phenomena of "Unity and Identity of Opposites" as they appear informally in [[Georg Hegel]]'s _[[Science of Logic]]_. 

(One might therefore say the notion was suggested to capture the idea of "dialectic", though there is some debate as to wether Hegel's  somewhat mythical "creation out of [[paradox]]" should really go by this term, see [this Wikipeda entry](#Wikipedia) ).

## Definition

In ([Lawvere 94](#Lawvere94)) an _adjoint cylinder_ is defined to be an [[adjoint triple]] such that the middle adjoint is [[full and faithful functor|full and faithful]].

To make the role of the opposites more pronounced here, notice that this is equivalently an [[adjoint pair]] of a [[monad]]/[[comonad]]

$$
  \mathbf{L} \dashv \mathbf{R}
$$

hence an [[adjoint pair]] of [[modal operators]] (as in _[[modal type theory]]_).

Given any such, we may say that that the "Unity" expressed by the two opposites is exhibited by the canonical [[natural transformation]]

$$
  \array{
    \mathbf{L} X &\longrightarrow& X &\longrightarrow& \mathbf{R}X
    \\
    opposite\;1 && unity && opposite\;2
  }
$$

## Examples

### Werden : Sein $\dashv$ Nichts

$$
  \array{
    \emptyset \longrightarrow X \longrightarrow \ast
  }
$$

### Continuuum : repulsion $\dashv$ cohesion

$$
  \array{
    \flat X \longrightarrow X \longrightarrow \int X
  }
$$



## References

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ in A. Carboni, M. Pedicchio, G. Rosolini, _Category Theory_  , [[Como|Proceedings of the International Conference held in Como]], Lecture Notes in Mathematics 1488, Springer (1991)
 {#Lawvere91}


* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_, Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([[LawvereCohesiveToposes.pdf:file]])
  {#Lawvere94}

* Wikipedia, _[Hegelian dialectic](http://en.wikipedia.org/wiki/Hegelian_dialectic)_
  {Wikipedia}

[[!redirects adjoint cylinders]]
