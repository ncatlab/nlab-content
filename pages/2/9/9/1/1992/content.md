Sometimes for categories having some fixed property and/or structure, one can produce a recipe which gives (up to suitable equivalence) all the examples (and nothing else). 

There are several typical classes of reconstruction theorems (which are all to some extent related).

__Tannakian reconstruction theorems__ reconstruct an algebraic symmetry object (group, groupoid, gerbe, Hopf algebra, Hopf algebroids) from the monoidal category of representations of that object (typically rigid and symmetric or braided). The correspondence between the summetry object and the corresponding category of representations is called Tannaka duality.
Examples include classical Tannaka theorem and Krein theorem, Doplicher--Roberts reconstruction theorem in physics, Woronowicz's Tannaka duality for compact matrix pseudogroups, Saavedra-Rivano and Deligne reconstruction theorems for neutral and mixed Tannakian categories, Ulrich's reconstruction theorem, reconstruction theorems of Majid, Grothendieck's version of Galois group in algebraic geometry and so on. The notion of the fiber functor (due Grothendieck) is central to these considerations. 

__Reconstruction theorems for schemes__ (or varieties only) reconstruct a scheme (variety) out of the category of qausicoherent or only coherent sheaves (or a derived category version of them). In that class one can find Gabriel--Rosenberg theorem, Bondal--Orlov theorem, reconstruction theorems of [P. Balmer](http://www.math.ucla.edu/~balmer) and of [G. Garkusha](http://www-maths.swan.ac.uk/staff/gg) and so on. There is also a class of reconstructions where for some derived categories a realization as derived categories of representation of quivers can be reconstructed.

There is a large class of __abelian reconstruction theorems__, for example the Gabriel--Popescu theorem. In _topos theory_ the __Giraud theorem__ is also a reconstruction theorem (of a site out of a topos, though a nonuniqueness of the resulting site is involved, not affecting cohomology, hence, according to Grothendieck, nonessential). 

Typically in the proofs of most reconstruction theorems implicitly Yoneda lemma is involved. Various embedding theorems of classes of categories (as well as theorems on realization as quotient categories) are closely related, e.g. Barr embedding theorem and Freyd--Mitchell embedding theorem. 


## Lawvere's Reconstruction Theorem ##

This is a famous result from Lawvere's thesis.

A __finite products theory__ or [[Lawvere theory]] $C$ is a category with finite [[products]] where all objects are finite products of copies of a given object $x$.  A __model__ is a functor $F: C \to Set$ preserving finite products, and a morphism of models is a natural transformation between such functors. This gives us a category $Mod(C)$ of models of $C$.

What is going on here?  A model $F$ is really just a set $F(x)$ together with a bunch of $n$-ary operations coming from the morphisms in $C$, satisfying equational laws coming from the equations between morphisms in $C$. Any sort of algebraic gadget that's just a set with a bunch of $n$-ary operations satisfying equations can be described using a theory of this sort. For example: monoids, groups, abelian groups, rings... and so on. We can describe any of these using a suitable algebraic theory, and in each case, the category $Mod(C)$ will be the category of these algebraic gadgets.

There is a functor

$$R: Mod(C) \to Set$$

which carries each model $F$ to the set $F(x)$. We can think of this as a functor which forgets all the operations of our algebraic gadget and remembers only the underlying set.  This should make you desire a [[adjoint functor|left adjoint]]

$$L: Set \to Mod(C)$$

sending each set to the "free" algebraic gadget on this set. Indeed, such a left adjoint exists!

Given this pair of adjoint functors we we can talk about the category of "finitely generated free models" of our theory.  The objects here are objects of $Mod(C)$ of the form $L(S)$ where $S$ is a finite set, and the morphisms are the usual morphisms in $Mod(C)$. Let us call this category $fg Free Mod(C)$.

Here is a way to reconstruct $C$ from its category of finitely generated free models:

+-- {: .un_theorem}
###### Theorem

If $C$ is a Lawvere theory, $C$ is equivalent to $fg Free Mod(C)^{op}$ (i.e., $fg Free Mod(C)$ is equivalent to the opposite of the category $C$). 
=--

+-- {: .proof}
###### Proof

See William F. Lawvere's Ph.D. thesis,  [Functorial Semantics of Algebraic Theories](http://www.tac.mta.ca/tac/reprints/articles/5/tr5abs.html).
=--

In other words, you can reconstruct a Lawvere theory from its category of finitely generated free algebras in the simplest manner imaginable: just reversing the direction of all the morphisms!

The above all continues to apply in suitable form even when we replace "finite products" throughout by any other structure given by limits; e.g., "finite limits", "arbitrary (small) products", or "arbitrary (small) limits". (Of course, for each case, we must also look at a correspondingly wider class of "free" models than merely those freely generated on finite sets; specifically, we recover the theory from its representable models, comprising one "freely generated" model for each object of $C$). In particular, in the "arbitrary (small) products" case, we can recover the theory from its free models on arbitrary sets. Indeed, in this case $L$ takes the particularly nice definition $L(k)(b) = Hom_C(x^k, b)$, and, in fact, the adjunction between $L$ and $R$ is [[monadic]]; that is, $Mod(C)$ is equivalent to the [[Eilenberg–Moore category]] of the monad $RL(-) = Hom_C(x^{(-)}, x)$, with the functors $R$ and $L$ corresponding under this equivalence to the forgetful and free functors of the Eilenberg--Moore construction. In fact, every monad can be seen to arise uniquely in this way, taking $C$ as the dual of its [[Kleisli category]] (automatically a category with small products generated by a single object, as $Set$ is a category with small coproducts generated by the single object $1$, and the Kleisli category is generated by a left adjoint applied to $Set$); thus, we have a correspondence between monads on $Set$ and categories with small products generated by a single object, both equally well representing single-sorted, infinitary algebraic theories, and, in the former setting, the above recoverability result is just the immediate fact that a monad can be recovered from the forgetful functor on its Eilenberg--Moore category (as, indeed, it can of course be recovered from any adjunction giving rise to it).

(This all also works just as well for inescapably multi-sorted theories (that is, even without the restriction that $C$ be generated by a single object); in this case, we can't help but recognize that there are multiple forgetful functors from $Mod(C)$ to $Set$, one for each object of $C$, each with a corresponding free model on $1$ (by the [[Yoneda lemma]]), and, again, the theory is recovered as the dual of the category of all these models (by the [[Yoneda embedding lemma]]))


##References##

* Andr&#233; Joyal and Ross Street, [An introduction to Tannaka duality and quantum groups](http://www.maths.mq.edu.au/~street/CT90Como.pdf), in Part II of _Category Theory, Proceedings, Como 1990_, eds. A. Carboni, M. C. Pedicchio and G. Rosolini,  Lectures Notes in Mathematics __1488__, Springer, Berlin, 1991, pp. 411&#8211;492.

* [UC Davis site with three articles on Tannaka Krein Duality](http://front.math.ucdavis.edu/author/Amini-M*). **This link does not work!**


[[!redirects reconstruction theorems]]
[[!redirects reconstruction]]