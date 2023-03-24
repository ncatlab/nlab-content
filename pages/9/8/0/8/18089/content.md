+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An _EI-category_ is a [[category]] in which every [[endomorphism]] is an [[isomorphism]], hence an [[automorphism]].


Similarly an _EI $(\infty,1)$-category_ is an [[(∞,1)-category]] in which every [[endomorphism]] is an [[equivalence in an (∞,1)-category|equivalence]].

## Examples

* A [[poset]]

* The [[path category]] of an acyclic [[quiver]]. 

* A group, $G$, understood as [delooped](group#delooping) to a pointed connected [[groupoid]].

* A [[one-way category]], which is a category in which every endomorphism is an identity, is trivially an EI-category.

Let $\mathcal{S}$ be a set of [[subgroups]] of a [[group]] $G$. The following are all EI-categories ([Webb08, p. 4078](#Webb08)):

*  The *transporter category* $\mathcal{T}_{\mathcal{S}}$ has as its objects the members of $\mathcal{S}$, and morphisms $Hom(H,K) = N_G(H,K) = \{g \in G|{}^{g}H \subseteq K\}$.

* The [[orbit category]] $\mathcal{O}_{\mathcal{S}}$ associated to $\mathcal{S}$ in which the objects are the [[coset spaces]] $G/H$ where $H \in S$ and the morphisms are the $G$-[[equivariant functions]].

* {#FundamentalCategoryOfAGSpace} More generally: the [fundamental category of a $G$-space](orbit category#FundamentalCategoryOfAGSpace) is an EI-category.

* The *Frobenius category*  $\mathcal{F}_{\mathcal{S}}$ has the elements of $\mathcal{S}$ as its objects, and $Hom_{\mathcal{F}_{\mathcal{S}}} = N_G(H,K)/C_G(H)$. The morphisms may be identified with the set of group homomorphisms $H \to K$ which are of the form 'conjugation by $g$' for some $g \in G$.

## Properties

### General

EI-categories may be seen as those categories satisfying a  kind of [[Schröder–Bernstein theorem]].

\begin{proposition}
A category $C$ is EI if and only if every antiparallel pair $X \rightleftarrows Y$ exhibits a pair of isomorphisms.
\end{proposition}

\begin{proof}
Assume that $C$ is EI, and let $f \colon X \rightleftarrows Y : g$ be an antiparallel pair. Consider $X \xrightarrow{f} Y \xrightarrow{g} X \xrightarrow{f} Y$. Since isomorphisms have the [[2-out-of-6 property]], and $gf$ and $fg$ are isomorphisms, $f$ and $g$ are also isomorphisms. Conversely, suppose that $C$ satisfies the assumption of the proposition. Let $i \colon X \to X$ be an endomorphism. Then $i \colon X \rightleftarrows X : i$ exhibits exhibits an antiparallel pair, so in particular $i$ is an isomorphism.
\end{proof}

In particular, assuming [[excluded middle]], the [[Schröder–Bernstein theorem]] states that [[Inj]], the wide subcategory of [[Set]] spanned by [[monomorphisms]], is an EI-category.

### Partial ordering

Given an EI-category, $C$, the [[set]] of [[isomorphism classes]] $[x]$ of [[objects]] $x \in C$ forms a [[partially ordered set]] under the [[relation]] 

$$
  [x] \leq [y] 
  \phantom{AA} \text{if and only if}
  \phantom{AA} 
  \text{there is a morphism } x \to y
$$

### Representation theory

A finite EI-category contains finitely many morphisms. 

The [[category algebra]] $k C$ of a finite EI-category, $C$, for a fixed [[base ring]] $k$  and has as [[linear basis|basis]] the set of morphisms in $C$ with multiplication induced by composition of morphisms. It is thus a generalization of the [[group algebra]] of a [[finite group]], the [[path algebra]] of a finite [[quiver]] without oriented cycles or the [[incidence algebra]] of a finite poset. There is a stratification of $k C$ of depth equal to the number of isomorphism classes in the category.

The [[category of modules]] over the [[category algebra]] $k C$ is equivalent to the category of $k$-[[linear representations]] of $C$, i.e., the [[functor category]] $Fun(C, Mod k)$.

## Related concepts

* [[inverse EI (∞,1)-category]]

## References

Maybe the earliest explicit observation that in an [[orbit category]], and its relatives, *endomorphisms are automorphisms* is in:

* {#tomDieck1987} [[Tammo tom Dieck]], p. 73 of: *[[Transformation Groups]]*, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

Discussion in the context of [[algebraic K-theory]]:

* {#Lueck89} [[Wolfgang Lück]], _Transformation Groups and Algebraic K-Theory_, Lecture Notes in Mathematics **1408** (Springer 1989) ([doi:10.1007/BFb0083681](https://doi.org/10.1007/BFb0083681))

On the [[representation theory]] of EI-categories:

* {#Webb08} [[Peter Webb]], _Standard stratifications of EI categories and Alperin's weight conjecture_, Journal of Algebra
**320** 12 (2008) 4073-4091 ([doi:10.1016/j.jalgebra.2006.03.052](https://doi.org/10.1016/j.jalgebra.2006.03.052))

* Karsten Dietrich, _Representation Theory of EI-categories_, 2010 ([urn:nbn:de:hbz:466-20100701014](https://digital.ub.uni-paderborn.de/hsmig/content/titleinfo/1708), [pdf](https://d-nb.info/1007029781/34), [[Dietrich_EICategories.pdf:file]])

* Liping Li, *A generalized Koszul theory and its application*, Transactions of the American Mathematical Society **366** 2 (2014) 931-977 ([arXiv:1109.5760](https://arxiv.org/abs/1109.5760), [jstor:23812975](https://www.jstor.org/stable/23812975))

* Ergün Yalçın, *Projective resolutions over EI-categories*, 2012 ([hdl:11693/15472](http://hdl.handle.net/11693/15472))


[[!redirects EI-categories]]
[[!redirects EI category]]
[[!redirects EI categories]]

[[!redirects EI (∞,1)-categories]]
[[!redirects EI (∞,1)-category]]

