
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A __first-order theory__ is a [[theory]] written in the language of [[first-order logic]] i.e it is a set of formulas or sequents (or generally, [[axioms]] over a signature) whose [[quantification|quantifiers]] and variables range over individuals of the underlying domain, but not over subsets of individuals nor over functions or relations of individuals etc. A first-order theory is called [[infinitary logic|infinitary]] when the expressions contain infinite disjunctions or conjunctions, else it is called _finitary_.

Another name for a first-order theory is _elementary theory_ which is found in the older literature but by now has gone extinct though it has left its traces in names like [[elementary topos]], [[elementary embedding]], [[ETCC]] etc.

The characterization of set-theoretic [[models]] of (finitary) first-order theories is the topic of traditional [[model theory]].

## Examples

Formulations of [[set theory]] are usually first-order theories, such as

* [[material set theory]]: [[ZFC]]

* [[structural set theory]]: [[fully formal ETCS]]

## Remark

In particular, the precise formulation of the former in first-order predicate logic by [[Some remarks on axiomatized set theory|Skolem in 1922]] provided the impetus for the hold that first-order predicate logic gained over mathematical logic in the following.

It is somewhat ironic that classical first-order logic owes its promotion to prominence to intuitionistic mathematicians like [[Hermann Weyl|Weyl]] (1910,1918) and [[Thoralf Skolem|Skolem]].

## Properties

+-- {: .num_prop}
###### Proposition
Let $\mathbb{T}$ be a finitary first-order theory. There exists a [[Grothendieck topos]] $\mathcal{E}$ and a $\mathbb{T}$-model $N_{\mathbb{T}}$ in $\mathcal{E}$ such that the first-order sequents satisfied in $N_{\mathbb{T}}$ are precisely those provable in $\mathbb{T}$.
=--

This result due to [[Peter Freyd|P. Freyd]] is discussed in Johnstone ([2002](#JT02), p.900) or Freyd-Scedrov ([1990](#FrSc90), p.130).

If $\mathbb{T}$ is a theory over a countable signature, then $\mathcal{E}$ can be taken as the topos $Sh(2^{\mathbb{N}})$ of sheaves on the [[Cantor space]] $2^{\mathbb{N}}$. This completeness result shows that $Sh(2^{\mathbb{N}})$ plays in constructive first-order logic a role similar to the role of $Set$ in classical first-order logic.

## Related entries

* [[second-order logic]]

* [[geometric theory]]

* [[coherent logic]]

* [[Skolem paradox]]

## References

* Carsten Butz, [[Peter Johnstone]], _Classifying toposes for first-order theories_ , APAL **91** (1998) pp.33-58.

* {#FrSc90}[[Peter Freyd|P. J. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990. (pp.129ff)

* {#JT02}[[Peter Johnstone]], _Sketches of an Elephant II_ , Oxford UP 2002. (D1.3, D3.1, pp.899f)

[[!redirects first-order theories]]
[[!redirects first-order logical theories]]
[[!redirects first-order logical theory]]
[[!redirects elementary theory]]
