
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
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



## Statement

[[Gabriel's theorem]] ([Gabriel 72](#Gabriel72)) says that connected [[quivers]] with a [[finite number]] of [[indecomposable object|indecomposable]] [[quiver representations]] over an [[algebraically closed field]] are precisely the _[[Dynkin quivers]]_: those whose [[underlying]] [[undirected graph]] is a [[Dynkin diagram]] in the [[ADE classification|ADE series]].

Moreover, the [[indecomposable object|indecomposable]] [[quiver representations]] in this case are in [[bijection]] with the [[positive number|positive]] [[root (in representation theory)|roots]] in the [[root system]] of the [[Dynkin diagram]]. 

## Examples

In the following we write $\mathbb{K}$ for the given [[ground field]] (typically $\mathbb{K} = \mathbb{C}$ the [[complex numbers]], but much of the following works for general fields, eg. $\mathbb{K} = \mathbb{R}$ the [[real numbers]] or $\mathbb{K} = \mathbb{F}_p$ a [[finite field]]).

Given a [[quiver]] $Q$ and a [[quiver representation]] $\rho$, we denote for any [[edge]] $v \xrightarrow{\;e\;} v'$ in $Q_1$ the corresponding value of $\rho$ by

\begin{tikzcd}[column sep = small, row sep=small]
  v
  \ar[r, "{e}"]
  &
  v'
  \\
  V_e
  \ar[r, "{ \rho(e) }"]
  &
  V_{e'}
\end{tikzcd}

### A-type quivers
  {#ATypeQuivers}

For $n \in \mathbb{N}_+$ consider the $\mathbb{A}_{n}$-quiver, hence with this underlying undirected graph:

\begin{tikzcd}[column sep = small, row sep=small]
  1 
  \ar[r, -]
  &
  2
  \ar[r, -]
  &
  3
  \ar[r,-]
  &
  \cdots
  \ar[r,- ]
  &
  n
\end{tikzcd}

\begin{example}
\label{IndecomposableRepsOfAn}
The [[indecomposable object|indecomposable]] [[quiver representations]] of $\mathbb{A}_n$ are labeled by [[pairs]] $a,b \in \mathbb{N}^2$ with $1 \leq a \lt b \leq n$ and are given as follows (see also [Carlsson & de Silva 2010](#CarlssonDeSilva10), reviewed in [Oudot 15, p. 17](#Oudot15)):

\begin{tikzcd}[column sep = small, row sep=small]
  1
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  (a-1)
  \ar[r,-]
  &
  a
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  b
  \ar[r,-]
  &
  (b+1)
  \ar[r,-]
  &
  \cdots
  \ar[r,-]
  &
  n
  \\
  \mathbb{K}^0
  \ar[r, -, "{0}"]
  &
  \cdots
  \ar[r, -, "{0}"]
  &
  0
  \ar[r,-, "{0}"]
  &
  \mathbb{K}^1
  \ar[r,-, "{\mathrm{id}}"]
  &
  \cdots
  \ar[r,-, "{\mathrm{id}}"]
  &
  \mathbb{K}^1
  \ar[r,-,"{0}"]
  &
  \mathbb{K}^0
  \ar[r,-,"{0}"]
  &
  \cdots
  \ar[r,-,"{0}"]
  &
  \mathbb{K}^0
\end{tikzcd}

for any given [[orientation]] of the [[edges]].

So for instance if the quiver is the *linear* $\mathbb{A}_n$-quiver

\begin{tikzcd}[column sep = small, row sep=small]
  1 
  \ar[r]
  &
  2
  \ar[r]
  &
  3
  \ar[r]
  &
  \cdots
  \ar[r]
  &
  n
\end{tikzcd}

then its indecomposable representations are of this form:

\begin{tikzcd}[column sep = small, row sep=small]
  1
  \ar[r]
  &
  \cdots
  \ar[r]
  &
  (a-1)
  \ar[r]
  &
  a
  \ar[r]
  &
  \cdots
  \ar[r]
  &
  b
  \ar[r]
  &
  (b+1)
  \ar[r]
  &
  \cdots
  \ar[r]
  &
  n
  \\
  \mathbb{K}^0
  \ar[r, "{0}"]
  &
  \cdots
  \ar[r, "{0}"]
  &
  0
  \ar[r, "{0}"]
  &
  \mathbb{K}^1
  \ar[r, "{\mathrm{id}}"]
  &
  \cdots
  \ar[r, "{\mathrm{id}}"]
  &
  \mathbb{K}^1
  \ar[r, "{0}"]
  &
  0
  \ar[r, "{0}"]
  &
  \cdots
  \ar[r, "{0}"]
  &
  0
\end{tikzcd}
\end{example}

\begin{remark}
\label{RelationToPersistencyModules}
Example \ref{IndecomposableRepsOfAn} is of key relevance in the discussion of [[persistent homology]] (notably in [[topological data analysis]]): 
Here an $\mathbb{A}_n$-[[quiver representation]] is called a *[[zigzag persistence|zig-zag]] [[persistence module]]* and the statement of Ex. \ref{IndecomposableRepsOfAn} is interpreted as saying that every persistence module is spanned by elements which

* *appear* at some *resolution* $a$,

* *persist* across a range $b - a$,

* *disappear* at some resolution $b$.

The [[multiset]] of these [[pairs]] $(a,b)$ is then called the *[[barcode]]* or *[[persistence diagram]]* of the [[persistence module]].

This relation between quiver representation theory and persistent homolology was originally highlighted by [Carlsson & de Silva 2010](#CarlssonDeSilva10).
\end{remark}


## Related concepts

* [[ADE classification]]

* [[Dynkin quiver]], [[McKay quiver]]

## References

The result is due to 

* {#Gabriel72} [[Peter Gabriel]], _Unzerlegbare Darstellungen. I_, Manuscripta Mathematica 6: 71&#8211;103, (1972) $[$[doi:10.1007/BF01298413](https://link.springer.com/article/10.1007/BF01298413)$]$
 
Lecture notes:

* _Quiver representations and Gabriel's theorem_ ([pdf](https://www2.math.ethz.ch/education/bachelor/seminars/hs2009/clualg/Cluster-A5.pdf))

See also:

* Wikipedia, _[Gabriel's theorem](http://en.wikipedia.org/wiki/Gabriel%27s_theorem)_

Re-proof of Gabriel's theorem in the case of A-type quivers and relation to [[persistent homology]]:

* {#CarlssonDeSilva10} [[Gunnar Carlsson]], [[Vin de Silva]], *Zigzag Persistence*, Found Comput Math **10** (2010) 367–405 $[$[arXiv:0812.0197](https://arxiv.org/abs/0812.0197), [doi:10.1007/s10208-010-9066-0](https://doi.org/10.1007/s10208-010-9066-0)$]$

reviewed in:

* {#Oudot15} [[Steve Y. Oudot]], *Persistence Theory: From Quiver Representations to Data Analysis*, Mathematical Surveys and Monographs **209** AMS (2015)
$[$[ISBN:978-1-4704-3443-4](https://bookstore.ams.org/surv-209/), [pdf](https://geometrica.saclay.inria.fr/team/Steve.Oudot/books/o-pt-fqrtda-15/surv-209.pdf)$]$


[[!redirects Gabriel theorem]]
