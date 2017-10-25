
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea

A [[categorification]] of the [[Dold-Kan correspondence]] appears in ([Dyckerhoff17](#Dyckerhoff17)), where [[Ab]], the [[category]] of [[abelian groups]], is replaced by the [[(∞,2)-category]] of [[stable (∞, 1)-categories]]. 

The [[equivalence]] between [[simplicial abelian groups]] and [[connective chain complex|connective]] [[chain complexes]] from the ordinary [[Dold-Kan correspondence]] becomes an equivalence between 2-simplicial stable (∞, 1)-categories and connective chain complexes of stable (∞, 1)-categories.

This should lead to a categorified version of [[homological algebra]] and of [[cohomology]], for example, through a categorified version of an [[Eilenberg-Mac Lane spectrum]]. 

## Categorified nerve functor

The [nerve](nerve#nerve_of_chain_complexes) in the ordinary Dold-Kan correspondence sends a connective chain complex in, $A$, an abelian category to a simplicial object in $A$. The categorified nerve, $\mathcal{N}$, is playing an analogous role on connective chain complexes of stable (∞, 1)-categories. This nerve unifies various known constructions from [[algebraic K-theory]], in particular, for $\mathcal{B}, \mathcal{B}_0, \mathcal{B}_1$ all stable (∞, 1)-categories:

* For $\mathcal{B}[1]$, the chain complex concentrated in degree 1, $\mathcal{N}(\mathcal{B}[1])$ is a $(\infty,1)$-version of the [[Waldhausen S-construction]].

* For $f: \mathcal{B}_1 \to \mathcal{B}_0$, then applying $\mathcal{N}$ to the corresponding chain complex concentrated in degrees $0$ and $1$ is a relative $(\infty,1)$-version of the Waldhausen S-construction.

* For the chain complex concentrated in degree $2$, $\mathcal{N}(\mathcal{B}[2])$ is an $(\infty,1)$-version of Hesselholt-Madsen's $S^{2,1}_{\bullet}$-construction. (See the reference at [[real algebraic K-theory]].)

* For the chain complex concentrated in degree $k$, $\mathcal{N}(\mathcal{B}[k])$ can be seen as a categorification of the [[Eilenberg-Mac Lane space]] $N(B[k])$.

## Related concepts

* [[Waldhausen S-construction]]
* [[real algebraic K-theory]]


##References

* {#Dyckerhoff17} [[Tobias Dyckerhoff]], _A categorified Dold-Kan correspondence_ ([arXiv:1710.08356](https://arxiv.org/abs/1710.08356))