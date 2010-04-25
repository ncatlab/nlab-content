
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

By the [[xyz-embedding theorem]] one can choose an embedding $e:E \hookrightarrow \mathbb{R}^n$ for some $n \in \mathbb{N}$. From this one obtains an embedding

$$
  (p,e) : E \hookrightarrow B \times \mathbb{R}^n
  \,.
$$

Let $N_{(p,e)} (E)$ be the [[normal bundle]] of $E$ relative to this embedding. It is a rank $n- dim F$ bundle over the image of $E$ in $B \times \mathbb{R}^n$.

Fix a tubular neighborhood of $E$ in $B \times \mathbb{R}^n$ and identify it with the total space of $N_{(p,e)}$. Then collapsing the whole $B \times \mathbb{R}^n - N_{(p,e)}(E)$ to a point gives the [[Thom space]] of $N_{(p,e)}(E)$, and the quotient map

$$
  B \times \mathbb{R}^n 
  \to 
  B \times \mathbb{R}^n / (B \times \mathbb{R}^n - N_{(p,e)}(E))
  \simeq
  Th(N_e(E))
$$
 factors through the [[one-point compactification]] $(B \times \mathbb{R}^n)^*$
of $B \times \mathbb{R}^n$. Since $(B \times \mathbb{R}^n)^*\cong \Sigma^n B_+$,
the $n$-fold [[suspension]] of $B_+$ (or, equivalently, the [[smash product]] of $B$ with the $n$-sphere: $\Sigma^n B_+= S^n \wedge B$), we obtain a factorization
$$
  B \times \mathbb{R}^n \to \Sigma^n B_+ \stackrel{\tau}{\to} Th(N_{(p,e)}(E))
  \,,
$$
where $\tau$ is called the 
[[Pontrjagin-Thom collaps map]].

This defines a morphism

$$
  \tau : \Sigma^n B_+ \stackrel{}{\to} Th(N_{(p,e)}(E))
  ,.
$$

Now let $H$ be some [[multiplicative cohomology theory]], and assume that the Thom space $Th(N_{(p,e)}(E))$ has an $H$-[[orientation in generalized cohomology|orientation]], so that we have a  [[Thom isomorphism]]. Then combined with the [[suspension isomorphism]] the pullback along $\tau$ produces a morphism

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
   H^{\bullet + n - dim F}(D(N_{(p,e)}(E)),S(N_{(p,e)}(E)))
   \\
   \downarrow^{\mathrlap{\simeq}}
   \\
   \tilde H^{\bullet + n - dim F}(Th(N_{(p,e)}(E)))
   &
   \stackrel{\tau^*}{\to}
   &
   \tilde H^{\bullet + n - dim F}(\Sigma^n B_+)
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

More details are in 

* [[Ralph Cohen]], [[John Klein]], _Umkehr Maps_ ([arXiv:0711.0540](http://arxiv.org/abs/0711.0540))

...