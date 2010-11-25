
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **Batalin-Vilkovisky algebra** or **BV-algebra** for short is

* a [[Gerstenhaber algebra]] $(A, \cdot, [-,-])$

* equipped with a unary [[linear operator]] $\Delta : A \to A$ of degree +1

* such that

  1. $\Delta$ is a [[derivation]] for $[-,-]$;

  1. $[-,-]$ is the failure of $\Delta$ being a derivation for $\cdot$:

     $$
        [-,-] = \Delta \circ (-\cdot -) - (\Delta(-) \cdot - ) - (- \cdot \Delta(-))
      \,.
     $$

## Properties

+-- {: .un_theorem}
###### Theorem

The [[operad]] for BV-algebras is the [[homology]] of the [[framed little 2-disk operad]].

=--

This is due to ([Getzler](#Getzler))

## Related concepts

* **BV-algebra**

* [[homotopy BV-algebra]].

## References

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159 (1994), no. 2, 265&#8211;285. ([arXiv](http://arxiv.org/abs/hep-th/9212043))
{#Getzler}


[[!redirects BV-algebras]]

[[!redirects Batalin-Vilkovisky algebra]]
[[!redirects Batalin-Vilkovisky algebras]]