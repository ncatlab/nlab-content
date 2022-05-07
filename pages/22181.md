+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _suspension type_ is an [[axiom|axiomatization]] of the [[suspension object]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the suspension is given by


    Inductive Suspension (A : Type) : Type
      | north : Suspension A
      | south : Suspension A
      | meridian : A -> Id Suspension A north south

This says that the type is [[dependent type|dependent]] on the type A and inductive constructed from two [[terms]] in the suspension, whose [[semantics|interpretation]] is as the north and south poles of the suspension, together with a term in the [[function type]] from A to the [[identity type]] of paths between these two terms, representing the meridians from the north to the south pole.

## Examples

* The [[two-valued type]] $\mathbf{2}$ is the suspension type of the [[empty type]] $\mathbf{0}$. 

* The [[interval type]] $I$ is the suspension type of the [[unit type]] $\mathbf{1}$. 

* The [[circle type]] $S^1$ is the suspension type of $\mathbf{2}$.

* The homotopical disk type $G_2$ is the suspension type of $I$.

* Homotopical $n$-sphere types of dimension $n:\mathbb{N}$, $S^n$, are suspension types of $S^{n-1}$. 

* Homotopical $n$-[[globe]] types of dimension $n:\mathbb{N}$, $G_n$, are suspension types of $G_{n-1}$.

* In general, the suspension type $\Sigma A$ of a type $A$ is the [[homotopy pushout]] of the [[span]] $\mathbf{1} \leftarrow A \rightarrow \mathbf{1}$. 

## Related concepts

* [[suspension object]]

  * **suspension type**

  * [[suspension]], [[reduced suspension]]

* [[homotopy pushout]]

[[!redirects suspensio  types]]