[[!redirects global elements]]

# Idea #

One striking difference between [[set theory]] and [[category theory]] is that, while [[objects]] of a [[category]] need not have any other structure, a [[set]] comes equipped with the notion of _element_, identifying other sets which belong to it.  Sometimes, a category turns out to possess a similar structure, designating certain [[morphisms]] as __global elements__ of an object.

# Definition #

If a category $C$ has a [[terminal object]] $1$, a __global element__ of another object $x$ is a morphism $1 \to x$-

So a global element is a [[generalized element]] at "stage of definition" $1$.

For example:

* In [[Set]], global elements are just elements: a function from a one-element set into $x$ picks out a single element of $x$.

* In [[Cat]], global elements are objects: the terminal category $1$ is the [[discrete category]] with one object, and a [[functor]] from $1$ into a category $C$ singles out an object of $C$.

* In a [[topos]], a global element of the [[subobject classifier]] is called a [[truth value]].

* Working in a [[over category|slice category]] $C/b$, a global element of the object $\pi: e \to b$ is a map into it from the terminal object $1_b: b \to b$; i.e., a [[right inverse]] for $\pi$.  In the context of [[bundles]], a global element of a bundle is called a *[[global section]]*.

#Variation#

Many (but not all) of the examples above are [[cartesian closed categories]].  In a more general [[closed category]], a morphism from the unit object to $x$ can be called an _element_ of $x$. For example, an element of an [[abelian group]] $x$ is a morphism form the group $\mathbf{Z}$ of integers to $x$, and of course this equivalent to the usual notion of elment of $x$. But here the adjective 'global' is not used.

In contrast to a global element, a morphism to $x$ from _any_ object $i$ whatsoever may be seen as a [[generalized element]] of $x$. For example, if $i$ is the [[unit interval]] (in topology, chain complexes, etc), then a map from $i$ to $x$ is a *path* (rather than a point) in $x$. Or in a slice category $C/b$, if $\rho: a \to b$ is an [[embedding]], then a morphsism from $\rho$ to $\pi$ is a _local_ section of $\pi$.