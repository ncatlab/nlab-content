+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

\tableofcontents


## Idea

The *Cartan matrix* of a complex [[semisimple Lie algebra]] $\mathfrak{g}$ (or of its [[root system]]) is the [[square matrix]] of [[integers]] ("Cartan integers") that records the relative [[angles]] and [[lengths]] of a choice of [[simple root|simple]] [[root (in representation theory)|roots]] $\alpha_1, \cdots, \alpha_n$:
$$
  a_{i j}
  \;\coloneqq\;
  \frac{ 2 (\alpha_i, \alpha_j) }{ (\alpha_i, \alpha_i) }
  \,.

$$
Here we use the convention of [Kac 1990](#Kac90); some authors (e.g. [Humphreys 1972, §11.1](#Humphreys72)) use the [[transpose matrix|transpose]]. 

For example, for type $B_2$ (with $\alpha_1$ long and $\alpha_2$ short) the two conventions give, respectively,
$$
  \left(
  \array{
    2 & -1
    \\
    -2 & 2
  }
  \right)
  \;\;\;\;
  \text{and}
  \;\;\;\;
  \left(
  \array{
    2 & -2
    \\
    -1 & 2
  }
  \right)
  \,.
$$

The diagonal entries are all $a_{i i} = 2$. The off-diagonal entries are in $\{0, -1, -2, -3\}$, with $a_{i j} = 0$ iff $a_{j i} = 0$. Up to the ordering of the simple roots, the Cartan matrix does not depend on the choice of simple roots (i.e. of a *base* $\Delta \subset \Phi$ in the sense of [Humphreys 1972, §10.1](#Humphreys72)), since the [[Weyl group]] acts transitively on these ([Humphreys 1972, Thm. 10.3](#Humphreys72)), nor on the choice of [[Cartan subalgebra]], since all of these are conjugate ([Humphreys 1972, Cor. 16.4](#Humphreys72)). It is nonsingular, and it is equivalently encoded in the [[Dynkin diagram]].

The Cartan matrix determines the [[root system]] up to [[isomorphism]] ([Humphreys 1972, Prop. 11.1](#Humphreys72)), and hence the [[Lie algebra]] up to [[isomorphism]] ([Humphreys 1972, Thm. 18.4](#Humphreys72)). In fact, $\mathfrak{g}$ is presented by generators $e_i, f_i, h_i$ and the relations
$$
  [h_i, h_j] = 0
  \,,
  \;\;\;
  [e_i, f_j] = \delta_{i j}\, h_i
  \,,
  \;\;\;
  [h_i, e_j] = a_{i j}\, e_j
  \,,
  \;\;\;
  [h_i, f_j] = - a_{i j}\, f_j
$$
together with the [[Serre relations]] $(\mathrm{ad}_{e_i})^{1 - a_{i j}}(e_j) = 0 = (\mathrm{ad}_{f_i})^{1 - a_{i j}}(f_j)$ for $i \neq j$ ([Humphreys 1972, §18](#Humphreys72)).

For example, the Cartan matrix of $\mathfrak{sl}(3)$ (type $A_2$) is
$$
  \left(
  \array{
    2 & -1
    \\
    -1 & 2
  }
  \right)
  \,.
$$

More generally, a *generalized Cartan matrix* is any integer square matrix with $a_{i i} = 2$, $a_{i j} \leq 0$ for $i \neq j$, and $a_{i j} = 0 \Leftrightarrow a_{j i} = 0$. The same presentation then defines a [[Kac-Moody algebra]] (for symmetrizable matrices; in general one passes to a quotient), which is finite-dimensional precisely if the matrix is a Cartan matrix in the above sense ([Kac 1990](#Kac90)). Allowing in addition diagonal entries $a_{i i} \leq 0$ leads to [[Borcherds algebras]].


## References

* {#Humphreys72} [[James Humphreys]]: *Introduction to Lie Algebras and Representation Theory*, Graduate Texts in Mathematics **9**, Springer (1972) &lbrack;[doi:10.1007/978-1-4612-6398-2](https://doi.org/10.1007/978-1-4612-6398-2)&rbrack;

  (§9.1 for the Cartan integers, §11.1 for the Cartan matrix, Table 1 in §11.4 for the list of Cartan matrices, §18 for the Serre relations and Serre's theorem)

* {#Kac90} [[Victor Kac]]: Ch. 1 in: *Infinite dimensional Lie algebras*, Cambridge University Press, 3rd edition (1990) &lbrack;[doi:10.1017/CBO9780511626234](https://doi.org/10.1017/CBO9780511626234)&rbrack;

* Wikipedia: _[Cartan matrix](https://en.wikipedia.org/wiki/Cartan_matrix)_


[[!redirects Cartan matrices]]

[[!redirects generalized Cartan matrix]]
[[!redirects generalized Cartan matrices]]