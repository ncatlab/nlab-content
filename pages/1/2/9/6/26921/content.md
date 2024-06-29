
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

\tableofcontents

## Idea


In [[algebra]] one speaks of *internal* direct sums for [[direct sums]] of [[subobjects]] of a given [[object]] that are themselves again canonically subobjects of that object. 

In contrast to this situation, the ordinary direct sum is sometimes called the *[[external direct sum]]*.

## Definition

### For modules


Traditionally this is considered for [[modules]] $N$ over a [[ring]] $R$ and stated as follows (see the references [below](#TradDefinitionReferences)):

Let $\big\{N_i \subset N\big\}_{i \in I}$ be an [[indexed set]] of of [[submodules]] $N_i \hookrightarrow N$. Then a submodule

\[
  \label{InternalDirectSumOfModules}
  \oplus^{int}_{i \in I} N_i
  \,\xhookrightarrow{\;\; q \;\;}\,
  N
\]

is called their *internal direct sum* if the following condition holds

* For every $n \in \bigoplus^{int}_{i \in I} N_i$ there is a unique $I$-[[tuple]] $(n_i \in N_i)_{i \in I}$ such that their [[sum]] in $N$ is $\sum_i n_i \,=\, n$.

Of course, this is equivalent to the condition:

* $\bigoplus^{int}_{i \in I} N_i \,\simeq\, \bigoplus_{i \in I} N_i$ is [[isomorphism|isomorphic]] to the abstract ([[external direct sum|external]]) [[direct sum]], and $q$ in (eq:InternalDirectSumOfModules) is the [[universal property|universal]] morphism  induced from the inclusions $N_i \hookrightarrow N$.

In this form the definition clearly generalizes.

### Generally

Given an object $B$ and a [[family]] of [[subobjects]] $A_i$ of $B$ (or more generally a family of morphisms $A_i \to B$, or equivalently a map $\coprod_i A_i \to B$), suppose that the direct sum $\bigoplus_i A_i$ exists.  Suppose further that the map $\coprod_i A_i \to B$ factors through the map $\coprod_i A_i \to \bigoplus_i A_i$ (which means that it factors uniquely if $\coprod_i A_i \to \bigoplus_i A_i$ is an [[epimorphism]], as it must be in a [[regular category]]).  Finally, suppose that the (or a) [[quotient map]] $\bigoplus_i A_i \to B$ is an [[isomorphism]].  Then we say that $B$ is the __internal direct sum__ of the $A_i$.

In contrast, the abstractly defined direct sum $\bigoplus_i A_i$ may be called an __external direct sum__.  These terms are usually used with [[concrete categories]] where the $A_i$ may either be given independently (for an external direct sum) or as [[subsets]] of some ambient space (either $B$ or something of which $B$ is a subset) for an internal direct sum.  In too abstract a context, there is no difference: on the one hand, any internal direct sum is a fortiori isomorphic to any external direct sum; on the other hand, given an external direct sum, there is a natural map $\coprod_i A_i \to \bigoplus_i A_i$, relative to which the external direct sum is an internal direct sum.


# References

{#TradDefinitionReferences} On the tradition definition:

* {#ProofWiki} [ProofWiki](https://proofwiki.org/wiki/Main_Page), *[Internal Direct Sum of Modules](https://proofwiki.org/wiki/Definition:Internal_Direct_Sum_of_Modules)*

* Lia-Ming Liou, *External direct sum and Internal direct sum of vector spaces*, lecture notes &lbrack;[pdf](https://www.math.ncku.edu.tw/~fjmliou/advcal/sumvspace.pdf)&rbrack;

[[!redirects internal direct sums]]

[[!redirects internal direct summand]]
[[!redirects internal direct summands]]






