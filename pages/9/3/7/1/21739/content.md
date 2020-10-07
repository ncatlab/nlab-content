+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A partial evaluation is an instruction to evaluate a [[formal expression]] piecewise, without necessarily obtaining the final result.

For a simple example, the sum "$3+4+5$" can be evaluated to "$12$", but also _partially_ evaluated to "$7+5$".


## Definition

Let $(T,\mu,\eta)$ be a [[monad]] on [[Set]], and let $(A,a)$ be an [[algebra over a monad|algebra]] over $T$. Given two elements $p,q\in T A$, a **partial evaluation** from $p$ to $q$ is an element $r\in T T A$ such that $\mu(r)=p$, and $T a(r)=q$.

Equivalently, partial evaluations are the 1-simplices of the [[bar construction]] (considered as a [[simplicial set]]) of the algebra $(A,a)$.

(...)


## Examples

(...)

* For many [[probability monads]], partial evaluations correspond to [[conditional expectation]] of functions;
* For the [[free cocompletion]] monad, partial evaluations correspond to pointwise left [[Kan extensions]].


## See also 

* [[bar construction]], [[monad]], [[algebra over a monad]], [[operad]], [[algebra over an operad]]
* [[simplicial set]], [[Segal space]], [[Segal conditions]] [[Kan complex]]

 
## References

* [[Tobias Fritz]] and [[Paolo Perrone]], _Monads, partial evaluations, and rewriting_. ([arXiv](https://arxiv.org/abs/1810.06037))

* [[Carmen Constantin]], [[Tobias Fritz]], [[Paolo Perrone]] and [[Brandon Shapiro]], _Partial evaluations and the compositional structure of the bar construction_. ([arXiv](https://arxiv.org/abs/2009.07302))


[[!redirects partial evaluations]]
[[!redirects partially evaluate]]
[[!redirects partially evaluated]]
[[!redirects partially evaluating]]