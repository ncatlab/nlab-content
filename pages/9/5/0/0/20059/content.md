+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

# Cubical-type model categories

* table of contents
{: toc}

## General

A cubical-type model category is a [[model category]] [[mathematical structure|structure]] arising from a construction due to [[Christian Sattler]] and its generalizations.
These constructions are motivated by [[cubical type theory]] and can in particular be applied in certain [[categories]] of [[cubical sets]].

### Assumptions

Let $\mathbb{C}$ be a [[small category]] with [[finite products]].
Assume there is a (cartesian) [[interval object]] $\mathbb{I}$, i.e.,
an [[object]] $\mathbb{I}$ with two [[parallel morphisms]] $0,1  \colon e \to \mathbb{I}$, where $e$ is the [[terminal object]] in $\mathbb{C}$.

Assume further that we have [[connection on a cubical set|connection
maps]] $\vee,\wedge : \mathbb{I}\times\mathbb{I} \to \mathbb{I}$ such
that $x \vee 0 = 0 \vee x = x$ and $x \wedge 1 = 1 \wedge x = x$.

We also need a face lattice $\mathbb{F}$, that is, a [[subobject|sub]]-[[lattice]] of the [[subobject classifier]] $\Omega$ in the [[presheaf category]] $cSet = \mathbb{C}^{op} \to Set$ containing the endpoints of each [[cylinder object]] $J^+ = J \times \mathbb{I}$ for each object $J$ of $\mathbb{C}$, and an operation $\forall \colon \mathbb{F}^\mathbb{I} \to \mathbb{F}$ [[right adjoint]] to the [[projection]] in the sense that $\psi \le \forall \delta$ iff $\psi p \le \delta$, where $p : \mathbb{F} \times \mathbb{I} \to \mathbb{F}$.

If we want the model to be effective, we also require that each [[proposition]] $\psi = 1$ with $\psi \in \mathbb{F}(I)$ is [[decidability|decidable]]. (This rules out taking $\mathbb{F} = \Omega$.)

### Instances of the assumptions

A simple and central example is the [[full subcategory]] of the category
of [[posets]] $Pos$ on powers of $\mathbb{I} = (0 \lt 1)$. This is
also the [[Lawvere theory]] of [[distributive lattices]]. The
[[idempotent completion]] is the full subcategory of $Pos$ on finite
lattices.

Other prominent examples are the Lawvere theories of [[de Morgan algebra|de
Morgan]], [[Kleene algebra|Kleene]], and [[boolean algebra|boolean]] algebras.

For computational purposes we can take $\mathbb{F}$ to be the smallest
lattice containing the cylinder endpoints (the faces of cubes). To get
[[Cisinski model structures]] we can take $\mathbb{F} = \Omega$.

## Equivalence with simplicial sets

One may wonder whether these models structures are equivalent to the model in [[simplicial sets]]. This is not the case for Cartesian cubes; see [mailing-list](https://groups.google.com/d/msg/homotopytypetheory/RQkLWZ_83kQ/tAyb3zYTBQAJ). However, this model does form a Grothendieck [[(infinity,1)-topos]], because it satisfies the Giraud axioms. For deMorgan cubical sets the geometric realization is not a Quillen equivalence (because of the reversal map); the counterexample is the unit interval quotient by the symmetry); see [Sattler](#sattlerHIM). Whether they are equivalent by another map is not yet excluded.
The question whether the geometric realization for the cubical sets based on distributive lattices is an equivalence is still open, cf. also [Hackney and Rovelli](#hrInduced) and [Streicher and Weinberger](#swCuSi).

## References

Sattler's construction is in

* {#sattlerEEP} [[Christian Sattler]], *The equivalence extension property and model structures* $[$[arXiv:1704.06911](https://arxiv.org/abs/1704.06911)$]$

The following two notes describe the construction,  specialized to cubical sets, in more type-theoretic language.

* {#mod2} [[Thierry Coquand]], *A model structure on some presheaf categories*, [pdf](http://www.cse.chalmers.se/~coquand/mod2.pdf)

* {#cis3} [[Thierry Coquand]], *Some examples of complete Cisinski model structures*, [pdf](http://www.cse.chalmers.se/~coquand/cis3.pdf)

A refactoring of part of the construction through the notion of "cylindrical premodel structure" is described in Section 3 of

* {#csElegance} [[Evan Cavallo]] and [[Christian Sattler]], *Relative elegance and cartesian cubes with one connection*, $[$[arXiv:2211.14801](https://arxiv.org/abs/2211.14801)$]$

and in the unpublished note

* {#sattlerInterval} [[Christian Sattler]], *Cylindrical model structures*, [pdf](https://www.cse.chalmers.se/~sattler/docs/interval-model-structure.pdf)

On equivalences with the model structure on simplicial sets:

* {#sattlerHIM} [[Christian Sattler]], *Do cubical models of type theory also model homotopy types*, lecture at Hausdorff Trimester Program: Types, Sets and Constructions, [youtube](https://www.youtube.com/watch?v=wkPDyIGmEoA)

* {#hrInduced} [[Philip Hackney]] and [[Martina Rovelli]], *Induced model structures for ∞-categories and ∞-groupoids*, $[$[arXiv:2102.01104](https://arxiv.org/abs/2102.01104)$]$, [Proc. Amer. Math. Soc., June 10, 2022](https://www.ams.org/journals/proc/0000-000-00/S0002-9939-2022-15982-6/home.html)

* {#swCuSi} [[Thomas Streicher]] and [[Jonathan Weinberger]], *Simplicial sets inside cubical sets* $[$[arXiv:1911.09594](https://arxiv.org/abs/1911.0959)$]$, [Theory and Applications of Categories, Vol. 37, 2021, No. 10, pp 276–286](http://www.tac.mta.ca/tac/volumes/37/10/37-10abs.html)

[[!redirects type-theoretic model structures]]
[[!redirects type theoretic model structures]]
[[!redirects type theoretic model structure]]
[[!redirects type-theoretic model structure]]
[[!redirects cubical-type model categories]]
[[!redirects cubical-type model structure]]
[[!redirects cubical-type model structures]]
