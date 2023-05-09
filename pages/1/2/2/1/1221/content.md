
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Karoubian category_ or  _pseudo-abelian category_ (also: pseudoabelian). is a [[pre-additive category]] $C$ such that every [[idempotent]] morphism $p: A \to A$ in $C$ has a [[kernel]], and hence (one can easily show) also a [[cokernel]].

This is stronger than [[pre-additive category|pre-additivity]] but weaker than [[abelian category|abelianness]], which requires that _every_ morphism has a [[kernel]] and [[cokernel]].

These categories are named after the French mathematician [[Max Karoubi]].


## Definition

Let $C$ be a category and $p : X \to X$ an [[idempotent]] [[endomorphism]] of an object $X$.  One says that $p$ **admits an image** if the functor $Ker(id_X, p)$ is [[representable]], and the representing object is called the image of $p$.  Here $Ker(id_X, p)$ is the functor $C^{op} \to \underline{Set}$ mapping

$$ Y \mapsto Ker(Hom(Y, X) \rightrightarrows Hom(Y, X)); \qquad (\ast) $$

in other words the image of $p$ is the [[equaliser|difference kernel]] of $(id_X, p)$, when it exists.

Now $C$ is called **Karoubian** if every idempotent $p$ admits an image. Since $p: X \to X$ is idempotent iff $id_X - p$ is idempotent, this is the same as saying every idempotent has a kernel. 

## Properties

### General

One can show that for any idempotent $p$, $Ker(id_X, p)$ is representable if and only if $Coker(id_X, p)$ is, and that in fact their representing objects are canonically isomorphic.

Recall that one says $p$ **[[split idempotent|splits]]** if there exists an object $Y$, and morphisms $f : X \to Y$, $g : Y \to X$, such that $f \circ g = id_Y$ and $g \circ f = p$.  Observe that when $p$ admits an image $K$, it splits: by definition there are functorial isomorphisms $\Phi_Y$ for all $Y$ between the image of the functor $(\ast)$ and $\Hom(Y, K)$; now take $f : X \to K$ the morphism corresponding to $p$ via $\Phi_X$, $g : K \to X$ the morphism corresponding to $id_K \in Hom(K, K)$ via $\Phi_K$.  Conversely, if $p$ splits via a pair $(f, g)$, then $g: Y \to X$ is a difference kernel of $(id_X, p)$: we have $g = g \circ f \circ g = p \circ g$, and if $h: Z \to X$ satisfies $h = p \circ h = g \circ f \circ h$, then $h$ clearly factors through $g$, and uniquely so since sections $g$ are monomorphisms. 

### Karoubi envelope

There is a [[reflective subcategory|universal functor]] from the category of (say, small) [[preadditive categories]] to the category of Karoubian categories, the __[[Karoubinization functor]]__; its value on a preadditive category $C$ is also called the __[[Karoubian envelope]]__ or the __[[pseudo-abelian completion]]__ of $C$. 

In more detail, there exists a Karoubian category $kar(C)$ associated to any category $C$, and a fully faithful functor $\varphi : C \to kar(C)$, which is [[universal property | universal]] in the sense that for any Karoubian category $C'$, the functor

$$\underline{Hom}(kar(C), C') \to \underline{Hom}(C, C')$$

taking a functor $F : kar(C) \to C'$ to the composite $F \circ \varphi$ is an [[equivalence]] of categories.  $kar(C)$ is called the **[[Karoubi envelope]]** of $C$ (aka the _[[Cauchy completion]]_, or the _[[idempotent-splitting completion]]_).  It can be realized explicitly by taking as objects pairs $(X, p)$, with $p$ idempotent, and as morphisms $(X, p) \to (Y, q)$ the morphisms $f : X \to Y$ that satisfy $f = q \circ f \circ p$.

## Examples

The requirement that, say, a [[dg-category]] or a [[triangulated category]] be Karoubian is a natural requirement in a number of contexts. 

The Karoubian envelope is also used in the construction of the [[category of pure motives]], and in [[K-theory]].

## Related concepts

* [[semi-abelian category]]

* [[quasi-abelian category]]

* [[abelian category]]


## References

* [[Alexandre Grothendieck]], [[Jean-Louis Verdier]].  Exercice 7.5 in _Topos_, Expos&#233; IV of [[SGA 4]], volume 1.

[[!redirects pseudo-abelian category]]
[[!redirects pseudoabelian category]]

[[!redirects pseudo-abelian categories]]
[[!redirects pseudoabelian categories]]

