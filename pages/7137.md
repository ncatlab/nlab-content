
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _local Langlands conjectures_ are certain [[conjectures]] in the context of the [[Langlands program]]. Where the genuine [[Langlands correspondence]] concerns [[global fields]], the local Langlands correspondence concerns [[local fields]].

In the case of the [[algebraic group]] $GL_n$, the local Langlands conjectures assert a correspondence between F-semisimple Weil-Deligne [[representations]] of the [[Weil group]] of a  [[local field]] $F$ and irreducible admissible [[representations]] of $GL_n(F)$, generalizing  local [[class field theory]] from [[abelian group|abelian]] [[Galois groups]] to non-abelian Galois groups.

More generally, it states that for a local field $F$ and a reductive group $G$, the isomorphism classes of irreducible admissible representations of $G(F)$ are partitioned into _L-packets_ by the equivalence classes of _L-parameters_.

##Important definitions:

Let $F$ be a $p$-adic field.

A representation of $G(F)$ on a vector space $V$ is *irreducible* if the only $G(F)$-invariant subspaces are $0$ and $V$.

A representation of $G(F)$ on a vector space $V$ is *admissible* if for any open subgroup $U$ of $G(F)$ the fixed subspace $V^{U}$ is finite-dimensional.

Let $\kappa$ be the residue field of $F$. The *Weil group* $W_F$ is the subgroup of $\mathrm{Gal}(\overline{F}/F)$ defined as the inverse image of $\mathrm{Frob}^{\mathbb{Z}}\subset \mathrm{Gal}(\overline{\kappa}/\kappa)$ under the surjective map $\mathrm{Gal}(\overline{F}/F)\to\mathrm{Gal}(\overline{\kappa}/\kappa)$.

A *Weil-Deligne representation* is a pair $(\rho_{0},N)$ where $\rho_{0}:W_{F}\to GL_{n}(\mathbb{C})$ is a representation of the Weil group and $N$ is a nilpotent _monodromy operator_ satisfying $\rho_{0}(\sigma)N\rho_{0}(\sigma)^{-1}=\Vert\sigma\Vert N$ for all $\sigma\in W_{F}$, where $\Vert\sigma\Vert$ is the valuation of the corresponding element of $F^{\times}$ under the isomorphism of local class field theory.

## Example: The local Langlands correspondence for $GL_1$

Let $F$ be a $p$-adic field. The only irreducible admissible representations of $GL_1(F)$ ($=F^\times$) are continuous group homomorphisms $\chi:F^\times\to\mathbb{C}^{\times}$. The $1$-dimensional Weil-Deligne representations $(\rho_{0},N)$ of $W_F$ must have monodromy operator $N=0$ and must factor through the abelianization $W_F^{\mathrm{ab}}$. The local Langlands correspondence in this case is the same as local class field theory, and sends $\chi$ to the Weil-Deligne representation $(\rho_{0},0)$, where $\rho_{0}$ is the composition $W_{F}\to W_{F}^{\mathrm{ab}}\xrightarrow{\mathrm{rec}^{-1}}F^{\times}\xrightarrow{\chi}\mathbb{C}^{\times}$, with $\mathrm{rec}:F^{\times}\xrightarrow{\sim}W_{F}^{\mathrm{ab}}$ being the Artin reciprocity map of local class field theory. 

## Related concepts

* [[global analytic geometry]]

## References

Part of the above material is taken from

* Wikipedia, _[Local Langlands conjectures](http://en.wikipedia.org/wiki/Local_Langlands_conjectures)_.

See also

* Colin Bushnell, Guy Henniart, _The local Langlands conjecture for $GL(2)$_ .
* [Topics on Automorphic Forms](http://www.math.columbia.edu/~chaoli/docs/AutomorphicForm.html), course notes by Chao Li from a course taught by Jack Thorne
* [Kevin Buzzard's MSRI Summer School on automorphic forms](http://wwwf.imperial.ac.uk/~buzzard/MSRI/)

For an approach via the [[Fargues-Fontaine curve]]

* [[Laurent Fargues]], [[Peter Scholze]], _Geometrization of the local Langlands correspondence_ ([arXiv:2102.13459](https://arxiv.org/abs/2102.13459))


[[!redirects local Langlands conjectures]]

[[!redirects local Langlands program]]
[[!redirects local langlands program]]

[[!redirects local Langlands duality]]
[[!redirects local Langlands dualities]]

[[!redirects local Langlands correspondence]]
[[!redirects local Langlands correspondences]]
