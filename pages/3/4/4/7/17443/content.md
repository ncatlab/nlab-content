#Contents#
* table of contents
{:toc}

## Idea

Essential [[sublocales]] are a generalization of [[locally connected geometric morphism|locally connected sublocales]].

## Definition

+-- {: .num_defn}
###### Definition
A [[sublocale]] $X_j$ of a [[locale]] $X$, given by a [[nucleus]] $j : \mathcal{O}(X) \to \mathcal{O}(X)$, is called *essential* (sometimes also *principal*) if and only if the following equivalent conditions are satisfied:

1. There is a monotone map $b : \mathcal{O}(X) \to \mathcal{O}(X)$ which is [[left adjoint]] to $j$.
2. The nucleus $j$ preserves arbitrary (not only finite) meets.
3. For any $u \in \mathcal{O}(X)$, there is a smallest $v \in \mathcal{O}(X)$ such that $u \preceq j(v)$.
4. The pullback functor $\mathrm{Sh}(X) \to \mathrm{Sh}(X_j)$ possesses a left adjoint (it always has a right adjoint).
5. The [[geometric embedding]] $\mathrm{Sh}(X_j) \hookrightarrow \mathrm{Sh}(X)$ is an [[essential geometric morphism]].
=--

+-- {: .proof}
###### Proof of equivalence
* The equivalence of (1) and (2) is by the [[adjoint functor theorem]] for complete lattices, which furthermore gives an explicit formula for the left adjoint $b$, namely
$$ b(u) \coloneqq inf \{ v \in \mathcal{O}(X) \,|\, u \preceq j(v) \}. $$
This also shows the equivalence of (1) and (3).
* The equivalence of (4) and (5) is by definition.
* Recall that the pullback of the representable sheaf $Hom_{\mathcal{O}(X)}(\cdot,u)$ is $Hom_{\mathcal{O}(X)}(\cdot,j(u))$. Therefore [[continuous functor|continuity]] of the pullback functor translates to continuity of $j$. This shows that (4) implies (2).
* Conversely, assume (3). Then the explicit description of the pullback functor given below (which is valid under this assumption) shows that the pullback functor preserves arbitrary limits. By the adjoint functor theorem for Grothendieck toposes, statement (4) follows.
=--

+-- {: .num_remark}
###### Remark
The left adjoint $b$ automatically satisfies $b(u) \preceq u$, $b(b(u)) = u$, $j(b(u)) = j(u)$, and $b(j(u)) = b(u)$ for all $u \in \mathcal{O}(X)$. These relations follow from playing around with the adjunction.
=--


## Examples

* Any [[open sublocale]] is essential: The nucleus for an open sublocale is of the form $j = (u \rightarrow -)$. Its left adjoint is $b = (- \wedge u)$.

* More generally, any [[locally connected geometric morphism|locally connected sublocale]] is essential.


## Properties

* For a general sublocale $i : X_j \hookrightarrow X$ and a sheaf $\mathcal{F}$ on $X$, the pullback $i^{-1} \mathcal{F}$ is the [[sheafification]] of the presheaf
$$ u \mapsto \colim_{u \preceq j(v)} \mathcal{F}(v). $$
In the case that $X_j$ is an essential sublocale, this presheaf is simply given by the formula
$$ u \mapsto \mathcal{F}(b(u)) $$
and is already a sheaf, so sheafification is not necessary.

* A sublocale of the one-point locale is essential if and only if it is [[open morphism|open]]. This is because the extra [[Frobenius reciprocity]] condition demanded by openness is automatically satisfied (in classical mathematics and in impredicative [[constructive mathematics]]).

* The lattice of essential sublocales of a given locale is [[complete lattice|complete]]. Suprema are calculated as in the lattice of all sublocales; infima, however, are not. There are counterexamples in ([Kelly and Lawvere (1989)](#KL89)), however in the slightly different context of essential [[localizations of categories]].
 

## In the internal language

Let $X_j \hookrightarrow X$ be a sublocale. From the [[internal language|internal point of view]] of the [[topos]] $Sh(X)$, this sublocale looks like a sublocale of the one-point locale and it's interesting to compare the properties of $X_j$ with this [[internal locale]].

+-- {: .num_prop}
###### Proposition
The following statements are equivalent:

1. $Sh(X) \models X_j \hookrightarrow 1 \,\text{is an essential sublocale}$.
2. $Sh(X) \models X_j \hookrightarrow 1 \,\text{is an open sublocale}$.
3. $X_j \hookrightarrow X$ is an open sublocale.

Note that none of these statements are equivalent to $X_j \hookrightarrow X$ being an essential sublocale.
=--


## References

* {#KL89}[[G. M. Kelly]], [[F. W. Lawvere]], _On the complete lattice of essential localizations_, Bull. Soc. Math. de Belgique **XLI** (1989) pp. 261&#8211;299.

* Guilherme Frederico Lima, _[From essential inclusions to local geometric morphisms](https://www.youtube.com/watch?v=YsoGN91Rh_s)_, talk at Topos &#224; l'IH&#201;S in September 2015.


## Related concepts

* [[essential subtopos]]

* [[essential geometric morphism]]