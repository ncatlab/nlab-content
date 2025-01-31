
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Segal types are the (infinity,1)-categorical version of [[precategories]] in [[simplicial type theory]]

## Definition

There are multiple different formalisms of simplicial homotopy type theory; two of them are given in [Gratzer, Weinberger, & Buchholtz 2024](#GWB24) and in [Riehl & Shulman 2017](#RiehlShulman17), and in each formalism there is a different way to define Segal types. 

#### Directed interval via axioms

In [[simplicial homotopy type theory]] where the directed interval primitive $\mathbb{2}$ is defined via axioms, let the 2-simplex type be defined as 

$$\Delta^2 \coloneqq \sum_{s:\mathbb{2}} \sum_{t:\mathbb{2}} s \leq t$$

and let the 2-1-horn type be defined as 

$$\Lambda_1^2 \coloneqq \sum_{s:\mathbb{2}} \sum_{t:\mathbb{2}} [(s =_\mathbb{2} 0) + (t =_\mathbb{2} 1)]$$

where $[P]$ is the [[propositional truncation]] of the type $P$. For each type $A$ there is a canonical restriction function $i:(\Delta^2 \to A) \to (\Lambda_1^2 \to A)$. 

$A$ is a **Segal type** if the restriction function $i$ is an [[equivalence of types]]. 

#### Type theory with shapes formalism

In [[simplicial type theory]] in the [[type theory with shapes]] formalism, a **Segal type** is a type $A$ such that given elements $x:A$, $y:A$, and $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$, the type 
$$\sum_{h:\mathrm{hom}_A(x, z)} \left\langle \Delta^2 \to A \vert_{[x, y, z, f, g, h]}^{\partial \Delta^2} \right\rangle$$
is a [[contractible type]], where $\Delta^2$ is the $2$-simplex probe shape and $\partial \Delta^2$ is its boundary. 

## Related concepts

* [[hom type]]
* [[discrete Segal type]]
* [[Rezk type]]
* [[isomorphism in a Segal type]]
* [[Segal space]]
* [[op modality]]
* [[twisted arrow modality]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects Segal type]]
[[!redirects Segal types]]