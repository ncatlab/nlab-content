+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea ##
One of the central theorems in [[(∞,1)-category theory]] is the fully faithfulness of the Rezk nerve 
\[
\begin{aligned}
    \mathsf{Cat}_{(\infty,1)}&\to \mathsf{sAn},\\
 C&\mapsto ([n]\mapsto \operatorname{Map}([n]),C),
\end{aligned}
\]
where $\mathsf{sAn}$ is the [[(∞,1)-category]] of simplicial [[animae]].

The mapping anima $\operatorname{Map}([n]),C)$ is simply the subcategory of the functor [[(∞,1)-category]] $\operatorname{Fun}([n],C)$ consisting of [[equivalences]]. 

The relative Rezk nerve replaces equivalences by maps in a prescribed [[wide subcategory]] $W\subset C$ and gives an alternative presentation of the [[localization of an (∞,1)-category]] of $C$. (See [below](#thm:MGloc))

## Definition ##
Let $C$ be an [[(∞,1)-category]] and $W\subset C$ be a wide sub [[(∞,1)-category]]. The *relative Rezk nerve* of $(C,W)$ is the simplicial anima $N^{\mathrm{rel}}(C,W)$ given by
\[
 [n] \mapsto |\operatorname{Fun}([n],C)\times_{C^{n+1}} W^{n+1}|,
\]
where $|-|:\mathsf{Cat}_{(\infty,1)}\to \mathsf{An}$ is the left adjoint to the inclusion. 

Relative Rezk nerve was introduced by Rezk in [Rezk01, Section 3](#Rezk01) under the name *classification diagram*.

## Properties ##
One of the fundamental property of relative Rezk nerve is that its associated [[(∞,1)-category]] computes [[localization of an (∞,1)-category]]:
\begin{theorem} 
\label{thm:MGloc}
For every [[(∞,1)-category]] $C$ and every [[wide subcategory]] $W\subset C$, we have
\[
\mathrm{ac}\circ N^{\mathrm{rel}}(C,W) \simeq C[W^{-1}],
\]
where $\mathrm{ac}\colon \mathsf{sAn}\to \mathsf{Cat}_{(\infty,1)}$ denotes the left adjoint to the Rezk nerve (computing *associated ($\infty$,1)-category*).
\end{theorem}
This was first established by Mazel-Gee in [MG19](#MG19). Shorter proofs are in [Ara23](#Ara23) and [AC25](#AC25). In special cases, Rezk proved a version of this theorem when $(C,W)$ is part of a simplicial model category in [Rez01, Theorem 8.3](#Rez01); Bergner proved this for model categories in [Ber09, Theorem0.2](#Ber09).

Another fundamental property of the relative Rezk nerve is that its [[Segalification]] admits an explicit presentation:
\begin{theorem} 
The [[Segalification]] of $N^{\mathrm{rel}}(C,W)$ can be described in terms of zig-zags in $C$ in which one is allowed to go backward only via maps in $W$.

The mapping animae of the Segalification agrees (or generalizes) with the one appearing in [[hammock localization]]. ([AC26, Theorems A and B](#AC26))
\end{theorem}


## Related concepts

* [[localization of an (∞,1)-category]]


## References

**Classical references:**

* {#Rez01} [[Charles Rezk]], *A model for the homotopy theory of homotopy theory*, Trans. Amer. Math. Soc. **353** (2001), no. 3, 973–1007 ([arXiv:math/9811037](https://arxiv.org/abs/math/9811037), [doi:10.1090/S0002-9947-00-02653-2](https://doi.org/10.1090/S0002-9947-00-02653-2)).

* {#Ber09} [[Julia E. Bergner]], *Complete Segal spaces arising from simplicial categories*, Trans. Amer. Math. Soc. **361** (2009), no. 1, 525–546 ([arXiv:0704.1624](https://arxiv.org/abs/0704.1624)), [doi:10.1090/S0002-9947-08-04616-3](https://doi.org/10.1090/S0002-9947-08-04616-3)

**Relation to [[localization of an (∞,1)-category]]:**

* {#MG19} [[Aaron Mazel-Gee]], *The universality of the Rezk nerve*, Algebr. Geom. Topol. **19** (2019), no. 7, 3217–3260 ([arXiv:1510.03150](https://arxiv.org/abs/1510.03150), [doi:10.2140/agt.2019.19.3217](https://doi.org/10.2140/agt.2019.19.3217)).

* {#AC25} [[Kensuke Arakawa]], [[Bastiaan Cnossen]], *A short proof of the universality of the relative Rezk nerve*, Proc. Amer. Math. Soc. **154** (2026), no. 5, 1849–1853 ([arXiv:2505.14123](https://arxiv.org/abs/2505.14123), [doi:10.1090/proc/17483](https://doi.org/10.1090/proc/17483)).

* {#Ara23} [[Kensuke Arakawa]], *Classification diagrams of marked simplicial sets* (2023), [arXiv:2311.01101](https://arxiv.org/abs/2311.01101) [math.AT].

[AC25](#AC25) offers a rather "model-agnostic" viewpoint, while [Ara23](#Ara23) offers a generalization using [[quasicategories]].

**Relation to [[hammock localization]]:**

* {#AC26} [[Kensuke Arakawa]], [[Bastiaan Cnossen]], *Hammock localization via Segal animae* (2026), [arXiv:2608.19870](https://arxiv.org/abs/2608.19870) [math.CT].

**A generalization to [[dendroidal complete Segal spaces]]:**

* {#ACP26} [[Kensuke Arakawa]], [[Victor Carmona]], [[Francesca Pratali]], *Relative dendroidal Rezk nerve and applications* (2026), [arXiv:2606.11895](https://arxiv.org/abs/2606.11895) [math.AT].

[[!redirects classification diagram]]
[[!redirects Rezk classification diagram]]