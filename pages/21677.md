
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
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop} 
###### Proposition
**([[Quillen adjunction between simplicial sets and connective dgc-algebras]])**

The [[PL de Rham complex]]-construction is the [[left adjoint]] in a [[Quillen adjunction]] between

* the [[opposite model structure|opposite]] of the [[projective model structure on connective dgc-algebras]]

* the [[classical model structure on simplicial sets]]

$$
  \big(
    DiffGradedCommAlgebras^{\geq 0}_{k}
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
  SimplicialSets_{Qu}
$$

=--

+-- {: .proof}
###### Proof

That the [[PL de Rham complex]] [[functor]] preserves [[cofibrations]], hence sends injections of simplicial sets to surjections of dgc-algebras, is immediate from its construction.

That its [[right adjoint]] preserves fibrations, hence sends cofibrations of dgc-algebras to [[Kan fibrations]], is the statement of [Bousfield-Gugenheim 76, Lemma 8.2](#BousfieldGugenheim76).

=--

## Related statements

* [[fundamental theorem of dg-algebraic rational homotopy theory]]

* [[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]]

* [[rational homotopy theory]], [[real homotopy theory]]

## References


* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

