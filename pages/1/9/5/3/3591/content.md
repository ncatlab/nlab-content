
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Equilogical spaces
* table of contents
{: toc}

## Definition

An __equilogical space__ is a [[separation axioms|Kolmogorov]] ($T_0$) [[topological space]] $T$ along with an arbitrary [[equivalence relation]] $\equiv$ on its points (of note, the equivalence relation need not match the topological structure in any way). A morphism between equilogical spaces $(T, {\equiv})$ and $(U, {\cong})$ is a [[continuous function]] $f\colon T \to U$ such that $x \equiv y$ implies $f(x) \cong f(y)$, for all points $x$ and $y$ in $T$. Two such morphisms $f$ and $g$ are considered equal if for all points $x$ in $T$, $f(x) \cong g(x)$.

## Properties

The category __$Equ$__ of equilogical spaces obviously contains the category of $T_0$ topological spaces as a [[full subcategory]] (by using the trivial equivalence relation of [[equality]] on points). Moreover, as opposed to the latter, $Equ$ is in fact [[cartesian closed]]; this can be seen using the [[equivalence of categories|equivalence]] of $Equ$ and the category of [[partial equivalence relation]]s over [[algebraic lattice]]s.

On the other hand, $Equ$ can be identified with a [[reflective subcategory|reflective]] [[exponential ideal]] in the [[ex/lex completion]] of the category $Top_0$ of $T_0$ topological spaces.  This provides an alternative proof of the cartesian closure of $Equ$, since an exponential ideal in a cartesian closed category is cartesian closed, and $(Top_0)_{ex/lex}$ is cartesian closed (in fact, [[locally cartesian closed category|locally cartesian closed]]) since $Top_0$ is weakly locally cartesian closed.

Moreover, in this way we can see that the embedding $Top_0 \to Equ$ preserves all existing [[exponential law for spaces|exponentials]], since the embedding $C \to C_{ex/lex}$ does so, and $Equ$ is closed under exponentials in $(Top_0)_{ex/lex}$ and contains the image of $Top_0$.  This embedding also preserves all [[limits]], but it does not in general preserve [[colimits]].

## Related concepts

* [[effective topological space]]

## References

The concept was originally introduced for [[domain theory]] in [a privately circulated manuscript](#Scott) by [[Dana Scott]].

* {#Scott}[[Dana Scott]], _A New Category? Domains, Spaces, and Equivalence Relations_, 

It is then discussed in more detail in

* {#Bauer00} [[Andrej Bauer]], section 4 of _The Realizability Approach to
Computable Analysis and Topology_, PhD thesis CMU (2000) ([pdf](http://andrej.com/thesis/thesis.pdf))

* {#BBS} [[Andrej Bauer]], [[Lars Birkedal]], [[Dana Scott]], _Equilogical Spaces_, 2001  ([ps](http://www.andrej.com/papers/equ-paper.ps), [[BBSEquilogical.pdf:file]])



[[!redirects equilogical space]]
[[!redirects equilogical spaces]]