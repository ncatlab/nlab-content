
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An _abelian group_ (named after [[Nils Abel]]) is a [[group]] $A$ where the multiplication satisfies the commutative law: for all elements $x, y\in A$ we have

$$
  x y = y x
  \,.
$$

The [[category]] with abelian groups as [[object|objects]] and group homomorphisms as [[morphism|morphisms]] is called [[Ab]]. 

## Properties

### In homtopy theory

From the [[nPOV]], just as a [[group]] $G$ may be thought of as a ([[pointed object|pointed]]) [[groupoid]] $\mathbf{B}G$ with a single object -- as discussed at [[delooping]] -- an abelian group $A$ may be understood as a (pointed) [[2-groupoid]] $\mathbf{B}^2 A$ with a single object and a single morphism: the delooping of the delooping of $A$.

$$
  \mathbf{B}^2 A
  =
  \left\{
    \array{
      & \nearrow \searrow^{\mathrlap{Id}}
      \\
      \bullet
      &\Downarrow^{a \in A}&
      \bullet
      \\
      & \searrow \nearrow_{\mathrlap{Id}}
    }
  \right\}
  \,.
$$ 

The [[exchange law]] for the composition of [[2-morphisms]] in a [[2-category]] forces the product on the $a \in A$ here to be commutative. This reasoning is known as the [[Eckmann-Hilton argument]] and is the same as the reasoning that finds that the second [[homotopy group]] of a space has to be abelian.

So the identitfication of abelian groups with one-object, one-morphism 2-groupoids may also be thought of as an identification with 2-[[truncated]] and 2-[[connected]] [[homotopy types]].

### Relation to other concepts

A [[monoid]] in [[Ab]] with its standard [[monoidal category]] structure, equivalently a ([[pointed object|pointed]]) [[Ab]]-[[enriched category]] with a single object, is a [[ring]].

## Generalizations

Generalizations of the notion of abelian group in [[higher category theory]] include 

* abelian [[group object in an (infinity,1)-category|group objects in an (∞,1)-category]]

* notably abelian [[simplicial groups]]

* and [[spectrum|spectra]].

## Related entries

* [[tensor product of abelian groups]]

* [[free abelian group]]

* [[abelianization]]

* [[anabelian group]]

* [[module]], [[ring]]

* [[Ab]]

* [[Ab-enriched category]], [[abelian category]]



[[!redirects abelian groups]]
[[!redirects Abelian group]]
[[!redirects Abelian groups]]