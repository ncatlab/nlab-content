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

The _join type_ is an [[axiom|axiomatization]] of the [[join of topological spaces]] in [[algebraic topology]] in the context of [[homotopy type theory]].

## Definition 

The join type of a [[type]] $A$ and $B$, $A * B$, is the [[pushout type]] of the following span

$$A \xleftarrow{\text{fst}} A \times B \xrightarrow{\text{snd}} B$$

## Examples

* Given a type $A$ and two [[subtypes]] $B \hookrightarrow A$ and $C \hookrightarrow A$, the structural [[union]] $B \cup C$ of subtypes $B$ and $C$ is the join of $B$ and $C$. 

* Given two [[mere propositions]] $P$ and $Q$, the [[disjunction]] $P \vee Q$ of $P$ and $Q$ is the join of $P$ and $Q$. 

## See also

* [[higher inductive type]]

* [[join of topological spaces]]

* [[bracket type]]

* [[disjunction]]

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* {#Shulman13} [[Mike Shulman]], *Cohomology*, Homotopy type theory blog ([web](http://homotopytypetheory.org/2013/07/24/cohomology/))

* [[Egbert Rijke]], *The join construction*, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

* [[Egbert Rijke]], *Homotopy pushouts*, Lecture 13 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

* {#RijkeDraft22} [[Egbert Rijke]] (2022), *[[Introduction to Homotopy Type Theory]]*, draft. ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf))