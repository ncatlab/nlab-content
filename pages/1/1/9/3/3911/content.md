
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

Quotienting by the complement of a [[tubular neighbourhood]] $\mu$ of $E$ in $E \times \mathbb{R}^n$ gives the [[Pontrjagin-Thom collaps map]]

$$
  B \times \mathbb{R}^n \to \Sigma^N B_* \stackrel{\tau}{\to} E^\nu
  \,,
$$

where

* $\nu$ is the [[normal bundle]] of $e$;

* $E^\nu = D(\nu)/S(\nu)$ is the [[Thom space]] of $\nu$.

Now let $H$ be some [[generalized (Eilenberg-Steenrod) cohomology]] theory, and assume that the Thom space $E^\nu$ has an $H$-[[orientation in generalized cohomology|orientation]], so that we have a  [[Thom isomorphism]]. Then combined with the [[suspension isomorphism]] the pullback along $\tau$ produces a morphism

$$
  \int_F : H^\bullet(E) \to H^{\bullet - dim F}(B)
$$

of cohomologies. This operation is independent of the choices involved. It is the **fiber integration** of $H$-cohomology along $p : E \to B$.

## Examples

...

## References

...