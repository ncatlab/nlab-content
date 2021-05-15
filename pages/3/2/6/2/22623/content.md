
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *hook length formula* counts the [[number]] of [[semistandard Young tableaux|(semi-)]][[standard Young tableaux]] with fixed underlying [[Young diagram]]. 

In the case of [[standard Young tableau]] this number is also equal to the [[dimension]] of the [[irreducible representation]] of the [[symmetric group]] $Sym(n)$ corresponding to $\lambda$, a [[partition]] of $n$ (the [[Specht module]], see at *[[representation theory of the symmetric group]]*).

## Preliminaries

Given a [[Young diagram]], the *hook* at any one of its boxes is the collection of boxes to the right and below that box, and including the box itself. We write "$\ell hook_\lambda$" for the *length* of such a hook, i.e. for the number of boxes it contains. Formally:

\begin{defn}\label{HookLength}
**(hook length)** \linebreak
Let $\lambda = (\lambda_1 \geq \cdots \geq \lambda_{rows(\lambda)})$ be a [[partition]]/[[Young diagram]]. Then for 

* $i \in \{1, \cdots, rows(\lambda)\}$,

* $j \in \{1, \cdots, \lambda_i\}$

the *hook length* at $(i,j)$ is

$$
  \ell hook_\lambda(i,j)
  \;\coloneqq\;
  1 +
  (\lambda_i - j) + (\lambda'_j - 1)
  \,,
$$

where $\lambda'$ denotes the *conjugate partition* (see [there](Young+diagram#Conjugation)).

\end{defn}

\begin{definition}
**(numbers of (semi-)standard Young tableaux)** \linebreak
Given a [[partition]] $\lambda \in Part(n)$, and a [[positive number|positive]] [[natural number]] $N \in \mathbb{N}_+$, consider

* the number of [[standard Young tableaux]]:

  \[
    \label{NumberOfStandardYoungTableauxOfFixedShape}
    \left\vert sYTableaux_\lambda\right\vert
    \;\in\;
    \mathbb{N}_+
  \]

* the number of [[standard Young tableaux]] with bounded entries $T_{i j} \leq N$:

  \[
    \label{NumberOfSemiStandardYoungTableauxOfFixedShape}
    \left\vert ssYTableaux_\lambda(N)\right\vert
    \;\in\;
    \mathbb{N}_+
  \]

of shape $\lambda$.
\end{definition}


## Details


### For standard Young tableaux

\begin{prop}
**(hook length formula for standard Young tableaux)** \linebreak
Given a [[partition]] ([[Young diagram]]) $\lambda$ of $n$ (boxes), the number (eq:NumberOfStandardYoungTableauxOfFixedShape) of [[standard Young tableaux]] of shape $\lambda$ equals the [[factorial]] of $n$ over the [[multiplication|product]] of the hook lengths (Def. \ref{HookLength}) at all the boxes of $\lambda$:

$$
  \left\vert 
    sYTableaux_\lambda
  \right\vert
    \;=\; 
  \frac{
    n!  
  }{
    \prod_{(i,j)} \ell hook_\lambda(i,j)
  }.
$$

\end{prop}

### For semi-standard Young tableaux
 {#ForSemiStandardYoungTableaux}

\begin{prop}
**(hook length formula for semi-standard Young tableaux)** \linebreak
Given 

  * a [[partition]] ([[Young diagram]]) $\lambda$ of $n$ (boxes), 

  * a [[positive number|positive]] [[natural number]] $N \in \mathbb{N}_+$, 

the number (eq:NumberOfSemiStandardYoungTableauxOfFixedShape) of semi-standard Young tableaux of shape $\lambda$ and entries $\leq N$ ([hence](semistandard+Young+tableau#eq:RelationToSchurPolynomialsOfFinitelyManyVariables) the value of the [[Schur polynomial]] $s_\lambda(x_1, \cdots, x_N)$ at $x_i = 1$) is:

$$
  \left\vert
    ssYTableaux_\lambda(N)
  \right\vert
  \;=\;
  s_\lambda
  \big(
    \underset{
      \mathclap{
        N\; arguments
      }
    }{
    \underbrace{
      1, \cdots, 1
    }
    }
  \big)
    \;=\; 
  \underset{(i,j)}{\prod}
  \frac{
    N - i + j
  }{
    \ell hook_\lambda(i,j)
  }
  \,.
$$

\end{prop}


## Related concepts

* [[hook-content formula]]

## References

Review:

* [[Yufei Zhao]], _Young Tableaux and the Representations of the Symmetric Group_ ([pdf](https://yufeizhao.com/research/youngtab-hcmr.pdf), [[ZhaoYoungTableaux.pdf:file]])

See also:

* Wikipedia, *[Hook length formula](https://en.wikipedia.org/wiki/Hook_length_formula)*

[[!redirects hook length formulas]]

[[!redirects hook-length formula]]
[[!redirects hook-length formulas]]


