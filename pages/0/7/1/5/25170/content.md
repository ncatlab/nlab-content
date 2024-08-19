
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a [[commutative ring]] $R$, $R$ is **reduced** or has a **trivial nilradical** if $x \cdot x = 0$ implies that $x = 0$ for all $x \in R$. 

\begin{theorem}
For every natural number $n$, $x^{n + 1} = 0$ implies that $x = 0$ for all $x \in R$.
\end{theorem}

\begin{proof}
Let the function $f:\mathbb{N} \to \mathbb{N}$ be defined as the [[ceiling]] of half of $n$, $f(n) \coloneqq \lceil n/2 \rceil$. Then $x^{n + 1} = 0$ implies that $x^{f(n + 1)} = 0$, and for every natural number $n$, the $(n + 1)$-th iteration of the function $f$ evaluated at $n + 1$ is always equal to $1$, $f^{n + 1}(n + 1) = 1$, thus resulting in $x^{f^{n + 1}(n + 1)} = x = 0$. Thus, the nilradical of $R$ is trivial. 
\end{proof}

As a result, the theory of a reduced ring is a [[coherent theory]]. 

## Properties

* Every [[integral domain]] is a reduced ring. Thus, every field is a reduced ring. 

* An example of a reduced ring which is not an [[integral domain]] is the quotient ring $R[x, y]/(x \cdot y)$. 

* Given a [[square-free integer]] $n$, the [[integers modulo n]] $\mathbb{Z}/n\mathbb{Z}$ is a reduced ring. Since for every integer $n$,  $\mathbb{Z}/n\mathbb{Z}$ is a [[prefield ring]], $\mathbb{Z}/n\mathbb{Z}$ is an [[integral domain]] and thus a [[field]] if and only if $n$ is a [[prime number]]. 

* Given a [[discrete field]] $F$, let $\overline{F}$ denote its [[algebraic closure]]. Given a [[square-free polynomial]] $q \in \overline{F}[x]$, the [[quotient ring]] $\overline{F}[x]/q\overline{F}[x]$ is a reduced ring. Since for every polynomial $q \in \overline{F}[x]$, $\overline{F}[x]/q\overline{F}[x]$ is a [[prefield ring]], $\overline{F}[x]/q\overline{F}[x]$ is an [[integral domain]] and thus a [[field]] if and only if $q$ is a prime polynomial in $\overline{F}[x]$, a [[monic polynomial]] of degree one; the resulting quotient ring is equivalent to $\overline{F}$.  

## See also

* [[radical]]

* [[reduction modality]]

| [[commutative ring]] | [[reduced ring]] | [[integral domain]] |
---------------------|-----------------|-----------------|
| [[local ring]] | [[reduced local ring]] | [[local integral domain]] |
| [[Artinian ring]] | [[semisimple ring]] | [[field]] |
| [[Weil ring]] | [[field]] | [[field]] |

## References

* Wikipedia, [Reduced ring](https://en.wikipedia.org/wiki/Reduced_ring)

[[!redirects reduced ring]]
[[!redirects reduced rings]]

[[!redirects reduced algebra]]
[[!redirects reduced algebras]]

[[!redirects trivial nilradical]]
[[!redirects trivial nilradicals]]
