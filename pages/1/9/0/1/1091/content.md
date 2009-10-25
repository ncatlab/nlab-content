**Base change** is another term for [[pullback]] of a morphism:

+--{+ .query}
((Zoran)) This is too narrow understanding of "base change". Base is an object over which we work, for example base scheme, base field and so on. One has a category living over it, which is
typically a fiber in a (co)fibered category, or some analogue, possibly higher categorical. Base change means replacing original fiber and its projection by the ones from the inverse image in the sense of whatever fibered category-like thing we have. If the fibered category is the codomain fibration of the arrow category then we get what is described in this post. But many other fibered categories are interesting and one still talks about base change (truly in those situations one may also talk about "pullback", but it is less customary; "inverse image functor" in my understanding then refers then to the functor from fiber to the fiber over the new base, not to the projection of the new fiber, nor the new fiber itself).
=--

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

#Remarks#

* The [[duality|dual]] concept is [[cobase change]].


[[!redirects change of base]]