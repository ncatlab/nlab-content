> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***
\linebreak

* [[André Coimbra]], [[Charles Strickland-Constable]], [[Daniel Waldram]]: *Supergravity as Generalised Geometry II: $E_{d(d)} \times \mathbb{R}^+$ and M theory* \[<a href="https://doi.org/10.1007/JHEP03(2014)019">doi:10.1007/JHEP03(2014)019</a>, [arXiv:1212.1586 hep-th](https://arxiv.org/abs/1212.1586)\]

* Paulo Pires Pacheco, [[Daniel Waldram]]: *M-theory, exceptional generalised geometry and superpotentials*, J. High Energy Physics **2008** JHEP09 (2008) \[<a href="https://doi.org/10.1088/1126-6708/2008/09/123">doi:10.1088/1126-6708/2008/09/123</a>, <a href="https://arxiv.org/abs/0804.1362">arXiv:0804.1362</a>\]


* [[André Coimbra]], [[Charles Strickland-Constable]], [[Daniel Waldram]]: *$E_{d(d)} \times \mathbb{R}^+$ Generalised Geometry, Connections and M theory*,  J. High Energ. Phys. **2014** 54 (2014) \[<a href="https://doi.org/10.1007/JHEP02(2014)054">doi:10.1007/JHEP02(2014)054</a>, <a href="https://arxiv.org/abs/1112.3989">arXiv:1112.3989 hep-th</a>\]





\linebreak

\linebreak



$$
  \left(
  \begin{matrix}
    A & B 
    \\
    0 & C
  \end{matrix}
  \right)
  \left(
  \begin{matrix}
    A^{-1}
    & 
    - A^{-1} B C^{-1}
    \\
    0 & C^{-1}
  \end{matrix}
  \right)
  =
  \begin{matrix}
    1 & 
    \\
  \end{matrix}
$$

+-- {: .num_theorem #TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}
###### Theorem

([Milne 2017, Propositions 3.24, 3.25](#Milne17)). Let $k$ be an algebraically closed field. The categories of affine varieties and affine $k$-algebras are [[dual equivalence|anti-equivalent]].

=--

The following result particularizes the [[schemes as sheaves on affine schemes#SchemesAsPresheaves|fundamental theorem on morphisms of schemes]] to prevarieties.

+-- {: .num_prop #PropositionSpmAndGammaAreMutuallyRightAdjoint}
###### Proposition

[Milne 2017, Propositions 5.11](#Milne17). Let $k$ be an algebraically closed field. Let $V$ be an algebraic $k$-prevariety. Let $A$ be an affine $k$-algebra. Then we have the following natural bijection:

$$
Hom(V,Spm(A))\cong Hom_{k\text{-algebra}}(A,\Gamma(V,\mathcal{O}_V)).
$$

=--

In other words, the maximal spectrum functor and the global sections functor, defined between the categories of affine $k$-algebras and $k$-prevarieties, are [[dual adjunction|mutually right adjoint]]. Note that Milne states the result for quasi-compact varieties, but his proof applies in the general case and never uses quasi-compactness nor separation. Note that from \ref{PropositionSpmAndGammaAreMutuallyRightAdjoint} we recover \ref{TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}.

See this table, 

|Header 1|Header 2|
|:--------:|:--------:|
|Item 1|Item 2|
|Item 3|Item 4|