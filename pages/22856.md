#Contents#
* automatic table of contents
{:toc}

## Idea

A divided power algebra is an algebra $A$ together with an ideal $I$ and a collection of operations $\{\gamma_{n}\colon I\to A\}_{n\in\mathbb{N}}$ which behave like operations of taking divided powers $x\mapsto x^{n}/n!$ in power series.

## Definition

Let $R$ be a ring. A __divided power $R$-algebra__, or __PD-$R$-algebra__, is a triple $(A,I,\gamma)$ with

- $A$ an $R$-algebra;
- $I$ an ideal of $A$;
- $\gamma=\{\gamma_{n}\colon I\to A\}_{n\in\mathbb{N}}$ a collection of maps;

satisfying the following conditions:

1. For each $x\in A$, we have $\gamma_{0}(x)=1$.
2. For each $x\in A$, we have $\gamma_{1}(x)=x$.
3. For each $x\in A$ and each $n\geq2$, we have $\gamma_{n}(x)\in I$.
4. For each $x,y\in A$, we have
$$\gamma_{n}(x+y)=\sum_{k=0}^{n}\gamma_{n-k}(x)\gamma_{k}(y).$$
5. For each $\lambda$ in $A$ and each $x\in I$, we have
$$\gamma_{n}(\lambda x)=\lambda^{n}\gamma_{n}(x).$$
6. For each $x\in A$ and each $m,n\in\mathbb{N}$, we have
$$\gamma_{n}(x)\gamma_{m}(x)=\frac{(n+m)!}{n!m!}\gamma_{n+m}(x).$$
7. For each $x\in A$ and each $m,n\in\mathbb{N}$, we have
$$\gamma_{m}(\gamma_{n}(x))=\frac{(nm)!}{(n!)^{m}m!}\gamma_{nm}(x).$$

## Related concepts

* [[crystalline cohomology]]

## References

Divided power algebras were originally introduced in 

* [[Pierre Berthelot]], A. Ogus, _Notes on crystalline cohomology_, Princeton Univ. Press 1978. vi+243, ISBN0-691-08218-9

* [[Pierre Berthelot]], _Cohomologie cristalline des sch&#233;mas de caract&#233;ristique $g \gt 0$, Lecture Notes in Mathematics, Vol. 407, Springer- Verlag, Berlin, 1974. MR 0384804

* de Jong et al. The Stacks Project, [Chapter 09PD](https://stacks.math.columbia.edu/tag/09PD).

[[!redirects PD-algebra]]
[[!redirects divided power structure]]