
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

Let $\big(\mathcal{C}, \otimes, \mathbb{1}\big)$ be a [[closed monoidal category]]. For $S, D \in C$ two [[objects]], with [[internal hom]] $[S, \text{-}]$ [[right adjoint functor|right adjoint]] to the [[tensor product]] $S \otimes (\text{-})$, the *evaluation map*

$$
  ev \;\colon\; S \otimes [S, D]  \to D
$$

is the [[counit of an adjunction|counit]] of this [[adjoint functor|adjunction]], hence the [[adjunct]] of the [[identity]] morphism

$$
  Id \;\colon\; [S,D] \to [S,D]
  \,.
$$

Concretely for $\mathcal{C}$ = [[Sets]] or generally on [[generalized elements]], the evaluation map is given by evaluating a [[function]] at a value, whence the name:

$$
  \array{
    S \times [S,D] &\overset{ev}{\longrightarrow}& D
    \\
    \big(
      s
      ,\,
      f
    \big)
    &\mapsto&
    f(s)
    \mathrlap{\,.}
  }
$$

If $\mathcal{C}$ is moreover [[compact closed category|compact]] then for $D = \mathbb{1}$ the [[tensor unit]] we have that $[S, \mathbb{1}] \,=\, S^\ast$ is the [[dual object]] to $S$, whence the evaluation map becomes the pairing of objects with their duals
$$
  S \otimes S^\ast \overset{ev}{\longrightarrow} \mathbb{1}
  \,.
$$ 
Therefore, sometimes the pairing map on [[dual objects]] may be called "evaluation" even when the ambient category is not [[compact closed category|compact closed]].


## Properties

### Syntax and semantics
 {#SyntaxAndSemantics}

In a [[cartesian closed category]] the evaluation map 

$$
  [X,Y]\times X \stackrel{eval}{\to} Y
$$

is the [[categorical semantics]] of what in the [[type theory]] [[internal language]] is the [[dependent type]] whose [[syntax]] is

$$
  f \colon X \to Y
  ,\; 
  x \colon X 
  \; \vdash \; f(x) \colon Y
$$

expressing  _[[function application]]_. On [[propositions]] ([[(-1)-truncation|(-1)-truncated]] [[types]]) this is the [[modus ponens]] [[deduction]] [[inference rule|rule]].


## See also

* [[coevaluation map]]

* [[state monad]], [[costate comonad]]

* [[concrete category]] (for the external version)

[[!redirects evaluation]]
[[!redirects evaluation maps]]
[[!redirects evaluation morphism]]
[[!redirects evaluation morphisms]]
