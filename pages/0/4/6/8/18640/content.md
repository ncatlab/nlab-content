  +-- {: .rightHandSide}
  +-- {: .toc .clickDown tabindex="0"}
  ###Context###
  #### Constructivism, Realizability, Computability
  +-- {: .hide}
  [[!include constructivism - contents]]
  =--
  #### Category theory
  +-- {: .hide}
  [[!include category theory - contents]]
  =--
  =--
  =--


# Thunk-force category
* table of contents
{:toc}

## Idea

A **thunk-force category** is a category that models [[call-by-value]] programming languages with effects.
More commonly, terms in a call-by-value language are modelled as morphisms in the [[Kleisli category]] of a [[strong monad]].
A thunk-force category axiomatizes the Kleisli category _directly_ and is also called an **abstract Kleisli category**[^terminology].
The original category can be recovered from this category if it satisfies certain properties.

The name derives from programming terminology. A **thunk** means a value that represents an unevaluated computation, which can later be **forced** to be evaluated and perform its [[side effects]]. This is represented by the object $L A$ which could be read as a "thunk of $A$" or a "lazy $A$". The thunking arrow $\theta_A : A \to L A$ delays any effects performed by its input, and the force $\epsilon_A : L A \to A$ forces the evaluation of its thunked input. These don't normally appear as programming features in a call-by-value language, but if the language supports first-class functions, they are equivalent to the usual implementation of a thunk as a function of unit input.
On the model side this is because if a thunk-force category is [[monoidal closed]] in an appropriate sense, then $L A$ is equivalent to $I \harpoon A$ and $\theta, \epsilon$ can be defined using this structure.

## Definition

A thunk-force category [F&#252;hrmann 99](F99) consists of

* a category $K$
* a functor $L : K \to K$
* a [[unnatural transformation|possibly unnatural transformation]] $\theta : Id_K \to L$ pronounced **thunk**
* a [[natural transformation]] $\epsilon : L \to Id_K$ pronounced **force**

such that

* $\theta L$ is a natural transformation
* $(L\theta)\theta = (\theta L)\theta$
* $\epsilon\theta = \id$
* $(L\epsilon)(\theta L) = \id$

A morphism $f : A \to B$ in a thunk-force category is **thunkable** if $(Lf)\theta = \theta f$.
Another way to phrase the definition is that $(L,\epsilon,\theta L)$ is a comonad and $\theta$ is thunkable.

## Relation to Monads

Let $T$ be a [[monad]] on a category $C$. The [[Kleisli category]] of $T$ is a thunk-force category. Let $F \dashv G$ denote the adjunction between $C$ and the Kleisli category $C_T$. Define $L = FG$ and $\epsilon$ the counit of the comonad. To define $\theta$, take $F\eta : F \to FT = L$ and, using the fact that $F$ is an [[identity-on-objects functor]] (or at least bijective on objects), treat it as an [[unnatural transformation]] from $Id_{C_T}\to L$. Then it follows immediately by naturality that every morphism in the image of $F$ is thunkable.

More explicitly, using the "Kleisli arrow" definition of the Kleisli category, $L$ 
is just $T$, $\epsilon_A : T A \to T A$ is the identity, and $\theta_A = \eta_{T A} \eta_{A} : A \to T^2 A$.

The thunkable morphisms in a thunk-force category form a subcategory, and $L$ can be used to define a monad on that subcategory whose Kleisli category is equivalent to $K$.
These two constructions exhibit thunk-force categories as a [[reflective subcategory]] of the category of monads [F&#252;hrmann 99](F99).

## References

Thunk-force categories were introduced (under the name "abstract Kleisli categories" in 

* {#F99} Carsten F&#252;hrmann, "Direct Models of the Computational Lambda-calculus" Electronic Notes in Theoretical Computer Science 1999

[^terminology]: We prefer the term thunk-force category since it is ambiguous whether [[Kleisli category]] refers to the Kleisli category of a [[monad]] or a [[comonad]].