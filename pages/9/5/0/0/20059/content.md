+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Type-theoretic model structure

* table of contents
{: toc}

## General

These are a class of model structures on certain categories of [[cubical sets]], due to [[Christian Sattler]].

### Assumptions

Let $\mathbb{C}$ be a [[small category]] with [[finite products]].
Assume there is a (cartesian) [[interval object]] $\mathbb{I}$, i.e.,
an object $\mathbb{I}$ with two morphisms $0,1 : e \to \mathbb{I}$,
where $e$ is the terminal object in $\mathbb{C}$.

Assume further that we have [[connection on a cubical set|connection
maps]] $\vee,\wedge : \mathbb{I}\times\mathbb{I} \to \mathbb{I}$ such
that $x \vee 0 = 0 \vee x = x$ and $x \wedge 1 = 1 \wedge x = x$.

We also need a face lattice $\mathbb{F}$, that is, a sublattice of the
[[subobject classifier]] $\Omega$ in the [[presheaf category]] $cSet =
\mathbb{C}^{op} \to Set$ containing the endpoints of each cylinder
$J^+ = J \times \mathbb{I}$ for each object $J$ of $\mathbb{C}$, and
an operation $\forall : \mathbb{F}^\mathbb{I} \to \mathbb{F}$ right
adjoint to the projection in the sense that $\psi \le \forall \delta$
iff $\psi p \le \delta$, where $p : \mathbb{F} \times \mathbb{I} \to
\mathbb{F}$.

If we want the model to be effective, we also require that each
proposition $\psi = 1$ with $\psi \in \mathbb{F}(I)$ is decidable.
(This rules out taking $\mathbb{F} = \Omega$.)

### Instances of the assumptions

A simple and central example is the full subcategory of the category
of [[posets]] $Pos$ on powers of $\mathbb{I} = (0 \lt 1)$. This is
also the [[Lawvere theory]] of [[distributive lattices]]. The
[[idempotent completion]] is the full subcategory of $Pos$ on finite
lattices.

Other prominent examples are the Lawvere theories of [[de Morgan algebra|de
Morgan]], [[Kleene algebra|Kleene]], and [[boolean algebra|boolean]] algebras.

For computational purposes we can take $\mathbb{F}$ to be the smallest
lattice containing the cylinder endpoints (the faces of cubes). To get
[[Cisinski model structures]] we can take $\mathbb{F} = \Omega$.

## References

* {#mod2} [[Thierry Coquand]], *A model structure on some presheaf categories*, [pdf](http://www.cse.chalmers.se/~coquand/mod2.pdf)

* {#cis3} [[Thierry Coquand]], *Some examples of complete Cisinski model structures*, [pdf](http://www.cse.chalmers.se/~coquand/cis3.pdf)

* {#sattlerHIM} [[Christian Sattler]], *Do cubical models of type theory also model homotopy types*, lecture at Hausdorff Trimester Program: Types, Sets and Constructions, [youtube](https://www.youtube.com/watch?v=wkPDyIGmEoA)

[[!redirects type-theoretic model structures]]
[[!redirects type theoretic model structures]]
[[!redirects type theoretic model structure]]
