
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Arithmetic gauge theory_ is a theory proposed by [Kim 2018 ](#Kim18) to look at [[Galois representations]] with an action of another group (the [[gauge group]]) as being analogous to [[gauge fields]] in [[gauge theory]]. It is an approach to Diophantine problems such as the effective [[Mordell conjecture]] and is influenced by the theory of the Selmer group and Chabauty's method.

## Definitions

Let $K$ be a field of characteristic zero and let $G_{K}$ be its [[absolute Galois group]]. A _gauge group over $K$_ is a [[topological group]] $U$ with a continuous action of $G_{K}$.

A _$U$-gauge field_, or _$U$-principal bundle_, is a topological space $P$ with compatible continuous left $G_{K}$-action and simply transitive continuous right $U$ action.

## Examples

This section follows section 8 of [Kim 2018](#Kim18).

Let $V$ be a variety over $\mathbb{Q}$ equipped with a base point $b\in V(\mathbb{Q})$. Our motivation is determining the set $V(\mathbb{Q})$ of rational points of $V$. For our gauge group $U$ we let

$$U=\pi_{1}(\overline{V},b)_{\mathbb{Q}},$$

the $\mathbb{Q}_{p}$-pro-unipotent fundamental group of $V$. For our gauge field $P$ we let

$$P(x)=\pi_{1}(\overline{V},b,x),$$ 

the $U$-torsor of pro-unipotent paths from $b$ to $x$.

Let $S$ be a finite set of primes. Let $H_{f}^{1}(\mathbb{Z}_{S},U)$ be the set of $U$-torsors over $\mathbb{Q}$ which are unramified outside $S$ and crystalline at $p$ (see [[p-adic Hodge theory]] for the meaning of crystalline). Similarly let $H^{1}(\mathbb{Q}_{p},U)$ be the set of $U$-torsors over $\mathbb{Q}_{p}$. We have a localization map

$$H_{f}^{1}(\mathbb{Z}_{S},U)\to\prod^{'}H^{1}(\mathbb{Q}_{v},U)$$

where the restricted product on the right means that all but finitely many of the components are unramified, and at $p$ the corresponding component is crystalline.

Recall that we are interested in $V(\mathbb{Q})$, the set of rational points of $V$. Now we have a map $A:V(\mathbb{Q})\to H_{f}^{1}(\mathbb{Z}_{S},U)$ given by

$$x\mapsto P(x).$$

where $P(x)=\pi_{1}(\overline{V},b,x)$ as above. This map fits into the diagram

$$
  \array{& V(\mathbb{Q}) & \rightarrow & V(\mathbb{Q}_{p}) & \\
          A & \downarrow &&\downarrow & A_{p} \\
          & H_{f}^{1}(\mathbb{Z}_{S},U) & \underset{loc_{p}}\rightarrow& H_{f}^{1}(\mathbb{Q}_{p},U) & 
}$$

Kim conjectures the following:

\begin{conjecture}
Suppose $V$ is a smooth projective curve of genus $g\geq 2$. Then
$$V(\mathbb{Q})=A_{p}^{-1}(Im(loc_{p})).$$
\end{conjecture}

## Relation to L-functions

## Related ideas

* [[gauge theory]]

* [[Mordell conjecture]]

* [[arithmetic Chern-Simons theory]]

## References

* {#Kim18} [[Minhyong Kim]], *Arithmetic Gauge Theory: A Brief Introduction*,  Modern Physics Letters A **33** 29 (2018) 1830012 &lbrack;[arxiv:1712.07602](https://arxiv.org/abs/1712.07602), [doi:10.1142/S0217732318300124](https://doi.org/10.1142/S0217732318300124)&rbrack;

* [[Minhyong Kim]], _Recent Progress on the Effective Mordell Problem_, lecture at the Sydney Mathematical Research Institute [YouTube](https://www.youtube.com/watch?v=NDQ_aO7QDEU)

* [[Minhyong Kim]], _Foundations of nonabelian Chabauty_, lectures at the Arizona Winter School 2020 [Slides1](https://swc-math.github.io/aws/2020/2020KimNotes1.pdf), [Slides2] (http://swc-alpha.math.arizona.edu/video/2020/2020KimLecture2Slides.pdf) [Slides3] (https://swc-math.github.io/aws/2020/2020KimNotes3.pdf) [Slides4] (https://swc-math.github.io/aws/2020/2020KimNotes4.pdf)

[[!redirects arithmetic gauge theories]]
