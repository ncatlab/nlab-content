
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Premonoidal categories
* table of contents
{: toc}

## Idea

A premonoidal category is a generalisation of a [[monoidal category]], applied by [[John Power]] and his collaborators to [[denotational semantics]] in [[computer science]]. There, the [[Kleisli category]] of a [[strong monad]] provides a model of [[call-by-value]] programming languages. In general, if the original category is monoidal, the Kleisli category will only be premonoidal.

Recall that a [[bifunctor]] from $C$ and $D$ to $E$ (for $C,D,E$ [[categories]]) is simply a [[functor]] to $E$ from the [[product category]] $C \times D$.  We can think of this as an operation which is 'jointly functorial'.  But just as a [[function]] to $X$ from $Y$ and $Z$ (for $X,Y,Z$ [[topological spaces]]) may be [[continuous map|continuous]] in each variable yet not [[jointly continuous function|jointly continuous]] (continuous from the [[Tychonoff product]] $Y \times Z$), so an operation between categories can be functorial in each variable separately yet not jointly functorial.

Recall that a [[monoidal category]] is a [[category]] $C$ equipped with a bifunctor $C \times C \to C$ (equipped with [[extra structure]] such as the [[associator]]).  Similarly, a premonoidal category is a category equipped with an operation $C \times C \to C$, which is (at least) a [[function]] on [[objects]] as shown, but one which is functorial only in each variable separately.


## Definition

A __binoidal category__ is a [[category]] $C$ equipped with

*  for each pair $x,y$ of [[objects]] of $C$, an object $x \otimes y$;
*  for each object $x$ a [[functor]] $x \rtimes -$ whose action on objects sends $y$ to $x \otimes y$
*  for each object $x$ a [[functor]] $- \ltimes x$ whose action on objects sends $y$ to $y \otimes x$

A [[morphism]] $f\colon x \to y$ in a binoidal category is __central__ if, for every morphism $f'\colon x' \to y'$, the diagrams
$$ \array {
   x \otimes x'                      & \overset{x \rtimes f'}\to  & x \otimes y' \\
   \mathllap{f \ltimes x'}\downarrow &                            & \downarrow\mathrlap{f \ltimes y'} \\
   y \otimes x'                      & \underset{y \rtimes f'}\to & y \otimes y' \\
   } $$
and
$$ \array {
   x' \otimes x                      & \overset{x' \rtimes f}\to  & x' \otimes y \\
   \mathllap{f' \ltimes x}\downarrow &                            & \downarrow\mathrlap{f' \ltimes y} \\
   y' \otimes x                      & \underset{y' \rtimes f}\to & y' \otimes y \\
   } $$
commute.  In this case, we denote the common composites $f \otimes f'\colon x \otimes x' \to y \otimes y'$ and $f' \otimes f\colon x' \otimes x \to y' \otimes y$.

A __premonoidal category__ is a binoidal category equipped with:

*  an object $I$;
*  for each triple $x,y,z$ of objects, a central [[isomorphism]] $\alpha_{x,y,z}\colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$; and
*  for each object $x$, central isomorphisms $\lambda_x\colon x \otimes I \to x$ and $\rho_x\colon I \otimes x \to x$;

such that the following conditions hold.

*  all possible [[natural transformation|naturality squares]] for $\alpha$, $\lambda$, and $\rho$ (which make sense since we have central morphisms) commute.  Note that when written out explicitly in terms of the functors $x\rtimes -$ and $-\ltimes x$, we need three different naturality squares for $\alpha$.  (But it is possible to rephrase $\alpha$ as a single natural transformation using the slick version below.)
*  the pentagon law holds for $\alpha$, as in a [[monoidal category]].
*  the triangle law holds for $\alpha$, $\lambda$, and $\rho$, as in a monoidal category.

A __strict premonoidal category__ is a premonoidal category in which $(x \otimes y) \otimes z = x \otimes (y \otimes z)$, $x \otimes I = x$, and $I \otimes x = x$, and in which $\alpha_{x,y,z}$, $\lambda_x$, and $\rho_x$ are all [[identity morphisms]].  (We need the underlying category $C$ to be a [[strict category]] for this to make sense.)

Similarly, a **symmetric premonoidal category** is a premonoidal category equipped with a central natural isomorphism $x\otimes y \cong y\otimes x$ (as for $\alpha$, there are two naturality squares unless we use the slick approach), satisfying the usual axioms of a symmetry.


## Slick version

As a [[strict monoidal category]] is a [[monoid]] in the [[cartesian monoidal category]] [[Cat]], so a strict premonoidal category is a monoid in the [[symmetric monoidal category]] $(Cat,\Box)$, where $\Box$ is the [[funny tensor product]].

