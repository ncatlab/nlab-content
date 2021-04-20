
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

This page shows the [[Cayley graph]] of the [[symmetric group]] on $3$ elements, $Sym(3)$ and makes explicit some of its properties.

In all of the following we abbreviate [[permutations]] of 3 elements as 

$$
  i j k 
  \;\coloneqq\;
  \left(
    \array{
      1 & 2 & 3
      \\
      i & j & k
    }
  \right)
  \,.
$$


## Definition


The following shows the [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent), hence whose [[graph distance]] is the [[Cayley distance]]:

\begin{tikzcd}[row sep=-6pt, column sep=14pt]
  123
  \ar[rrrr,-]
  \ar[ddddd,-]
  \ar[ddrrr,-]
  &&
  &&
  132
  \ar[ddddd,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  &&&
  \scalebox{.8}{$321$}
  \ar[dddr,-]
  \\
  &
  \scalebox{1.2}{231}
  \ar[ddl,-]
  \ar[uuurrr,-, crossing over]
  \ar[urr,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  213
  \ar[rrrr,-]
  &&&&
  312
\end{tikzcd}

## Properties

### Cayley distance
 {#CayleyDistance}

If we order the 6 elements of $Sym(3)$ as

$$
  \vec \sigma
  \;\coloneqq\;
  \left[
  \array{
    123
    \\
    213
    \\
    132
    \\
    321
    \\
    312
    \\
    231
  }
  \right]
$$

then the [[Cayley distance]], regarded as a $6 \times 6$ [[matrix]]

$$
  [d_C]
  \;\coloneqq\;
  \big(
  d_C
  \big( 
    \sigma_i, \sigma_j
  \big)
  \big)_{i,j}
  \;\in\;
  Mat_{6 \times 6}(\mathbb{N})
$$

is

\[
  \label{ExplicitCayleyDistanceMatrix}
  [d_c]
  \;=\;
  \left[
  \array{
    0 & 1 & 1 & 1  & 2 &  2
    \\
    1 & 0 & 2 & 2 & 1 & 1
    \\
    1 & 2 & 0 & 2 & 1 & 1
    \\
    1 & 2 & 2 & 0 & 1 & 1 
    \\
    2 & 1 & 1 & 1 & 0 & 2 
    \\
    2 & 1 & 1 & 1 & 2 & 0
  }
  \right]
\]

### Cayley distance kernel

For $\lambda \in \mathbb{R}_+$, write

\[
  \label{CayleyDistanceKernel}
  \big[
    e^{- \lambda \cdot d_C}
  \big]
  \;\in\;
  Mat_{6 \times 6}(\mathbb{R})
\]

for *Cayley distance [[kernel method|kernel]]* on $Sym(3)$, hence the [[matrix]] which is the [[exponential]] of the [[Cayley distance]]-matrix (eq:ExplicitCayleyDistanceMatrix) multiplied by $- \lambda$.


The [[eigenvalues]] of this matrix are (from [here](https://www.wolframalpha.com/input/?i=eigenvalues++exp%5B+-+ln%5Blambda%5D+*++%7B++%7B0%2C1%2C1%2C1+%2C2%2C+2%7D%2C+%7B1%2C+0+%2C+2%2C+2%2C+1%2C+1%7D%2C+%7B1%2C+2%2C+0%2C+2%2C+1%2C+1%7D%2C+%7B1%2C2%2C+2%2C0%2C1%2C+1+%7D%2C+%7B2%2C+1%2C+1%2C+1%2C+0%2C+2+%7D%2C+%7B2%2C1%2C1%2C1%2C2%2C0%7D++%7D+%5D))

$$
  \frac
    {
      e^ {2\lambda} -1 
    }
    {e^ {2\lambda}}  
  \,,\;\;\;
  \frac
    {
      e^{2\lambda} \pm 3 e^{\lambda}  + 2 
    }
    {e^{2\lambda}}  
  \,,
$$

where the first one appears with multiplicity 4 and is positive since $\lambda$ is positive. The only eigenvalue that can become non-positive for $\lambda \in \mathbb{R}_+$ is:

$$
  e^2\lambda - 3 e^\lambda + 2
  \;\;is\;\;
  \left\{
  \array{
    \lt 0 &\vert& \lambda \lt ln(2)
    \\
    = 0 &\vert& \lambda = ln(2)
    \\
    \gt 0 &\vert& \lambda \gt ln(2)
  }
  \right.
$$

In conclusion:

The [[Cayley distance kernel]] (eq:CayleyDistanceKernel), regarded as a [[bilinear form]] on the [[linear span]] $\mathbb{R}[Sym(3)]$ is:

$$
  \array{
    \text{indefinite} & \text{for} & \lambda \lt ln(2)
    \\
    \text{positive semi-definite} &\text{for}& \lambda = ln(2)
    \\
    \text{positive definite} &\text{for}&  \lambda \gt ln(2)
  }
$$

## References

See the references at:

* [[geometric group theory]]

* [[Cayley graph]]

* [[Cayley distance]]

* [[Cayley distance kernel]]



[[!redirects Cayley distance on Sym(3)]]

[[!redirects Cayley distance kernel on Sym(3)]]

