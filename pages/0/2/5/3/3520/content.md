
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Statement

The **Hadamard lemma** states that for every [[smooth function]] $f \in C^\infty(\mathbb{R})$ on the [[real line]] there is a smooth function $g$ such that

$$
  f(x) = f(0) + x \cdot g(x)
  \,.
$$

This function $g$ is also called a **Hadamard quotient**.

It follows that $g(0) = f'(0)$ is the derivative of $f$ at 0. By applying this repeatedly the lemma says that $f$ has a partial Taylor expansion whose remainder $h$ is a smooth function:

$$
  f(x) = f(0) + x f'(0) + x^2 f''(0) + \cdots + x^n h(x)
  \,.
$$

More generally, for smooth functions on any [[Cartesian space]] $\mathbb{R}^n$ the lemma says that there are for each $f \in C^\infty(X)$ $n$ smooth functions $g_i$ such that

$$
 f(\vec x) = f(0) + \sum_i x_i g_i(x)
 \,.
$$

So at the origin these smooth functions compute the partial derivatives of $f$

$$
  g_i(0) = \frac{\partial f}{\partial x_i}(0)
  \,.
$$


## Remarks

* The Hadamard lemma implies that the [[derivation]]s of the algebra $C^\infty(X)$ of smooth functions on a smooth [[manifold]] are in bijection with the [[vector field]]s on $X$. See [[derivation]] for details.

* A more abstract way to state the Hadamard lemma (and a bit more) is to say that [[generalized smooth algebra|smooth function rings]] form a [[Fermat theory]]. As such the Hadamard lemma is a crucial ingredient for [[Models for Smooth Infinitesimal Analysis|well-adapted models]] of [[synthetic differential geometry]].

## References

The Hadamard lemma is what makes the standard _convenient models_ for [[synthetic differential geometry]] tick. Its role in this respect can be seen from proposition 1.2 on in 

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)


[[!redirects Hadamard's lemma]]
[[!redirects Hadamard quotient]]