

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

A *cellular category* in the sense of [Makkai & Rosický 2014](#MakkaiRosický14) is a ([[cocomplete category|cocomplete]]) [[category]] equipped with a minimum of extra information indicating that some of its [[morphisms]] behave like [[relative cell complexes]]. 

## Definition

\begin{definition}
\label{CellularCategory}
([Makkai & Rosický 2014, Def. 2.1](#MakkaiRosický14))
\linebreak
A *cellular category* is:

1. a [[cocomplete category]] $\mathcal{C}$,

1. a [[class]] of morphisms $Cell(\mathcal{C}) \,\subset\, Mor(\mathcal{C})$,

such that 

1. $Cell(\mathcal{C})$ contains all [[isomorphisms]],

1. $Cell(\mathcal{C})$ is closed under [[pushouts]] and [[transfinite composition]].

\end{definition}

## Examples

\begin{example}
**(model categories with their cofibrations)**
\linebreak
  Given a [[model category]] $\big(\mathcal{C}, (\mathrm{W},\, Fib, Cof) \big)$, then -- understood as equipped (just) with its [[cofibrations]] $Cof$ or (just) with its [[acyclic cofibrations]] $Cof \cap \mathrm{W}$ -- it is a cellular category in the sense of Def. \ref{CellularCategory}.

More to the point, if such a [[model category]] is [[cofibrantly generated]] by generating sets $I \,\subset\, Cof$ (and $J \,\subset\, Cof \cap \mathrm{W}$), then $\mathcal{C}$ equipped with the closure of $I$ under [[pushout]] and [[transfinite composition]] is cellular (by construction) and in this case the class $Cell(-)$ is that which one ordinarily addresses as [[relative cell complexes]] with [[attaching maps]] in $I$. (The full class of cofibrations is the re-obtained by further closing the class of relative cell complexes under forming [[retracts]]).
\end{example}

## Related concepts

* [[cell complex]], [[relative cell complex]]

* [[cofibrantly generated model category]]

* [[model structure on functors]]

* [[transferred model structure]]

* the notions of *cellular categories* and of *[[cellular model categories]]* are vaguely related, but not as systematically as the (independently chosen) terminology might suggest


## References

The notion is due to:

* {#MakkaiRosický14} [[M. Makkai]], [[J. Rosický]], _Cellular categories_, J. Pure Appl. Alg. **218** (2014) 1652-1664 &lbrack;[arXiv:1304.7572](https://arxiv.org/abs/1304.7572), [doi:10.1016/j.jpaa.2014.01.005](https://doi.org/10.1016/j.jpaa.2014.01.005)&rbrack;


[[!redirects cellular categories]]

