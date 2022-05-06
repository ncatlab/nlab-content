
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Up to [[isomorphism]] there is only one [[split composition algebra]] of dimension 8; this is called the algebra of _split octonions_. 

## Definition

The multiplication may be deduced from the fundamental result on doubling multiplication or may be expressed as follows. Denote scalars by letters like $r, s$ and 3-vectors by letters like $x, y$. Let $\langle x, y \rangle$ denote the standard inner product 
$$x_1 y_1 + x_2 y_2 + x_3 y_3$$ 
and let $x \wedge y$ denote the standard cross-product, so that $\langle x \wedge y, z \rangle = det(x, y, z)$. Elements of $V$ are represented by $2 \times 2$ arrays 
$$\left( 
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right)$$
and multiplication is given by the following formula, highly reminiscent of matrix multiplication but with some cross-product cross terms: 
$$\left(
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right) 
\cdot
\left(
\begin{aligned}
r' & x'\\
y' & s'
\end{aligned}
\right) = 
\left(
\begin{aligned}
r r' + \langle x, y' \rangle & r x' + s' x + y \wedge y'\\ 
r' y + s y' + x \wedge x' & \langle y, x' \rangle + s s'
\end{aligned}
\right)
$$
The norm is given by a kind of determinant formula 
$$N\left(
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right) = r s - \langle x, y \rangle
$$

## Related concepts

* [[octonions]]

* [[Albert algebra]]

* [[split quaternions]]

## References

* [[John Baez]], [[John Huerta]], _$G_2$ and the Rolling Ball_, Trans. Amer. Math. Soc., Vol. 366 No. 10 (2014), 5257-5293 ([arXiv:1205.2447](https://arxiv.org/abs/1205.2447))

See also

* Wikipedia, _[Split-octonion](https://en.wikipedia.org/wiki/Split-octonion)_


[[!redirects split octonion]]

[[!redirects split-octonions]]
[[!redirects split-octonion]]
