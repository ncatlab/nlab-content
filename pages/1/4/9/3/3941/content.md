#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[cospan]]

$$
  \array{
    F_B &&&& F_C
    \\
    & \searrow && \swarrow
    \\
    && F_A
  }
$$

in a category $\mathcal{C}$ is called _quadrable_ , if there exists a  [[cone]]

$$
  \array{
    && N
    \\
    & \swarrow && \searrow 
    \\
    F_B &&&& F_C
    \\
    & \searrow && \swarrow
    \\
    && F_A
  }
  \,.
$$


## Definition

Let $Sp = \left\{\array{ B &&&& C \\ & \nwarrow && \nearrow \\ && A}\right\}$ denote the [[span]] [[diagram|diagram category]], that is, the category with three objects $A,B,C$ and two non-identity morphisms $A\to B$ and $A\to C$.

Let $\mathcal{C}$ be any category and let $\Delta$ denote the [[diagonal]] $\mathcal{C}\to [Sp^{op},\mathcal{C}]$ into the [[functor category]] sending an object $X\mapsto c_X$, where $c_X$ is the constant functor sending all objects and all morphisms of $Sp^{op}$ to $X$ and $id_X$ respectively.

For $F\in [Sp^{op}, \mathcal{C}]$ let $*_F$ denote the unique functor $*\to [Sp^{op},\mathcal{C}]$ from the [[terminal category]] such that the unique object of $*$
maps to $F$.

We say that a [[cospan]] $F$ in a category $\mathcal{C}$, that is, an object of the [[functor category]] $[Sp^{op},\mathcal{C}]$ is **quadrable** if there exists a [[cone]] $N$ for $F$, that is, an object $N$ in the [[comma category]] $(\Delta \downarrow *_F)$.

Dually, we say that a [[span]] $G$ in a category $C$, that is, an object of the functor category $[Sp,\mathcal{C}]$ is **coquadrable** if there exists a [[cocone]] $N$ for $G$, that is, an object $N$ in the comma category $(*_G \downarrow \Delta)$.

We say that a category $\mathcal{C}$ is quadrable (resp. coquadrable) if all cospans (resp. spans) in $C$ are quadrable (resp. coquadrable).  


## Note on terminology

The term _quadrable_ is supposed to be a translation of the French  _carrable_ , whose use is more wide-spread. (However, note that this is a different meaning than [[carrable morphism]]).


[[!redirects quadrability]]
[[!redirects carrable cospan]]
[[!redirects coquadrable span]]
[[!redirects quadrable span]]

[[!redirects quadrable cospans]]
[[!redirects coquadrable spans]]
[[!redirects quadrable spans]]

