
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


Given a [[function]] $f: X \to Y$ and a [[subset]] $S$ of $Y$, the __preimage__ (sometimes also called the __[[inverse image]]__, though that may mean something different) of $S$ under $f$ is a [[subset]] of $X$, consisting of those arguments whose values belong to $S$.  

That is,
$$ f^*(S) = \{ a: X \;|\; f(a) \in S \} .$$
A traditional notation for $f^*$ is $f^{-1}$, but this can conflict with the notation for an [[inverse function]] of $f$ (which indeed might not even exist). In fact $f^\ast$ is borrowed from a notation for [[pullbacks]]; indeed, a preimage is an example of a pullback: 

$$\array{
f^\ast(S) & \hookrightarrow & X \\ 
\downarrow & (pb) & \downarrow \mathrlap{f} \\ 
S & \hookrightarrow & Y
}$$ 

Notice also that $f^\ast$ may be regarded as an operator $P(Y) \to P(X)$ between [[power sets]]. Power sets $P(X)$ are [[exponential objects]] $2^X$ in the [[topos]] $Set$; under this identification the pre-image operator $f^\ast$ is thereby identified with the map $2^f: 2^Y \to 2^X$ (variously called "pulling back along $f$ or substituting along $f$) obtained by [[currying]] the composite map 

$$2^Y \times X \stackrel{1 \times f}{\to} 2^Y \times Y \stackrel{eval}{\to} 2.$$ 

The appearance of the asterisk as a *superscript* in $f^\ast$ serves as a reminder of the [[contravariant functor|contravariance]] of the map $f \mapsto f^\ast = 2^f$. Similarly, one uses a subscript notation such as $f_*$ (or sometimes $f_!$) for the direct [[image]], considered as an operator $f_\ast: 2^X \to 2^Y$ in the *covariant* direction. 

Naturally all of this generalizes to the context of [[toposes]], where the set $2$ is replaced by the [[subobject classifier]] $\Omega$ and $f^\ast = \Omega^f$, with a pullback description similar to the above. 


## Properties

* [[interactions of images and pre-images with unions and intersections]]:

  * [[pre-images preserve unions and intersections]] (a general reason for this being that unions are colimits, intersections are limits, and $f^\ast$ is simultaneously a left- and a right-adjoint: $f^\ast$ is right-adjoint to the [[existential quantifier]] $\exists_f$ and left-adjoint to the [[universal quantifier]] $\forall_f$) 

As emphasized by [Lawvere](#Lawvere73), the quantifiers $\exists_f, \forall_f$ are vastly generalized by the concept of [[enriched category theory|enriched]] [[Kan extensions]] which provide left and right adjoints to pulling-back operators $V^f: V^D \to V^C$ for $V$-enriched functors $f: C \to D$. 


## Related concepts

* [[level set]], [[zero locus]]

* [[image]], [[coimage]] 

For a generalisation to [[sheaf|sheaves]], see [[inverse image]].

## References 

*  {#Lawvere73}  [[F. William Lawvere]], _Metric spaces, generalized logic and closed categories_, [[TAC]] Reprint, 1986.  [Web](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html).


[[!redirects preimage]]
[[!redirects preimages]]
[[!redirects pre-image]]
[[!redirects pre-images]]
