
<div class="rightHandSide toc">

[[!include cohomology - contents]]

***

[[!include functorial quantum field theory - contents]]

</div>


There are well-known _geometric models_ for some [[cohomology theory|cohomology theories]]. For instance

* [[integral cohomology]] is modeled by [[line bundle]]s and [[bundle gerbe]]s, etc. 

and 

* [[K-theory]] is modeled by [[vector bundle]]s.

A geometric model for [[elliptic cohomology]] is supposed to be an analogous construction for [[elliptic cohomology]] or for [[tmf]].

It is an old idea that analogous to how [[differential K-theory]] is modeled by parallel transport in [[vector bundle]]s and hence by [[functor]]s $Bord_1(X) \to Vect$,   [[elliptic cohomology]] should somehow be modeled by functors $Bord_2(X) \to Vect$, where $Bord_2(X)$ is a 1-category of [[cobordism]]s equipped with maps to $X$.

[[Stephan Stolz]] and [[Peter Teichner]] have initiated a program studying this in the article [[What is an elliptic object?]]. 

The fundamental idea of this program is essentially to encode [[parallel transport]] along [[cobordism]]s with maps into a given space $X$ pretty much along the lines of [[schreiber:differential cohomology|functorial differential cohomology]]. One expects that this encodes actually the differential refinements of the corresponding [[cohomology|cohomology theories]], such as [[differential K-theory]]. However, currently in the program one divides out [[concordance]] which effectively divides out the differential information and keeps just the underlying topological information.

The fundamental result of this program so far is that there is a useful notion of 2d [[FQFT]] over $X$ such that its [[partition function]] is indeed [[topological modular form]]-valued, so that it is a candidate for a model of [[tmf]].

The following is going to be an exposition of this partial result:

* Outline of the constructions and statements

  * [[Axiomatic field theories and their motivation from topology]]

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]

* Definitions

  * [[bordism categories following Stolz-Teichner]]

  * [[(2,1)-dimensional Euclidean field theories]]

#References#

The program was initiated in 

* [[Stephan Stolz]], [[Peter Teichner]], _[[What is an elliptic object?]]_

After the original sketch in terms of extended [[FQFT]] subsequent work concentrated on ordinary 1-categorical constructions, the goal being to make very clear, and transparent and rigorous the constructions involved and the claim that 

> the [[partition function]] of a (2|1)-dimensional -Eudlidean [[FQFT]] is an [[integral modular form]].

This latest development on this is in 

* [[Stephan Stolz]], [[Peter Teichner]], _Super symmetric field theories and integral modular forms_ ([pdf](http://www.nd.edu/~stolz/SusyQFT.pdf))

> **warning** [[Urs Schreiber|I]] am being told that this is by now outdated and to be replaced by an improved version, wich however is apparently not available yet

[[!redirects geometric models for tmf]]
[[!redirects geometric models for TMF]]