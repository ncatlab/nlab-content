
# $C(n)$-extendible cardinals
* table of contents
{:toc}

## Idea

A $C(n)$-extendible cardinal is a type of [[large cardinal]] which generalizes [[extendible cardinals]].  They come up in formulating refined versions of [[Vopěnka's principle]].

## Definition

We work in [[ZFC]].  Let $C(n)$ denote the class of infinite [[cardinal numbers]] $\kappa$ such that $V_\kappa$ (see [[von Neumann hierarchy]]) is a $\Sigma_n$-elementary submodel of the universe $V$, i.e. such that the embedding preserves and reflects the truth of $\Sigma_n$-[[Lévy hierarchy|formulas]].  In particular:

* $\kappa$ is $C(0)$ if and only if it is infinite, and

* $\kappa$ is $C(1)$ if and only if it is uncountable and $V_\kappa$ coincides with the *hereditarily $\kappa$-sized sets* $H(\kappa)$, i.e. those whose [[transitive closure]] has cardinality $\lt\kappa$.

+-- {: .un_defn}
###### Definition
If $\kappa\lt\lambda$ and both are in $C(n)$, we say $\kappa$ is **$\lambda$-$C(n)$-extendible** if there is an [[elementary embedding]] $j:V_\lambda \to V_\mu$ with critical point $\kappa$, such that $\mu\in C(n)$, $j(\kappa)\gt \lambda$, and $j(\kappa)\in C(n)$.

We say $\kappa\in C(n)$ is **$C(n)$-extendible** if it is $\lambda$-$C(n)$-extendible for all $\lambda\in C(n)$ with $\lambda\gt\kappa$.
=--

In particular:

* $\kappa$ is $C(0)$-extendible if and only if it is [[extendible cardinal|extendible]].


## References

* Joan Bagaria, [[Carles Casacuberta]], Adrian Mathias, [[Jiri Rosicky]] _Definable orthogonality classes in accessible categories are small_, [arXiv](http://arxiv.org/abs/1101.2792)
{#BagariaCasacubertaMathiasRosicky}

[[!redirects C(n)-extendible cardinals]]
