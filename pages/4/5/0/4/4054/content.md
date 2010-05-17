#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
This page is about the polar decomposition of [[bounded operators]] on [[Hilbert spaces]]. Any complex number $z$ has a representation as $z = r e^{i \phi}$ with $r \in \mathbb{R}, r \ge 0$ being the absolute value of $z$ and the complex number $e^{i \phi}$ of norm $1$ being the modulus, or the complex sign, of $z$. The polar decomposition of a bounded operator is a generalization of this representation. 


## Definition ##
Let $\mathcal{H}$ be a [[Hilbert space]] and $S_1, S_2$ be closed linear subspaces.

+-- {: .un_def}
###### Definition
An unitary isomorphism
$$
   U: S_1 \to S_2
$$
is called a **partial isometry** with **initial space** $S_1$ and **final space** or range $S_2$
=--

Let $T$ be a bounded operator on $\mathcal{H}$

+-- {: .un_def}
###### Definitions
The positive operator 
$$
   |T| := (T^*T)^{\frac{1}{2}}
$$
is called the **modulus** of T.
=--


## The Theorem ##
For every bounded operator $T$ on $\mathcal{H}$ there exists a unique partial isometry $U$ such that

1. U has initial space $\overline{R(|T|)}$ and range $\overline{R(T)}$

2. $T = U |T| = U (T^*T)^{\frac{1}{2}}$

## Properties ##
We have stated the theorem for the [[operator algebra]] $\mathcal{B}(\mathcal{H})$ only, for a general [[C-star algebra]] $C$ it need not hold because the partial isometry $U$ need not be contained in $C$. 

This is true however for every [[von Neumann algebra]].

## Examples ##

## References ##
Most textbooks about operators on Hilbert spaces mention the polar decomposition, for example it can be found in the beginning of

* Kadison, Ringrose: _Fundamentals of the Theory of Operator Algebras_ , volume 2, _Advanced Theory_

[[!redirects polar decompositions]]