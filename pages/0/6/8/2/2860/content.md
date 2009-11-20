{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:forklaring: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: forklaring}
### Initial Purpose of Page ###
The ideas on this page are things that I, [[Andrew Stacey]], want to use.  I suspect that they are well-known and well-developed in the literature but have no idea how to track them down.  So I'm expounding on them here in the hope that some kindly soul will fill in the gaps for me.
=--

+-- {: .query}
So should we merge this with [[PRO]] now?  ---Toby

Yes.  However, not knowing what is standard and what isn't, I'm not sure I could do that merge.  The stuff on this page is what I want to know about so I don't want to lose any of it in the merge. ---Andrew

Understood.  I\'m not sure how to do it either, but I\'ll think about it.  ---Toby

I should say that if any of this _doesn't_ fit in the merge then I'm happy for it to find a home elsewhere.  My main purpose in scribbling this lot is to find out what is and isn't known so I don't have to reprove the known stuff just to make use of it. ---Andrew

Now I want to wait until Todd figures out what you really want to do here.  (^_^)  ---Toby
=--


### The Basic Idea ###

The idea is that one tries to "do" [[universal algebra]] in a [[monoidal category]] by using the monoidal products in place of the standard cartesian ones.  The extent to which this is possible is closely related to the extent to which the monoidal product resembles the cartesian product of sets.

### In More Detail ###

Let us consider only finitary theories; that is, with [[Lawvere theories]].  In categorical language, recall that a Lawvere theory is  a [[category]] $T$ with finite cartesian products in which every object is isomorphic to a finite cartesian power of a distinguished object.  A model for that theory in some category $C$ is then a product-preserving functor $T \to C$.  In a [[monoidal category]], we can ask for this to be a _monoidal_ functor.

The problem with this naive definition is that as the product in $T$ **is** the cartesian product, it comes along with a whole heap of extra structure that may not be strictly needed.  We therefore need to weaken the definition of a Lawvere theory.

