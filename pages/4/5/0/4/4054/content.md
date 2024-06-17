
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents


## Idea ##

The *polar decomposition* of [[bounded operators]] (on some [[Hilbert space]]) generalizes the decomposition of [[complex numbers]] $z$ as products $z = r e^{i \phi}$ with $r \in \mathbb{R}, r \ge 0$ being the [[absolute value]] of $z$ and the complex number $e^{i \phi}$ of norm $1$ being the modulus, or the complex sign, of $z$. 


## Definition ##

Let $\mathcal{H}$ be a [[Hilbert space]] and $S_1, S_2$ be 
[[closed subset|closed]] [[linear subspaces]].

+-- {: .un_def}
###### Definition

A [[unitary map|unitary]] [[isomorphism]]
$$
   U \,\colon\, S_1 \longrightarrow S_2
$$
is called a **partial isometry** with **initial space** $S_1$ and **final space** or range $S_2$
=--

Let $T$ be a [[bounded operator]] on $\mathcal{H}$

\begin{definition}

The [[positive operator]] 
$$
   |T| \,\coloneqq\, \big(T^* T\big)^{\frac{1}{2}}
$$
is called the **modulus** of T.

\end{definition}



## Properties ##

### Existence

\begin{proposition}
For every [[bounded operator]] $T$ on $\mathcal{H}$ there exists a unique partial isometry $U$ such that

1. U has initial space $\overline{R(|T|)}$ and range $\overline{R(T)}$

2. $T = U |T| = U (T^*T)^{\frac{1}{2}}$

\end{proposition}


\begin{remark}
Beware that this statement does not generalize from algebras of [[bounded operators]] $\mathcal{B}(\mathcal{H})$ to general [[C-star algebra|$C^\ast$-algebras]] $C$, because the partial isometry $U$ need not be contained in $C$. 

However, the analog statement is again true for [[von Neumann algebras]].
\end{remark}

## Related entries

* [[matrix decomposition]]

  * [[Gauss decomposition]]

  * [[QR decomposition]]

  * [[LU decomposition]]


## References ##

Most textbooks on [[operator algebra]] and [[Hilbert spaces]] mention the polar decomposition, for example it can be found in the beginning of

* [[Richard V. Kadison]], [[John R. Ringrose]], _Fundamentals of the theory of operator algebras_,  Vol II *Advanced Theory*, Graduate Studies in Mathematics **16**, AMS 1997 &lbrack;[ISBN:978-0-8218-0820-7](https://bookstore.ams.org/gsm-16)&rbrack;

See also:

* Wikipedia, [Polar decomposition](http://en.wikipedia.org/wiki/Polar_decomposition)


[[!redirects polar decompositions]]
