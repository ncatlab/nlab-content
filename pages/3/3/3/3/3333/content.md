

#Contents#
* automatic table of contents goes here
{:toc}


## Definition

In an [[(∞,1)-category]] $C$, for $X \in C$ an [[object]], its **free loop space object** $\mathcal{L}X$ is the $(\infty,1)$-[[pullback]]

$$
  \array{
    \mathcal{L} X &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    X &\stackrel{(Id,Id)}{\to}& X \times X
  }
  \,.
$$

This is the $(∞,1)$-categorical [[span trace]] of the identity-[[span]]

$$
  \mathcal{L}X =
  Tr
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
       \\
       X &&&& X
    }
  \right)
  \,.
$$

## Examples 

* in [[Top]]: ordinary concept of free loop space

* the fiber over a [[point]] in $X$ is the corresponding (based) [[loop space object]] of $X$.

* [[quasicoherent ∞-stack]]s on $\mathcal{L}X$ form the [[Hochschild cohomology|Hochschild homology]] object of $X$ (if the axioms of [[geometric function theory]] are met) as described there.