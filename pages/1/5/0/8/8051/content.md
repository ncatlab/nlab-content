#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The idea is that there should be some kind of "complete [[local ring]]" $\mathbb{Z}_\infty$ corresponding to the archimedean [[valuation]] on $\mathbb{Q}$, by analogy with the (genuine!) complete local rings $\mathbb{Z}_p$ corresponding to the (non-archimedean) $p$-adic valuations on $\mathbb{Q}$. However, the na&#239;ve approach taking
$$\mathbb{Z}_\infty = \lbrace x \in \mathbb{R} : -1 \le x \le 1 \rbrace$$
fails because this is not a subring of $\mathbb{R}$!

[[Nikolai Durov]]'s definition of $\mathbb{Z}_\infty$ is inspired by classical [[Arakelov geometry]] and starts with the observation that any $\mathbb{Z}_p$-lattice $\Lambda$ in a finite-dimensional $\mathbb{Q}_p$-[[vector space]] $E$ defines a maximal compact subgroup submonoid $M_\Lambda$ of $End(E)$, and $M_\Lambda = M_{\Lambda'}$ if and only if $\Lambda$ and $\Lambda'$ are similar lattices; accordingly, a $\mathbb{Z}_\infty$-lattice up-to-similarity should correspond to maximal compact submonoids of $End(E)$ for a finite-dimensional $\mathbb{R}$-vector space $E$, i.e. the monoid of $\mathbb{R}$-linear endomorphisms of $E$ that are [[short map|short]] with respect to some [[norm]] on $E$. Thus, Durov defines a $\mathbb{Z}_\infty$-lattice to be a finite-dimensional _normed_ $\mathbb{R}$-vector space, and a morphism of $\mathbb{Z}_\infty$ lattices is defined to be a [[short map|short]] $\mathbb{R}$-[[linear map]]. This gives a category $\mathbb{Z}_{\infty}\mathbf{\text{-Lat}}$ with finite limits and colimits. (Note, however, that it is not an additive category!)

Now, notice that every [[flat module|flat]] $\mathbb{Z}_p$-module is the [[filtered colimit]] of its finite-dimensional $\mathbb{Z}_p$-submodules (which are necessarily free because $\mathbb{Z}_p$ is a local ring), and in fact the category of flat $\mathbb{Z}_p$-modules is equivalent to the category of [[ind-object|ind-objects]] of $\mathbb{Z}_{p}\mathbf{\text{-Lat}}$. So we may define a flat $\mathbb{Z}_\infty$-module to be an ind-object of $\mathbb{Z}_{\infty}\mathbf{\text{-Lat}}$. One may also give the following explicit description: a flat $\mathbb{Z}_\infty$-module $E$ is a (possibly infinite-dimensional) $\mathbb{R}$-vector space $E_{\mathbb{R}}$ together with a symmetric convex body $E_{\mathbb{Z}_\infty}$, and a morphism $E \to E'$ is an $\mathbb{R}$-linear map $E_{\mathbb{R}} \to E'_{\mathbb{R}}$ that restricts to a map $E_{\mathbb{Z}_\infty} \to E'_{\mathbb{Z}_\infty}$. This defines a category $\mathbb{Z}_{\infty}\mathbf{\text{-FlMod}}$.

Finally, noting that the forgetful functor $U : \mathbb{Z}_{\infty}\mathbf{\text{-FlMod}} \to \mathbf{\text{Set}}$ taking a flat $\mathbb{Z}_\infty$-module $E$ to its underlying symmetric convex body $E_{\mathbb{Z}_\infty}$ has a [[left adjoint]] $F$, Durov defines a (not necessarily flat) $\mathbb{Z}_\infty$-module to be a [[module over a monad|module]] for the induced monad $\Sigma_\infty = U F$.

## Definition

(To follow shortly)