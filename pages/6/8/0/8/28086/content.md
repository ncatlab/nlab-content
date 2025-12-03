
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Noncommutative geometry
+-- {: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

An **$H^*$-algebra** is a $\mathbb{C}$-[[associative unital algebra |algebra]] $A$ that is simultaneously a [[Hilbert space]] $(A, \langle \cdot, \cdot \rangle_A)$ with an anti-linear [[involution]] $\dagger: A \to A$ such that

\[ 

\langle a b, c \rangle_A = \langle b, a^{\dagger} c \rangle_A = \langle a , c b^{\dagger} \rangle_A
\]

for all $a,b,c \in A$.

## Classifying Frobenius Algebras

[[Frobenius algebra | Frobenius structures]] in the [[category]] of [[finite-dimensional Hilbert space |finite-dimensional Hilbert spaces]] can be classified via $H^*$-algebras.

\begin{theorem}
A [[monoid in a monoidal category |monoid]] $(A, \mu, \eta)$ internal to [[finite-dimensional Hilbert space | $\mathrm{FdHilb}$]] is a [[Frobenius algebra |symmetric dagger Frobenius monoid]] if and only if it is a finite-dimensional $H^*$-algebra, where the the involution is defined by sending an element $a \in A$ to
\begin{centre}
    \begin{tikzcd}
\mathbb{C} \arrow[r, "\eta"] & A \arrow[r, "\mu^{\dagger}"] & A \otimes A \arrow[r, "1_A \otimes a"] & A \otimes \mathbb{C} \arrow[r] & A.
    \end{tikzcd}
\end{centre}
\end{theorem}

## References

An exposition of the classification of Frobenius structures in finite-dimensional Hilbert spaces as $H^*$-algebras is detailed in

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]]: *Categories for Quantum Theory*, Oxford University Press (2019) \[<a href="https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616">ISBN:9780198739616</a>\]

  based on:

  {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], *Lectures on categorical quantum mechanics* (2012) \[<a href="https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf">pdf</a>, [[HeunenVicary-QuantumLectures.pdf:file]]\]

[[!redirects H-star-algebra]]
[[!redirects H-star-algebras]]
[[!redirects H-star algebra]]
[[!redirects H-star algebras]]
[[!redirects H*-algebra]]
[[!redirects H* algebra]]
[[!redirects H*-algebras]]
[[!redirects H* algebras]]
[[!redirects H-*-algebra]]
[[!redirects H-* algebra]]
[[!redirects H-*-algebras]]
[[!redirects H-* algebras]]