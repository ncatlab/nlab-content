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

The cone type is an axiomatization of the [[cone]] in the context of homotopy type theory.

## Definition

As a higher inductive type, the cone is given by

    Inductive Cone (A : Type) : Type
      | vertex : Cone A
      | base :  A -> Cone A
      | edge : A -> Id Cone A vertex base(a)

It can equivalently be defined as the (homotopy) [[pushout]] of $A$ and the unit type $1$ under $A$.  This definition makes it clear that the cone type is always contractible.

## Examples

* The [[unit type]] $1$ is the cone type of an empty type $0$. 

* The [[interval type]] $I$ is the cone type of the unit type $1$

* A [[simplex type]] $\Delta_n$ is the cone type of the simplex type $\Delta_{n-1}$. $\Delta_1 = I$ and $\Delta_0 = 1$. 

## See also

* [[cone]]