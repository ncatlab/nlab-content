



#Contents#
* table of contents
{:toc}

## Definition

A *semistandard Young tableau* is a [[Young tableaux]] such that its values are:

1. weakly increasing to the right (along rows),

1. strictly increasing downwards (along columns).

## Examples

For example:

$$
\array{
  1 & 1 & 1 & 3
  \\
  2 & 3
  \\
  4
}
$$

## Properties

### Relation to Schur polynomials


Given a [[semistandard Young tableau]] $T$, we write $X^T$ for  the [[monomial]] which contains one factor of the [[variable]] $x_k$ for each occurrence of $k$ in the Young tableau: 

\[
  \label{MonomialAssociatedWithSemistandardYoungTableau}
  x^T
  \;\coloneqq\;
  x_1^{\#1s}
  x_1^{\#2s}
  \cdots
  \,.
\]

We write 

$$
  ssYT(\lambda)
$$

for the set of semistandard Youn tableaux whose underlying [[partition]] (i.e. forgetting its labels) is $\lambda$.

\begin{prop}
  For $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, the corresponding Schur polynomial $s_\lambda$ is equal to the [[sum]] over the [[monomials]] (eq:MonomialAssociatedWithSemistandardYoungTableau) associated with all [[semistandard Young tableau]] of shape $\lambda$:

$$
  s_\lambda
  \;\;=\;\;
  \underset{
    {T \in ssYT(\lambda)},
  }{\sum}
  x^T
  \,.
$$
\end{prop}


([Sagan 01, Def. 4.4.1](#Sagan01), review in [Sagan Enc., p. 1](#SaganEnc))





## References

Textbook account:

* {#Sagan01} [[Bruce Sagan]], Def. 2.9.5 of: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

Survey in the context of [[Schur functions]]:

* {#SaganEnc} [[Bruce E. Sagan]], _Schur functions_, in: [[Michiel Hazewinkel]] (ed.), *[[eom|Encyclopaedia of Mathematics]]*, Springer 2002 ([pdf](http://www.mth.msu.edu/~sagan/Papers/Old/schur.pdf), [[SaganSchurFunctions.pdf:file]])


See also the references at *[[Young tableau]]*.

