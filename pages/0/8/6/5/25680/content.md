
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

## Idea

In [[dependent type theory]], a [[hom type]] on a type $A$ is a [[dependent type]] $\mathrm{hom}_A(x, y)$ which models the [[hom spaces]] of [[(infinity,1)-category|$\infty$-categories]]. 

## Definition 

### In simplicial type theory

There are multiple different formalisms of [[simplicial homotopy type theory]]; two of them are given in [Gratzer, Weinberger, & Buchholtz 2024](#GWB24) and in [Riehl & Shulman 2017](#RiehlShulman17), and in each formalism there is a different way to define the hom type. 

#### Directed interval via axioms

In [[simplicial homotopy type theory]] where the [[interval poset]] $\mathbb{I}$ is defined via axioms as a [[bounded total order]], the hom type is defined as the [[dependent sum type]]

$$\mathrm{hom}_A(x, y) \coloneqq \sum_{f:\mathbb{I} \to A} (f(0) =_A x) \times (f(1) =_A y)$$

#### Type theory with shapes formalism

In [[simplicial homotopy type theory]] in the [[type theory with shapes]] formalism, the hom type is defined as the [[extension type]]

$$\mathrm{hom}_A(x, y) \coloneqq \langle \Delta^1 \to A \vert_{[x,y]}^{\partial \Delta^1} \rangle$$

where $\Delta^1$ is the directed interval primitive $\mathbb{2}$ and $\partial \Delta^1$ is the [[boundary]] of $\Delta^1$. 

### In dependent type theory

More generally, hom types can be defined for any type $A$ and any [[bounded poset]] $I$ with a [[bottom element]] $0:I$ and a [[top element]] $1:I$, as the type 

$$\mathrm{hom}_{A, I}(x, y) \coloneqq \sum_{f:I \to A} (f(0) =_A x) \times (f(1) =_A y)$$

## Related concepts

* [[identity type]]
* [[bridge type]]
* [[function type]]
* [[directed univalence]]
* [[hom set]]
* [[composite]]
* [[composable pair]]
* [[commutative triangle]]
* [[Segal type]], [[Rezk type]]
* [[covariant type family]]
* [[heterogeneous hom type]]
* [[simplicial homotopy type theory]]
* [[directed homotopy type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects morphism in simplicial type theory]]
[[!redirects morphisms in simplicial type theory]]

[[!redirects hom types]]
[[!redirects hom-type]]
[[!redirects hom-types]]