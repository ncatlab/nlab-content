
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


\tableofcontents

## Definition

For any [[monoidal category]] $V$ with [[coequalisers]], one can form a [[bicategory]] $Bimod(V)$ of [[bimodules]] as follows:

* The [[objects]] of $Bimod(V)$ are [[monoids]] $R$, $S$ [[monoid object|internal]] to $V$. 

* The [[1-morphisms]] are $(R,S)$-[[bimodules]]. That is, objects $A$ in $V$ with a compatible left [[action]] of $R$ and right [[action]] of $S$. The [[composition]] is given by a  generalization of the usual notion of [[tensor product]]: For an $(R,S)$-bimodule $A$ and an $(S,T)$-bimodule $B$, a new $(R,T)$-bimodule $A \otimes_S B$ is computed as the [[coequaliser]] of $A$'s right action and $B$'s left action of $S$.

  \[
    A \otimes S \otimes B
    \begin{matrix}
      \overset{\rho \otimes B}{\rightarrow} \\
      \underset{A \otimes \lambda}{\rightarrow}
    \end{matrix}\,\,
    A \otimes B \rightarrow A \otimes_S B
  \]

* [[2-morphisms]], are bimodule [[homomorphisms]]. 

In the case where $V =$ [[Ab]], this recovers the usual notion of [[bimodules]] and [[tensor product of modules|their tensor product]].

More generally, [[profunctors]] over any [[monoidal category]] are referred to as [[bimodule objects]]. Composition in this case replaces the [[colimit]] above with a [[coend]].

## See also

* [[bimodule]]

* [[bimodule object]]

* [[Mod]]


