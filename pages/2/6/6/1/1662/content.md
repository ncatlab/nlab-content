
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

## Iterated preimages

For [[partial function|partial]] [[endofunctions]], one could also consider iterating the construction of the preimage of the partial endofunction. 

For every [[set]] $T$ and [[subset]] $S \subseteq T$, let $f:S \to T$ be a function from the subset $S$ to $T$. Given any subset $R \subseteq T$, the preimage $f^{-1}(R)$ by definition is a subset of $S$ and thus a subset of $T$. One could restrict the domain of $f$ to $f^{-1}(R)$ and the codomain of $f$ to $R$, and find the preimage of $f^{-1}(R)$ under $f$, or the 2-fold iterated preimage of $R$ under $f$:

$$f^{-2}(R) \coloneqq \{x \in S \vert \exists b \in f^{-1}(R).f(x) = b\}$$

One could repeat this definition indefinitely, which could be formalised by the indexed sets $f^{-n}(R)$ representing the __$n$-fold iterated preimage of $R$ under $f$__. 

$$f^{-0}(R) \coloneqq R$$

and for $n \in \mathbb{N}$,

$$f^{-(n+1)}(S) \coloneqq \{x \in S \vert \exists b \in f^{-(n)}(R).f(x) = b\}$$

One example of an iterated preimage is the set of [[iterated differentiable functions]] and the iterated [[continuously differentiable functions]] $C^n(\mathbb{R})$, which are the $n$-th iterated preimage of all functions and [[pointwise continuous functions]] on the [[real numbers]] under the [[derivative]]/[[Newton-Leibniz operator]] respectively. 

## Infinitely iterated preimages

The above definition of an iterated preimage is [[inductive]]; one could also consider the [[coinductive]] version of above. This leads to infinitely iterated preimages: 

For every set $T$ and subset $S \subseteq T$, let $f:S \to T$ be a function from the subset $S$ to $T$. Given any subset $R \subseteq T$, the infinitely iterated preimage is defined as the largest subset $f^{-\infty}(R) \subseteq T$ such that the preimage of $f^{-\infty}(R)$ under $f$ is $f^{-\infty}(R)$ itself.

One example of an infinitely iterated preimage is the set of [[smooth functions]]  $C^\infty(\mathbb{R})$, which is the infinitely iterated preimage of [[pointwise continuous functions]] under the [[derivative]]/[[Newton-Leibniz operator]]. 

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

[[!redirects iterated preimage]]
[[!redirects iterated preimages]]

[[!redirects infinitely iterated preimage]]
[[!redirects infinitely iterated preimages]]