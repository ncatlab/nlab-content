
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _essentially surjective and full functor_ is a [[functor]] which is both [[essentially surjective functor|essentially surjective]] and [[full functor|full]].

Sometimes this condition is abbreviated _eso and full_, where "eso" is short for "essentially surjective on objects".

## Properties

### As 0-connected morphisms

+-- {: .num_prop #EsoAndFullIs0Connected}
###### Proposition

Let $f \colon X \longrightarrow Y$ be a [[functor]] between [[small categories]] that happen to be [[groupoids]], and write  $i \;\colon\; Grpd \hookrightarrow \infty Grpd$ for the [[fully faithful (infinity,1)-functor|full inclusion]] of groupoids into the [[(∞,1)-topos]] [[∞Grpd]] of [[∞-groupoids]]. Then the following are equivalent:

* $F$ is essentially surjective and full

* $i(F)$ is a [[0-connected morphism]]

=--

+-- {: .proof}
###### Proof

As discussed there, an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] in [[∞Grpd]] between 1-groupoids is precisely an
[[essentially surjective functor]].

So it remains to check that for an essentially surjective $f$, being
0-connected is equivalent to being full.

The [[homotopy pullback]] $X \times_Y X$ is given by the groupoid 
whose objects are triples $(x_1, x_2 \in X, \alpha : f(x_1) \to f(x_2))$
and whose morphisms are corresponding tuples of morphisms in $X$ making the
evident square in $Y$ commute.

By prop. \ref{CharacterizationByDiagonal} 
it is sufficient to check that the [[diagonal]] functor $X \to X \times_Y X$ is
(-1)-connected, hence, as before, essentially surjective, precisely if $f$ is full.
 
First assume that $f$ is full. 
Then for $(x_1,x_2, \alpha) \in X \times_Y X$
any object, by [[full functor|fullness]] of $f$ 
there is a morphism $\hat \alpha : x_1 \to x_2$ in $X$,
such that $f(\hat \alpha) = \alpha$.

Accordingly we have a morphism
$(\hat \alpha,id) : (x_1, x_2) \to (x_2, x_2)$ in $X \times_Y X$ 

$$
  \array{
     f(x_1) &\stackrel{f(\hat \alpha)}{\to}& f(x_2)
     \\
     \downarrow^{\mathrlap{\alpha}} && \downarrow^{\mathrlap{id}}
     \\
     f(x_2) &\stackrel{id}{\to}& f(x_2)
  }
$$

to an object in the diagonal.

Conversely, assume that the diagonal is essentially surjective. Then 
for every pair of objects $x_1, x_2 \in X$ such that there is a morphism
$\alpha : f(x_1) \to f(x_2)$ we are guaranteed morphisms
$h_1 : x_1 \to x_2$ and $h_2 : x_2 \to x_2$ such that 

$$
  \array{
    f(x_1) &\stackrel{f(h_1)}{\to}& f(x_2)
    \\
    \downarrow^{\mathrlap{\alpha}} && \downarrow^{\mathrlap{id}}
    \\
    f(x_2) &\stackrel{f(h_2)}{\to}& f(x_2)
  }
  \,.
$$

Therefore $h_2^{-1}\circ h_1$ is a preimage of $\alpha$ under $f$,
and hence $f$ is full.

=--

 
### Eso+full/faithful factorization system

In the [[2-topos]] [[Cat]], the [[pair]] of [[classes]] of [[morphisms]] consisting of 

* left class: essentially surjective and full functors

* right class: [[faithful functors]]

form a [[factorization system in a 2-category]] -- the [[(eso and full, faithful) factorization system]].

When restricted to the [[(2,1)-topos]] [[Grpd]] and in view of Prop. \ref{EsoAndFullIs0Connected}, this is the special case of the [[n-connected/n-truncated factorization system]] in the [[(∞,1)-topos]] [[∞Grpd]] for the case that $(n = 0)$ and restricted to [[1-truncated]] [[objects]]. More on this is at _[infinity-image --  Of Functors between groupoids](infinity-image#NImagesOf1FunctorsBetweenGroupoids)_.

[[!redirects essentially surjective and full functors]]

## Related concepts

[[!include properties of functors -- contents]]

[[!redirects eso and full functor]]
[[!redirects eso and full functors]]

