
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Fiber integration is a process that sends [[cohomology]] classes on a [[bundle]] $E \to B$ of [[manifold]]s to cohomology classes on the base $B$ of the bundle, by _evaluating them on each fiber_ in some sense. This sense is such that if the cohomology in question is [[de Rham cohomology]] then fiber integration is ordinary [[integration]] of [[differential form]]s over the fibers. Generally, the fiber integration over a bundle of $k$-dimensional fibers reduces the degree of the cohomology class by $k$.

Composing pullback of cohomology classes with fiber integration yields the notion of [[transgression]].

## Definition


Here is the rough outline of the construction:

Let $p : E \to B$ be a [[bundle]] of smooth compact [[manifold]]s with typical [[fiber]] $F$. 

By the [[Whitney embedding theorem]] one can choose an embedding $e:E \hookrightarrow \mathbb{R}^n$ for some $n \in \mathbb{N}$. From this one obtains an embedding

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
  Th(N_{(p,e)}(E))
$$

factors through the [[one-point compactification]] $(B \times \mathbb{R}^n)^*$
of $B \times \mathbb{R}^n$. Since $(B \times \mathbb{R}^n)^*\cong \Sigma^n B_+$,
the $n$-fold [[suspension]] of $B_+$ (or, equivalently, the [[smash product]] of $B$ with the $n$-sphere: $\Sigma^n B_+= S^n \wedge B_+$), we obtain a factorization
$$
  B \times \mathbb{R}^n \to \Sigma^n B_+ \stackrel{\tau}{\to} Th(N_{(p,e)}(E))
  \,,
$$
where $\tau$ is called the [[Pontrjagin-Thom collapse map]].

Explicitly, as sets we have $\Sigma^n B_+ \simeq B \times \mathbb{R}^n \cup \{\infty\}$ and $Th(N_{(e,p)}(E)) = N_{(e,p)} \cup \{\infty\}$, and for $U \subset \Sigma^n B_+$ a tubular neightbourhood of $E$ and $\phi : U \to N_{(e,p)}(E)$ an isomorphism, the map 

$$
  \tau : \Sigma^n B_+ \stackrel{}{\to} Th(N_{(p,e)}(E))
$$

is defined by

$$
  \tau : x \mapsto 
  \left\{
    \array{
      \phi(x) & | x \in U
      \\
      \infty & | otherwise
    }
  \right.
  \,.
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

When $B$ is a point, one obtains integration aginst the fundamental class of $E$, 
$$
\int_E:H^\bullet(E)\to H^{\bullet-dim E}(*)
$$
taking values in the coefficients of the given chomology theory. Note that in this case $\Sigma^n B_+=S^n$, and this hints to a relationship between the Thom-Pontryagin construction and [[Spanier-Whitehead duality]]. And indeed [[Atiyah duality]] gives a homotopy equivalence between the [[Thom spectrum]] of the stable normal bundle of $E$ and the Spanier-Whitehead dual of $E$.
...

## References

A quick summary can be found from [slide 14](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf#page=14) on in

* [[Robin Koytcheff]], _A homotopy-theoretic view of Bott-Taubes integrals_ ([pdf slides](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf))

More details are in 

* [[Ralph Cohen]], [[John Klein]], _Umkehr Maps_ ([arXiv:0711.0540](http://arxiv.org/abs/0711.0540))

...