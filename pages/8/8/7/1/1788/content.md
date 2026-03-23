
> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak

***



# Donsker–Varadhan nonequilibrium correction

## Idea

Given an irreducible continuous-time Markov chain at stationarity, the Hessian of the [[Donsker–Varadhan rate function]] splits into a detailed-balance part and a remainder. The remainder — the **nonequilibrium correction** — measures how much the chain's fluctuation structure exceeds that of its reversibilisation.

The result below shows that in reduced [[Fisher information metric|Fisher coordinates]] this correction factors exactly as a Gram operator built from the skew part of the generator. The factorisation follows from completing a quadratic form in the Donsker–Varadhan variational envelope.

## Definitions

Let $Q$ be the generator of an irreducible continuous-time [[Markov chain]] on $\{1,\dots,n\}$ with stationary distribution $\pi$, so $\pi_i \gt 0$ for all $i$ and $\pi Q = 0$.

**Fisher-conjugated generator.** Set $D_\pi = \mathrm{diag}(\pi_1,\dots,\pi_n)$ and define

$$L_\pi \;=\; D_\pi^{1/2}\, Q\, D_\pi^{-1/2}.$$

In components, $(L_\pi)_{ij} = \sqrt{\pi_i}\, Q_{ij} / \sqrt{\pi_j}$.

**Euclideanised tangent space.** Set $e_\pi = (\sqrt{\pi_1},\dots,\sqrt{\pi_n})^T$. The Euclideanised Fisher tangent space at $\pi$ is

$$T_\pi \;=\; \{u \in \mathbb{R}^n : \langle u, e_\pi \rangle = 0\}.$$

The orthogonal projector onto $T_\pi$ is $P_\pi = I - e_\pi e_\pi^T$. The space $T_\pi$ is $L_\pi$-invariant. After this change of variables the [[Fisher information metric]] at $\pi$ becomes the standard Euclidean inner product, so all orthogonality and adjointness below are Euclidean.

**Reduced coordinates.** Choose an orthonormal matrix $C \in \mathbb{R}^{n \times (n-1)}$ whose columns span $T_\pi$, so $C^T C = I_{n-1}$ and $C C^T = P_\pi$. Define the reduced Fisher-conjugated generator and its decomposition by

$$\widehat{K} = C^T L_\pi\, C, \qquad \widehat{G} = \tfrac{1}{2}(\widehat{K} + \widehat{K}^T), \qquad \widehat{J} = \tfrac{1}{2}(\widehat{K} - \widehat{K}^T).$$

Here $\widehat{G}$ is the reduced dissipative backbone (symmetric, negative definite) and $\widehat{J}$ is the reduced skew channel (skew-symmetric). The chain satisfies [[detailed balance]] if and only if $\widehat{J} = 0$.

**Donsker–Varadhan Hessian.** The [[large deviation theory|Donsker–Varadhan rate function]] for the empirical measure is

$$I_{DV}(\mu) \;=\; \sup_{h}\Bigl(-\sum_{i,j} \mu_i\, Q_{ij}\,(e^{h_j - h_i} - 1)\Bigr)$$

with $I_{DV}(\pi) = 0$. Its Hessian at $\pi$ in reduced Fisher coordinates is the positive-definite $(n{-}1) \times (n{-}1)$ matrix $H_{DV}$.

**Detailed-balance Hessian.** The canonical detailed-balance reference is the chain with Fisher-conjugated generator equal to the symmetric part $\widehat{G}$. Its reduced Donsker–Varadhan Hessian is

$$H_0 \;=\; -\tfrac{1}{2}\,\widehat{G}.$$

This is positive definite (since $\widehat{G}$ is negative definite on the reduced space).

**Nonequilibrium correction.**

$$\Delta_{DV} \;=\; H_{DV} - H_0.$$

## Statement

