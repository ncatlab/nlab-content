# Canonical morphisms
* table of contents
{: toc}


## Idea

A canonical morphism is a [[morphism]] which is equivariant under an [[automorphism group]], with [[actions]] mediated by two [[functors]].  It may be seen as a [[natural transformation]] in a particular context.  Conversely, canonical morphisms can be combined into a notion of transformation more general than a natural transformation, although this also may be seen as a natural transformation in a particular context.

This usage of the word 'canonical' is due to [[Jim Dolan]].  In general, this term is often used in mathematics to mean that the result of a construction may be specified using only the data at hand, without making arbitrary choices.  The idea behind using the word here is, roughly, that only canonical morphisms may be specified (in the situations in which they appear) without [[evil]].  (Both avoiding arbitrary choices and avoiding evil are related to avoiding the [[axiom of choice]], but that does not seem to be directly relevant.)

Arguably, 'natural' would be a better term for this intuition, but canonical morphisms are more general than the natural transformations that appear in the same contexts, so that word is taken.  Another possible term is 'core-natural' or 'groupoid-natural', since (as will be seen below) canonical morphisms may be interpreted as natural transformations between functors restricted to the [[core]] (underlying [[groupoid]]) of a given category.  The terms 'basis/coordinate--free/invariant' and 'generally covariant' also capture the same intuition, although these tend to be restricted to certain disciplines (linear algebra, geometry, physics).


## Definitions

Given [[categories]] $C$ and $D$, [[functors]] $F, G\colon C \to D$, and an [[object]] $x$ of $C$, a __canonical morphism__ from $F(x)$ to $G(x)$ is a [[morphism]] $h\colon F(x) \to G(x)$ in $D$ such that the diagram

$$ \array {
   F(x)            & \overset{h}\to  & G(x) \\
   F(u) \downarrow &                 & \downarrow G(u) \\
   F(x)            & \underset{h}\to & G(x)
} $$

commutes for any [[automorphism]] $u$ of $x$ in $C$.

As $F$ and $G$ are only ever applied to [[isomorphisms]], this definition makes sense even when they are defined only on the [[core]] of $C$.  In fact, as they are applied only to $x$ and its automorphisms, the definition makes sense when they are defined only on the $Aut_C(x)$, the [[automorphism group]] of $x$ in $C$.  In that case, $F$ and $G$ are [[representations]] of $Aut_C(x)$ in $D$, and a canonical morphism is precisely an [[intertwiner]] between these representations.

In the other direction, we can consider a family of canonical morphisms, one for each object of $C$, which are coherent in the sense that

$$ \array {
   F(x)            & \overset{h_x}\to  & G(x) \\
   F(u) \downarrow &                   & \downarrow G(u) \\
   F(y)            & \underset{h_y}\to & G(y)
} $$

commutes for every [[isomorphism]] $u\colon x \to y$ in $C$.  Such a family may be called a __canonical transformation__ from $F$ to $G$, although this should not be confused with a [[canonical coordinate transformation]].  Note that every natural isomorphism is canonical, but not conversely.  The main use of having a term like 'canonical' at all is to say that an expression for a morphism in $D$, involving a variable for an object in $C$, is 'canonical' in that variable, as a weaker condition than saying that the expression is 'natural' in that variable.

By the [[axiom of choice]], if there exists a canonical morphism from $F(x)$ to $G(x)$ for every object $x$, then there exists a canonical transformation from $F$ to $G$ (the converse is obvious).  Actually, this does not require the full axiom of choice; it uses only ... (that groupoid-relevant version, I need to find its name).