+-- {: mynumdef #monlawth}
###### Definition
A **monoidal Lawvere theory** is a monoidal category $(T, \otimes, I)$ in which every object is isomorphic to a finite monoidal product of some distinguished object.
=--

It will be important for later to note what is missing between a __monoidal__ Lawvere theory and an ordinary one.  The missing components are:

1. No projection morphisms; e.g. $x^n \to x$
2. No diagonal morphisms; e.g. $x \to x^n$
3. No symmetry morphisms; e.g. $x^2 \to x^2$

With this definition, we can define a model of such a theory in a monoidal category.

+-- {: mynumdef #model}
###### Definition
Let $(C, \otimes, I)$ be a [[monoidal category]].  Let $(T, \otimes, I)$ be a  monoidal Lawvere theory.  A **monoidal $T$-object** in $(C,\otimes, I)$ is a monoidal functor $T \to C$.
=--

### The Trade ###

Any Lawvere theory is automatically a monoidal Lawvere theory and so one can consider monoidal models of an ordinary Lawvere theory in a monoidal category.  However, as ordinary Lawvere theories have all the extra structure of projections, diagonals, and symmetry, the underlying object (i.e. the image of the distinguished object in the Lawvere theory) needs to have them as well.  Indeed, if one were looking for candidates for such models one would be well-advised to look in the subcategories of objects which have such structure.  Let us therefore give these names.

+-- {: mynumdef #cartcats}
###### Definition
Let $(C, \otimes, I)$ be a monoidal category.  We define the following full subcategories of $C$.

1. $C^{\operatorname{sym}}$ is the largest **symmetric** monoidal subcategory.  That is, it is the full subcategory where the switcheroo functor is naturally isomorphic to the identity.
2. $C^{\operatorname{co}}$ is the subcategory of commutative, associative, unital **comonoids**.  Note that we take morphisms in $C$, not morphisms of comonoids.  These are the objects that come equiped with diagonal and projection morphisms.
=-- 

+--{.query}

[[Todd Trimble|Todd]]: Sorry, I don't know what you mean by the switcheroo functor for a monoidal category. 

There is what is called the [[center]] of a monoidal category, which is a braided monoidal category. The center of the center should be symmetric monoidal (although I'd have to think this through again carefully). Comonoids in the center or center of center form a monoidal category, and I'm thinking something like this would be a natural habitat to consider. 

[[Andrew Stacey|Andrew]]: Knowing that none of my terminology would be right, I let myself get carried away there.  Apologies.  I mean the functor that swaps the order of the product, namely that takes $A \otimes B$ to $B \otimes A$.  (Actually, now I come to think about it I'm not convinced that such must exist in an arbitrary monoidal category.)  What I mean is that if I have a monoidal category then even if it isn't symmetric, there may still be an object that is itself symmetric.  I guess I don't need the category of such to be symmetric monoidal and I don't need it to commute with products of other objects, just with itself.  So I could still have a commutative monoid in an arbitrary monoidal category.

Or maybe I can't.  Now I write it, it seems a lot more tenuous than when I thought it.  It'd be useful to get that clear.

[[Todd Trimble|Todd]]: Not sure I can add anything else useful right now. I don't think there's a general switcheroo functor. In some sense a monoidal functor $Fin^{op} \to M$ to a monoidal category $M$ ought to simulate a cocommutative comonoid in $M$, but I'm not sure how useful an observation this is for you. 

Is there a specific setting you have in mind where what you want to do is unproblematic? 

[[Andrew Stacey|Andrew]]: Yes.  I want to do it in the category of models in set of a [[commutative algebraic theory]].  Over there, it doesn't say anything about the monoidal structure being symmetric but I have an inkling that it is.  However, not every object is a coalgebra.

(As a little background: I'm returning to some stuff that I thought about a while ago and am trying to finish off, but I don't remember all of what I thought when I originally thought about it which is why I'm not as clear as I would like to be)

_Toby_:  Even in a symmetric monoidal category, I don\'t know how to define a functor that takes $A \otimes B$ to $B \otimes A$.  Of course, there is a functor $C \times C \to C$ that takes $(A,B)$ to $B \otimes A$, but that doesn\'t help as far as I can see.

There\'s an inherent problem with considering the largest (or any) symmetric subcategory of a given monoidal category, which is that being symmetric is not a property but a structure on a monoidal category.  So it\'s more like looking for the largest commutative submonoid of a given *set* than looking for the largest commutative submonoid of a given monoid.

Even if that worked, I wouldn\'t understand the full subcategory of CAU comonoids, since again being a CAU comonoid is not a property but a structure on an object in a given symmetric monoidal category.  This is like asking for the full subcategory of $Set$ consisting of groups; it doesn\'t parse.  At best, I would understand this as the full subcategory of sets that have at least one group structure, but you\'re no longer keeping track of that structure (and in fact, at least assuming the axiom of choice, this is just $Set \setminus \{\empty\}$, which has nothing much to do with groups at all).

[[Andrew Stacey|Andrew]]: Okay, let me be absolutely specific here.  I was trying to get at the general story first, but that's the wrong way round for _here_ (it's the right way round for the paper, but that's once I've understood what the general story is!).

This is tied up with [[Tall-Wraith monoids]].  If you start with a set and take the free ring on that set, then that's again a biring (co-ring object in rings).  Now start with abelian groups instead.  If you take the free ring on an abelian group, then that's not a biring, but still has a certain amount of co-structure because a ring is a monoid in $(Ab, \otimes, \mathbb{Z})$.  To make it a biring, I need to start with a coalgebra - that's enough to supply the missing pieces of the co-structure.

*  _Toby_:  OK, this makes sense.  In general, you start with a comonoid in your monoidal category; a comonoid in $(Ab,\otimes)$ is a coalgebra, while a comonoid in $(Set,\times)$ is simply a set (by an argument that applies whenever the monoidal category is cartesian).

Furthermore, if I wish to interpret the resulting biring as representing a functor from abelian groups to rings, then I can only do so on the subcategory of coalgebras - but I need to take abelian group homs not coalgebra homs.

*  _Toby_:  H\'m, this is odd.  I still don\'t know exactly what the 'subcategory' of coalgebras is, since being a coalgebra is not a property of an abelian group.  Since the forgetful functor from coalgebras to abelian groups is faithful, you can make it a literal [[subcategory]] up to equivalence, then consider the corresponding full subcategory; or (equivalently) just take the category whose objects are coalgebras and whose morphisms are homomorphisms of the underlying abelian groups.  (In general, this concept is the [[full image]] of a functor; here we are taking the full image of the forgetful functor from coalgebras to abelian groups.)

   But I don\'t understand why you need to use this instead of simply the category of coalgebras.  After all, if you have a functor from the full image, then you certainly have a functor from the category of coalgebras by composing with the inclusion functor of coalgebras into the full image.  On the other hand, it seems very strange that you can define this functor on arbitrary abelian group homomorphisms.  Applying this to abelian group isomorphisms, you are basically saying that, if you start with two different coalgebra structures on a given abelian group, the resulting birings will be isomorphic.  Is that true?

   Andrew --- Okay, I still wasn't being completely clear.  I _do_ mean the category of coalgebras.  But the _functor_ is constructed by taking the composition of the functor from coalgebras to abelian groups and _then_ taking the hom-functor _in abelian groups_ with a biring.  So if $C$ is a coalgebra and $B$ is a biring then I want to consider $Hom_{Ab}(C,B)$.  That's again a ring and it's functorial for _coalgebra_ morphisms.

   Phew!  "Oh what a tangeled web we weave, when first we practise to understand category theory."

This all generalises quite nicely: replace abelian groups by a [[commutative algebraic theory]] and replace rings (rather, replace monoids) by a [[PRO]].  Then the PRO-objects in the commutative algebraic theory will again be an algebraic theory and the free functor from the commutative theory to the other one has lots of nice properties.

But this _felt_ like it was a specialisation of an even more general story.  My mistake was to try to guess the general story first rather than tell you the special case.

(Not that I regard this particularly as a _mistake_!  It was enough to learn about [[PRO|PROs]] and it's all part of learning how to ask good questions.)

=--


Thus to be able to consider *arbitrary* Lawvere theories we need to be in the intersection of $C^{\operatorname{sym}}$ and $C^{\operatorname{co}}$.  However, there are many Lawvere theories that do not need such structure.  Accordingly we can interpose a finer classification on Lawvere theories according to whether or not they need the symmetric or comonoid structure.

If one is given a presentation of a Lawvere theory in terms of operations and identities, it is quite simple to identify what level of structure it requires.  The key is to look at the identities and express them in terms of elements (this is, of course, [[evil]]).  An identity consists of two ways of applying operations starting with an ordered list of _distinct_ elements.

1. If an identity involves changing the order of the elements, it needs the symmetric structure.
2. If an identity involves duplicating an element, it needs the diagonal structure.
3. If an identity involves ignoring an element, it needs the projection structure.

### A Worked Example ###

The passage from the theory of unital, associative [[monoids]] to that of [[abelian groups]] is a good illustration of all of this.  The Lawvere theory of unital, associative monoids has a presentation with 2 operations: one zeroary, $1$, and one binary, $\mu$, together with the identities:

1. Associativity
   $$
   \mu(a,\mu(b,c)) = \mu(\mu(a,b),c)
   $$
2. Unit
   $$
   \mu(a,1) = a, \qquad \mu(1,a) = a
   $$

None of these identities involve swaps, repetitions, or omissions and so this presentation is also of a monoidal Lawvere theory (note that $1$ is an operation not an element).

Now let us add in an inverse.  That is, a unary operation $\iota$ with the identities:

1. Inverses
   $$
   \mu(\iota(a),a) = 1, \qquad = \mu(a, \iota(a)) = 1
   $$

These involve both a duplication and an omission.  The duplication is on the left-hand side in each case, the omission on the right.  Note that the starting point for each is the ordered list $(a)$.  Therefore a **group** object in a monoidal category must lie in the subcategory of comonoids.

Let us forget the inverse for a moment and add in the commutativity identity instead.  This is the identity:

1. Commutativity
   $$
   \mu(a,b) = \mu(b,a)
   $$

This obviously involves a swap, and thus requires a _symmetric_ object as its model.

Finally, for an abelian group object we need both: symmetry and comonoid.

### Representing Functors ###

One of the applications of Lawvere theories is to the theory of representing objects.  Under mild conditions, a model of a Lawvere theory is equivalent to a lift of a representable contravariant functor $C \to \operatorname{Set}$ to a functor $C \to \operatorname{Set}T$, where $\operatorname{Set}T$ is the category of models of $T$ in $\operatorname{Set}$.  However, except for very simple theories (i.e. those with no binary or higher operations), this does not carry over to the monoidal case because the construction of the operations on the Hom sets involves extensive use of diagonal morphisms.

However, where it does work is when one restricts to the subcategory of comonoid objects _with comonoid-structure preserving morphisms_.  That is, if $C^{\operatorname{co}}_{c}$ denotes the subcategory of $C$ of comonoids with such morphisms then a model $G$ for $T$ in $(C,\otimes,I)$ represents a functor $C^{\operatorname{co}}_{c} \to \operatorname{Set}T$ via

$$
C^{\operatorname{co}}_c \to C \overset{Hom(-,G)}{\to} \operatorname{Set}T
$$

### Questions ###

Apart from the obvious question of finding the literature behind all of this (and thus getting the terminology correct), certain other questions spring to mind.  Well, okay, one question springs to mind.

1. Suppose that I have two monoidal Lawvere theories, $T_1$ and $T_2$, that are equivalent as ordinary Lawvere theories.  Are they equivalent as monoidal Lawvere theories?  More concretely, suppose that I have two presentations for the same Lawvere theory in terms of operations and identities and both define monoidal Lawvere theories (so neither has identities involving repetition, omission, or exchanging[^minute]), are the **monoidal** Lawvere theories equivalent? 

_Todd_: My previous answer (which has been deleted) was based on a too-hasty reading of the question. I'll try to set aside some time to find a better answer. 

###References###

S. Lack, Composing PROPS, [Theory Appl. Categ.](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html) 13 (2004), No. 9, 147--163. 

[^minute]: I keep wanting to write "repetition, hesitation, or deviation".