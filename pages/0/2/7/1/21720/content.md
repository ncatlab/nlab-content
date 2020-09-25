
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop} 
###### Proposition
**([[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]])**

Let $G$ be a [[finite group]].

The $G$-[[equivariant PL de Rham complex]]-construction is the [[left adjoint]] in a [[Quillen adjunction]] between

* the [[opposite model structure|opposite]] of the [[projective model structure on equivariant connective dgc-algebras]]

* the [[model structure on equivariant simplicial sets]] 

  (i.e.: the global projective [[model structure on functors]] from the [[opposite category|opposite]] of the [[orbit category]] to the [[classical model structure on simplicial sets]])

$$
  \big(
    G dgcAlgebras^{\geq 0}_{k}
  \big)^{op}_{proj}
  \underoverset
    {
      \underset
        {\;\;\; exp \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\;\Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot_{\mathrlap{Qu}}}
  G SimplicialSets_{Qu}
$$

=--

([Scull 08, Prop. 5.1](#Scull08))

## Related statements

* [[fundamental theorem of equivariant dg-algebraic rational homotopy theory]]

* [[Quillen adjunction between simplicial sets and connective dgc-algebras]]

## References


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))