## Alternative characterisations
{#asNatural}

As remarked above, [[intertwiner|intertwiners]] between [[representations]] of [[groups]] may be seen as canonical morphisms between functors defined on (the [[delooping]] of) a group.  Conversely, we may *define* a canonical morphism from $F(x)$ to $G(x)$ to be an intertwiner between the restrictions of $F$ and $G$ to the [[automorphism group]] of $x$, thought of as representations of that group.

Simlarly, we may *define* a canonical transformation from $F$ to $G$ to be a [[natural transformation]] between the restrictions of $F$ and $G$ to the [[core]] $\tilde{C}$ of $C$.  This is the origin of the alternative term 'core-natural transformation'.

Finally, we note that just as every natural transformation between functors $F,G\colon C \to D$ defines a [[functor]] from $C$ to the [[arrow category]] $Arr D$ (and conversely), so a canonical transformation between such functors defines a functor from $\tilde{C}$ to $Arr D$ (and conversely if we allow the functors to be defined only on isomorphisms).


***


## Examples

Of course, any [[natural transformation]] is canonical.  A [[dinatural transformation]] (such as an [[extranatural transformation]]) can also be interpreted as a special kind of canonical transformation between functors defined on the core.  Below, we will look at examples that are not natural in any of these ways.

Consider the [[identity functor]] on [[FinSet]].  The only *natural* transformation from $\id_{Fin Set}$ to itself is the [[identity natural transformation]], as can be seen by applying the naturality condition to morphisms of the form $u\colon 1 \to y$.  However, there is another *canonical* transformation, most of whose components are still the [[identity function]] but whose component on a $2$-element set is the non-identity [[involution]].

This example may serve to motivate the term 'canonical'.  If we wish to define a non-identity function from a $2$-element set to itself, there are three options: the involution used in the example above and the two [[constant functions]].  However, there is no way to specify either constant function without using some property of the specific elements of the set in question; there is no 'canonical' way to define either of those (and indeed, we need a form of the [[axiom of choice]], the [axiom of choice from finite sets](http://foldoc.org/russell%27s+attic), to prove that it can be done for all $2$-element sets at once).  If we wish to define a non-identity function from a $3$-element set to itself, then there is no canonical way at all to do this.

On the other hand, consider the category $Fin Ord$ of finite [[well-ordered sets]].  Because these sets are equipped with linear orders, each element is uniquely identifiable, and any of the three non-identity functions from a $2$-element ordered set to itself can be defined canonically.  (Since most of these functions do not preserve the order, we must formalise this in a canonical transformation from the [[forgetful functor]] $U_{Ord}\colon Fin Ord \to Fin Set$ to itself.)  Similarly, we can define non-identity functions on ordered sets with more than $2$ elements, so in all there are infinitely many canonical transformations from $U_{Ord}$ to itself.  However, only the identity transformation is natural, by the same argument as for $id_{Fin Set}$.

Now consider the operation of [[ordinal number|ordinal]] addition on $Fin Ord$.  We add two well-ordered sets $x$ and $y$ by taking their [[disjoint union]] as sets and placing the elements of $x$ before the elements of $y$.  This operation is associative up to a unique isomorphism, which is natural and so makes $Fin Ord$ into a [[monoidal category]].  (The coherence conditions of a monoidal category are automatically satisfied since the isomorphism in $Fin Ord$ is unique.)  The operation is also commutative up to a unique isomorphism, but the commutativity transformation is not natural.  (Thus the monoidal category $(Fin Ord,+)$ cannot be [[symmetric monoidal category|symmetric]] or even [[braided monoidal category|braided]].)  Nevertheless, it is canonical (as it must be, being unique).

The examples above are all of canonical *isomorphisms*.  However, we can adjust the last example for a canonical transformation that is not an isomorphism.  Consider two functors from $Fin Ord \times Ord$ to $Ord$, given by ordinal addition in the two possible orders.  The canonical isomorphism in the last paragraph exends to a canonical transformation from $(x, y \mapsto x + y)$ to $(x, y \mapsto y + x)$.  As the canonical isomorphism above encapsulates the equation $x + y = y + x$ for finite ordinal numbers, so this canonical transformation encapsulates the equation $x + y \leq y + x$ for ordinal numbers when $x$ is finite.


## References

* [old Usenet thread](http://groups.google.com/group/sci.math/browse_frm/thread/9f5ca96dc1a95ada/47a1bb21f6566547) introducing the contrast between 'natural' and 'canonical' (note that 'Robert Scott' is really [[Jim Dolan]])

The notion for higher functors makes a prominent appearance in [[Chris Schommer-Pries]]'s work on [[FQFT]] with defects/[[bi-brane]]s. See _slide 81_ (the penultimate page) here:

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0))


[[!redirects canonical transformation]]
[[!redirects canonical transformations]]

[[!redirects canonical map]]
[[!redirects canonical maps]]
[[!redirects canonical morphism]]
[[!redirects canonical morphisms]]

[[!redirects core-natural transformation]]
[[!redirects core-natural transformations]]
[[!redirects groupoid-natural transformation]]
[[!redirects groupoid-natural transformations]]
