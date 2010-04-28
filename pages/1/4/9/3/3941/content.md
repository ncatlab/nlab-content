##Definition##

Let $Sp$ denote [[span]] category, that is, the category with three objects $A,B,C$ and two non-identity morphisms $A\to B$ and $A\to C$.

Let $\Delta$ denote the [[diagonal]] $C\to [Sp^{op},C]$ sending an object $X\mapsto c_X$, where $c_X$ is the constant functor sending all objects and all morphisms of $Sp^{op}$ to $X$ and $id_X$ respectively.

For $F\in [Sp^{op}, C]$ let $*_F$ denote the unique functor $*\to [Sp,C]$ from the [[terminal category]] such that the unique object of $*$
maps to $F$.

We say that a cospan $F$ in a category $C$, that is, an object of the functor category $[Sp^{op},C]$ is **quadrable** if there exists a [[cone]] $N$ for $G$, that is, an object $N$ in the [[comma category]] $(\Delta \downarrow *_F)$.

Dually, we say that a span $G$ in a category $C$, that is, an object of the functor category $[Sp,C]$ is **coquadrable** if there exists a [[cocone]] $N$ for $G$, that is, an object $N$ in the comma category $(*_G \downarrow \Delta)$.

We say that a category $C$ is quadrable (resp. coquadrable) if all cospans (resp. spans) in $C$ are quadrable (resp. coquadrable).  