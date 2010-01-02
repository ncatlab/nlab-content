A 'Fermat theory' is an [[algebraic theory]] that extends the usual theory of [[commutative rings]] by permitting differentiation.  The idea of a Fermat theory seems to have been invented by Anders Kock.  But as the name suggests, it has its roots in an old observation of Fermat.  Namely: if $f : \mathbb{R} \to \mathbb{R}$ is a smooth function, then

$$f (x+y) = f(x) + y \tilde{f}(x,y) $$

for a unique smooth function $\tilde{f} : \mathbb{R}^2 \to \mathbb{R}$.  Note also that

$$f'(x) = \tilde{f}(x,0)$$

Fermat noted this for $f$ a polynomial; Hadamard generalized it to smooth $f$.  Most of the basic rules for derivatives can be efficiently derived from this formula.

This is also true if $f$ is parametrized, that is, a smooth function from $\mathbb{R} \times \mathbb{R}^n$ to $\mathbb{R}$, where the $n$ extra variables serve as 'parameters'.

This suggests defining the following kind of algebraic theory.  A **Fermat
theory** is an extension of the algebraic theory of commutative rings,
such that for any $(n+1)$-ary operation $f$ there is a unique $(n+2)$-ary
operation $\tilde{f}$ such that

$$ f(x + y, \vec{z}) =
f(x, \vec{z}) + y \tilde{f}(x,y,\vec{z})$$

where $\vec{z}$ is a list of $n$ variables, which act as parameters.  Here we are abusing language by writing the operations $f$ and $\tilde{f}$ as if they were functions, to avoid unintuitive commutative diagrams.

This lets us define an operation

$$\frac{\partial f}{\partial x} (x, \vec{z}) $$

by

$$\frac{\partial f}{\partial x} (x, \vec{z})  = \tilde{f}(x,0,\vec{z})$$

With a bit of more work we get for each $n$-ary operation $F$ a list of $n$-ary operations $\partial_i F$.   So, if $T(n)$ denotes the set of $n$-ary operations in our algebraic theory $T$, we get maps

$$\partial_i : T(n) \to T(n) $$

For any algebraic theory, $T(n)$ is an algebra of that theory --- the free
$T$-algebra on $n$ generators.  So, when $T$ is a Fermat theory, $T(n)$ is
automatically a commutative ring.  One can check that each map

$$\partial_i : T(n) \to T(n) $$

is a derivation of this ring --- this is really just the chain rule.

<b>Theorem:</b> The map

$$\langle \partial_1, \dots, \partial_n \rangle : T(n) \to \prod_{i = 1}^{n}  T(n) $$

is the universal $T$-derivation of $T(n,1)$.

[[John Baez]]: Alas, I'm not quite sure what this theorem means.  But I think it's
something like this: if $M$ is a module of $T(n)$ and $\delta : T(n) \to M$
is a derivation, then $\delta$ factors through the map $\langle \partial_1,
\dots, \partial_n \rangle$.

So, this theorem gives us a version of [[Kähler differentials]] for $T(n)$.

