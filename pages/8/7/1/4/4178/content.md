## Idea

A *paracategory* is a [[category]] where [[composition]] is only partially defined.

The definition is "unbiased" in that it comes with basic (partial) $n$-ary composition operations for all $n$, and unlike in the total case these cannot always be reduced to binary and nullary operations.  A paracategory in which all the composites are generated from binary and nullary ones is sometimes called a *precategory*.

## Definition

A **paracategory** is a [[quiver]] $C_1 \rightrightarrows C_0$ together with the following structure.  We write $C_n$ for the iterated pullback $C_1 \times_{C_0} \dots\times_{C_0} C_1$, the set of length-$n$ strings of composable arrows.

* Partial functions $\circ_n \colon C_n \rightharpoonup C_1$, over $C_0\times C_0$

* $\circ_0 \colon C_0 \to C_1$ is total, so all identity arrows exist.

* $\circ_1\colon C_1 \to C_1$ is the identity.

* If $\circ_n \vec{y}$ is defined, then $\circ_{m+1+k}(\vec{x},\circ_n \vec{y},\vec{z}) = \circ_{m+n+k}(\vec{x}\vec{y}\vec{z})$ (the equality being [[Kleene equality]].

## References

The definition is due to [[Peter Freyd]] in apparently unpublished work.  It has been studied further by [[Claudio Hermida]].

[[!redirects paracategories]]
[[!redirects precategory]]
[[!redirects precategories]]
[[!redirects partial category]]
[[!redirects partial categories]]
