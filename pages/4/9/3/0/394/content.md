
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Essentially surjective functors
* table of contents
{: toc}

## Idea

A [[functor]] $F\colon C \to D$ is **essentially surjective**, or **essentially surjective on objects** (sometimes abbreviated to **eso**), if it is surjective on objects "up to isomorphism".


## Definition

$F\colon C \to D$ is **essentially surjective** if for every [[object]] $y$ of $D$, there exists an object $x$ of $C$ and an [[isomorphism]] $F(x) \cong y$ in $D$.

### In homotopy type theory 

A [[functor]] $F : C \to D$ is **essentially surjective** if for all $y:D$ there *merely* exists an $x:C$ such that $F(x) \cong y$.

## Examples

* A functor between [[discrete categories]] (or, more generally, [[skeletal categories]]) is essentially surjective iff it is a [[surjective function]] between the classes of objects.

* Any [[bijective-on-objects functor]] or [[surjective-on-objects functor]] is essentially surjective.

* A [[composition]] of any two essentially surjective functors is essentially surjective.

* If $g f$ is essentially surjective, then $g$ is essentially surjective.

* An essentially surjective functor is additionally [[fully faithful functor|fully faithful]] precisely when it is an [[equivalence of categories]].

* The [[inclusion functor]] of a [[subcategory]] is essentially surjective precisely when the subcategory is [[essentially wide subcategory|essentially wide]].

* Every [[split essentially surjective functor]] is essentially surjective. The converse is true for [[strict functors]] in the presence of the [[axiom of choice]]. 

## Properties

* Strengthening the last example, there is an [[factorization system in a 2-category|orthogonal factorization system]] (in the up-to-isomorphism [[strict 2-category|strict]] sense) on $Cat$, in which eso functors are the left class and fully faithful functors are the right class.

  This is an "up-to-isomorphism" version of the [[bo-ff factorization system]], which is a 1-categorical orthogonal factorization system on $Cat$ in which the left class consists of [[bijective-on-objects functors]].  Thus the notion of essential surjectivity is a version of "bijective on objects" which does respect the [[principle of equivalence]], i.e. the version which views [[Cat]] as a [[bicategory]].

  In particular, while a functor factors uniquely-up-to-isomorphism as a b.o. functor followed by a fully faithful one, it factors only uniquely-up-to-equivalence as an e.s.o. functor followed by a fully faithful one.  Since b.o. functors are also e.s.o., any (eso,ff) factorization of some functor is equivalent to its (bo,ff) factorization.

* In any 2-category there is a notion of [[eso morphism]] which generalizes the essentially surjective functors in [[Cat]].  In a [[regular 2-category]], these form a [[factorization system in a 2-category]] together with the [[ff morphisms]].

## Related concepts

[[!include properties of functors -- contents]]

[[!redirects essentially surjective functor]]
[[!redirects essentially surjective functors]]
[[!redirects essentially surjective on objects functor]]
[[!redirects essentially surjective on objects functors]]
[[!redirects eso functor]]
[[!redirects eso functors]]
[[!redirects essentially surjective]]