
<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Fiber integration is a process that sends [[cohomology]] classes on a [[bundle]] $E \to B$ of [[manifold]]s to cohomology classes on the base $B$ of the bundle, by _evaluating them on each fiber_ in some sense. This sense is such that if the cohomology in question is [[de Rham cohomology]] then fiber integration is ordinary [[integration]] of [[differential form]]s over the fibers. Generally, the fiber integration over a bundle of $k$-dimensional fibers reduces the degree of the cohomology class by $k$.

## Definition


Here is the rough outline of the construction:

Let $p : E \to B$ be a [[bundle]] of smooth compact [[manifold]]s with typical [[fiber]] $F$. 

By the [[xyz-embedding theorem]] one can choose an embedding $E \hookrightarrow \mathbb{R}^N$ for some $N \in \mathbb{N}$. From this one obtains an embedding

$$
  e : E \stackrel{(e,p)}{\hookrightarrow} B \times \mathbb{R}^n
  \,.
$$

Let $N_e (E)$ be the [[normal bundle]] of $E$ relative to this $e$. This has rank $N - dim F$.

Then the quotient map

$$
  B \times \mathbb{R}^n 
  \to 
  B \times \mathbb{R}^n / (B \times \mathbb{R}^n - N_e(E))
  \simeq
  Th(N_e(E))
$$

to the [[Thom space]] of the normal bundle factors as the
[[Pontrjagin-Thom collaps map]] through the [[one-point compactification]] 
of $B \times \mathbb{R}^N$, which is the $n$-fold [[suspension]]/[[smash product]] of $B_+$ with the circle, $\Sigma^n B_+ = S^N \wedge B$.


$$
  B \times \mathbb{R}^n \to \Sigma^N B_+ \stackrel{\tau}{\to} Th(N_e(E))
  \,,
$$

This defines a morphism

$$
  \tau : \Sigma^N B_+ \stackrel{}{\to} Th(N_e(E))
  ,.
$$

Now let $H$ be some [[multiplicative cohomology theory]], and assume that the Thom space $Th(N_e(E))$ has an $H$-[[orientation in generalized cohomology|orientation]], so that we have a  [[Thom isomorphism]]. Then combined with the [[suspension isomorphism]] the pullback along $\tau$ produces a morphism

$$
  \int_F : H^\bullet(E) \to H^{\bullet - dim F}(B)
$$

of cohomologies

$$
  \array{
   H^\bullet(E)
   \\
   \downarrow^{\mathrlap{\simeq_{Thom}}{\to}}
   \\
   H^{\bullet + N - dim F}(D(N_e(E)),S(N_e(E)))
   \\
   \downarrow^{\mathrlap{\simeq}}
   \\
   \tilde H^{\bullet + N - dim F}(Th(N_e(E)))
   &
   \stackrel{\tau^*}{\to}
   &
   \tilde H^{\bullet + N - dim F}(\Sigma^N B_+)
   \\
   && \downarrow{\mathrlap{\simeq_{suspension}}}   
   \\
   &&
   H^{\bullet - dim F}(B)
   }
   \,.
$$


This operation is independend of the choices involved. It is the **fiber integration** of $H$-cohomology along $p : E \to B$.

## Examples

...

## References

A quick summary can be found from [slide 14](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf#page=14) on in

* [[Robin Koytcheff]], _A homotopy-theoretic view of Bott-Taubes integrals_ ([pdf slides](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf))

...