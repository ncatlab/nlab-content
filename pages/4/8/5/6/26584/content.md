
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given that the (shifted, reduced) [[topological K-theory]] group of a [[topological space]] $X$ can be computed as a [[colimit]] over [[mapping space|mapping spaces]] 

$$
\tilde{K}^1 (X) = \text{Top}(X,U) = \text{lim}_{\to n}  \text{Top}(X,U(n)),
$$

one may think of it as a [[stabilization]] of [[nonabelian cohomology]] theories $U_n (X)$ whose classifying spaces are the [[unitary group|unitary groups]] $U(n)$. For this reason, we may call the groups $[X,U(n)]$ the **unstable** $\tilde{K}^1$-theory groups of $X$.

## Definition

+-- {: .num_defn #UnstableKGroups}
###### Definition

Let $X$ be a topological space, and $U(n)$ the unitary group. The *unstable* $n$ $\tilde{K}^1$*-theory group* $U_n (X)$ of $X$ is defined as the connected components of the mapping space $[X,U(n)]$:

$$
U_n (X) := \pi_0 [X,U(n)]
$$

=--

From this definition one can see that, if $X$ is a finite-dimensional CW complex, $U_n(X)=\tilde{K}^1 (X)$ for sufficiently large $n$.

## Properties

The following properties are proven in [Hamanaka and Kono 2003](#HK03):

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.1 of [op.cit.](#HK03)) Let $\text{dim}(X)\leq 2n$. Then there exists an [[exact sequence]]

$$
\tilde{K}^0 (X)\xrightarrow{\Theta} H^{2n} (X;\mathbb{Z}) \to U_n (X)\to \tilde{K}^1 (X) \to 1,
$$

or, put in a different way by defining $N_n (X):= \text{coker}(\Theta)$ (see Section 3 of [op.cit.](#HK03) for the definition of $\Theta$):

$$
1\to N_n (X) \to U_n (X)\to \tilde{K}^1 (X)\to 1
$$
=--
In particular, this proposition shows that in general $U_n (X)$ is neither abelian nor does it [[injection|inject]] into $\tilde{K}^1 (X)$.

+-- {: .num_defn #LimitToKtheory}
###### Proposition
(Theorem 1.2 of [op.cit.](#HK03)) For $\text{dim}(X)\leq 2n$, the cokernel group $N_n (X)$ is a finite abelian group where the order of any element divides $n!$.
=--

## Related concepts

* [[topological K-theory]]


## References

* {#HK03} Hiroaki Hamanaka, and [[Akira Kono]]. *On $[X, U(n)]$ when $\text{dim}(X)$ is $2n$.* Journal of Mathematics of Kyoto University. 43, no. 2 (2003): 333-348. ([doi](https://doi.org/10.1215/kjm/1250283730))

* Hiroaki Hamanaka, and [[Akira Kono]]. *An application of unstable K-theory.* Journal of Mathematics of Kyoto University 44, no. 2 (2004): 451-456. ([doi](https://doi.org/10.1215/kjm/1250283560))

* Hiroaki Hamanaka. *Adams $ e $-invariant, Toda bracket and $[X, U (n)] $.* Journal of Mathematics of Kyoto University 43, no. 4 (2003): 815-827. ([doi](https://doi.org/10.1215/kjm/1250281737))