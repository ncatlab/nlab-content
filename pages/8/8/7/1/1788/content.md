> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.




***


* [[Grigorios Giotopoulos]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Nesselwang 2026|Higher Superspace Supergravity & its IR Completions]]* &lbrack;[arXiv:2607.20312](https://arxiv.org/abs/2607.20312)&rbrack;



***

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

For additional information, look at this very related typing graph. 

$$\frac{\Gamma \vdash A ,; \Gamma \vdash B}{\Gamma \vdash A\times B}$$
