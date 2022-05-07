
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

Schur-Weyl duality is a relation between the [[finite-dimensional vector space|finite-dimensional]] [[irreducible representations]] of the [[general linear groups]] $GL(k)$ and of the [[symmetric group]] $Sym(n)$.

Concretely, for $k, n \in \mathbb{N}$ consider the $k \times n$-dimensional [[complex vector space]]; regarded as a [[tensor product of vector spaces|tensor product]] of $n$ copies of $\mathbb{C}^n$:

$$
  \underset{
    n \; tensor \; factors
  }{
    \underbrace{
      \mathbb{C}^k \otimes \cdots \otimes \mathbb{C}^k
    }
  }
  \;\;\;
  \in
  \;
  \mathbb{C}VectorSpaces
$$

As such, this carries 

* a canonical [[linear representation|linear]] [[group action]] by $GL(k) \coloneqq GL(k,\mathbb{C})$, namely the $n$-fold [[diagonal action]] of its defining action on $\mathbb{C}^k$ (its [[fundamental representation]]);

* a canonical [[linear representation|linear]] [[group action]] by $Sym(n)$ given by [[permutation]] of the $n$ tensor factors.

The statement of Schur-Weyl duality is that the decomposition of this [[linear representation]] of the [[direct product group]] $GL(k) \times Sym(n)$ decomposes as a [[direct sum]] of [[tensor product of vector spaces|tensor products]] of [[irreducible representations]] for either group, as follows:

$$
  \underset{
    n \; tensor \; factors
  }{
    \underbrace{
      \mathbb{C}^k \otimes \cdots \otimes \mathbb{C}^k
    }
  }
  \;\simeq\;
  \underset{
    {
    (\lambda_1 \geq \cdots \geq \lambda_k)
    }
    \atop
    {
    \underset{i}{\sum} \lambda_i = n
    }
  }{\oplus}
  D^{(\lambda)}
  \otimes
  S^{(\lambda)}
$$

Here the [[direct sum]] is indexed by [[partitions]] $\lambda$ of $n$ by $k$ [[positive number|positive]] summands, and $D^{(\lambda)}$ and $S^{(\lambda)}$ denote the [[irreducible representations]] of the [[general linear group]] and of the [[symmetric group]] ([[Specht modules]]), respectively, which are indexed by these according to the [[representation theory of the general linear group]] and the [[representation theory of the symmetric group]], respectively.


## Related concepts

* [[representation theory of the general linear group]]

* [[representation theory of the symmetric group]]

* [[Schur-Weyl measure]]

## References 

Review:

Textbook accounts:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], Section 6.1 of: _Representation Theory: a First Course_, Springer, Berlin, 1991 ([doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9))

* Ambar N. Sengupta, Section 10.2 of: *Representing Finite Groups -- A Semisimple Introduction*, Springer 2012 ([doi:10.1007/978-1-4614-1231-1](https://link.springer.com/book/10.1007/978-1-4614-1231-1))


In a context of [[quantum information theory]]:

* Jordi Tura i Brugués, *Schur-Weyl duality* ([pdf](https://link.springer.com/content/pdf/bbm%3A978-3-319-49571-2%2F1.pdf)), Appendix A in: *Characterizing Entanglement and Quantum Correlations Constrained by Symmetry*,  Springer Theses (2017) ([doi:10.1007/978-3-319-49571-2](https://link.springer.com/book/10.1007/978-3-319-49571-2))

See also

* Wikipedia, *[Schur-Weyl duality](https://en.wikipedia.org/wiki/Schur%E2%80%93Weyl_duality)*

In the [[AdS-CFT correspondence]]:

* [[Sanjaye Ramgoolam]], *Schur-Weyl duality as an instrument of Gauge-String duality*, AIPConf. Proc. 1031:255-265, 2008 ([arXiv:0804.2764](https://arxiv.org/abs/0804.2764))





[[!redirects Schur Weyl duality]]

