**Base change** is another term for [[pullback]] of a morphism:

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

#Remarks#

* The [[duality|dual]] concept is [[cobase change]].