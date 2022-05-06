
#Contents#
* table of contents
{:toc}

## Idea

### General

In [[quantum field theory]] and [[statistical physics]], a _single trace operator_ is an [[observable]]/[[correlator]] on [[square matrix]]- or rather [[adjoint representation]]-valued [[scalar fields]]/[[random variables]] $\{\phi_i\}_{i \in I}$ which is built from the elementary [[field observables]] $\mathbf{\Phi}_i$ as a [[trace]] over the [[matrix product]] of a finite string of them:

\[
  \label{ASingleTraceObservable}
  \mathcal{O}_{i_1, \cdots i_n}
  \;=\;
  Tr\big(
   \mathbf{\Phi}_{i_1}
   \cdot
   \mathbf{\Phi}_{i_2}
    \cdot
    \cdots
    \cdot
   \mathbf{\Phi}_{i_n}
  \big)
\]

or more generally as [[linear combinations]] thereof.

If the [[field (physics)|fields]] $\phi_i$ indeed take values in the [[adjoint representation]] of a given [[gauge group]], then the [[trace]] in the expression (eq:ASingleTraceObservable) ensures that this [[observable]] is [[gauge invariant]]. More general [[gauge invariant]] [[observables]] are hence _multi-trace operators_ which are [[linear combinations]] of products of single-trace observables.


### In AdS/CFT

Single trace operators/observables in [[conformal field theories]] such as [[super Yang-Mills theories]] play a special role in the [[AdS-CFT correspondence]], under which they correspond to single [[string]] excitations on the [[AdS spacetime|AdS]]-[[supergravity]] side of the correspondence, where, curiously, the "string of characters" in the argument of the trace gets literally mapped to a [[superstring]] in [[spacetime]] (see the references [below](#ReferencesRelationToStringExcitations)).

(...)

## Properties

### Relation to weight systems on chord diagrams

For [[field (physics)|fields]] $\phi$ valued in a [[Lie algebra representations]] $C \in \mathfrak{g}Mod$ of a [[metric Lie algebra]], with $\{\phi_a\}$ a [[linear basis]] for $C$ and $\{\phi^a\}$ denoting the dual basis, those single trace operators involving only metric pairs of fields, such as

$$
  \mathcal{O}
  \;\coloneqq\;
  Tr_C
  \big(
    \mathbf{\Phi}_{a_1}
    \cdot
    \mathbf{\Phi}_{a_2}
    \cdot
    \mathbf{\Phi}^{a_1}
    \cdot
    \mathbf{\Phi}^{a_2}
  \big)
$$

(using [[Einstein summation convention]]) are equivalently values of [[Lie algebra weight systems]] on the [[chord diagram]] that expresses the index pairing.

Such binary pairings inside the trace are induced notably after statistical averaging in  the [[SYK model]] and related systems, and has been argued to appear generically for [[AdS/CFT|dual]] [[observables]] of [[black hole thermodynamics]] ([Berkooz-Narayan-Simón 18, Section 2.1](#BerkoozNarayanSimon18)). 

For more on this see at _[[weight systems on chord diagrams in physics]]_.


## References

### General

(...)

### Relation to string excitations under AdS/CFT
 {#ReferencesRelationToStringExcitations}

Relation of single trace operators to [[superstring]] excitations under the [[AdS-CFT correspondence]]:

* [[David Berenstein]], [[Juan Maldacena]], [[Horatiu Nastase]], _Strings in flat space and pp waves from $\mathcal{N} = 4$ Super Yang Mills_, JHEP 0204 (2002) 013 ([arXiv:hep-th/0202021](https://arxiv.org/abs/hep-th/0202021))

* {#Kruczenski04} Martin Kruczenski, _Spiky strings and single trace operators in gauge theories_, JHEP 0508:014, 2005 ([arXiv:hep-th/0410226](https://arxiv.org/abs/hep-th/0410226))

(...)

### Relation to weight systems on chord diagrams

A general relation between [[single trace operators]] for [[observables]] on [[black hole thermodynamics]] and [[Lie algebra weight systems]] on [[chord diagrams]] (though not using the term "weight system") is proposed in

* {#BerkoozNarayanSimon18} [[Micha Berkooz]], [[Prithvi Narayan]], [[Joan Simón]], Section 2.1 of: _Chord diagrams, exact correlators in spin glasses and black hole bulk reconstruction_, JHEP 08 (2018) 192 ([arxiv:1806.04380](https://arxiv.org/abs/1806.04380))

For more on this see at _[[weight systems on chord diagrams in physics]]_.

[[!redirects single trace operators]]

[[!redirects single-trace operator]]
[[!redirects single-trace operator]]

[[!redirects single trace observable]]
[[!redirects single trace observables]]

[[!redirects single-trace observable]]
[[!redirects single-trace observables]]

