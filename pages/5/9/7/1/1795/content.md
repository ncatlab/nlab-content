#Idea#

The notion of _essential image_ is an adaptation of the notion of [[image]] from a [[category theory|1-categorical]] to the 
[[2-category|2-categorical]] context [[Cat]], i.e. to the image of [[functor]]s. 



#Definitions#


(A concrete realization of)
the __essential image__ of a [[functor]] $F: A\to B$ between [[category|categories]] or $n$-[[n-category|categories]] is the smallest [[replete subcategory]] of the target $n$-category $B$ containing the __image__ of $F$, which is in turn the smallest [[subcategory]] which contains all the $n$-cells which are strictly the images of $n$-cells in $A$.  Note that the property of belonging to the image is [[evil]]; of two [[equivalence|equivalent]] objects, one may belong while the other does not.  Passing to the essential image precisely removes this evil.

+-- {: .query}
_Zoran_: I disagree that it removes. Usual image in Set splits maps into epi onto image and mono into target.
If in Cat one splits the functor into functor into image
then the rest can be split into equivalence from image to essential image and a functor form essential image into final category which is fully faithful and replete. Repletness is a part which is still "evil".

_Toby_:  It is *the property of belonging to the image* (said of an object or morphism) which is evil, while the property of belonging to the essential image (said of an object or morphism) is *not* evil.  Of course the property of being equal to the essential image (said of a subcategory) is evil; it must be, as it refers to equality of something other than top-level morphisms.  Even the property of being replete (again, said of a subcategory) is evil ... but $D$ is a replete subcategory of $C$ if and only if the property of belonging to $D$ (said of an object or morphism) is not evil.
=--

Note that:

* the *image* may contain some morphisms or cells which are not the images of any cell in $A$, namely the [[composite|compositions]] of $B$-composable chains of such image cells, whose preimage cells do not form any $A$-composable chain;
* the *essential image* in addition contains precisely all equivalent $k$-cells to the $k$-cells of the image for all $0 \leq k \leq n$.