From this point of view, a binoidal category is just a category $C$ with a functor $C \Box C \to C$

It may be possible to make $(Cat,\Box)$ a [[symmetric monoidal 2-category]], in which a [[pseudomonoid]] object is precisely a non-strict premonoidal category, but if so, nobody seems to have written this up yet.  It is possible, however, to describe part of the structure of a non-strict premonoidal category in terms of $(Cat,\Box)$.  For instance, a binoidal structure on $C$ is precisely a functor $C\Box C \to C$, and the naturality of the associator $\alpha$ can be expressed by saying that it is a natural transformation (with central components) between functors $C\Box C\Box C \to C$.


## Examples

* Every [[monoidal category]] is a premonoidal category.

* If $T$ is a [[strong monad|bistrong monad]] on a monoidal category $C$ (e.g. a strong monad on a braided monoidal category), then the [[Kleisli category]] $C_T$ of $T$ inherits a premonoidal structure, such that the functor $C\to C_T$ is a strict premonoidal functor.  This premonoidal structure is only a monoidal structure if $T$ is a [[commutative monad]].

* A strict premonoidal category is the same as a [[sesquicategory]] with one object, so any object of a sesquicategory has a corresponding premonoidal category whose objects are endomorphisms and arrows are 2-cells.


## Properties

The central morphisms of a premonoidal category $C$ form a [[subcategory]] $Z(C)$, called the __centre__ of $C$, which is a [[monoidal category]].  This defines a [[right adjoint functor]] to the inclusion $MonCat \hookrightarrow PreMonCat$ 
 using the definition of functor of premonoidal categories in [Power-Robinson 97](#PR97).

In the same way that a (strict) monoidal category can be identified with a (strict) [[2-category]] with one object, a strict premonoidal category can be identified with a [[sesquicategory]] with one object.  In fact, a sesquicategory is precisely a category [[enriched category|enriched]] over the monoidal category $(Cat,\otimes)$ described above.

## Morphisms

A notion of (non-strict) *premonoidal functor* is somewhat tricky to define.  Part of the definition is clear: it should be a functor that preserves the tensor product up to specified coherent *central* isomorphism.  However, the tricky part is whether it should also be required to preserve centrality of morphisms (or even just isomorphisms).  Desiderata pulling in opposite directions include:

1. If a premonoidal functor is not required to preserve centrality at least of isomorphisms, then premonoidal functors may not be closed under composition, since we may not be able to define central coherence isomorphisms for $G \circ F$ if $G$ does not preserve the centrality of the coherence isomorphisms for $F$.

1. A morphism $T_1 \to T_2$ of bistrong monads on a monoidal category $C$ induces a functor $C_{T_1} \to C_{T_2}$ which preserves the premonoidal structures *strictly*, hence clearly up to coherent central isomorphism.  However, such a functor does not in general preserve centrality even of isomorphisms; a counterexample can be found in [SL13](#SL13), section 5.2.

It seems unlikely that these desiderata can be reconciled purely in the world of premonoidal categories as usually defined.  One solution is to pass to [[Freyd-categories]], which are essentially premonoidal categories equipped with a family of "special" central morphisms forming a cartesian monoidal category with the same tensor product.  Morphisms of Freyd-categories are easy to define, and include all the morphisms $C_{T_1} \to C_{T_2}$ if $C$ is cartesian (and if it isn't, then there should be a suitable non-cartesian generalization of Freyd-categories).  Other solutions that use different ways of representing a "special subfamily of central (iso)morphisms" are to consider the tensor product functor of a premonoidal category to be a not-necessarily-saturated [[anafunctor]], or (in [[homotopy type theory]]) to allow the underlying category of a premonoidal category to be merely a [[homotopytypetheory:precategory]].

## References

* {#PR97} [[John Power]] and [[Edmund Robinson]], _Premonoidal categories and notions of computation_, Math. Structures Comput. Sci., 7(5):453&#8211;468, 1997. Logic, domains, and programming languages (Darmstadt, 1995). 
 [PostScript](http://www.eecs.qmul.ac.uk/~edmundr/pubs/mscs97/premoncat.ps)

* Alan Jeffrey, _Premonoidal categories and a graphical view of programs,_ [pdf file](http://fpl.cs.depaul.edu/ajeffrey/papers/premonA.pdf)

* {#SL13} Sam Staton and Paul Blain Levy, *Universal Properties of Impure Programming Languages*.  ACM Sigplan Notices, 2013, [doi](https://doi.org/10.1145/2480359.2429091).

[[!redirects premonoidal category]]
[[!redirects premonoidal categories]]
[[!redirects binoidal category]]
[[!redirects binoidal categories]]
