
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The analogue of a [[Segal space]] in [[simplicial type theory]]. 

## Definition

There are multiple different formalisms of simplicial homotopy type theory; two of them are given in [Gratzer, Weinberger, & Buchholtz 2024](#GWB24) and in [Riehl & Shulman 2017](#RiehlShulman17), and in each formalism there is a different way to define Segal types. 

#### Directed interval via axioms

In [[simplicial type theory]] where the directed interval primitive $\mathbb{I}$ is defined as a type via axioms, a **Segal type** is a type $A$ such that every [[pair of composable morphisms]] in $A$ is [[uniquely composable]]

$$\mathrm{isSegal}(A) \coloneqq \prod_{x:A} \prod_{y:A} \prod_{z:A} \prod_{f:\mathrm{hom}_A(x, y)} \prod_{g:\mathrm{hom}_A(y, z)} \mathrm{isContr}(\mathrm{fiber}(p, (x, y, z, f, g))$$

where $p$ is the function from composites to pairs of composable morphisms

$$p:\left(\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, z)\right) \to \left(\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z)\right)$$

which discards the morphism in $\mathrm{hom}_A(x, z)$ from the tuple. 

#### Type theory with shapes formalism

In [[simplicial type theory]] in the [[type theory with shapes]] formalism, a **Segal type** is a type $A$ such that given elements $x:A$, $y:A$, and $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$, the type 
$$\sum_{h:\mathrm{hom}_A(x, z)} \left\langle \Delta^2 \to A \vert_{[x, y, z, f, g, h]}^{\partial \Delta^2} \right\rangle$$
is a [[contractible type]], where $\Delta^2$ is the $2$-simplex probe shape and $\partial \Delta^2$ is its boundary. 

## Categorical semantics

The categorical semantics of a Segal type is a [[Segal space object]] in a [[locally cartesian closed (infinity,1)-category|locally cartesian closed $(\infty,1)$-category]] $\mathbf{H}$. 

## Related concepts

* [[hom type]]
* [[discrete Segal type]]
* [[Rezk type]]
* [[isomorphism in a Segal type]]
* [[Segal space]]
* [[precategory]]
* [[skeletal Segal type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects Segal type]]
[[!redirects Segal types]]