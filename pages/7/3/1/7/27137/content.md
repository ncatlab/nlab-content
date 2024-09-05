
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



# Contents
* automatic table of contents goes here
{:toc}

## Idea

A **separable monad**  is a [[monad]] that categorifies [[idempotent|idempotents]] by replacing the equation $p^2 = p$ with a retract of $p^2$ onto $p$.

This is to distinguish from [[idempotent monad|idempotent monads]], for which the equation $p^2 = p$ is replaced with an invertible 2-cell.

## Definition

Note that for a monad $(t:a\to a,\mu:t\circ t\to t,\eta:1_a\to t)$, associativity and unitality turn $(t,\mu)$ into a $t,t$-[[module over a monad|bimodule]].

\begin{definition}
A __separable monad__  is a [[monad]] $(t,\mu,\eta)$ in a [[bicategory]] such that the multiplication $\mu:t\circ t\to t$ admits a $t,t$-bilinear section.
\end{definition}

## Examples

* (Separable adjunctions) An [[adjunction]] in a 2-category is __separable__ if the counit $\varepsilon:l\circ r \to 1_a$ admits a section, i.e. a 2-cell $\sigma:1_a\to l\circ r$ such that $\varepsilon\circ\sigma = 1_{1_a}$.
The [[induced monad|monad]] $r\circ l$ is canonically separable.

* (Split separable monads) Separable monads that arise from a separable adjunction are called **split**.
The name derives from similarities between the behaviour of split separable monads and [[split idempotent|split idempotents]].
A 2-category is [[Karoubi complete 2-category|Karoubi complete]] if it is locally idempotent complete and all separable monads split.
This is one of the conditions for a linear 2-category to be [[fusion 2-category|fusion]].

## References

* [[Christopher L. Douglas]], [[David J. Reutter]], *Fusion 2-categories and a state-sum invariant for 4-manifolds* &lbrack;[arXiv:1812.11933](https://arxiv.org/abs/1812.11933)&rbrack;


* [[Theo Johnson-Freyd]], [[David J. Reutter]], *Minimal nondegenerate extensions* &lbrack;[arXiv:2105.15167](https://arxiv.org/abs/2105.15167)&rbrack;

* [[Xiao-Wu Chen]], *A note on separable functors and monads* &lbrack;[arXiv:1403.1332](https://arxiv.org/abs/1403.1332)&rbrack;