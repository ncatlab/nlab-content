

<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
***
[[!include topos theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the strict sense, **base change** is another term for [[pullback]] of a morphism. In the wider sense it means something more general.


## Definition

In the strict sense, **base change** is another term for [[pullback]] of a morphisms, in that

if

$$
  \array{
    U \times_X Y &\to & Y
    \\
    \downarrow && \downarrow
    \\
    U &\to& X 
  }
$$

is a [[pullback]] square in some [[category]] then the [[morphism]] $U \times_X Y \to U$ is the **base change** or **base extension** of $Y \to X$ along $U \to X$.

Here we think of the morphism $Y \to X$ as a [[bundle]] over $X$, so base change gives us a bundle over $U$.  So in general, a morphism $f: U \to X$ defines a **base change functor** $f^*$ from the [[over category]] $C/X$ to the over category $C/U$ (where $C$ is the original category).

The concept of base change generalises from this case to other [[fibered category|fibred categories]].

The [[duality|dual]] concept is [[cobase change]].

## Base change geometric morphisms

If $\mathbf{H}$ is a [[topos]] (or [[(∞,1)-topos]], etc.) $f : X \to Y$ a [[morphism]] in $\mathbf{H}$, then base change provides a functor over [[overcategories]] (which are again [[topos]]es)

$$
  f^* : \mathbf{H}/Y \to \mathbf{H}/X
$$

and this has a [[right adjoint]] $f_* : \mathbf{H}/X \to \mathbf{H}/Y$ and a [[left adjoint]] $f_! : \mathbf{H}/X \to \mathbf{H}/Y$. These form an [[essential geometric morphism]]

$$
  f : \mathbf{H}/X \to \mathbf{H}/Y
$$

of toposes, the **base change geometric morphism**. If $B = *$ is the [[terminal object]], then this is also called an [[etale geometric morphism]].

([[Elephant]], Example A.4.1.2).

## Discussion

A previous version of this entry led to the following discussion 

+--{+ .query}
((Zoran)) This is too narrow understanding of "base change". Base is an object over which we work, for example base scheme, base field and so on. One has a category living over it, which is
typically a fiber in a (co)fibered category, or some analogue, possibly higher categorical. Base change means replacing original fiber and its projection by the ones from the inverse image in the sense of whatever fibered category-like thing we have. If the fibered category is the codomain fibration of the arrow category then we get what is described in this post. But many other fibered categories are interesting and one still talks about base change (truly in those situations one may also talk about "pullback", but it is less customary; "inverse image functor" in my understanding then refers then to the functor from fiber to the fiber over the new base, not to the projection of the new fiber, nor the new fiber itself).
=--



[[!redirects change of base]]

[[!redirects base change geometric morphism]]
