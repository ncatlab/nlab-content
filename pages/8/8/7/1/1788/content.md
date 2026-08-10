> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.




***

Problematic content from elsewhere:

## On the geometric realization of a chain complex of $\mathbb{C}$-modules

Recall from the study of the [[Dold-Kan correspondence]] that there is a [[Quillen equivalence]] $\Gamma : Ch_\bullet^+ (\mathbb{C}\text{-mod}) \rightarrow (\mathbb{C}\text{-mod})^{\Delta^{op}}$ defined by 

$$
(\Gamma C)_n = \bigoplus_{k \in \{0, ..., n \}, \alpha : \{ 0, ..., n \} \twoheadrightarrow \{ 0, .., k \} } C_k
$$

and from the study of [[geometric realization]] of simplicial sets that the geometric realization functor $| - | :  (\mathbb{C}\text{-mod})^{\Delta^{op}} \rightarrow \text{Top}$ is a [product-preserving](https://ncatlab.org/nlab/show/geometric+realization#TopologicalRealizationPreservesFiniteProducts) Quillen equivalence. 

The functor $\Gamma$ also preserves products, as can be seen directly from its formula. Indeed, since for each $n \in \mathbb{N}$ and each $k \in \{0,...,n \}$, there are only finitely many surjections $\alpha : \{ 0, ..., n \} \twoheadrightarrow \{ 0, .., k \}$, there is an isomorphism

$$
\Gamma(C \times D)_n \cong \Gamma(C)_n \times \Gamma(D)_n
$$

for each $n \in \mathbb{N}$

A Hermitian form on the realization $|\Gamma(V_*)|$ of a [[chain complex]] of $\mathbb{C}$-modules has the confounding property that, while such a form may result from the [geometric realization](https://ncatlab.org/nlab/show/geometric+realization#OfSimplicialSets)
$$
|\Gamma(V_*)| \times |\Gamma(V_*)|  \stackrel{\cong}{\rightarrow} | \Gamma(V_*) \times \Gamma(V_*)| \stackrel{\cong}{\rightarrow} |\Gamma(V_*)| \times |\Gamma(V_*)| \stackrel{| \Gamma ( \langle - , - \rangle) | }{\rightarrow} |\Gamma(\mathbb{C})| \stackrel{\simeq}{\rightarrow} \mathbb{C}_{disc}
$$ 
of a [differential-graded](https://ncatlab.org/nlab/show/tensor+product+of+chain+complexes) [bilinear form](https://ncatlab.org/nlab/show/bilinear+form#from_ab_to_monoidal_categories) $\langle -, - \rangle : V_* \otimes V_* \rightarrow \mathbb{C}$, even one with trivial differentials, the coincidence of the resulting topology on the topological $\mathbb{C}_{disc}$-vector space $|\Gamma(V_*)|$ with its topology as a Hilbert-space would imply the existence of a [[deformation retract]] onto the point $\{ 0 \}$ occurring as the restriction of the realization of the scalar function $|\Gamma(\mathbb{C})|  \times |\Gamma(V_*)| \rightarrow |\Gamma(V_*)|$. 

In the case that $V_*$ has nonzero chain-homology outside of degree $0$, this is impossible due to the identity $\pi_*(|\Gamma(V_*)|) \simeq H_*(V_*)$, even though the contractible analytic topology on $|\Gamma(V_*)|$ can of course be restored from the Hermitian form itself.




***

