

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



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

$$
  f^* A \mapsto X \times_Y A
  \,.
$$

This has a [[left adjoint]] $f_! : \mathbf{H}/X \to \mathbf{H}/Y$ given by postcomposition with $f$

$$
  f_! : (A \to X) \mapsto (A \to X \stackrel{f}{\to} Y)
  \,.
$$


It also has a [[right adjoint]] $f_* : \mathbf{H}/X \to \mathbf{H}/Y$ and 

The triple $(f_! \dashv f^* \dashv f_*) : \mathbf{H}/X \to \mathbf{H}/Y$ is an  [[essential geometric morphism]] of toposes, the **base change geometric morphism**. 

If $Y = *$ is the 
[[terminal object]], then this is also called an **[[etale geometric morphism]]**.

## References

* [[Peter Johnstone]],  [[Elephant]], Example A.4.1.2


[[!redirects change of base]]

[[!redirects base change geometric morphism]]
