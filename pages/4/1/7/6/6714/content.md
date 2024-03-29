
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition



The [[short exact sequence]] of [[abelian group]]s

$$
0\to \mathbb{Z}\stackrel{\cdot2}{\to} \mathbb{Z}\to\mathbb{Z}/2\mathbb{Z}\to 0
$$

induces a [[fiber sequence]]

$$
\cdots\to\mathbf{B}^n \mathbb{Z}\to \mathbf{B}^n\mathbb{Z}\to \mathbf{B}^n\mathbb{Z}/2\mathbb{Z}\to \mathbf{B}^{n+1}\mathbb{Z}\to \cdots
$$

and so, for any object $X$, a [[fiber sequence]]

$$
\cdots\to\mathbf{H}(X,\mathbf{B}^n \mathbb{Z})\to \mathbf{H}(X,\mathbf{B}^n\mathbb{Z})\to \mathbf{H}(X,\mathbf{B}^n\mathbb{Z}/2\mathbb{Z})\stackrel{\beta_2}{\to} \mathbf{H}(X,\mathbf{B}^{n+1}\mathbb{Z})\to \cdots
$$

of [[cocycle]] [[∞-groupoid]] (with respect to any ambient [[(∞,1)-topos]] $\mathbf{H}$, such as [[Top]] $\simeq$ [[∞Grpd]]), where $\beta_2$ is the [[Bockstein homomorphism|Bockstein morphism]] asociated with the multiplication by 2.

The image via $\beta_2$ of the $n$-th [[Stiefel-Whitney class|Stiefel-Whitney map]] $w_n\in \mathbf{H}(X,\mathbf{B}^n\mathbb{Z}/2\mathbb{Z})$ in $\mathbf{H}(X,\mathbf{B}^{n+1}\mathbb{Z})$ is called the $(n+1)$st **integral Stiefel-Whithey map** and is denoted by $W_{n+1}$. 

One usually uses the same symbol to denote the image of this characteristic map in [[cohomology]] (on [[0-truncated|connected components]] ) of $W_{n+1}$ in $H^{n+1}(X;\mathbb{Z})=\pi_0\mathbf{H}(X,\mathbf{B}^{n+1}\mathbb{Z})$, and calls this the $(n+1)$-th **integral Stiefel-Whitney class**.

## Examples

### Third integral SW class

The third integral Stiefel-Whitney class $W_3(T X)$ of the [[tangent bundle]] of an [[oriented]] $n$-dimensional [[manifold]] $X$ vanishes if and only if the second [[Stiefel-Whitney class]] $w_2(T X)$ is in the image of the reduction mod 2 morphism 

$$
  H^2(X;\mathbb{Z})\to H^2(X;\mathbb{Z}/2\mathbb{Z})
  \,.
$$

Since $H^2(X;\mathbb{Z})$ classifies [[isomorphism classes]] of $U(1)$-[[principal bundles]] over $X$ and $W_3(T X)$ is the obstruction to the existence of a [[spin^c structure]] on $X$, we see that $X$ has a $spin^c$ structure if and only if there exists a principal $U(1)$-bundle on $X$ "killing" the second Stiefel-Whitney class of $X$. 

In particular, when $w_2(T X)$ is killed by the trivial $U(1)$-bundle, i.e., when $w_2(T X)=0$, then $X$ has a [[spin structure]].

The vanishing of the third integral SW class, hence [[spin^c-structure]] is the [[orientation in generalized cohomology|orientation condition]] in [[complex K-theory]] $KU$ over oriented manifolds. In the context of [[string theory]] this is also known as the [[Freed-Witten anomaly]] cancellation condition.


### Seventh integral SW class

Analogously, the vanishing of the seventh integral SW class is essentially the condition for [[orientation in generalized cohomology|orientation]] in second [[integral Morava K-theory]].

In the context of [[string theory]] this is also known as the [[Diaconescu-Moore-Witten anomaly]] cancellation condition.

## Related concepts

* [[integral Steenrod square]]

* [[integral Wu structure]]

[[!include orientations in higher quantization - table]]

\linebreak

## References

* {#RudolhSchmidt} Gerd Rudolph, Matthias Schmidt, around Def. 4.2.20 of _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


[[!redirects integral Stiefel-Whitney classes]]