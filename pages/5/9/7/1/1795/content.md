
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# The essential image of a functor
* table of contents
{: toc}

## Idea

The notion of _essential image_ is supposed to be an adaptation of the notion of [[image]] from a [[category theory|1-categorical]] to the 
[[2-category|2-categorical]] context [[Cat]], i.e. to the image of [[functors]]. But some care has to be exercised.

For another definition of image of a functor, see [(2,1)-image](http://ncatlab.org/nlab/show/image#InfImageExamples).



## Definitions

(A concrete realization of) the __essential image__ of a [[functor]] $F: A\to B$ between [[category|categories]] or $n$-[[n-category|categories]] is the smallest [[replete subcategory]] of the target $n$-category $B$ containing the __image__ of $F$.  (The *image* is, in turn, the smallest [[subcategory]] which contains all the $n$-cells which are strictly the images of $n$-cells in $A$.)

Note that if $F$ is not [[pseudomonic functor|pseudomonic]], then its essential image, defined in this way, need not be equivalent to its ordinary image.

## Considerations of the principle of equivalence

Note that the property of "belonging to the image" (said of an object or morphism) breaks the [[principle of equivalence]] of [[category theory]]; of two [[equivalence|equivalent]] objects, one may belong while the other does not.  Passing to the essential image removes this, so that the property of "belonging to the essential image" respects the [[principle of equivalence]].

Of course, the property of "being equal to the essential image" (said of a subcategory) violates the [[principle of equivalence]], as is the property of "being replete".  But $D$ is a replete subcategory of $C$ if and only if the property of belonging to $D$ (said of an object or morphism) does not violate the principle of equivalence.

## Remarks

* the *image* of a functor $F:A\to B$  may contain some morphisms or cells which are not the images of any cell in $A$, namely the [[composite|compositions]] of $B$-composable chains of such image cells, whose preimage cells do not form any $A$-composable chain;
* the *essential image* in addition contains precisely all equivalent $k$-cells to the $k$-cells of the image for all $0 \leq k \leq n$.

[[!redirects essential images]]
