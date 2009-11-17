{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:forklaring: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: forklaring}
### Initial Purpose of Page ###
The ideas on this page are things that I, [[Andrew Stacey]], want to use.  I suspect that they are well-known and well-developed in the literature but have no idea how to track them down.  So I'm expounding on them here in the hope that some kindly soul will fill in the gaps for me.
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
2. $C^{\operatorname{co}}$ is the subcategory of commutative, associative, unital **comonoids**.  Note that we take morphisms in $C$, not morphisms of comonoid.  These are the objects that come equiped with diagonal and projection morphisms.
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

[^minute]: I keep wanting to write "repetition, hesitation, or deviation".