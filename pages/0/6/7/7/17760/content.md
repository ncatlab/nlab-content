## Idea

The Frobenius-Perron theorem is a foundational result in the theory of non-negative matrices. In its simplest form it says that the largest eigenvalue of any square matrix with positive entries is real, is of multiplicity one, and that it has an eigenvector with strictly positive entries. The largest real eigenvalue of a matrix with non-negative entries is aptly known as the Frobenius-Perron eigenvalue, and its corresponding positive eigenvector is the Frobenius-Perron eigenvector. 

Seeing as matrices with positive/non-negative entries are ubiquitous across mathematics, this theorem has a plethora of applications. For instance,

* [[stochastic processes]]/[[Markov chains]], where the Frobenius-Perron eigenvector corresponds to a stable state/limiting behavior of the process.

* Algebraic graph theory - the study of linear-algebraic properties of graphs. That is, situations where one studies the linear algebra of adjacency matrices of graphs. Adjacency matrices are necessarily non-negative, and the Frobenius-Perron eigenvector can be of great utility. This theory is used strongly, for instance, in the proofs of many [[ADE classifications]].

* [[fusion rings]]/[[fusion categories]]. Here, the fusion rules of the category will naturally induce non-negative matrices. The Frobenius-Perron eigenvalue of fusion matrix corresponding to an element is known as its [[Frobenius-Perron dimension]] and serves a key role in theory.

## Statements

There are a collection of related results all known as the Frobenius-Perron theorem, which require more or less strong strong conditions and give more or less strong results. The most canonical "Frobenius-Perron theorem" is as follows:

\begin{theorem} The eigenvalue of largest absolute value for any matrix with positive entries will be a positive real number. It's corresponding eigenspace will be one-dimensional, and it will have an eigenvector with all positive entries.
\end{theorem}

Conversely, we have the following result:

\begin{theorem} If an eigenvector to a positive matrix has positive entries, then its eigenvalue must be the Frobenius-Perron eigenvalue.
\end{theorem}

This gives a very simple way of computing the Frobenius-Perron eigenvalue of a positive matrix. Namely, all one has to do is construct a positive eigenvector and measure its eigenvalue.

Often, one will be applying the Frobenius-Perron theorem to matrices with non-negative entries. Here, we can say the following:

\begin{theorem} The eigenvalue of largest absolute value for any matrix with non-negative entries will be a non-negative real number. It will have an eigenvector with all non-negative entries.
\end{theorem}

There are many non-negative matrices for which the stronger positive-matrix formulation of the theorem still holds. Namely, we have the following:

\begin{theorem} Let $A$ be a matrix such that $A^m$ is positive for some $m\geq 1$. The eigenvalue of largest absolute value for $A$ will be a positive real number. It's corresponding eigenspace will be one-dimensional, and it will have an eigenvector with all positive entries.
\end{theorem}

## Related concepts

* [[Frobenius-Perron dimension]]

* [[fusion category]]

## References

* [[Damien Calaque]], [[Pavel Etingof]], section 4 of  _Lectures on tensor categories_ ([arXiv:math/0401246](https://arxiv.org/abs/math/0401246))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 3.2 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))

* Wikipedia, _[Perron-Frobenius theorem](https://en.wikipedia.org/wiki/Perron%E2%80%93Frobenius_theorem)_


[[!redirects Perron-Frobenius theorem]]
