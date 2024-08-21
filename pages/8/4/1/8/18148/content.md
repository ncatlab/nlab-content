
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}

## Definition

A [[magma]] $(S,\cdot)$ is called _unital_ if it has an [[identity element]] $1 \in S$, hence an element such that for all $x \in S$ it satisfies the [[equation]]

$$
  1 \cdot x = x = x \cdot 1
$$

holds. The identity element is [[idempotent]]. 

Some authors take a magma to be unital by default (cf. [[Borceux-Bourn]] Def. 1.2.1). 

There is also a possibly empty version, where the identity element is replaced with a [[constant function]] $1:S \to S$ such that for all $x,y \in S$, $1(x)\cdot y = y$ and $x\cdot 1(y) = x$. 

## Properties

The [[Eckmann-Hilton argument]] holds for unital magmas: two compatible ones on a set must be equal, associative and commutative.

## Examples

Examples include [[unital rings]] etc.

## Generalizations

This concept could be generalized from the [[category of sets]] to any [[monoidal category]]:

A **unital magma object** or **unital algebra object** in a [[monoidal category]] $(C, I, \otimes)$ is an object $A \in C$ with morphisms $\iota:I \to A$ and $\pi:A \otimes A \to A$ such that the following [[commuting diagram|diagrams commute]]:

   $$
     \array{
       I \otimes A 
         &\overset{\iota \otimes \mathrm{id}_A}{\longrightarrow}&
       A \otimes A
       \\
       \downarrow^{\lambda_A} & & \downarrow^{\pi} 
       \\
       A &\overset{\mathrm{id}_A}{\longrightarrow}& A
     }
     \,,
   $$

   $$
     \array{
       A \otimes I 
         &\overset{\mathrm{id}_A \otimes \iota}{\longrightarrow}&
       A \otimes A
       \\
       \downarrow^{\rho_A} & & \downarrow^{\pi} 
       \\
       A &\overset{\mathrm{id}_A}{\longrightarrow}& A
     }
     \,,
   $$

where $\lambda_A:I \otimes A \to A$ and $\rho_A:A \otimes I \to A$ are the left and right [[unitors]] of the [[monoidal category]]. 

In the [[category of modules]], unital magma objects are called **[[nonassociative algebra|nonassociative]] [[unital algebras]]**, and in the [[category of abelian groups]], unital magma objects are called **[[nonassociative rings]]**. 

## Related concepts

* [[associative magma]]

* [[commutative magma]]

* [[nonassociative group]]

* [[paraunital magma]]

[[!include oidification - table]]

[[!redirects unital magma]]
[[!redirects unital magmas]]
[[!redirects unitary magma]]
[[!redirects unitary magmas]]

[[!redirects unital magma object]]
[[!redirects unital magma objects]]
[[!redirects unital algebra object]]
[[!redirects unital algebra objects]]