+-- {: .num_theorem #BridgeTheorem}
###### Theorem (Dunkley 2025)

In reduced Euclidean Fisher coordinates at $\pi$,

$$\Delta_{DV} \;=\; \tfrac{1}{4}\;\widehat{J}\;H_0^{-1}\;\widehat{J}^{\,T}.$$

=--

+-- {: .proof}
###### Proof

Set $S = -\widehat{G}$, so $S$ is positive definite and $H_0 = \frac{1}{2}S$. The reduced Donsker–Varadhan envelope expanded to second order in reduced Fisher coordinates $x$ and reduced logarithmic coordinates $y$ gives

$$\mathcal{L}(x,y) = -y^T S\, y + x^T(S + \widehat{J})\,y + O(3)$$

using $\widehat{K} = \widehat{G} + \widehat{J} = -S + \widehat{J}$ and the fact that $y^T \widehat{J}\,y = 0$ for skew-symmetric $\widehat{J}$. Completing the square in $y$:

$$\mathcal{L}(x,y) = -\Bigl(y - \tfrac{1}{2} S^{-1}(S + \widehat{J})x\Bigr)^T S \Bigl(y - \tfrac{1}{2} S^{-1}(S + \widehat{J})x\Bigr) + \tfrac{1}{4}\, x^T (S + \widehat{J})^T S^{-1} (S + \widehat{J})\, x + O(3).$$

Supremising over $y$:

$$I_{DV}(\mu(x)) = \tfrac{1}{4}\, x^T (S + \widehat{J})^T S^{-1}(S + \widehat{J})\, x + O(|x|^3).$$

Since $\widehat{J}^T = -\widehat{J}$:

$$(S + \widehat{J})^T S^{-1}(S + \widehat{J}) = (S - \widehat{J})S^{-1}(S + \widehat{J}) = S - \widehat{J}\,S^{-1}\widehat{J} = S + \widehat{J}\,S^{-1}\widehat{J}^T.$$

Therefore $I_{DV}(\mu(x)) = \frac{1}{4} x^T(S + \widehat{J}\,S^{-1}\widehat{J}^T)\,x + O(|x|^3)$. Since $I_{DV}(\mu(x)) = \frac{1}{2} x^T H_{DV}\, x + O(|x|^3)$, we get

$$H_{DV} = \tfrac{1}{2} S + \tfrac{1}{2}\widehat{J}\,S^{-1}\widehat{J}^T.$$

Now $H_0 = \frac{1}{2}S$ and $H_0^{-1} = 2S^{-1}$, giving

$$\Delta_{DV} = H_{DV} - H_0 = \tfrac{1}{2}\widehat{J}\,S^{-1}\widehat{J}^T = \tfrac{1}{4}\widehat{J}\,H_0^{-1}\widehat{J}^T.$$

=--

### Signal operator form

Writing $A_{DV} = \frac{1}{2}\,\widehat{J}\,H_0^{-1/2}$, the correction takes [[Gram matrix]] form:

$$\Delta_{DV} = A_{DV}\,A_{DV}^T.$$

## Consequences

**Positivity and rank.** Since $\Delta_{DV} = A_{DV} A_{DV}^T$, positivity is manifest. Because $H_0$ is invertible, $\mathrm{rank}(\Delta_{DV}) = \mathrm{rank}(\widehat{J})$.

**Detailed-balance characterisation.** The following are equivalent: (1) the chain satisfies [[detailed balance]]; (2) $\widehat{J} = 0$; (3) $\Delta_{DV} = 0$.

**Optimal rank-$d$ observation.** The maximum trace of $\Delta_{DV}$ retained by any rank-$d$ orthogonal projection is $\frac{1}{4}\sum_{k=1}^{d} \sigma_k^2$, where $\sigma_1 \geq \cdots \geq \sigma_r \gt 0$ are the nonzero singular values of $A_{DV}$. This is a direct application of the [[Eckart–Young–Mirsky theorem]].

**Vanishing criterion.** The nonequilibrium correction is invisible to a rank-$d$ observer if and only if the observer's subspace is orthogonal to the top $d$ left singular vectors of $A_{DV}$.

## Related entries

* [[Donsker–Varadhan rate function]]

* [[Fisher information metric]]

* [[detailed balance]]

* [[Markov chain]]

* [[singular value decomposition]]

* [[Ky Fan norm]]

* [[large deviation theory]]

* [[information geometry]]

* [[entropy production]]

## References

* {#Dunkley2025} J. R. Dunkley, _Finite Observation of Nonequilibrium Markov Chains: Spectral Theory, Ky Fan Envelopes, and Detectability_, preprint (2025). ([doi:10.5281/zenodo.19102609](https://doi.org/10.5281/zenodo.19102609))

Background:

* {#DonskerVaradhan1975} M. D. Donsker, S. R. S. Varadhan, _Asymptotic evaluation of certain Markov process expectations for large time_, Communications on Pure and Applied Mathematics **28** (1975) 1–47.

* {#Fan1951} K. Fan, _Maximum properties and inequalities for the eigenvalues of completely continuous operators_, Proc. Nat. Acad. Sci. **37** (1951) 760–766.

