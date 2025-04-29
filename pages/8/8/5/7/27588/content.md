
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--

\tableofcontents



## Idea

Roughly, the Habiro ring is a ring of functions defined in formal neighborhoods of all roots of unity simultaneously, satisfying appropriate gluing conditions.

## Definition 

The Habiro ring over $\mathbb{Z}$ is defined as an inverse limit:
$$
	\mathcal{H}_{\mathbb{Z}} =  \lim_n \mathbb{Z}[q]/((q;q)_n)
$$
where $(q;q)_n = \prod_{i=1}^n(1-q^i)$, or equivalently, an inverse limit:
$$
	\mathcal{H}_{\mathbb{Z}} = \lim_{n,m} \mathbb{Z}[q]/((1-q^n)^m)
$$
where $(n_0,m_0) \le (n_1, m_1) := m_0\le m_1 \wedge n_0|n_1$.

## Properties

For any root of unity $\omega$ and $f \in \mathcal{H}_{\mathbb{Z}}$, one defines $f_\omega(x) := f(\omega + x) \in \mathbb{Z}[\omega][[x]]$. These satisfy compatibility conditions for varying $\omega$.

## Related concepts

* [[Chern-Simons invariant]]

* [[Donaldson-Thomas invariant]]

## References

* [[Stavros Garoufalidis]], [[Peter Scholze]], [[Campbell Wheeler]], [[Don Zagier]], *The Habiro ring of a number field* ([arXiv:2412.04241](https://arxiv.org/abs/2412.04241))

[[!redirects Habiro ring]]
[[!redirects Habiro rings]]