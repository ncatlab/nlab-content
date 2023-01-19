
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


\tableofcontents

## Idea

Just as there are two notions of [[judgmental equality]] in [[dependent type theory]], judgmental equality of terms and judgmental equality of types, there are two types in [[dependent type theory]] which could be considered **typal equality**: 

* Typal equality of [[terms]] is the [[identity type]] or [[path type]]
* Typal equality of [[types]] is the [[equivalence type]]

In [[type universes]] $U$, this means that small types $A:U$ have two notions of typal equality, one from the identity type between small types, and the other from the equivalence type between small types, and the [[univalence axiom]] states that these two types are equivalent (i.e. typally equal) to each other. 

## Parallels between judgmental equality and typal equality

The parallels between the structural rules for judgmental equality and typal equality are shown below:

| judgmental equality | typal equality |
|---------------------|----------------|
| judgmental equality of terms | identification |
| reflexivity of judgmental equality of terms | identity identification |
| symmetry of judgmental equality of terms | inverse identification |
| transitivity of judgmental equality of terms | composition of identifications |
| judgmental equality of types | equivalence |
| reflexivity of judgmental equality of types | identity equivalence |
| symmetry of judgmental equality of types | inverse equivalence |
| transitivity of judgmental equality of types | composition of equivalences |
| principle of substitution | transport |
| variable conversion rule | substitution of evaluation of inverse equivalence |

## Homogeneous and heterogeneous typal equality

| | homogeneous identification | heterogeneous identification | homogeneous equivalence | heterogeneous equivalence |
|-|----------|--------------------|-------------|-----------------------|
| type | $a =_A b$ | $x =_B^p y$ | $A \simeq B$ | $A \simeq B$ |
| identity term | $\mathrm{refl}_A(a):a =_A a$ | $\mathrm{apd}_B^p(f):f(a) =_B^p f(b)$ | $\mathrm{id}_A:A \simeq A$ | $\mathrm{tr}_B^p:B(a) \simeq B(b)$ |

## See also

* [[judgmental equality]]
* [[propositional equality]]

[[!redirects typal equality]]
[[!redirects typally equal]]