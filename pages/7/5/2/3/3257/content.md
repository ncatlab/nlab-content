# Canonical transformations
* table of contents
{: toc}


## Idea

The concept of [[natural transformation]], besides being the natural notion of [[morphism]] in a [[functor category]], was also an attempt by Eilenberg and Mac Lane (as founders of [[category theory]]) to make precise the term 'natural'.  For example, there is a map from a [[vector space]] $V$ to its double dual $V^{**}$ given by a natural transformation between the [[identity functor]] and double dual functors on $Vect$, and this map seems natural in that it can be described in very general way; other terms that one might use besides 'natural' are 'canonical', 'basis/coordinate--free/independent', and 'generally covariant'.  On the other hand, none of the maps from $V$ to $V^*$ in the general case (although there are many) seem particularly natural, and there is no natural transformation from the identity functor to the single dual functor.

However, not every transformation that appears naturally is given by a natural transformation, at least not involving the obvious categories.  Besides natural transformations, we have [[dinatural transformations]] (including [[extranatural transformations]]), and there are constructions that are neither natural nor dinatural.

Arguably, the general coherent (and non-[[evil]]) notion is very similar to a natural transformation but involves only the [[isomorphisms]] in one of the two relevant categories (the [[source]] category).  [[Jim Dolan]] has suggested the term 'canonical' in this respect.  Thus every natural transformation is canonical, but not every canonical transformation is natural.

Another term for canonical transformations is 'core-natural', which is justified by [the first alternative characterisation](#asNatural) below.  To avoid confusion with [[canonical coordinate transformation]]s, one can also use 'canonical map' or 'canonical morphism'.


## Warnings

This formalisation is far from accepted, even the regulars on this wiki.  There is nothing wrong with the definition itself; the question is whether anything like this really captures the meaning of 'canonical'.

Some arguments for this terminology may be found in the examples below, as well as in the Usenet thread in the references.

Do not confuse these with the [[canonical coordinate transformation]]s in [[symplectic geometry]] and [[Hamiltonian mechanics]].


## Definition

Given [[categories]] $C$ and $D$ and [[functors]] $F\colon C \to D$ and $G\colon C \to D$, a __canonical transformation__ $\eta\colon F \to G$ consists of a family of [[morphisms]] of $D$ indexed by the [[objects]] of $C$:

$$ \eta(x)\colon F(x) \to G(x) ,\;\;\; x\colon C ,$$

such that the following diagram commutes for every [[isomorphism] in $C$:

$$ \array {
   F(x)            & \overset{\eta(x)}\to  & G(x) \\
   F(u) \downarrow &                       & \downarrow G(u) \\
   F(y)            & \underset{\eta(y)}\to & G(y)
},\;\;\; u\colon x \overset{\sim}\to y\colon C .$$

Note that, while $u$ must be an isomorphism, $\eta(x)$ need not be.

Although above we have required $F,G$ to be functors on all of $C$, they are only ever applied to isomorphisms; thus, the definition still makes sense if $F,G$ are defined only on the [[core]] of $C$.


## Alternative charactersiations

### As natural transformations
{#asNatural}

A canonical transformation can be understood as a special kind of natural transformation.  Given $F, G\colon C \to D$ as in the definition, we can restrict $F$ and $G$ to the [[core]] (underlying groupoid) $\tilde{C}$ of $C$ to produce $\tilde{F}, \tilde{G}\colon \tilde{C} \to D$.  Then a canonical transformation from $F$ to $G$ is precisely a natural transformation from $\tilde{F}$ to $\tilde{G}$.  For this reason, canonical transformations may also be described as 'core-natural'.

In particular, if $C$ is already a [[groupoid]], then every canonical transformation between functors out of $C$ is natural.

If we extend the definition of canonical transformation to allow $F,G$ to be defined originally only on the core of $C$, then there is no need for the term 'canonical transformation' at all; we simply have a natural transformation from $F$ to $G$.

Accordingly, the main use of the term 'canonical' (as opposed to 'natural') is when $F,G$ are *not* explicitly given.  Instead, we may say that a certain expression for a morphism in $D$, involving a variable for an object in $C$, is 'canonical' in that variable, as a weaker condition than saying that the expression is 'natural' in that variable.


### As functors

Recall that every natural transformation between functors from $C$ to $D$ is given by a [[functor]] from $C$ to the [[arrow category]] $Arr D$; indeed, a functor $C \to Arr D$ specifies both the natural transformation and the functors that it goes between.

In a similar vein, a canonical transformation between functors from $\tilde{C}$ to $D$ is given by a functor from $\tilde{C}$ to $Arr D$.  As such, a canonical transformation is the general coherent notion of an operation from an object of $C$ to a morphism of $D$.


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


[[!redirects canonical transformations]]

[[!redirects canonical map]]
[[!redirects canonical morphism]]

[[!redirects core-natural transformation]]