
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
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

Where a linear [[persistence module]], as traditionally considered in [[persistent homology theory]], is a [[diagram]] of [[vector space]]/[[modules]] of the directed form

\begin{tikzcd}[column sep=small]
  \cdots
  \ar[r]
  &
  V_1
  \ar[r]
  & 
  V_2
  \ar[r]
  &
  V_3
  \ar[r]
  & 
  V_4
  \ar[r]
  & 
  \cdots
  \,,
\end{tikzcd}

in a *zig-zag persistence module* one allows the [[linear maps]] to go in either direction, such as in regular [[zigzags]]

\begin{tikzcd}[column sep=small]
  \cdots
  \ar[r]
  &
  V_1
  \ar[from=r]
  & 
  V_2
  \ar[r]
  &
  V_3
  \ar[from=r]
  & 
  V_4
  \ar[r]
  & 
  \cdots
  \,,
\end{tikzcd}

or in more general zigzags such as

\begin{tikzcd}[column sep=small]
  \cdots
  \ar[from=r]
  &
  V_1
  \ar[from=r]
  & 
  V_2
  \ar[r]
  &
  V_3
  \ar[from=r]
  & 
  V_4
  \ar[r]
  & 
  \cdots
  \,,
\end{tikzcd}

In the language of [[quiver theory]], zigzag persistence modules are precisely the [[quiver representations]] of [[ADE-classification|A-type]] [[quivers]]. But in [[quiver representation theory]] the classical [[Gabriel's theorem|Gabriel theorem]] says (see [there](Gabriel's+theorem#ATypeQuivers)) that for all possible zig-zag patterns as above the [[indecomposable object|indecomposable]] [[quiver representations]] are still "interval modules", ie. those for which the $V_i$ are [[zero object|zero]] except in some [[interval]] where they are [[dimension of a vector space|1-dimensional]] and connected by ([[zigzags]] of) [[identity maps]].

This means that the key property of [[persistence modules]] -- namely that they are entirely characterized by [[persistence barcodes]], i.e. by [[multisets]] of such intervals -- immediately generalizes to zigzag persistence modules.

A typical type of a zigzag persistence module appearing in the practice of [[topological data analysis]] consists of [[homology groups]] $H(X_i)$ of stages $\cdots \hookrightarrow X_{i - 1} \hookrightarrow X_i \hookrightarrow X_{i + 1} \hookrightarrow \cdots$ of a [[filtered topological space]], as usual, but evaluating now on the [[zigzag]] of inclusions into the [[unions]] 

\begin{tikzcd}
  &
  X_i \cup X_j
  \ar[from=dr, hook', "{\iota_j^r}"{swap}]
  \\
  X_i
  \ar[ur, hook, "{\iota_i^l}"]
  &
  &
  X_j
\end{tikzcd}

of consecutive filter stages: 

\begin{tikzcd}[column sep=small]
  \cdots
  \ar[from=dr, hook']
  &
  &
  H(X_i \cup X_{i+1})
  \ar[from=dr, hook', "{H(\iota_{i+1}^r)}"{swap}]
  &
  &
  H(X_{i+1} \cup X_{i+2})
  \ar[from=dr, hook', "{H(\iota_{i+2}^r)}"{swap}]
  &
  & 
  \cdots
  \\
  &
  H(X_i)
  \ar[ur, hook, "{H(\iota_i^l)}"]
  &
  &
  H(X_{i+1})
  \ar[ur, hook, "{H(\iota_{i+1}^l)}"]
  &
  &
  H(X_{i+2})
  \ar[ur, hook]
  & 
\end{tikzcd}

It is claimed (...) that such zigzag persistence modules still retain the same persistent information of interest, but are more robust.

## References

The concept of zigzag persistence modules as a tool in [[topological data analysis]] and their relation to [[quiver representation theory]] (including a re-proof of [[Gabriel's theorem]] for the case of A-type quivers) is due to:

* {#CarlssonDeSilva10} [[Gunnar Carlsson]], [[Vin de Silva]], *Zigzag Persistence*, Found Comput Math **10** (2010) 367–405 $[$[arXiv:0812.0197](https://arxiv.org/abs/0812.0197), [doi:10.1007/s10208-010-9066-0](https://doi.org/10.1007/s10208-010-9066-0)$]$

Application to [[level sets]]:

* [[Gunnar Carlsson]], [[Vin de Silva]], [[Dmitriy Morozov]], *Zigzag persistent homology and real-valued functions*, in: *SCG '09: Proceedings of the twenty-fifth annual symposium on Computational geometry (2009) 247–256 $[$[doi:10.1145/1542362.1542408](https://doi.org/10.1145/1542362.1542408)$]$

* [[Gunnar Carlsson]], [[Vin de Silva]], [[Sara Kališnik]], [[Dmitriy Morozov]], *Parametrized Homology via Zigzag Persistence*, Algebr. Geom. Topol. **19** (2019) 657-700 $[$[arXiv:1604.03596](https://arxiv.org/abs/1604.03596), [doi:10.2140/agt.2019.19.657](https://doi.org/10.2140/agt.2019.19.657)$]$



Review:

* [[Steve Y. Oudot]], *Persistence Theory: From Quiver Representations to Data Analysis*, Mathematical Surveys and Monographs **209** AMS (2015)
$[$[pdf](https://geometrica.saclay.inria.fr/team/Steve.Oudot/books/o-pt-fqrtda-15/surv-209.pdf), [ISBN:978-1-4704-3443-4](https://bookstore.ams.org/surv-209/)$]$


[[!redirects zigzag persistence modules]]

[[!redirects zig-zag persistence module]]
[[!redirects zig-zag persistence modules]]

[[!redirects zigzag persistence]]
