
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[subobject]] given by a [[monomorphism]] $i: S \to X$ in a [[coherent category]] is called _complemented_ (also: _decidable_) if it has a [[complement]]: a subobject $\tilde{i} \colon \tilde{S} \to X$ such that 

1. their [[intersection]] is [[generalized the|the]] [[initial object]] 

   $$ 
     S \cap \tilde{S}
     \;\simeq\;
     \emptyset
   $$

1. their [[union]] is all of $X$ 

   $$
     S \cup \tilde{S} \simeq X
   $$  

## Examples

In [[constructive mathematics]], a complemented subobject in [[Set]] is called a _[[decidable subset]]_.

## Related entries

* [[constructive model structure on simplicial sets]]

## Properties

Every subobject is complemented in a [[Boolean category]].

In [[classical mathematics]], every subset is decidable.  Indeed, the  [[law of excluded middle]] may be taken to say precisely that every subset of the [[point]] is complemented.

More generally, if every subobject of the [[terminal object]] of a [[well-pointed topos|well-pointed]] [[coherent category]] $C$ is complemented, then every subobject in $C$ is complemented.

## References

* [[Nicola Gambino]], [[Christian Sattler]], [[Karol Szumiło]], Section 1.1 of _The constructive Kan-Quillen model structure: two new proofs_ ([arXiv:1907.05394](https://arxiv.org/abs/1907.05394))

[[!redirects decidable inclusion]]
[[!redirects decidable inclusions]]