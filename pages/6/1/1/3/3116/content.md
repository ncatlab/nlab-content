[[!redirects fermat theory]]

## Idea ##

A 'Fermat theory' is a [[Lawvere theory]] that extends the usual theory of [[commutative rings]] by permitting differentiation.  

The idea of a Fermat theory seems to have been invented by Anders Kock.  But as the name suggests, it has its roots in an old observation of Fermat.  Namely: if $f : \mathbb{R} \to \mathbb{R}$ is a smooth function, then

$$f (x+y) = f(x) + y \tilde{f}(x,y) $$

for a unique smooth function $\tilde{f} : \mathbb{R}^2 \to \mathbb{R}$.  Clearly

$$ \tilde{f}(x,y) = \frac{f(x+y) - f(x)}{y} $$

for $y \ne 0$, but the interesting thing is that

$$\tilde{f}(x,0) = f'(x)$$

So, the function $\tilde{f}$ knows about the derivative of $f$!

Fermat noted this for $f$ a polynomial; Hadamard generalized it to smooth $f$.   The function $\tilde{f}$ is also called a **Hadamard quotient**.    

If we take $\tilde{f}(x,0) = f'(x)$ as a _definition_ of the derivative, we can derive many of the basic rules for derivatives from the formula

$$f(x+y) = f(x) + y \tilde{f}(x,y) $$

using just algebra --- no limits!  As an exercise, the reader should check these rules:

$$(f + g)' = f' + g'$$

$$(f g)' = f' g + f g' $$

$$(f \circ g)' = (f' \circ g) g' $$

All these ideas also work if $f$ is parametrized, that is, a smooth function from $\mathbb{R} \times \mathbb{R}^n$ to $\mathbb{R}$, where the $n$ extra variables serve as 'parameters'.

## Definition ##

The above observations suggest defining the following kind of Lawvere theory.  A **Fermat theory** is an extension of the algebraic theory of commutative rings,
such that for any $(n+1)$-ary operation $f$ there is a unique $(n+2)$-ary operation $\tilde{f}$ such that

$$ f(x + y, \vec{z}) =
f(x, \vec{z}) + y \tilde{f}(x,y,\vec{z})$$

where $\vec{z}$ is a list of $n$ variables which act as parameters.  Here we are abusing language by writing the operations $f$ and $\tilde{f}$ as if they were functions, to avoid unintuitive commutative diagrams.

## Examples ##

There is a Lawvere theory called **the theory of $C^\infty$-rings**, whose $n$-ary operations are the smooth maps $f: \mathbb{R}^n \to \mathbb{R}$, with composition of operations defined in the obvious way.  An algebra of this Lawvere theory is called a **$C^\infty$-ring**.  

The theory of $C^\infty$-rings is a Fermat theory.  For any smooth manifold $M$, the algebra of smooth real-valued functions $C^\infty(M)$ is a $C^\infty$ ring.  More generally, if $M$ is any [[diffeological space]], [[Chen space]] or [[Frolicher space]], we can define $C^\infty(M)$, and this will be a $C^\infty$-ring.

## Partial derivatives ##

If $T$ is a Fermat theory and $f$ is any $(n+1)$-ary operation, we may define an operation $\partial_1 f$

by

$$\partial_1(x, \vec{z})  = \tilde{f}(x,0,\vec{z})$$

This acts like the partial derivative of $f$ with respect to its first argument. With a bit of more work we get a list of $n$-ary operations $\partial_i f$.   So, if $T(n)$ denotes the set of $n$-ary operations in our algebraic theory $T$, we get maps

$$\partial_i : T(n) \to T(n) $$

for $1 \le i \le n$.  

For any Lawvere theory, $T(n)$ is an algebra of that theory --- the free $T$-algebra on $n$ generators.  So, when $T$ is a Fermat theory, $T(n)$ is
automatically a commutative ring.  One can check that each map

$$\partial_i : T(n) \to T(n) $$

is a derivation of this ring --- this is really just the chain rule.

## K&#228;hler differentials for Fermat theories ##

<b>Theorem:</b> The map

$$\langle \partial_1, \dots, \partial_n \rangle : T(n) \to \prod_{i = 1}^{n}  T(n) $$

is the universal $T$-derivation of $T(n,1)$.

[[John Baez]]: Alas, I'm not quite sure what this theorem means.  I think it's
something like this: if $M$ is a module of $T(n)$ and $\delta : T(n) \to M$ is a derivation, then $\delta$ factors through the map $\langle \partial_1, \dots, \partial_n \rangle$.  Unfortunately by 'module' we probably mean something more than a module of the underlying commutative ring, and by '$T$-derivation' we probably means something more than a derivation in the usual sense.
  
Anyway, the point of this theorem is that it gives us a version of [[Kähler differentials]] for $T(n)$.

This material is a summary of the following talk:

* Anders Kock, K&#228;hler differentials for Fermat theories,  _Fields Workshop on Smooth Structures in Logic, Category Theory and Physics_, May 1, 2009, University of Ottawa.  ([abstract](http://aix1.uottawa.ca/~scpsg/Fields09/smooth.abstracts.html))

For more, see:

* Alexander Hoffnung, Smooth Structure in Ottawa II.  ([blog entry](http://golem.ph.utexas.edu/category/2009/05/smooth_structures_in_ottawa_ii.html#c030745))

and the comments on this blog entry.