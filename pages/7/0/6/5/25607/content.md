# Contents
* table of contents
{:toc}


## Idea

An implicative structure is an ample generalization of [[complete Heyting algebra|complete Heyting algebras]] introduced by Alexandre Miquel in [(Miquel '20a)](#Miquel20a).

Implicative structures are used to define [[implicative algebra|implicative algebras]], with are implicative structures equipped with a 'separator', which generalizes a filter for an Heyting algebra. From an implicative algebra, one can then construct an [[implicative tripos]], a construction which is the real motivation behind implicative structures and algebras.

These triposes end up generalizing many others, constructed from [[complete Heyting algebra|complete Heyting algebras]], [[partial combinatory algebras]], ordered combinatory algebras, and Krivine structures, thus unifying the methodology of realizability theory. More strikingly, Miquel proved all triposes over $\mathbf{Set}$ are implicative triposes [(Miquel'20b)](#Miquel20b).

## Definition
\begin{definition}
An **implicative structure** is a [[complete lattice|complete meet semilattice]] $(\mathcal{A}, \leq)$ equipped with a right-continuous monotone operation $\to : \mathcal{A}^{op} \times \mathcal{A} \to \mathcal{A}$. 
\end{definition}

Explicitly, this means $\mathcal{A}$ is a [[poset]] with all meets, and $\to$ satisfies two axioms:

1. for all $a' \leq a, b \leq b' \in \mathcal{A}$, $(a \to b) \leq (a' \to b')$,
2. for all $a \in \mathcal{A}, B \subseteq \mathcal{A}$, $a \to \bigwedge_{b \in B} b = \bigwedge_{b \in B} (a \to b)$

We don't assume $\to$ to also be left-continuous (i.e. commute with $\bigvee$ in the first argument, which comes out as a $\bigwedge$ because of the antimonotonicity), though in most examples $\to$ satisfies this additional property.

\begin{remark}

Two observations follow immediately from this definition:

1. A complete semi-lattice is, at the end of the day, the same thing as a complete lattice since $\bigvee A = \bigwedge (\mathcal{A}\setminus A)$, where $A \subseteq \mathcal{A}$.
2. By the [[adjoint functor theorem]] for posets, $a \to -$ has a left adjoint $- \otimes a : \mathcal{A} \to \mathcal{A}$. In this sense, implicative structures generalize Heyting algebras by weakening the requirement that $- \otimes a = - \wedge a$. In fact, we have no requirement whatsoever on $- \otimes a$, which makes $\to$ a much weaker operation than $\Rightarrow$, at least on paper.

\end{remark}

Hence an alternative definition of implicative structure is:

\begin{definition}
An implicative structure is a complete lattice $\mathcal{A}$ equipped with a left-continuous, monotone operation $\otimes : \mathcal{A} \times \mathcal{A} \to \mathcal{A}$.
\end{definition}

In this form, it is easy to see this as broadly generalizing [[poset|posetal]] [[Benabou cosmoi]], more commonly known as [[quantale|quantales]].
In fact implicative structures are quantales, but for the fact that $\otimes$ doesn't satisfy the axioms of a monoidal operation on $\mathcal{A}$.

This is interesting since cosmoi are 'good enrichment bases' for *categories*, while implicative structures are 'good enrichment bases' for *sets*.

## See also

* [[implicative algebra]]
* [[realizability]]
* [[forcing]]
* [[tripos]], in particular [[implicative tripos]]

## References
* {#Miquel20a} Alexandre Miquel, _Implicative algebras: a new foundation for realizability and forcing_, Mathematical Structures in Computer Science 30 (5): 458–510. [(doi)](https://doi.org/10.1017/S0960129520000079).
* {#Miquel20b} Alexandre Miquel. 2020. _Implicative Algebras II: Completeness w.r.t. Set-Based Triposes_. arXiv. https://doi.org/10.48550/arXiv.2011.09085.
 [(arxiv)](https://arxiv.org/abs/2011.09085)
