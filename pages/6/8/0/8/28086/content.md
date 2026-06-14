
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



\tableofcontents


## Definition

\begin{definition}\label{HStarAlgebra}
An **$H^*$-algebra** is a (not necessarily [[unitality|unital]]) [[Banach algebra]] $A$ that is simultaneously a [[Hilbert space]] $(A, \langle \cdot, \cdot \rangle_A)$ with a compatible [[star-algebra]] [[structure]], namely with an [[antilinear map|anti-linear]] [[involution]] $\dagger \colon A \to A$ such that

\[ 
  \langle a b, c \rangle_A 
    = 
  \langle b, a^{\dagger} c \rangle_A 
    = 
  \langle a , c b^{\dagger} \rangle_A
  \,,
  \;\;\;
  \text{for all}\; a,b,c \in A.
\]

\end{definition}
([Ambrose 1945 Def. 1.2](#Ambrose1945))

\begin{definition}\label{ProperHStarAlgebra}
  An $H^\ast$-algebra $A$ (Def. \ref{HStarAlgebra}) is called *proper* if 

* The only element $a \in A$ such that $a \cdot (-)$ is the [[zero]] map $A \to A$ is $a = 0$.

or equivalently

* The only element $a \in A$ such that $(-) \cdot a$ is the [[zero]] map $A \to A$ is $a = 0$.

\end{definition}
([Ambrose 1945 Def. 2.1](#Ambrose1945))


## Properties

### Classifying Frobenius Algebras

[[Frobenius algebra| Frobenius structures]] in the [[category]] of [[finite-dimensional Hilbert space|finite-dimensional Hilbert spaces]] can be classified via $H^*$-algebras.

\begin{theorem}\label{AsFrobeniusAlgebra}
A [[monoid in a monoidal category|monoid]] $(A, \mu, \eta)$ internal to [[Hilb|$\mathrm{FdHilb}$]] is a [[Frobenius algebra|symmetric dagger Frobenius monoid]] if and only if it is a [[finite-dimensional Hilbert space|finite-dimensional]] proper $H^*$-algebra (Def. \ref{ProperHStarAlgebra}), where the the involution is defined by sending an element $a \in A$ to
\begin{centre}
    \begin{tikzcd}
\mathbb{C} \arrow[r, "\eta"] & A \arrow[r, "\mu^{\dagger}"] & A \otimes A \arrow[r, "1_A \otimes a"] & A \otimes \mathbb{C} \arrow[r] & A.
    \end{tikzcd}
\end{centre}
\end{theorem}

(cf. [Abramsky & Heunen 2012](#AbramskyHeunen2012))


## Related concepts

* [[C-star algebra|$C^\ast$-algebra]]

* [[H-star-category|$H^\ast$-category]]

## References

The original article:

* {#Ambrose1945} [[Warren Ambrose]]: *Structure Theorems for a special class of Banach Algebras*, Transactions of the American Mathematical Society **57** (1945) 364--386 &lbrack;[doi:10.2307/1990182](https://doi.org/10.2307/1990182), [jstor:1990182](https://www.jstor.org/stable/1990182),  [pdf](https://scispace.com/pdf/structure-theorems-for-a-special-class-of-banach-algebras-36z9t9hi9q.pdf)&rbrack;

Discussion in relation to [[Frobenius algebra]]-[[structures]] on [[finite-dimensional Hilbert spaces]]:

* {#AbramskyHeunen2012} [[Samson Abramsky]], [[Chris Heunen]]: *$H^\ast$-algebras and nonunital Frobenius algebras: first steps in infinite-dimensional categorical quantum mechanics*, in *Clifford Lectures*, AMS Proceedings of Symposia in Applied Mathematics **71** (2012) 1--24 &lbrack;[arXiv:1011.6123](https://arxiv.org/abs/1011.6123)&rbrack;

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