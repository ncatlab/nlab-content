+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _idempotent monoidal functor_ is a [[functor]] $F : C \to D$ between [[monoidal categories with diagonals]], that is, a [[monoidal functor]] which respects the diagonals on both sides.

In [[computer science]], where [[lax monoidal functors]] are used to represent certain kinds of [[side effect|effects]] (as [[applicative functors]]), idempotent lax monoidal functors represent effects that can be executed one or more times with the same result: for example, [[reader monad|reading from an immutable data source]] or raising an [[exception]].

## Definition

A (lax) [[monoidal functor]] $F : (C,\otimes) \to (D, \otimes)$, with monoidal structure $\nabla$, between [[monoidal categories with diagonals]] is **idempotent** if for all $A \in C$ the diagram

\begin{tikzcd}
	FA & {FA \otimes FA} \\
	& {F (A \otimes A)}
	\arrow["{\Delta_{FA}^{\mathcal{D}}}", from=1-1, to=1-2]
	\arrow["{\nabla_{A,A}}", from=1-2, to=2-2]
	\arrow["{F\Delta_A^{\mathcal{C}}}"', from=1-1, to=2-2]
\end{tikzcd}

commutes.

Dually, if $F$ is an [[oplax monoidal functor]], then it is idempotent if the diagram

\begin{tikzcd}
	FA & {FA \otimes FA} \\
	& {F (A \otimes A)}
	\arrow["{\Delta_{FA}^{\mathcal{D}}}", from=1-1, to=1-2]
	\arrow["{\nabla_{A,A}}"', from=2-2, to=1-2]
	\arrow["{F\Delta_A^{\mathcal{C}}}"', from=1-1, to=2-2]
\end{tikzcd}

commutes.

+-- {: .num_remark}
###### Note

This has little to do with either notion of [[idempotent monoid in a monoidal category]]: one yields [[strong monoidal functors]] while the other is not quite equivalent to this. Perhaps a better name would be *diagonal monoidal functor*, but this risks confusion with [[diagonal functor]].

=--

## Properties

\begin{theorem}
For any [[lax monoidal functor|lax monoidal]] [[endofunctor]] $F : (\mathcal{C}, \times) \to (\mathcal{C}, \times)$ on a [[cartesian monoidal category]], $F$ is idempotent if and only if the following composite is the [[identity morphism|identity]] for all $A,B \in \mathcal{C}$:

\begin{tikzcd}
	{F (A \times B)} & {FA \times FB} & {F (A \times B)}
	\arrow["{\langle F\pi_1, F\pi_2 \rangle}", from=1-1, to=1-2]
	\arrow["{\nabla_{A,B}}", from=1-2, to=1-3]
\end{tikzcd}
\end{theorem}

\begin{proof}
See ([Orchard 2014, proposition 3.3.9](#Orchard)).
\end{proof}

## Examples

* Any [[lax monoidal functor]] induced by a [[strong monad|strong]] [[idempotent monad]] is idempotent.

## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* [[braided monoidal functor]]

* [[symmetric monoidal functor]]

* **idempotent monoidal functor**

* [[idempotent monad]]

## References

The (original?) definition is in

* {#Orchard} [[Dominic Orchard]], *Programming contextual computations*, PhD thesis, University of Cambridge, technical report 854 (2014) &lbrack;[pdf](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-854.pdf)&rbrack;


[[!redirects idempotent monoidal functor]]
[[!redirects idempotent monoidal functors]]
[[!redirects diagonal monoidal functor]]
[[!redirects diagonal monoidal functors]]
