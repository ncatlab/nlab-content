
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Just as the notion of a [[monad]] in a [[bicategory]] $K$ generalizes that of a [[monoid]] in a [[monoidal category]], [[module|modules]] over monoids generalize easily to modules over monads.

A special case of this (see below) is often called an _algebra_ for a monad.

## Definition

Let $K$ be a bicategory and $t \colon a \to a$ a monad in $K$ with structure 2-cells $\mu \colon t t \Rightarrow t$ and $\eta \colon 1_a \Rightarrow t$.  Then a **left $t$-module** is given by a 1-cell $x : b \to a$ and a 2-cell $\lambda : t x \Rightarrow x$, where
$$
\array{
  t t x & \overset{\mu x}{\to} & t x \\
  t\lambda\downarrow & & \downarrow \lambda \\
  t x & \underset{\lambda}{\to} & x
}
\qquad \qquad
\array{
  x \cong 1 x & \overset{\eta x}{\to} & t x \\
  & 1\searrow & \downarrow \lambda \\
  & & x
}
$$
commute.  Similarly, a **right $t$-module** is given by a 1-cell $y : a \to c$ and a 2-cell $\rho : y t \Rightarrow y$, with commuting diagrams as above with $y$ on the left instead of $x$ on the right.

Given monads $s$ on $b$ and $t$ on $a$, an **$s,t$-bimodule** is given by a 1-cell $x: b \to a$, together with the structures of a right $s$-module $\rho : x s \Rightarrow x$ and a left $t$-module $\lambda : t x \Rightarrow x$ that are compatible in the sense that the diagram
$$
\array{
  t x s & \overset{t\rho}{\to} & t x \\
  \lambda s \downarrow & & \downarrow \lambda \\
  x s & \underset{\rho}{\to} & x
}
$$
commutes.

A **morphism** of left $t$-modules $(x,\lambda) \to (x',\lambda')$ is given by a 2-cell $\alpha : x \Rightarrow x'$ such that $\lambda' \circ t\alpha = \alpha \circ \lambda$.  Similarly, a morphism of right $t$-modules $(y,\rho) \to (y',\rho')$ is $\beta : y \Rightarrow y'$ such that $\rho' \circ \alpha s = \alpha \circ \rho$.  A morphism of bimodules $(x,\lambda,\rho) \to (x',\lambda',\rho')$ is given by $\alpha : x \Rightarrow x'$ that is a morphism of both left and right modules.

### Algebras for monads in Cat

If $K = Cat$ and $(T,\eta,\mu)$ is a monad on a category $C$, then a left $T$-module $A : 1 \to C$, where $1$ is the [[terminal category]], is usually called a **$T$-algebra**: it is given by an object $A \in C$ together with a morphism $\alpha : T A \to A$, such that
$$ \array {
  T(T(A))              & \stackrel{\mu_A}\rightarrow  & T(A) \\
  T(\alpha) \downarrow &                              & \downarrow \alpha \\
  T(A)                 & \stackrel{\alpha}\rightarrow & A
}
$$
and
$$ \array {
  A               & \stackrel{\eta_A}\rightarrow  & T(A) \\
  id_A \downarrow &                               & \downarrow \alpha \\
  A               & \stackrel{id_A}\rightarrow    & A
}
$$
commute.

$T$-algebras can also be defined as left [[modules]] over $T$ _qua_ monoid in $End(C)$.  There the object $A$ is represented by the constant endofunctor at $A$.

The [[Eilenberg-Moore category]] of $T$ is the category of these algebras.  It has a universal property that allows the notion of
_Eilenberg--Moore object_ to be defined in any bicategory.


## Tensor product

...



[[!redirects module of a monad]]
[[!redirects module for a monad]]

[[!redirects algebra of a monad]]
[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
