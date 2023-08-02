
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

\section{Definition}

\subsection{Of matrices}

The **Hadamard product** or **Schur product** or **element-wise product** of two matrices $A$ and $B$ in a commutative ring $R$ is a matrix $A \odot B$ whose elements $c_{i, j}$ are the product $a_{i, j} \cdot b_{i, j}$ of the respective elements $a_{i, j}$ in the matrix $A$ and $b_{i, j}$ in the matrix $B$. 

\subsection{Of power series}

The **Hadamard product** of two [[power series]] $p = \sum_{i = 0}^\infty a_i x^i$ and $q = \sum_{i = 0}^\infty b_i x^i$ with [[coefficients]] from a [[commutative ring]] $R$ is the [[power series]] defined by 

$$p \odot q \coloneqq \sum_{i = 0}^\infty a_i b_i x^i$$

\subsection{More generally}

Let $R$ be a [[commutative ring]], and let $[n]$ denote the finite set with $n$ elements. The $m$ by $n$ [[matrix algebra]] $M_{m, n}(R)$ is [[isomorphic]] to the [[function algebra]] $[m n] \to R$, where the Hadamard product in $M_{m, n}(R)$ corresponds to pointwise multiplication in $[m n] \to R$. Similarly, the [[power series ring]] $R[[x]]$ is [[isomorphic]] to the [[function algebra]] $\mathbb{N} \to R$, where the Hadamard product in $R[[x]]$ corresponds to pointwise multiplication in $\mathbb{N} \to R$. 

Thus, there is a generalization of the definition of Hadamard product from [[matrix algebras]] and [[power series rings]] to any [[commutative algebra]] with a [[isomorphism]] of [[commutative algebras]] to a [[function algebra]]: 

Let $S$ be a set, let $R$ be a commutative ring, and let $A$ be a commutative $R$-algebra with an isomorphism of commutative $R$-algebras $i:A \cong (S \to R)$. Then the **Hadamard product** in $A$ is a [[binary operation]] $(X, Y) \mapsto X \odot Y:A \times A \to A$ defined as 

$$X \odot Y \coloneqq i^{-1}(x \mapsto i(X)(x) \cdot i(Y)(x))$$

\section{Related concept}

* [[matrix]]

* [[power series]]

\section{References}

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices)</a>

* Wikipeida, <a href="https://en.wikipedia.org/wiki/Generating_function_transformation#Hadamard_products_and_diagonal_generating_functions">Generating function transformation#Hadamard products and diagonal generating functions</a>

[[!redirects Hadamard product]]
[[!redirects Schur product]]
[[!redirects element-wise product]]