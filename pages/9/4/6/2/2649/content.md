## Idea ##

A connected object is a generalisation of the concept of [[connected space]] from [[Top]] to an arbitrary [[category]].


## Definitions ##

Let $C$ be an [[extensive category]].

Then an [[object]] $X$ of $C$ is **connected** if the [[representable functor]]
$$ hom(X, -): C \to Set $$
preserves all [[coproducts]]. It\'s actually enough to require that it preserves *binary* coproducts; in that case, notice that we always have a map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
so $X$ is connected if this is always a [[bijection]].

By this definition, the [[initial object]] of $C$ is *not* connected (except for degenerate cases of $C$).  This matches the notion that the [[empty space]] should not be considered connected, discussed at [[connected space]].