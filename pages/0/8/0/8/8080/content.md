
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Conventional meaning

Let $V$ be a [[closed category]] (for example a [[closed monoidal category]]), with the [[internal hom]] denoted as $A \multimap B$ and the [[unit object]] as $I$,


+-- {: .num_defn}
###### Definition

The **dual** $\mathbb{D}A$ of an object $A \in V$ is the [[internal hom]] out of $A$ into the [[unit object]] 

$$
  \mathbb{D}A \coloneqq A \multimap I
$$ 

=--

This applies for example to categories of [[modules]] over a [[commutative ring]], to the category of [[Banach spaces]], etc., with their usual closed monoidal structures. 


+-- {: .num_remark}
###### Warning
A dual in the sense above might not be a [[dual object]] in other established senses of the word. For example, 

* The dual $X^\ast$ of a [[Banach space]] $X$ is generally not the dual in any sense that guarantees $X^\ast \otimes -$ is [[adjoint functor|left or right adjoint]] to $X \otimes -$, unless $X$ is finite-dimensional. (Here the monoidal product is the [[projective tensor product]], which makes the closed category of Banach spaces into a closed monoidal category.) In particular, there is generally no appropriate unit of the form $I \to X^\ast \otimes X$ (where $I$ is the [[ground field]]).

=--

For a [[compact closed category]], a dual object (in one or another monoidal category sense; see [[category with duals]]) _is_ the same as a dual in the closed category sense. But in general, monoidal duals are a stronger notion than duals in the closed category sense. 

Of course, where the monoidal product is not [[braided monoidal category|braided or symmetric monoidal]], due care must be exercised in distinguishing between between different types of monoidal dual (left or right dual). 

* If $V$ is a [[star-autonomous category]], "dual object" has a different meaning: it usually is taken to mean $A^\ast \cong A \multimap \bot$ where $\bot$ is the [[dualizing object]]. In a $\ast$-autonomous category where $\bot$ and $I = \top$ are not isomorphic (e.g., a [[Boolean algebra]]), this gives something genuinely different from "dual" in the sense of this page. But again, these two meanings, $A \multimap \top$ and $A \multimap \bot$, coincide in the case where the $\ast$-autonomous category is compact closed. 

## Applications

Closed duals play a central role in [[six operations]] yoga, notably in 
[[Verdier duality]] and in the [[Wirthmüller isomorphism]].

## Related concepts

* [[dualizing object in a closed category]]

* [[dual object]]

* [[duality]]


[[!redirects dual object in a closed monoidal category]]
[[!redirects dual objects in a closed monoidal category]]
[[!redirects dual objects in closed monoidal categories]]
[[!redirects dual in a closed monoidal category]]
[[!redirects duals in a closed monoidal category]]
[[!redirects duals in closed monoidal categories]]
[[!redirects dual object in a closed category]]
[[!redirects dual objects in a closed category]]
[[!redirects dual objects in closed categories]]
[[!redirects dual in a closed category]]
[[!redirects duals in a closed category]]
[[!redirects duals in closed categories]]

[[!redirects algebraic dual]]
[[!redirects algebraic duals]]

