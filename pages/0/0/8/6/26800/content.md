# Fundamental theorem of linear algebra

## Statement in operator form

If $f:V\to W$ is a linear operator among vector spaces where $V$ is finite-dimensional of dimension $n$ then 
$$
dim\,Ker\,f + dim\,Im\,f = n.
$$

## Statement in the matrix form

If $A$ is a finite rectangular matrix then the row rank (the dimension of the span of its rows ("row space")) plus the dimension of the solution space of equation $A x = 0$ ("nullspace") yields the number of columns. From the other side, column rank (the dimension of the space of columns) plus the dimension of the solution space of equation $y A = 0$ (or, equivalently, $A^T y^T = 0$) yields the number of rows. 

Notice that now we have two statements as a rectangular matrix can be thought as a linear operator in two ways: acting by left multiplication on column vectors or acting by right multiplication on row vectors. 

## Terminology

Sometimes additional statements are included by some authors. 

Most often the additional part quoted is that the row rank is the same as the column rank. This is a somewhat nontrivial statement in our formulation (dimension of the space of rows/columns); in some expositions of the theory the definitions of ranks are such that this statement is automatic. Namely, the rank is the minimal dimension $r$ such that the $m\times n$-matrix $A$ can be written in the form $V \Lambda^T$ where $\Lambda$ is $n\times r$, that is $\Lambda^T$ is $r\times n$, and $V$ is an $m\times r$ matrix. Then the transposed matrix can be written as $\Lambda V^T$. This is nothing than the [[image factorization]] of a linear map and its transpose which both go through the same intermediate space.

## Literature

The following 2 refereces have somewhat nonstandard exposition of linear algebra to be amenable to constructive/algorithmic treatments useful in numerical linear algebra:

* [[Carl de Boer]], _Linear algebra_, [pdf](https://pages.cs.wisc.edu/~deboor/book.pdf)
* [[Carl de Boer]], Numerical functional analysis, University of Wisconsin lecture notes, chapter 1 (linear algebra), [pdf](https://pages.cs.wisc.edu/~deboor/717/book/1.pdf)


category: algebra