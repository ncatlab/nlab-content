
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A connected object is a generalisation of the concept of [[connected space]] from [[Top]] to an arbitrary [[category]].


## Definitions

Let $C$ be an [[extensive category]].

Then an [[object]] $X$ of $C$ is **connected** if the [[representable functor]]
$$ hom(X, -): C \to Set $$
preserves all [[coproducts]].  It\'s actually enough to require that it preserves *binary* coproducts.  By definition, $hom(X,-)$ preserves binary coproducts if the canonically defined map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
is always a [[bijection]].

+--{: .query}
[[Mike Shulman]]: It's not obvious to me that preserving binary coproducts is enough to ensure preservation of infinitary coproducts.  Unless you meant "preserves all finite coproducts"?

_Toby_:  I just copied what was at [[connected space]].  It\'s true that homming out of a connected space preserves all coproducts, but it\'s not clear to me whether that is a theorem at this level either.  Maybe we need to distinguish finitarily connected objects of finitarily extensive categories from infinitarily connected objects of infinitarily extensive categories?
=--

By this definition, the [[initial object]] of $C$ is *not* connected (except for degenerate cases of $C$); it is [[too simple to be simple]].  This matches the notion that the [[empty space]] should not be considered connected, discussed at [[connected space]].


## Examples

* Connected objects in [[Top]] are precisely [[connected topological space]]s. 

* For a [[group]] $G$, connected objects in the category $G Set$ of [[permutation representation]]s are precisely the ([[inhabited set|inhabited]]) transitive $G$-sets. 

* Objects in a [[locally connected topos]] such as $G$-$Set$ are [[coproduct]]s of connected objects. 


[[!redirects connected objects]]