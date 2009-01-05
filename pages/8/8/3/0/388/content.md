# Idea #

In a [[category]] $C$ which is equipped with the structure of a [[model category]] there is a notion of _homotopy_ between morphisms, which is closely related to the higher morphisms in [[higher category theory]].


#Definition#

Let $X$ be an object in the [[model category]] $C$. 

* A **path object** $Path(X)$ for $X$ is a factorization of the diagonal $X \to X \times X$ as a weak equivalence followed by a fibration
$$
  X \to Path(X) \to X \times X
  \,.
$$

* A **cylinder object** $Cyl(X)$ is a factorization of the codiagonal $X \sqcup X \to X$ as a cofibration followed by a weak equivalence

$$
  X \sqcup X \to Cyl(X) \to X
  \,.
$$

(Think of $Path(X)$ as an [[closed category|internal hom]] $[I,X]$ for $I$ a model of the interval, and of $Cyl(X)$ as a [[tensor product|product]] $X \times I$. )

Then:

* A **left homotopy** between two morphisms $f,g : X \to Y$ in $C$ is a morphism $\eta : Cyl(X) \to Y$ such that
$$
  \array{
    X &\rightarrow& Cyl(X) &\leftarrow& X
    \\
    & {}_f\searrow &\downarrow^\eta& \swarrow_g
    \\
    && 
    Y
  }
  \,.
$$

* A **right homotopy** between two morphisms $f,g : X \to Y$ in $C$ is a morphism $\eta : X \to Path(Y)$ such that
$$
  \array{
    && X
    \\
    & {}^f\swarrow & \downarrow^\eta & \searrow^{g} 
    \\
    Y &\leftarrow& Path(Y) &\rightarrow& Y
  }
  \,.
$$

