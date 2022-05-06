[[!redirects dialgebras]]
[[!redirects dialgebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Dialgebras_ subsume the notion of [[algebras for an endofunctor]] and [[coalgebras for an endofunctor]].


## Definition

+-- {: .num_defn}
###### Definition

For [[categories]] $C, D$ and [[functors]] $F, G: C \to D$, a __dialgebra__ of $F$ and $G$ (or an $(F, G)$-dialgebra) is an [[object]] $X$ in $C$ (the __carrier__) and a [[morphism]] $\alpha\colon F(X) \to G(X)$.

A [[homomorphism]] between two $(F, G)$-dialgebras $(X, \alpha)$ and $(Y, \beta)$ is a morphism $m\colon X \to Y$ in $C$ such that the following [[commuting diagram|square commutes]] (that is, that $\alpha$ and $\beta$ form $X$- and $Y$-components of a [[natural transformation]] from $F$ to $G$):

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
    \\ G(X) 
    & 
    \stackrel{G(m)}{\rightarrow} & G(Y) 
  }
  \,. 
$$

[[composition|Composition]] of such morphisms of algebras is given by composition of the underlying morphisms in $C$.  This yields the [[category]] of $(F, G)$-dialgebras, $\text{Dialg}(F, G)$, which comes with a forgetful functor to $C$.
=--

+-- {: .num_remark}
###### Remark

When $C = D$, then an [[algebra for an endofunctor]] is simply an $(F, id_C)$-dialgebra and a [[coalgebra for an endofunctor]] is simply an $(id_C, F)$-dialgebra.

=--

## Relationship to inductive-inductive types

Initial dialgebras provide [[categorical semantics]] for [[inductive-inductive types]]. 


## Related concepts

* [[algebra for an endofunctor]], [[coalgebra over an endofunctor]]

* [[algebra for a profunctor]]


## References

* {#lam} Tatsuya Hagino, _A Typed Lambda Calculus with Categorical Type Constructors_, 2005, [link](https://link.springer.com/chapter/10.1007/3-540-18508-9_24)

* {#cat} Thorsten Altenkirch, Peter Morris, [[Fredrik Nordvall Forsberg]], [[Anton Setzer]],  _A Categorical Semantics for Inductive-Inductive Definitions_, CALCO, 2011 [link](https://link.springer.com/chapter/10.1007%2F978-3-642-22944-2_6)

[[!redirects dialgebras]]