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

The **partial evaluation relation** on $T A$ is defined by: _$p\to q$ if and only if there exists a partial evaluation from $p$ to $q$_.
In other words, it is the (0,1)-[[truncation]] of the bar construction. 

Similar definitions can be given [[internally]] to any category: instead of elements $p,q\in T A$, $r\in T T A$ one can take [[generalized elements]] (i.e. [[arrows]]) $p,q:X\to T A$, $r:X\to T T A$.


## Examples

* For many [[probability monads]], partial evaluations correspond to [[conditional expectation]] of [[algebra over a monad|algebra]]-valued [[random variables]];
* For the [[free cocompletion]] monad, partial evaluations correspond to pointwise left [[Kan extensions]].


## Properties

* Every expression $p\in T A$ admits a partial evaluation to itself (given by $T\eta(p)\in T T A$). This makes the partial evaluation relation [[reflexive relation|reflexive]]. 

* Every expression $p\in T A$ admits a partial evaluation to its *total* evaluation $\eta(a(p))\in T A$, given by $\eta(p)\in T T A$.

* The partial evaluation relation is the smallest [[internal relation]] (in the category of $T$-[[algebra over a monad|algebras]]) which relates a [[formal expression]] to its result.

* If the multiplication $\mu$ of the monad is a *weakly cartesian* natural transformation (i.e. its [[naturality]] square is a [[weak pullback]]), the partial evaluation relation is [[transitive]], and hence a [[preorder]]. 


## See also 

* [[bar construction]], [[monad]], [[algebra over a monad]], [[operad]], [[algebra over an operad]]
* [[simplicial set]], [[Segal space]], [[Segal conditions]], [[Kan complex]]

 
## References

* [[Tobias Fritz]] and [[Paolo Perrone]], _Monads, partial evaluations, and rewriting_, MFPS 2020. ([arXiv](https://arxiv.org/abs/1810.06037))

* Carmen Constantin, [[Tobias Fritz]], [[Paolo Perrone]] and Brandon Shapiro, _Partial evaluations and the compositional structure of the bar construction_, Theory and Applications of Categories 39, 2023. ([arXiv:2009.07302](https://arxiv.org/abs/2009.07302))

* Carmen Constantin, [[Tobias Fritz]], [[Paolo Perrone]] and Brandon Shapiro, _Weak cartesian properties of simplicial sets_, Journal of Homotopy and Related Structures, 2023. ([arXiv:2105.04775](https://arxiv.org/abs/2105.04775))

* [[Paolo Perrone]], [[Walter Tholen]], *Kan extensions are partial colimits*, Applied Categorical Structures, 2022. ([arXiv:2101.04531](https://arxiv.org/abs/2101.04531))


[[!redirects partial evaluations]]
[[!redirects partially evaluate]]
[[!redirects partially evaluated]]
[[!redirects partially evaluating]]
[[!redirects partial evaluation relation]]