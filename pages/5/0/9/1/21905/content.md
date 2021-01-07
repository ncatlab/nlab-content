
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea


The [[Adams operations]] $\psi^k$ on [[complex topological K-theory]] are compatible with the [[Chern character map]] to [[rational cohomology]] in that the effect of $\psi^k$ on the Chern character image in degree $2r$ is multiplication by $k^r$.


## Statement

+-- {: .num_defn #AdamsLikeOperationsOnRationalCohomology}
###### Definition
**(Adams-like operations on [[rational cohomology]])**

For $X$ a [[topological space]], with [[rational cohomology]] in even degrees denoted 

$$
  H^{ev}(X;\, \mathbb{Q})
  \;\colon\;
  \underset{r \in \mathbb{N}}{\prod}
  H^{2 r}(X;\, \mathbb{Q})
$$

define graded [[linear maps]]

$$
  \psi^k_{H} \;\colon\; H^{ev}(X) \longrightarrow H^{ev}(X)
$$

for $k \in \mathbb{N}$ by taking their restriction to degree $2r$ to act by multiplication with $k^r$:


\[
  \label{AdamsOperationOnOrdinaryCohomologyInDegree2r}
  \array{
    H^{2r}(X;\mathbb{Q})
    &\overset{\;\;\;\psi^k_H\;\;\;}{\longrightarrow}&
    H^{2r}(X;\mathbb{Q})
    \\
    \alpha_{2k} &\mapsto& k^{r} \cdot \alpha_{2k}
    \,.
  }
\]


=--

+-- {: .num_prop #AdamsOperationsAreCompatibleWithTheChernCharacter }
###### Proposition
**([[Adams operations compatible with the Chern character]])**

For $X$ a [[topological space]] with a finite [[CW-complex]]-[[mathematical structure]], the [[Chern character]] $ch$ on the [[complex topological K-theory]] of $X$ intertwines the [[Adams operations]] $\psi^n$ on K-theory with the Adams-like operations $\psi^n_H$ on [[rational cohomology]] from Def. \ref{AdamsLikeOperationsOnRationalCohomology}, for $k \geq 1$, in that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    K(X)
      &\overset{\;\;\;ch\;\;\;}{\longrightarrow}&
    H^{ev}(X;\,\mathbb{Q})
    \\
    {}^{ \mathllap{ \psi^k } }
    \big\downarrow
    &&
    \big\downarrow
    {}^{ \mathrlap{ \psi^k_H } }
    \\
    K(X)
      &\underset{\;\;\;ch\;\;\;}{\longrightarrow}&
    H^{ev}(X;\,\mathbb{Q})
    \,,
  }
$$

=--

([Adams 62, Thm. 5.1. (vi)](#Adams62), review in [Karoubi 78, Chapter V, Theorem 3.27](#Karoubi78), [Maakestad 06, Thm. 4.9](#Maakestad06))

+-- {: .proof}
###### Proof idea

Use the exponentional-formula for the [[Chern character]] with the  [[splitting principle]].

=--

## Related entries

* [[e-invariant]]



## References

The original statement:

* {#Adams62} [[John Adams]], Theorem 5.1 (vi) _Vector fields on spheres_, Bull. Amer. Math. Soc. Volume 68, Number 1 (1962), 39-41 ([euclid:bams/1183524456](https://projecteuclid.org/euclid.bams/1183524456), [pdf](https://www.math.ens.fr/~benoist/refs/Adams.pdf))

Textbook accounts:

* {#Karoubi78} [[Max Karoubi]], Theorem V3.27 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007/978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))

Review and exposition:

* {#Maakestad06} Helge Maakestad, _Notes on the Chern-character_, Journal of Generalized Lie Theory and Applications, 2017, 11:1 ([arXiv:math/0612060](https://arxiv.org/abs/math/0612060), [doi:10.4172/1736-4337.100025](https://www.hilarispublisher.com/open-access/notes-on-the-cherncharacter-.pdf))


[[!redirects Adams operations are compatible with the Chern character]]
[[!redirects the Adams operations are compatible with the Chern character map]]

