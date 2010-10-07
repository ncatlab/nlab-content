
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Canonical morphisms
* table of contents
{: toc}

## Idea

A *canonical morphism* is a [[morphism]] which is equivariant under an [[automorphism group]], with [[actions]] mediated by two [[functors]].  It may be seen as a [[natural transformation]] in a particular context.  Conversely, canonical morphisms can be combined into a notion of transformation more general than a natural transformation, although this also may be seen as a natural transformation in a particular context.

This usage of the word 'canonical' is due to [[Jim Dolan]].  In general, this term is often used in mathematics to mean that the result of a construction may be specified using only the data at hand, without making arbitrary choices.  The idea behind using the word here is, roughly, that only canonical morphisms may be specified (in the situations in which they appear) without [[evil]].  (Both avoiding arbitrary choices and avoiding evil are related to avoiding the [[axiom of choice]], but that does not seem to be directly relevant.)  However, there are certainly also uses of 'canonical' in mathematics that do not fall under this definition.

Arguably, 'natural' would be a better term for this intuition, but canonical morphisms are more general than the natural transformations that appear in the same contexts, so that word is taken.  Another possible term is 'core-natural' or 'groupoid-natural', since (as will be seen below) canonical morphisms may be interpreted as natural transformations between functors restricted to the [[core]] (underlying [[groupoid]]) of a given category.  The terms 'basis/coordinate--free/invariant' and 'generally covariant' also capture the same intuition, although these tend to be restricted to certain disciplines (linear algebra, geometry, physics).


## Definitions

Given [[categories]] $C$ and $D$, [[functors]] $F, G\colon C \to D$, and an [[object]] $x$ of $C$, a __canonical morphism__ from $F(x)$ to $G(x)$ is a [[morphism]] $h\colon F(x) \to G(x)$ in $D$ such that the diagram

$$ \array {
   F(x)            & \overset{h}\to  & G(x) \\
   F(u) \downarrow &                 & \downarrow G(u) \\
   F(x)            & \underset{h}\to & G(x)
} $$

commutes for any [[automorphism]] $u$ of $x$ in $C$.

As $F$ and $G$ are only ever applied to [[isomorphisms]], this definition makes sense even when they are defined only on the [[core]] of $C$.  In fact, as they are applied only to $x$ and its automorphisms, the definition makes sense when they are defined only on $Aut_C(x)$, the [[automorphism group]] of $x$ in $C$.  In that case, $F$ and $G$ are [[representations]] of $Aut_C(x)$ in $D$, and a canonical morphism is precisely an [[intertwiner]] between these representations.

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


## Examples

Let $G$ be a [[group]], let $C$ be the [[delooping]] $\mathbf{B}G$ of $G$ (that is $G$ thought of as a $1$-object category), let $x$ be the object of $C$.  Then the functors $F,G\colon C \to D$ are simply [[representations]] of $G$ in $D$, and a canonical morphism from $F(x)$ to $G(x)$ is an [[intertwiner]] between these representations.

More generally, let $C$ be a [[groupoid]].  Then a canonical (or core-natural) transformation from $F$ to $G$ is simply a [[natural transformation]] from $F$ to $G$, which should make sense since $C$ is its own [[core]].  If $C$ is any category whatsoever, then a natural transformation from $F$ to $G$ is still a canonical transformation, although in general there are other canonical transformations.

We now consider an example that may serve to further motivate the term 'canonical'.  Given a $2$-element [[set]] $x$, there are $4$ [[functions]] from $x$ to itself, the [[identity function]], the non-identity [[involution]], and the two [[constant functions]].  However, there is no way to specify either constant function without using some property of the specific elements of the set in question; there is no 'canonical' way to define either of those.  Correspondingly, if we take $C$ and $D$ to be [[FinSet]], $F$ and $G$ to be the [[identity functor]] on $Fin Set$, and $x$ to be this $2$-element, then there are only $2$ canonical morphisms from $F(x) = 2$ to $G(x) = 2$: the identity function and the non-identity involution.

If we wish to extend this example to an entire canonical transformation between these $F,G \coloneqq id_{Fin Set}$, then this is actually the only choice that we can make.  This is because, if $x$ has $3$ or more elements, then we have no way to choose among the $2$ or more elements that are not equal to any given element, so only the identity function on $x$ is canonical.  Thus we have $2$ core-natural transformations from $id_{Fin Set}$ to itself, only one of which (the [[identity natural transformation]]) is natural.

On the other hand, if we let $C$ be the category $Fin Ord$ of finite [[well-ordered sets]], then every element of every such set is uniquely identifiable.  Accordingly, given any well-ordered set $x$, every function from (the underlying set of) $x$ to itself is a canonical morphism from $F(x)$ to $G(x)$, where now $F,G$ are both the [[forgetful functor]] from $Fin Ord$ to $Fin Set$.  Now there are infinitely many canonical transformations from this functor to itself, but still only the identity transformation is natural.

Now consider the operation of [[ordinal number|ordinal]] addition on $Fin Ord$.  We add two well-ordered sets $x$ and $y$ by taking their [[disjoint union]] as sets and placing the elements of $x$ before the elements of $y$.  This operation is associative up to a unique isomorphism, which is natural and so makes $Fin Ord$ into a [[monoidal category]].  The operation is also commutative up to a unique isomorphism, but the commutativity transformation is not natural.  Nevertheless, it is canonical (as it must be, being unique).

The examples above are all of canonical *isomorphisms*.  However, we can adjust the last example for a canonical transformation that is not an isomorphism.  Consider two functors from $Fin Ord \times Ord$ to $Ord$, given by ordinal addition in the two possible orders.  The canonical isomorphism in the last paragraph exends to a canonical transformation from $(x, y \mapsto x + y)$ to $(x, y \mapsto y + x)$.  As the canonical isomorphism above encapsulates the equation $x + y = y + x$ for finite ordinal numbers, so this canonical transformation encapsulates the equation $x + y \leq y + x$ for ordinal numbers when $x$ is finite.


## References

* A 1993 [Usenet thread](http://groups.google.com/group/sci.math/browse_frm/thread/9f5ca96dc1a95ada/47a1bb21f6566547) may be the first public introduction of the contrast between 'natural' and 'canonical' by [[Jim Dolan]] (posting as 'Robert Scott'); see particularly posts 9&10.

* A 2010 [MathOverflow question](http://mathoverflow.net/questions/19644/what-is-the-definition-of-canonical) about the meaning of 'canonical', with many different answers, including this one.

An analogous notion for higher functors makes a prominent appearance in [[Chris Schommer-Pries]]'s work on [[FQFT]] with defects/[[bi-brane]]s. See _slide 81_ (the penultimate page) of:

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0))

See [[holographic principle of higher category theory]] for more on that.

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
