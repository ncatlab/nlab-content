<div class="rightHandSide toc">
[[!include categorification - contents]]
</div>

## Idea

Decategorification is the reverse of [[vertical categorification]] and turns an $n$-[[n-category|category]] into an $(n-1)$-category.  It corresponds in [[homotopy theory]] to [[truncation]] and taking the [[fundamental n-groupoid]].

+--{: .query}
[[Ben Webster]]: Perhaps something could be said about an extended TQFT $F$?  My understanding was that the decategorification of $F(X)$ was given by $F(X\times S^1)$; is this right?   

[[Urs Schreiber]]: that process certainly makes an $n$-dimensional QFT becomes an $(n-1)$-dimensional one. It is pretty much exactly the mechanism of fiber integration.

So this certainly does have a _flavor_ of decategorification. But the latter also has a precise sense in terms of taking equivalence classes in a category. So at face value fiber integration is something different. But perhaps there is some change of perspective that allows to regard it as decategorification in the systematic sense.

=--

## Definitions

Given a ([[small category|small]] or [[essentially small category|essentially small]]) [[category]] $C$, the [[set]] of __[[isomorphism]] classes__ $K(C)$ of objects of $C$ is called the **decategorification** of $C$.

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

Therefore one way to think of [[vertical categorification]] is as a [[right inverse]] to decategorification.


## Extra structure ##

If the category in question has extra structure, then this is usually inherited in some decategorified form by its decategorification. For instance if $C$ is a [[monoidal category]] then $K(C)$ is a [[monoid]].

A famous example are [[fusion category|fusion categories]] whose decategorifications are called _[[Verlinde ring]]s_.

There may also be extra structure induced more idirectly on $K(C)$. For instance the [[K-theory|K-group]] of an [[abelian category]] is the decategorification of its category of bounded [[chain complexes]] and this inherits a group structure from the fact that this is a [[triangulated category]] (a [[stable (∞,1)-category]]) in which there is a notion of [[fibration sequence|homotopy exact sequences]].


## Further examples ##

* The decategorifications of finite [[set]]s and finite [[vector space]]s are [[natural numbers]]
  $$
    K(FinSet) \simeq \mathbb{N}
  $$
 
  $$
    K(FinVect) \simeq \mathbb{N}
  $$


...

[[!redirects isomorphism class]]