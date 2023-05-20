
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a notion of [[real number]] $\mathbb{R}$, let $\sigma_j:\mathbb{R}^n \to \mathbb{R}$ denote the $j$-th [[elementary symmetric polynomial|elementary symmetric]] [[polynomial function]] in $\mathbb{R}$, 
and the polynomials functions 
$e_j:\mathbb{R}^n \to \mathbb{R}$ as 
$$e_j(x_1, x_2 \ldots x_n) \coloneqq \prod_{k \neq j} (x_k - x_j)$$ 
Let us define the polynomial function $f:\mathbb{R}^{n+1} \to \mathbb{R}$ as 
$$f(y, x_1, x_2 \ldots x_n) \coloneqq \prod_{j = 0}^n (y + x_j) = \sum_{j = 0}^n \sigma_{n - j}(x_1, x_2, \ldots x_n) y^j$$
Now, $\sigma_j(e_1(x_1, x_2 \ldots x_n), e_2(x_1, x_2 \ldots x_n), \ldots e_n(x_1, x_2 \ldots x_n))$ is by definition also a symmetric polynomial function. Thus, there exists a polynomial function $d_j:\mathbb{R}^n \to \mathbb{R}$ such that 
$$d_j(\sigma_1(x_1, x_2, \ldots x_n), \sigma_2(x_1, x_2, \ldots x_n), \ldots \sigma_n(x_1, x_2, \ldots x_n)) = \sigma_j(e_1(x_1, x_2 \ldots x_n), e_2(x_1, x_2 \ldots x_n), \ldots e_n(x_1, x_2 \ldots x_n))$$

The function $f$ is **unramifiable** if there exists a $j$ such that $d_j(\sigma_1(x_1, x_2, \ldots x_n), \sigma_2(x_1, x_2, \ldots x_n), \ldots \sigma_n(x_1, x_2, \ldots x_n))$ is invertible in $\mathbb{R}$. 

## Related concepts

* [[simple root]]
* [[elementary symmetric polynomial]]
* [[fundamental theorem of algebra]]

## References

* {#Ruitenberg91} Wim Ruitenberg, Constructing Roots of Polynomials over the Complex Numbers, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract, Vol. 84, Centre for Mathematics and Computer Science, Amsterdam, 1991, pp. 107–128. ([pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf))

[[!redirects unramifiable polynomial]]
[[!redirects unramifiable polynomials]]