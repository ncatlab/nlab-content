
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

An _EI-category_ is a [[category]] in which every [[endomorphism]] is an [[isomorphism]]. Given such a category, $C$, the set of isomorphism classes $[x]$ of objects $x$ in $C$ forms a [[poset]] under the relation $[x] \leq [y]$ if and only if there is a morphism $x \to y$.

Similarly an _EI $(\infty,1)$-category_ is an [[(∞,1)-category]] in which every [[endomorphism]] is an [[equivalence in an (∞,1)-category]].

## Examples

* A [[poset]]

* The [[path category]] of an acyclic [[quiver]]. 

* A group, $G$, understood as [delooped](group#delooping) to a pointed connected groupoid.

Let $\mathcal{S}$ be a set of subgroups of a group $G$.

*  The *transporter category* $\mathcal{T}_{\mathcal{S}}$ has as its objects the members of $\mathcal{S}$, and morphisms $Hom(H,K) = N_G(H,K) = \{g \in G|{}^{g}H \subseteq K\}$.

* The [[orbit category]] $\mathcal{O}_{\mathcal{S}}$ associated to $\mathcal{S}$ in which the objects are the coset spaces $G/H$ where $H \in S$ and the morphisms are the $G$-[[equivariance|equivariant]] mappings.

* The *Frobenius category*  $\mathcal{F}_{\mathcal{S}}$ has the elements of $\mathcal{S}$ as its objects, and $Hom_{\mathcal{F}_{\mathcal{S}}} = N_G(H,K)/C_G(H)$. The morphisms may be identified with the set of group homomorphisms $H \to K$ which are of the form 'conjugation by $g$' for some $g \in G$.

## Representation theory

A finite EI-category contains finitely many morphisms. The [[category algebra]] of a finite EI-category, $C$, for a fixed base ring $k$ is denoted $k C$ and has as basis the set of morphisms in $C$ with multiplication induced by composition of morphisms. It is thus a generalization of the [[group algebra]] of a finite group, the path algebra of a finite quiver without oriented cycles or the incidence algebra of a finite poset. There is a stratification of $k C$ of length equal to the number of isomorphism classes in the category.

The category of modules over the category algebra $k C$ is equivalent to the category of $k$-linear representations of $C$, i.e., the functor category $Fun(C, Mod k)$.

## Related concepts

* [[inverse EI (∞,1)-category]]

## References

* [[Peter Webb]], _Standard stratifications of EI categories and Alperin's weight conjecture_, ([doi](https://doi.org/10.1016/j.jalgebra.2006.03.052))

* [[Karsten Dietrich]], _Representation Theory of EI-categories_, ([pdf](https://d-nb.info/1007029781/34))

[[!redirects EI-categories]]

[[!redirects EI (∞,1)-categories]]
[[!redirects EI (∞,1)-category]]

