#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The idea is that there should be some kind of "complete [[local ring]]" $\mathbb{Z}_\infty$ corresponding to the archimedean [[valuation]] on $\mathbb{Q}$, by analogy with the (genuine!) complete local rings $\mathbb{Z}_p$ corresponding to the (non-archimedean) $p$-adic valuations on $\mathbb{Q}$. However, the na&#239;ve approach taking
$$\mathbb{Z}_\infty = \lbrace x \in \mathbb{R} : -1 \le x \le 1 \rbrace$$
fails because this is not a subring of $\mathbb{R}$!

[[Nikolai Durov]]'s definition of $\mathbb{Z}_\infty$ is inspired by classical [[Arakelov geometry]] and starts with the observation that any $\mathbb{Z}_p$-lattice $\Lambda$ in a finite-dimensional $\mathbb{Q}_p$-[[vector space]] $E$ defines a maximal compact subgroup submonoid $M_\Lambda$ of $End(E)$, and $M_\Lambda = M_{\Lambda'}$ if and only if $\Lambda$ and $\Lambda'$ are similar lattices; accordingly, a $\mathbb{Z}_\infty$-lattice up-to-similarity should correspond to maximal compact submonoids of $End(E)$ for a finite-dimensional $\mathbb{R}$-vector space $E$, i.e. the monoid of $\mathbb{R}$-linear endomorphisms of $E$ that are [[short map|short]] with respect to some [[norm]] on $E$. Thus, Durov defines a $\mathbb{Z}_\infty$-lattice to be a finite-dimensional _normed_ $\mathbb{R}$-vector space, and a morphism of $\mathbb{Z}_\infty$ lattices is defined to be a [[short map|short]] $\mathbb{R}$-[[linear map]]. This gives a category $\mathbb{Z}_{\infty}\mathbf{\text{-Lat}}$ with finite limits and colimits. (Note, however, that it is not an additive category!)

Now, notice that every [[flat module|flat]] $\mathbb{Z}_p$-module is the [[filtered colimit]] of its finite-dimensional $\mathbb{Z}_p$-submodules (which are necessarily free because $\mathbb{Z}_p$ is a local ring), and in fact the category of flat $\mathbb{Z}_p$-modules is equivalent to the category of [[ind-object|ind-objects]] of $\mathbb{Z}_{p}\mathbf{\text{-Lat}}$. So we may define a flat $\mathbb{Z}_\infty$-module to be an ind-object of $\mathbb{Z}_{\infty}\mathbf{\text{-Lat}}$. One may also give the following explicit description: a flat $\mathbb{Z}_\infty$-module $E$ is a (possibly infinite-dimensional) $\mathbb{R}$-vector space $E_{\mathbb{R}}$ together with a symmetric convex body $E_{\mathbb{Z}_\infty}$, and a morphism $E \to E'$ is an $\mathbb{R}$-linear map $E_{\mathbb{R}} \to E'_{\mathbb{R}}$ that restricts to a map $E_{\mathbb{Z}_\infty} \to E'_{\mathbb{Z}_\infty}$. This defines a category $\mathbb{Z}_{\infty}\mathbf{\text{-FlMod}}$.

Finally, noting that the forgetful functor $U : \mathbb{Z}_{\infty}\mathbf{\text{-FlMod}} \to \mathbf{\text{Set}}$ taking a flat $\mathbb{Z}_\infty$-module $E$ to its underlying symmetric convex body $E_{\mathbb{Z}_\infty}$ has a [[left adjoint]] $F$, Durov defines a (not necessarily flat) $\mathbb{Z}_\infty$-module to be a [[module over a monad|module]] for the induced [[monad]] $\Sigma_\infty = U F$. The comparison functor embeds $\mathbb{Z}_{\infty}\mathbf{\text{-FlMod}}$ as a full subcategory of $\mathbb{Z}_{\infty}\mathbf{\text{-Mod}}$.

## Definition

Let $\Sigma_\infty : \mathbf{\text{Set}} \to \mathbf{\text{Set}}$ be the functor sending a set $S$ to the set
$$\left\lbrace \vec{v} \in \mathbb{R}^{(S)} : \left\| \vec{v} \right\|_1 = \sum_{s \in S} \left| v_s \right| \le 1 \right\rbrace$$
i.e. the solid regular cross-polytope with $S$-many vertices. The action of $\Sigma_\infty$ on maps of sets is the obvious one. Let $\eta : id \Rightarrow \Sigma_\infty$ be the natural transformation given by insertion of generators, and let $\mu : \Sigma_\infty \Sigma_\infty \Rightarrow \Sigma_\infty$ be the natural transformation given by "evaluation" of "octahedral" combinations:
$$\sum_i \alpha_i \eta \left( \sum_j \beta_{i,j} \eta (s_j) \right) \mapsto \sum_{i, j} \alpha_i \beta_{i, j} \eta (s_j)$$
One may verify that this defines a [[monad]] $(\Sigma_\infty, \eta, \mu)$ on $\mathbf{\text{Set}}$. A **$\mathbb{Z}_\infty$-module** is defined to be a [[module over a monad|module]] for this monad.

## Properties

The $\Sigma_\infty$ monad is a [[monad with arities]]: the category of arities may be taken to be $\mathbf{\text{FinSet}}$. 

The $\mathbb{Z}_\infty$-module structure on a set $M$ is entirely determined by the map $\alpha_2 : \Sigma_\infty (2) \times M^2 \to M$ given by $((\lambda_1, \lambda_2), (x_1, x_2)) \mapsto \lambda_1 x_1 + \lambda_2 x_2$. Conversely, a set $M$ together with an element $\alpha_0$ and a map $\alpha_2 : \Sigma_\infty (2) \times M^2 \to M$ satisfying certain equations is a $\mathbb{Z}_\infty$-module. A map commuting with $\alpha_0$ and $\alpha_2$ is a homomorphism of $\mathbb{Z}_\infty$-modules, thus the theory of $\mathbb{Z}_\infty$-modules is a finitary [[algebraic theory]], with all that this implies. 

The category $\mathbb{Z}_{\infty}\mathbf{\text{-Mod}}$ has the following properties:

* It is a [[complete category]] (with the forgetful functor creating all limits).

* It is a [[cocomplete category]] (with the forgetful functor creating all filtered colimits).

* It has a [[zero object]].

* It has a [[tensor product]] and an [[internal hom]], making it into a [[symmetric monoidal category|symmetric]] [[monoidal closed category]].

## Examples

Every normed $\mathbb{R}$-vector space $V$ induces a flat $\mathbb{Z}_\infty$-module $E$ where $E_{\mathbb{R}} = V$ and $E_{\mathbb{Z}_\infty} = \left\lbrace \vec{v} \in V : \left\| \vec{v} \right\| \le 1 \right\rbrace$. (In the other direction, every flat $\mathbb{Z}_\infty$-module induces a _seminorm_ on the underlying $\mathbb{R}$-vector space.)

A finitely-generated flat $\mathbb{Z}$-module is the symmetric convex hull of a finite set of vectors.

## References

* Durov, Nikolai (2007), _New approach to Arakelov theory_. Ph.D. thesis, [arXiv:0704.2030](http://arxiv.org/abs/0704.2030/).