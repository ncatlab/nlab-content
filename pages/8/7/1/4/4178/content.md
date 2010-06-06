## Idea

A *paracategory* is a [[category]] where [[composition]] is only partially defined.

The definition is "unbiased" in that it comes with basic (partial) $n$-ary composition operations for all $n$, and unlike in the total case these cannot always be reduced to binary and nullary operations.  A paracategory in which all the composites are generated from binary and nullary ones is sometimes called a *precategory*.

## Definition

A **paracategory** is a [[quiver]] $C_1 \rightrightarrows C_0$ together with the following structure.  We write $C_n$ for the iterated pullback $C_1 \times_{C_0} \dots\times_{C_0} C_1$, the set of length-$n$ strings of composable arrows.

* [[partial function|Partial functions]] $\circ_n \colon C_n &#8640; C_1$, over $C_0\times C_0$

* $\circ_0 \colon C_0 \to C_1$ is total, so all identity arrows exist.

* $\circ_1\colon C_1 \to C_1$ is the identity.

* If $\circ_n \vec{y}$ is defined, then $\circ_{m+1+k}(\vec{x},\circ_n \vec{y},\vec{z}) = \circ_{m+n+k}(\vec{x},\vec{y},\vec{z})$ (the equality being [[Kleene equality]]).

A **functor** between paracategories is a quiver morphism $f\colon C\to D$ such that if $\circ_n \vec{x}$ is defined, then so is $\circ_n \vec{f(x)}$ and it equals $f(\circ_n \vec{x})$.  A **Kleene functor** is a functor such that if $\circ_n \vec{f(x)}$ is defined, then so is $\circ_n \vec{x}$; this is equivalently a quiver morphism such that $\circ_n \vec{f(x)}=f(\circ_n \vec{x})$ is a [[Kleene equality]].

## Examples

* If $D$ is any category and $C$ is a subclass of arrows in $D$ containing all the identities, then $C$ becomes a paracategory whose objects are the objects of $D$, whose arrows are the arrows in $C$, and where the composite of a string of arrows is defined iff the composite of that string in $D$ happens to lie in $C$.

* [[extranatural transformations]] and [[dinatural transformations]] form paracategories, since they are not always composable.  This is exploited in the definition of [[extraordinary 2-multicategory]].  This example can also be regarded as a case of the previous example, where the ambient category $D$ consists of "unnatural transformations."

* In fact, if $Cat_P$ denotes the category of categories equipped with a subclass of arrows containing the identities, then the functor $Cat_P \to ParCat$ defined above is actually a [[coreflection]], i.e. it has a [[fully faithful functor|fully faithful]] [[left adjoint]].  In particular, any paracategory is isomorphic to one obtained from a class of arrows in some category, and moreover in a universal way.

## Paracategories as generalized multicategories

Paracategories, and more general "partial algebras," can be considered as a special case of [[generalized multicategories]]; see the papers of Hermida.

## References

The definition is due to [[Peter Freyd]] in apparently unpublished work.  It has been studied further in the papers:

* [[Claudio Hermida|Hermida]] and Mateus, "Paracategories I: Internal Paracategories and Saturated Partial Algebras"

* [[Claudio Hermida|Hermida]] and Mateus, "Paracategories II: Adjunctions, fibrations and
examples from probabilistic automata theory"

[[!redirects paracategories]]
[[!redirects precategory]]
[[!redirects precategories]]
[[!redirects partial category]]
[[!redirects partial categories]]
