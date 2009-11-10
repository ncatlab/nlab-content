For a [[category]] $C$ and [[endofunctor]] $F$, an __algebra__ of $F$ is an object $X$ in $C$ and a map $\alpha: F(X) \to X$.

The dual concept is a [[coalgebra for an endofunctor]].

See also [[initial algebra]].

If $(F,\eta,\mu)$ is a [[monad]], then an __algebra__, or __[[module]]__, for $F$ is an algebra in the above sense such that the diagrams
$$ \array {
  F(F(x))              & \stackrel{\mu_x}\rightarrow  & F(x) \\
  F(\alpha) \downarrow &                              & \downarrow \alpha \\
  F(x)                 & \stackrel{\alpha}\rightarrow & x
} $$
and
$$ \array {
  x               & \stackrel{\eta_x}\rightarrow  & F(x) \\
  id_x \downarrow &                               & \downarrow \alpha \\
  x               & \stackrel{id_x}\rightarrow    & x
} $$
commute for every object $x$ of $C$.

The [[Eilenberg–Moore category]] of $F$ is the category of these algebras.


[[!redirects algebra of an endofunctor]]
[[!redirects algebra of a functor]]
[[!redirects algebra for a functor]]

[[!redirects algebra of a monad]]
[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects module of a monad]]
[[!redirects module for a monad]]
[[!redirects module over a monad]]