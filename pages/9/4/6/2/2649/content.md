## Idea ##

A connected object is a generalisation of the concept of [[connected space]] from [[Top]] to an arbitrary [[category]].


## Definitions ##

Let $C$ be an [[extensive category]].

Then an [[object]] $X$ of $C$ is **connected** if the [[representable functor]]
$$ hom(X, -): C \to Set $$
preserves all [[coproducts]].  It\'s actually enough to require that it preserves *binary* coproducts.  By definition, $hom(X,-)$ preserves binary coproducts if the canonically defined map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
is always a [[bijection]].

+--{: .query}
[[Mike Shulman]]: It's not obvious to me that preserving binary coproducts is enough to ensure preservation of infinitary coproducts.  Unless you meant "preserves all finite coproducts"?
=--

By this definition, the [[initial object]] of $C$ is *not* connected (except for degenerate cases of $C$).  This matches the notion that the [[empty space]] should not be considered connected, discussed at [[connected space]].
