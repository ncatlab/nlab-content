
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Decategorification is the reverse of [[vertical categorification]] and turns an $n$-[[n-category|category]] into an $(n-1)$-category.  

It corresponds in [[homotopy theory]] to [[truncated|truncation]].


## Definitions

Given a ([[small category|small]] or [[essentially small category|essentially small]]) [[category]] $C$, the [[set]] of __[[isomorphism classes]]__ $K(C)$ of objects of $C$ is called the **decategorification** of $C$.

This is a [[functor]]

$$
  K : Cat \to Set
$$

from the category (or even $2$-[[2-category|category]]) [[Cat]] of (small) categories to the category (or [[locally discrete 2-category]]) [[Set]] of sets. Notice that we may think of a [[set]] as [[0-category]], so that this can be thought of as

$$
  K : 1Cat \to 0Cat
  \,.
$$


Decategorification decreases categorical degree by forming equivalence classes. Accordingly for all $n \gt m $ and all suitable notions of [[higher category theory|higher categories]] one can consider decategorifications

$$
  n Cat \to m Cat
  \,.
$$

For instance forming the [[homotopy category of an (∞,1)-category]] means decategorifying as

$$
  (\infty,1)Cat \to 1 Cat
  \,.
$$

Therefore one way to think of [[vertical categorification]] is as a [[right inverse]] to decategorification.

## Decategorification of a 2-category ##

A precise way to define the decategorification of a 2-category in the above sense is to identify all 1-arrows which are 2-isomorphic (note that this defines an equivalence relation on 1-arrows and respects composition), and to discard the 2-arrows.

## Example ##

The decategorification, in the above sense, of the 2-category of (small) groupoids is equivalent to the (homotopy) category of [[homotopy 1-types]].

The decategorification in the same sense of the 2-category of (small) categories is equivalent to the full [[homotopy category of topological spaces|homotopy category]].

## Extra structure ##

If the category in question has extra structure, then this is usually inherited in some decategorified form by its decategorification. For instance if $C$ is a [[monoidal category]] then $K(C)$ is a [[monoid]].

A famous example are [[fusion category|fusion categories]] whose decategorifications are called _[[Verlinde ring]]s_.

There may also be extra structure induced more directly on $K(C)$. For instance the [[K-theory|K-group]] of an [[abelian category]] is the decategorification of its category of bounded [[chain complexes]] and this inherits a group structure from the fact that this is a [[triangulated category]] (a [[stable (∞,1)-category]]) in which there is a notion of [[fibration sequence|homotopy exact sequences]].


## Further examples ##

* The decategorifications of finite [[set]]s and finite dimensional [[vector space]]s are [[natural numbers]]
  $$
    K(FinSet) \simeq \mathbb{N}
  $$
 
  $$
    K(FinVect) \simeq \mathbb{N}
  $$


...

[[!redirects decategorifications]]

[[!redirects decategorification]]
[[!redirects decategorified]]
[[!redirects decategorifies]]
[[!redirects decategorify]]
[[!redirects decategorifying]]

