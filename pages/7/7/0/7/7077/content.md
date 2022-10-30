
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _locally cartesian closed model category_ is a [[locally cartesian closed category]] which is equipped with the structure of a [[model category]] in a compatible way.

## Definition

A [[model category]] $\mathcal{C}$ which is additionally a [[locally cartesian closed category]] is called a **locally cartesian closed model category** if for any [[fibration]] $g\colon A\to B$ between [[fibrant objects]], the [[dependent product]] [[adjunction]]
$$ 
  g^* : \mathcal{C}/B \rightleftarrows \mathcal{C}/A : \Pi_g 
$$
is a [[Quillen adjunction]] between the corresponding [[slice model structures]].

Concretely, this means that both [[cofibrations]] and [[trivial cofibrations]] are [[pullback-stability|stable]] under [[pullback]] along fibrations between fibrant objects.

Equivalently this means that for all $A \to B$ as above the [[internal hom]] [[adjunction]] in the [[slice category]] over $B$

$$
  (-) \times_{\mathcal{C}/_B} A 
  \;:\;
  \mathcal{C}/_B
  \rightleftarrows
  \mathcal{C}/_B
  \;:\;
  [A, -]_{\mathcal{C}/_B}
$$

is a [[Quillen adjunction]].


## Examples

Any [[right proper model category]] which is locally cartesian closed and in which the cofibrations are the [[monomorphisms]] is a locally cartesian closed model category.  This includes the classical [[model structure on simplicial sets]], as well as the [[injective model structure|injective]] [[global model structure on simplicial presheaves]].



## Applications

* Modulo questions of strictness and [[coherence]] (see [[identity type]] for details), locally cartesian closed model categories provide [[categorical semantics]] for [[homotopy type theory]] with [[function extensionality]].

## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]


* [[cartesian closed model category]], **locally cartesian closed model category**


* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]


