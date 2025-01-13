
\tableofcontents

## Definition

Given two [[A-set|$\mathcal{A}$-sets]] $A$ and $B$, the **cartesian product** $A \times B$ of $A$ and $B$ is given by an $\mathcal{A}$-set structure on the underlying [[product type]] $A \times B$ defined by 

$$(a, b) \sim_{A \times B} (c, d) \coloneqq (a \sim_A c) \wedge (b \sim_B d)$$

$$(a, b) \nsim_{A \times B} (c, d) \coloneqq (a \nsim_A c) \vee (b \nsim_B d)$$

Given a family of [[A-set|$\mathcal{A}$-sets]] $(B(x))_{x:A}$ indexed by a [[type]] $A$, the **indexed cartesian product** $\prod_{x:A} B(x)$ of $(B(x))_{x:A}$ is given by an $\mathcal{A}$-set structure on the underlying [[dependent product type]] $\prod_{x:A} B(x)$ defined by 

$$c \sim_{\prod_{x:A} B(x)} d \coloneqq \forall x:A.c(x) \sim_{B(x)} d(x)$$

$$c \nsim_{\prod_{x:A} B(x)} d \coloneqq \exists x:A.c(x) \nsim_{B(x)} d(x)$$

## Related concepts

* [[A-set]]

* [[cartesian product]]

* [[tensor product of A-sets]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects cartesian product of A-sets]]
[[!redirects cartesian products of A-sets]]

[[!redirects cartesian product of affine sets]]
[[!redirects cartesian products of affine sets]]

[[!redirects cartesian product of antithesis sets]]
[[!redirects cartesian products of antithesis sets]]

[[!redirects indexed cartesian product of A-sets]]
[[!redirects indexed cartesian products of A-sets]]

[[!redirects indexed cartesian product of affine sets]]
[[!redirects indexed cartesian products of affine sets]]

[[!redirects indexed cartesian product of antithesis sets]]
[[!redirects indexed cartesian products of antithesis sets]]

[[!redirects dependent cartesian product of A-sets]]
[[!redirects dependent cartesian products of A-sets]]

[[!redirects dependent cartesian product of affine sets]]
[[!redirects dependent cartesian products of affine sets]]

[[!redirects dependent cartesian product of antithesis sets]]
[[!redirects dependent cartesian products of antithesis sets]]