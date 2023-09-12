
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
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

In [[quantum physics]] and in particular in the context of [[quantum computing]] a [[linear map]] between spaces of [[linear operators]] (hence an "operator on operators") is sometimes called a _superoperator_.

Notably [[density matrices]] representing [[quantum states]] are given by linear operators and a [[quantum operation]] is a superoperator that preserves the defining properties of density matrices. (Beware that sometimes different or no distinctions between "[[quantum operation]]" and "superoperator" are made.)

## Details
 {#Details}

Specifically, in a [[symmetric monoidal closed category]] $(\mathcal{C}, \otimes, \mathbb{1})$ with [[internal hom]] denoted $(\text{-})\multimap (\text{-})$, a superoperator is a morphism of a form like

\[
  \label{OperatorOnInternalHoms}
  (\mathscr{H} \multimap \mathscr{H})
  \longrightarrow
  (\mathscr{K} \multimap \mathscr{K})  
  \,.
\]

If $(\mathcal{C}, \otimes, \mathbb{1})$ is also [[compact closed category|compact closed]] then (eq:OperatorOnInternalHoms) is [[isomorphism|isomorphic]] to a [[morphism]] of the form

\[
  \label{SuperoperatorOnMatrices}
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{K} \otimes \mathscr{K}^\ast
\]

(whence one also speaks of operators on spaces of ([[density matrix|density]]) [[matrices]]) 

which in turn is [[adjunct]], in particular, to a morphism of the form

\[
  \label{PartialAdjunctOfSuperoperator}
  \mathscr{K}^\ast \otimes \mathscr{H}
  \longrightarrow
  \mathscr{K}^\ast \otimes \mathscr{H}
  \mathrlap{\,.}
\]

Sometimes (eq:PartialAdjunctOfSuperoperator) is the more transparent incarnation of superoperators:

For example, if $(\mathcal{C}, \otimes, \mathbb{1})$ is even a [[dagger-compact category]], then a superoperator in the form (eq:OperatorOnInternalHoms) or (eq:SuperoperatorOnMatrices) is a *[[completely positive map]]* (and hence restricts to a "[[quantum operation]]" on [[density matrices]]) iff its adjunct (eq:PartialAdjunctOfSuperoperator) is a [[positive operator]] &lbrack;[Selinger 2005 Cor. 4.13](#Selinger05)&rbrack;.


## Related entries

* The [[Geometry of Interaction]]-construction is a genral abstract construction of a category of superoperators. See there for more.

## References

Traditional discussion:

* {#Kuperberg05} [[Greg Kuperberg]], Section 1.4 of: _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

See also:

* Wikipedia, _[Superoperator](http://en.wikipedia.org/wiki/Superoperator)_

In terms of [[string diagrams]] in [[dagger-compact categories]] (cf. [[quantum information theory via dagger-compact categories]]):

* {#Selinger05} [[Peter Selinger]], *Dagger-compact closed categories and completely positive maps*, Electronic Notes in Theoretical Computer Science, **170** (2007) 139-163 &lbrack;[doi:10.1016/j.entcs.2006.12.018](https://doi.org/10.1016/j.entcs.2006.12.018), [[SelingerPositiveMaps.pdf:file]]&rbrack;


Formalizing superoperators as [[arrows (in computer science)]]:

* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, *Structuring quantum effects: superoperators as arrows*, Mathematical Structures in Computer Science **16** 3 (2006)  453-468 &lbrack;[arXiv:quant-ph/0501151](https://arxiv.org/abs/quant-ph/0501151), [doi:10.1017/S0960129506005287](https://doi.org/10.1017/S0960129506005287)&rbrack;



[[!redirects superoperators]]

[[!redirects super-operator]]
[[!redirects super-operators]]