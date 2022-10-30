
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A [[concrete set|set]] $S$ of [[natural numbers]] is **recursive** if there is an [[algorithm]] which will decide in finitely many steps whether a given natural number belongs to $S$. 


## Definition

A [[subset]] $S$ of the set of [[natural numbers]] $\mathbb{N}$, or more generally of $\mathbb{N}^k$ with $k$ finite, is _recursive_ if there is a [[computable function]] (a [[total function|total]] [[partial recursive function|recursive]] function) $f: \mathbb{N}^k \to \mathbf{2} = \{0, 1\} \subseteq \mathbb{N}$ such that $S = f^{-1}(1)$. Recursive subsets are a proper subclass of the class of _[[recursively enumerable set|recursively enumerable]]_ sets, which are [[domains]] of [[partial recursive functions]] $f: \mathbb{N}^k \to \mathbb{N}$, or equivalently [[images]] of total recursive functions. 


## Properties

Recursive sets form a [[Boolean algebra|Boolean subalgebra]] of the [[power set]] algebra $P(\mathbb{N})$ (whereas recursively enumerable subsets do not form a Boolean subalgebra).  Even in [[constructive mathematics]] (where the power set algebra may be only a [[Heyting algebra]]), the recursive sets form a Boolean algebra (a Boolean subalgebra of the algebra of [[decidable subsets]]).


## Examples and counterexamples

* One can encode [[proofs]] in the formal theory $PA$ ([[Peano arithmetic]]) as natural numbers, via a process of [[Gödel-numbering]]. The set of codes of such formal proofs is a recursive set. In colloquial language: it is possible to program a computer to detect whether or not a string of symbols represents a valid proof in $PA$. 

* It follows that the set of codes of [[theorems]] (provable propositions) is recursively enumerable. However, it is **not** recursive. This is one way of saying that provability in PA cannot be decided by an algorithm, which is closely related to G&#246;del's [[incompleteness theorem]]s. 


## Related concepts

* [[definable set]], [[constructible set]]


[[!redirects recursive subset]]
[[!redirects recursive subsets]]
