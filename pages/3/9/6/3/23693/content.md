+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

A __$\sigma$-frame__ is a [[sigma-complete lattice|$\sigma$-complete lattice]] $(L, \leq, \bot, \vee, \top, \wedge, \Vee)$ such that for all elements $a \in L$ and sequences $s:\mathbb{N} \to L$, 
$$a \wedge \Vee_{n:\mathbb{N}} s(n) = \Vee_{n:\mathbb{N}} a \wedge s(n)$$

## Examples

* The [[Sierpinski space#Predicative|Sierpinski space]] in [[synthetic topology]] is the [[initial object|initial]] $\sigma$-frame. 

* The [[limited principle of omniscience]] implies that the [[boolean domain]] is a $\sigma$-frame. 

* The [[limited principle of omniscience]] or the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, \mathbb{2}}$ implies that the set of [[semidecidable truth values]] is a $\sigma$-frame. 

* The [[intrinsic topology]] on a set $A$, which is the [[function set]] $\Sigma^A$

* Malcev topologies for set $A$, which are a $\sigma$-[[subobject|subframe]] of the intrinsic topology $\Sigma^A$. 

* Any [[frame]] is a $\sigma$-frame. In particular, the [[poset of truth values]] is a $\sigma$-frame. 

## Category of $\sigma$-frames

$\sigma\mathrm{Frm}$ is the [[category]] whose [[objects]] are $\sigma$-frames and whose [[morphisms]] are $\sigma$-frame [[homomorphisms]], that is lattice [[homomorphisms]] that preserve [[countable]] joins. $\sigma\mathrm{Frm}$ is a [[replete subcategory|replete]] [[subcategory]] of [[Pos]] and [[DistLat]], and it is an [[algebraic category]].

The [[opposite category]] of $\sigma\mathrm{Frm}$ is the category $\sigma\mathrm{Loc}$ of [[sigma-locale|$\sigma$-locales]]; this is an example of the duality between [[space and quantity]].

## Related concepts

* [[sigma-complete lattice]]

* [[sigma-complete Heyting algebra]]

* [[sigma-complete Boolean algebra]]

* [[distributive lattice]]

* [[countably prime filter]]

* [[measure]]

* [[probability measure]]

* [[Dedekind cut]]

* [[Dedekind real numbers]]

* [[sigma-pretopos]]

* [[streak]]

* [[sigma-topological space]]

* [[sigma-locale]]

* [[sigma-coframe]]

* [[first countable space]]

* [[limited principle of omniscience]]

* [[sigma-frame of propositions]]

* [[Pos]], [[DistLat]], [[Frm]]

## References ##

* Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))

* [[Andrej Bauer]], *Spreen spaces and the synthetic Kreisel-Lacombe-Shoenfield-Tseitin theorem* ([arXiv:2307.07830](https://arxiv.org/abs/2307.07830))

* {#Gilbert17} Gaëtan Gilbert. *Formalising real numbers in homotopy type theory.* In CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs, pages 112–124, 2017. &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;.

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

* {#UFP13} Section 11.2 of Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* [[Raquel Bernardes]], *Lebesgue integration on $\sigma$-locales: simple functions*, ([arXiv:2408.13911](https://arxiv.org/abs/2408.13911))

* [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

[[!redirects sigma-frame]]
[[!redirects sigma-frames]]
[[!redirects σ-frame]]
[[!redirects σ-frames]]

[[!redirects sigma frame]]
[[!redirects sigma frames]]

[[!redirects category of sigma-frames]]
[[!redirects category of σ-frames]]
[[!redirects category of sigma frames]]
[[!redirects σ-Frm]]
[[!redirects σFrm]]
