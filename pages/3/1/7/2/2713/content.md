
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Here is an **unorthodox way** to state the idea of spectral triple in terms of [[FQFT]], which is in part just the reformulation of the [[quantum mechanics]] motivation that [[Alain Connes]] derived his definition from in the modern light of [[FQFT]], but which more concretely follows work by [[Maxim Kontsevich|Kontsevich]]-Soibelman and Soibelman (linked to at [[2-spectral triple]]) which [[Urs Schreiber|methinks]] is the _right_ one. 

> (but maybe eventually we should have a traditional idea section and move this here to a subsection on further interpretations)

Let $R Cob_{1|1}^{Feyn}$ be the [[cobordism category]] of [[Feynman graph]]s for the [[superparticle]] with a single type of interaction along the lines of [[(1,1)-dimensional Euclidean field theories and K-theory]]. So its morphisms are generated from $(1|1)$-dimensional super-Riemannian manifolds (i.e. super-intervals) and from a single interaction vertex

$$
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
$$

subject to the obvious associativity condition.

Then a spectral triple $(A,H,D)$ is the data encoding a sufficiently nice smooth [[functor]] 

$$
  Z_{(A,H,D)} : R Cob_{1|1}^{Feyn}  \to sVect
$$

to the [[category]] of [[super vector space]]s.

Here

* $A = Z_{(A,H,D)}(\bullet)_0$ is the even part of the [[super vector space]] assigned by the functor to the point, equipped with the structure of a [[algebra]] whose product is given by the image of the interaction vertex

  $$
    Z_{(A,H,D)}
    \left(
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
    \right)
  $$

* $H$ is some completion of $Z_{(A,H,D)}(\bullet)$  to a [[super Hilbert space]]

* and $D \in End(H)$ is an odd self-adjoint operator on $H$, which gives the value of the functor on the super-interval $(t,\theta)$ by

  $$
    (t,\theta) \mapsto \exp( - t D^2 + \theta D )
    \,.
  $$ 

(For technical details that I am glossing over see the field theory link above).

So this is the [[quantum mechanics]] of a [[superparticle]]. In the simplest case this comes from a spinor particle propagating on a [[spin structure]] [[Riemannian manifold]] $X$in which case

* $H = L^2(S)$ is the space of square integrable spinor sections;

* $D$ is the [[Dirac operator]]

* $A = C^\infty(X)$ is the space of smooth functions on $X$.

One point of a spectral triple is to take the view of world-line [[quantum mechanics]] as basic and _characterize_ the spin Riemannian geometry of $X$ entirely by this algebraic data. In particular the [[Riemannian metric]] on $X$ is encoded in the [[operator spectrum]] of $D$, which is where the notion "spectral triple" gets its name from.

Then with all the ordinary geoemtry re-encoded algebraically this way, in terms of the 1-dimensional [[quantum field theory]] that _probes_ this geometry, one can then use the same formulas to interpret spectral triple geometrically that do _not_ come from an ordinary geometry as in the above example.


#References#

* [[Alain Connes]] a)

* Alain Connes b)

* Alain Connes c)

* Alain Connes d)

## relation to physics ##

A series of blog posts looking at spectral triples from the perspective of [[FQFT]] and then concentrating on concrete examples of spectral triples that have been proposed as encoding a non-geometric [[Kaluza-Klein theory]] [[GUT]] model of particle physics is here:

* [[Urs Schreiber]], _Connes on Spectral Geometry of the Standard Model_ ([part I](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of.html), [part II](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_1.html) [part III](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_2.html), [part IV](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_3.html)) 



## von Neumann spectral triples ##

One variation uses [[von Neumann algebra]]s instead of [[C-star algebra]]s.

* M-T. Benameur, T. Fack, _On von Neumann spectral triples_ ([web](http://adsabs.harvard.edu/abs/2000math.....12233B)) 