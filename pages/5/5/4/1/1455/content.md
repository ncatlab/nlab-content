For a [[category]] $C$ and [[endofunctor]] $F$, an __algebra__ of $F$ is an object $X$ in $C$ and a map $\alpha: F(X) \to X$. ($X$ is called the __carrier__ of the algebra)

A morphism between two algebras $(X, \alpha)$ and $(Y, \beta)$ of $F$ corresponds to a morphism $m : X \to Y$ in $C$ such that the following square commutes:
$$ 
  \array{ 
    F(X) 
    & 
    \stackrel{F(m)}{\rightarrow} 
    & 
    F(Y) 
    \\ 
    \alpha\downarrow 
    && 
    \downarrow \beta 
    \\ X 
    & 
    \stackrel{m}{\rightarrow} & Y 
  }
  \,. 
$$
Composition of such morphisms of algebras is given by composition of the underlying morphisms in $C$.

The dual concept is a [[coalgebra for an endofunctor]]. Both algebras and coalgebras for endofunctors on $C$ are special cases of [[algebra for a C-C bimodule|algebras for C-C bimodules]].

If the endofunctor $F$ has the structure of a [[monad]], then an algebra (aka module) over that monad is an algebra for $F$ that satisfies an additional associativity property. Morphisms between algebras for monads are simply morphisms between algebras for the underlying functors. For more details see [[algebra over a monad]].

An [[initial object]] in the category of algebras for $F$ is an [[initial algebra]] of $F$. 


[[!redirects algebra of an endofunctor]]
[[!redirects algebra of a functor]]
[[!redirects algebra for a functor]]
[[!redirects algebra over an endofunctor]]