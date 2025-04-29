
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

Roughly, the *Habiro ring* is a [[ring of functions]] defined on [[formal neighborhoods]] of all [[roots of unity]] simultaneously, satisfying appropriate gluing conditions.

## Definition 

The Habiro ring over $\mathbb{Z}$ is defined as an [[inverse limit]]:

\[
  \mathcal{H}_{\mathbb{Z}} 
  \;\simeq\;  
  \lim_n \, \mathbb{Z}[q]/\big( (q;q)_n \big)
  \,,
\]
where $(q;q)_n = \prod_{i=1}^n(1-q^i)$, or equivalently, an inverse limit:
\[
  \mathcal{H}_{\mathbb{Z}} 
   \;\simeq\; 
  \lim_{n,m} \, \mathbb{Z}[q]/\big((1-q^n)^m\big)
  \,,
\]
where 
\[
  \label{le}
  (n_0,m_0) \le (n_1, m_1) 
  \;\;\;\colon\Leftrightarrow\;\;\; 
  m_0\le m_1 \;\wedge\; n_0|n_1
  \,.
\]

## Properties

For any root of unity $\omega$ and $f \in \mathcal{H}_{\mathbb{Z}}$, one defines $f_\omega(x) \coloneqq f(\omega + x) \in \mathbb{Z}[\omega][[x]]$. These satisfy compatibility conditions for varying $\omega$.

## Related concepts

* [[Chern-Simons invariant]]

* [[Donaldson-Thomas invariant]]

## References

* [[Stavros Garoufalidis]], [[Peter Scholze]], [[Campbell Wheeler]], [[Don Zagier]]: *The Habiro ring of a number field* &lbrack;[arXiv:2412.04241](https://arxiv.org/abs/2412.04241)&rbrack;

[[!redirects Habiro rings]]

