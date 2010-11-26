
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

+-- {: .un_def}
###### Definition


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

=--

+-- {: .un_def}
###### Definition

A **$(n+1)$-BV algebra** is a similar structure with a BV-operator being of degree $n$ if $n$ is odd, and of degree $n/2$ if it is even.

=--

See ([CohenVoronov, def. 5.3.1](#CohenVoronov)) for details.

## Properties

+-- {: .un_theorem}
###### Theorem

The [[operad]] for BV-algebras is the [[homology]] of the [[framed little 2-disk operad]].

=--

This is due to ([Getzler](#Getzler))


+-- {: .un_theorem}
###### Theorem

The [[operad]] for $(n+1)$-BValgebras is the [[homology]] of the [[framed little n-disk operad]].

=--

This appears as ([CohenVoronov, theorem 5.3.3](#CohenVoronov)).

## Related concepts

* **BV-algebra**

* [[homotopy BV-algebra]].

## References

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159 (1994), no. 2, 265&#8211;285. ([arXiv](http://arxiv.org/abs/hep-th/9212043))
{#Getzler}

* [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](http://arxiv.org/abs/math/0503625))
{#CohenVoronov}


[[!redirects BV-algebras]]

[[!redirects Batalin-Vilkovisky algebra]]
[[!redirects Batalin-Vilkovisky algebras]]