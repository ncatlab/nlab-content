

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Statement

For $n \in \mathbb{N}$, let $A \in Mat_{n+1 \times n +1}(\mathbb{C})$ be a [[hermitian matrix]] (for instance a [[symmetric matrix]] of all entries are [[real numbers]]). 

Then for every [[principal submatrix]] $B \in Mat_{n \times n }(\mathbb{C})$, obtained by deleting the $i$th column and the $i$th row from $A$, for some $i \in \{1,\cdots, n+1\}$, the [[eigenvalues]] 
$(b_1 \leq b_2 \leq \cdots b_n)$ 
of $B$ *interlace* the eigenvalues
$(a_1 \leq a_2 \leq \cdots a_{n+1})$ of $A$, in that

$$
  a_1 
    \;\leq\;
  b_1
    \;\leq\;
  a_2
    \;\leq\;
  b_2
    \;\leq\;
  \cdots
    \;\leq\;
  b_n
    \;\leq\;
  a_{n+1}  
  \,.
$$ 


## Related concepts

* [[principal submatrix]]

* [[Gershgorin circle theorem]]

## References

* Suk-Geun Hwang, *Cauchy's Interlace Theorem for Eigenvalues of Hermitian Matrices*, The American Mathematical Monthly Vol. 111, No. 2 (Feb., 2004), pp. 157-159 ([jstor:4145217](https://www.jstor.org/stable/4145217))


* Steve Fisk, *A very short proof of Cauchy's interlace theorem for eigenvalues of Hermitian matrices* ([arXiv:math/0502408](https://arxiv.org/abs/math/0502408))

See also:

* Wikipedia, *[Cauchy interlacing theorem](https://en.wikipedia.org/wiki/Min-max_theorem#Cauchy_interlacing_theorem)*

* Wikipedia, *[Poincaré separation theorem](https://en.wikipedia.org/wiki/Poincar%C3%A9_separation_theorem)*

[[!redirects Cauchy's interlace theorem]]
