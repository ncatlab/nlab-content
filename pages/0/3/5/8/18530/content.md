
#Contents#
* table of contents
{:toc}

## Idea

The _scaling degree_ or _degree of divergence_ ([Steinmann 71](#Steinmann71)) or more generally the _degree_ ([Weinstein 78](#Weinstein78)) of a [[distribution]] on [[Cartesian space]] $\mathbb{R}^n$  is a measure for how it behaves at the origin $0 \in \mathbb{R}^n$ under rescaling $x \mapsto \lambda x$ of the canonical [[coordinates]]. 

The concept controls the problem of [[extension of distributions]] from the [[complement]] $\mathbb{R}^n \setminus \{0\}$ of the origin to all of $\mathbb{R}^n$. Such extensions are important notably in the construction of [[perturbative quantum field theories]] via [[causal perturbation theory]], where the freedom in the choice of such extensions models the [[renormalization]] freedom ("counter-terms") in the construction.

## Definition

+-- {: .num_defn #SheavesOnCartSp}
###### Definition

Let $n \in \mathbb{N}$. For $\lambda \in (0,\infty) \subset \athbb{R}$ a [[positive number|positive]] [[real number]] and $u \in \mathcal{D}'(\mathbb{R}^n)$ a [[distribution]] on [[Cartesian space]] $\mathbb{R}^n$ the _rescaled distribution_ 

$$
  u_\lambda
  \;\in\;
  \mathcal{D}'(\mathbb{R}^n)
$$

is given as a [[generalized function]] by

$$
  u_\lambda(x) \coloneqq u(\lambda x)
$$

hence as a [[continous linear function]] on [[bump functions]] by

$$
  \array{
     \mathcal{D}(\mathbb{R}^n) 
       &\overset{ \leangle  u_\lambda, - \rangle}{\longrightarrow}&
     \mathbb{R}
     \\
     b &\mapsto& \lambda^{-n} \langle u , b(\lambda^{-1}\cdot (-))\rangle
  }
  \,.
$$




=--

## References

The concept is due to 

* {#Steinmann71} O. Steinmann, _Perturbation Expansions in Axiomatic Field Theory_, volume 11 of Lecture Notes in Physics, Springer, Berlin Springer Verlag, 1971.

and in more generality due to

* {#Weinstein78} [[Alan Weinstein]], _The order and symbol of a distribution_, Trans. Amer. Math. Soc. 241, 1&#8211;54 (1978).

Review includes

* Dorothea Bahns, Micha&#322; Wrochna, _On-shell extension of distributions_ ([arXiv:1210.5448](https://arxiv.org/abs/1210.5448))

[[!redirects scaling degree of distributions]]

[[!redirects degree of divergence of a distribution]]
[[!redirects degree of divergence of distributions]]

[[!redirects degree of a distribution]]
[[!redirects degree of distributions]]
