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

_Dialgebras_ subsume the notion of [[algebras for an endofunctor]] and [[coalgebras for an endofunctor]]. They were originally introduced by Lambek as "subequalizers".


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

## Relationship to program semantics (process calculi)

Dialgebras can be used to provide semantics to interactive programs; [[coalgebras]] have also been frequently used for the purpose. In contrast, dialgebras provide a natural way to express interactions (using the functor $F$). Semantics in dialgebras is not obtained via final objects (which are frequently absent in categories of dialgebras), but rather via quotients. 



## Related concepts

* [[algebra for an endofunctor]], [[coalgebra over an endofunctor]]

* [[algebra for a profunctor]]


## References

* {#subeq} [[Joachim Lambek]], _Subequalizers_, 1970

* {#lam} [[Tatsuya Hagino]], _A Typed Lambda Calculus with Categorical Type Constructors_, 2005, [link](https://link.springer.com/chapter/10.1007/3-540-18508-9_24)

* {#cat} [[Thorsten Altenkirch]], Peter Morris, [[Fredrik Nordvall Forsberg]], [[Anton Setzer]],  _A Categorical Semantics for Inductive-Inductive Definitions_, CALCO, 2011 [link](https://link.springer.com/chapter/10.1007%2F978-3-642-22944-2_6)

* {#ccs} Vincenzo Ciancia, _Interaction and Observation: Categorical Semantics of Reactive Systems Trough Dialgebras_, CALCO, 2013 [link](https://link.springer.com/chapter/10.1007%2F978-3-642-40206-7_10)

* {#abthesis} Alwin Blok, _Interaction, observation and denotation.
A study of dialgebras for program semantics_ Master Thesis, Institute for Logic, Language and Computation, University of Amsterdam. [link](https://eprints.illc.uva.nl/872/1/MoL-2012-06.text.pdf)

[[!redirects dialgebras]]
[[!redirects subequalizer]]
[[!redirects subequalizers]]
[[!redirects subequaliser]]
[[!redirects subequalisers]]