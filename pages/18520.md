
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An _even number_ is an [[integer]] $n \in \mathbb{Z}$ that is a multiple of 2, hence such that $n = 2 k$ for $k \in \mathbb{Z}$.

An _odd number_ is an integer that is not an even number.

## Properties

+-- {: .num_example #EvenAndOddIntegersAdjointModality}
###### Example
**([[adjoint modality]] of even and odd integers)**

Regard the [[integers]] as a [[preordered set]] $(\mathbb{Z}, \leq)$ in the canonical way, and thus as a [[thin category]].

Consider the [[full subcategory]] inclusions

$$
  \array{
    (\mathbb{Z}, \leq ) 
    & \overset{even}{\hookrightarrow}& 
    (\mathbb{Z},\leq)
    \\
    n &\mapsto & 2 n
  }
  \phantom{AAAAA}
  \array{
    (\mathbb{Z}, \leq ) 
    & \overset{odd}{\hookrightarrow}& 
    (\mathbb{Z},\leq)
    \\
    n &\mapsto & 2 n + 1
  }
$$

of the [[even number|even]] and the [[even number|odd]] [[integers]], as well as the functor

$$
  \array{
    (\mathbb{Z}, \leq ) 
    & \overset{\lfloor-/2\rfloor}{\longrightarrow}& 
    (\mathbb{Z},\leq)
    \\
    n &\mapsto& \lfloor n/2 \rfloor
  }
$$

which sends any $n$ to the [[floor]] $\lfloor n/2 \rfloor$ of $n/2$, hence to the largest integer which is smaller or equal to the [[rational number]] $n/2$.

These functors form an [[adjoint triple]]

$$
  even \;\dashv\; \lfloor -/2 \rfloor \;\dashv\; odd
$$

and hence induce an [[adjoint modality]]

$$
  Even \;\dashv\; Odd
$$

on $(\mathbb{Z}, \leq)$ with 

1. $Even \coloneqq 2 \lfloor -/2 \rfloor$ sending any integer to its "even floor value"

1. $Odd \coloneqq 2 \lfloor -/2 \rfloor + 1$ sending any integer to its "odd ceiling value".

=--

+-- {: .proof}
###### Proof

Observe that for all $n \in \mathbb{Z}$ we have

$$
  2 \lfloor n/2 \rfloor
    \overset{ \epsilon_n }{\leq} 
  n
    \overset{ \eta_n }{\leq}
  2 \lfloor n/2 \rfloor  + 1 
  \,,
$$

where the first inequality is an equality precisely if $n$ is even, while the second is an equality precisely if $n$ is odd. Hence this provides candidate [[unit of an adjunction|unit]] $\eta$ and [[counit of an adjunction|counit]].

Hence by [this characterization](adjoint+functor#UniversalArrow) of [[adjoint functors]] 

1. the adjunction $\lfloor -/2 \rfloor \dashv odd$ is equivalent to the condition that

   for every $n \leq 2 k + 1$ we have $2 \lfloor n/2 \rfloor + 1  \leq 2 k + 1$;

1. the adjunction $even \dashv \lfloor -/2 \rfloor $ is equivalent to the condition that

   for every $2k \leq n$ we have $2k \leq 2 \lfloor n/2 \rfloor $,

which is readily seen to be the case


=--


[[!redirects even numbers]]

[[!redirects odd number]]
[[!redirects odd numbers]]

[[!redirects odd natural number]]
[[!redirects odd natural numbers]]

[[!redirects odd integer]]
[[!redirects odd integers]]

