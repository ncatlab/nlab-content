> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

## Invitation to Categories 

### Preview

The first thing to highlight is that category theory is the theory of *duality*.

Of course, its basic notions are that of "categories", "functors" and "natural transformation", but by themselves, these are just an *organizing principle* for mathematical concepts. That's what the term "*category*" is referring to.

Which is already useful, no question. For example, [Geroch 1985](https://ncatlab.org/nlab/show/category+theory#Geroch85): *Mathematical Physics* is a textbook that is largely concerned with showing how key mathematical concepts used in mathematical physics are organized into categories (Vector spaces, Lie algebras, Lie groups, Topological spaces, ...).

But the actual *theory* supported by categories, as a body of powerful theorems, begins only in the next step, with the notion of *adjunction*, a general notion of *duality*.

This important fact is sometimes overlooked by beginners (and not so beginners), who see just the basic concept formation of categories, functors, and natural transformations and wonder what all the fuss is about and that category theory seems to have "no theorems". Indeed, that's because the actual theory starts only in the next step, with adjunctions and the universal constructions that these encode.



### Categories

So what is a category? First of all its a set (or a class) of things, like in set theory. For instance vector spaces make a category, or Lie algebras make a category. There are more exotic kinds of categories (non-concrete categories) but to begin with it is good to think of a category literally as a "category of mathematical structures".

So what is the difference then to a set (or class)? It's that categories actually know about the *structure* of these mathematical structures. Beyond just collecting all these structures indiscriminently in a large bag, in a category the nature of these structures is transparently alive.

So how does this work? The key idea here is *structuralism*: The idea that to know the nature of a mathematical object is to know how it *relates* to all other objects of its kind (namely: in its category!); and by that we mean: To know the *homomorphisms* between these objects, namely the ways of consistently "mapping them" or "transforming them" into each other.

For instance, consider a topological space $X$, an object of the category $Top$ of topological spaces. (Think of a manifold, if you like, for instance think of the 2-sphere.) To get a first idea of what this topological space is like we want to know the points that it consists of, hence the elements of its underlying set. To get our hands on these, in an operational manner, consider the singleton space, $\ast$, the one that consist of just a single point and nothing else. Then picking a map $\ast \longrightarow X$ is exactly the same as picking a point of $X$! Hence the underlying set of points of $X$ is "relationally" or "structurally" identified with the set of maps $\ast \longrightarrow X$. We are *probing* $X$ by the abstract point $\ast$ to discover all the actual points inside $X$.

But, of course, in $X$, all these points are not disconnected, but the main part of the structure of $X$ is how these points are "bound to" each other, how they *cohere*. To detect that in a relational way, consider the real line $\mathbb{R}$ with its usual topology. Then consider the maps $\mathbb{R} \longrightarrow X$. These maps, of course, are now continuous *curves of points* in $X$. Their collection gives us some finer idea of the structure of the space $X$. For example, we can detect that $X$ has two disconnected components (if it does) once we see that (if this is the case) there are two points of $X$ which never appear jointly as images of a map $\mathbb{R}^1 \longrightarrow X$.

> We may also look at maps the other way around: $X \longrightarrow \mathbb{R}$ or, say, $X \longrightarrow \mathbb{C}$. Under pointwise product, the collection of these maps forms an algebra, in fact a (commutative non-unital) "C-star algebra". It turns out that from these algebras one may recover much of the information about the spaces $X$ (a first example of general *duality between geometry and algebra*, here called "Gelfand duality").

To learn more about the topological space $X$, we would *probe* it by yet more of its peers. Considering maps like $\mathbb{R}^n \longrightarrow X$, etc. 

In this manner it turns out that the structure of $X$ is fully determined, relationally: To know the system of *all* sets of maps $U \longrightarrow X$ from *all* other topological spaces $U$ into $X$ is to known $X$! This fact is the infamous *Yoneda lemma*.

We still haven't said what a category actually is, but now we are ready to do so: In view of this observation/claim that a mathematical structure is fully determined (relationally, structurally) by how it maps to/from other mathematical structures of its kind, hence in its category, it is a most elegant idea to declare that a category of mathematical structures is

* the set (class) of all of them

* together with all maps (homomorphisms) *between them*.

That's the simple idea. Passing from sets (classes) to categories of things means to retain not just the things themselves, but their relation to each other by way of all the maps between them.

And then we bootstrap that into a definition of mathematical structures by making it the definition of a category: 

A category is a set (class) of *objects* $X, Y, \cdots$ together with sets of maps/homomorphisms $X \longrightarrow Y$ between any pair of them.

All we need to add here is a info that these "maps" really behave like maps are meant to behave. Which means: If we have any pair of consecutive maps $X \xrightarrow{f} Y \xrightarrow{g} Z$, then there should be a specified "composite" map $X \xrightarrow{ g \circ f } Z$. And this composition should be associative and unital, in the evident sense.

So: *Categories are sets/classes with maps between their elements.*

In the example of categories of topological spaces, the elements are the topological spaces and the maps are the usual continuous functions.

Generally, for mathematical structures like groups or algebras, they are the elements of categories whose maps are the standard homomorphic functions between them.

But the profound idea of category theory at this point is that the maps/morphisms in a category *need* not be *declared* as *actual maps* that map points to other points. Because in order to say that maps are mapping points around, we are already assuming that we can and have "looked inside" our objects to inspect them what they consist of. But, no, we can be fully "structural" and 'relational" and just remember that for a pair $X$, $Y$ of obejcts, there is *some set* of would-be maps between them, called $Hom(X,Y)$ (for *homomorphisms*), and some rule for how to compose these, when composable.


A basic example of a "non-concrete" category, whose objects are not "sets with extra structure" and whose "maps" don't map points around is the "delooping groupoid" $\mathbf{B}G$ of a group $G$. This category has a single object, $\ast$, and it has one morphism $\ast \xrightarrow{g} \ast$ for each element $g \in G$. The composition rule for morphisms is given by the group operation. This category exhibits the idea of the "quintessential $G$-symmetry", in that its object $\ast$ is a thing we know nothing about except that the group $G$ *operates* on it.

To make this more vivid, consider a "concrete" category like the category $Set$ of sets, and consider the 3-element set $\{1,2,3\}$ in there. Then consider the group of all maps/morphisms from this set to itself, which are invertible under the composition operation. This is the "permutation group" or "symmetric group" $Sym(3)$ on three elements. 

But before long we might be considering this group as an abstract group, without necessarily remembering how exactly its elements actually act on the set $\{1,2,3\}$, for instance since it might actually be acting on another set, like $\{a,b,c\}$. As such, we are just looking at the one-object category $\mathbf{B}Sym(3)$. 

So then we want to say that by remembering $\{1,2,3\}$ as the actual object being acted on by the group of 3-element permutation, we have found an "image" the category $\mathbf{B}G$ inside the large category $Set$.

This notion of "image" of one category inside another is the notion of *functor* between categories.


### Functors

The maps $S \longrightarrow T$ between sets are *functions*, mapping each element of $S$ to an element of $T$. Since categories are sets (or classes) with maps between them, we clearly want the *maps of categories* to respect/preserve this structural information. Such a "function extended from elements to the maps between them" is called a *functor*.

Concretely, a functor $\mathcal{C} \xrightarrow{F} \mathcal{D}$ between categories is a function $F_0$ mapping their objects, and a function $F_1$ mapping their maps, morphsism, such that $F_1$ is a homomorphism for the composition operation on maps.

So if $C_1 \xrightarrow{f} C_2 \xrightarrow{g} C_3$ composes to $C_1 \xrightarrow{ g \circ f } C_3$ in $\mathcal{C}$, then under a functor $F$, $F_0(C_1) \xrightarrow{F_1(f)} F_0(C_2) \xrightarrow{F_1(g)} F_0(C_3)$ composes to $F_0(C_1) \xrightarrow{ F_1(g \circ f) } F_0(C_3)$ in $\mathcal{C}$.

Let's look at a basic example, a functor $\rho : \mathbf{B}G \longrightarrow Vect$, from the delooping groupoid of a group $G$ to the category of vector spaces:

* The single object $\ast$ of $\mathbf{B}G$ is sent by the functor to some object $V$ of $Vect$, hence to a vector space.

* Each morphism $\ast \xrightarrow{g} \ast$ of $\mathbf{B}G$ is sent to some endomorphism $V \xrightarrow{\rho_g} V$ in $Vect$, hence to a linear map!.

* Such that composition is respected: $\rho_{g_2} \circ \rho_{g_1} = \rho_{ g_2 \cdot g_1 }$.

But this is exactly the data of a *linear representation* of the group $G$:

*Functors $\mathbf{B}G \longrightarrow Vect$* are equivalently linear representations of $G$.

This illustrates nicely how, with categories being *sets relationally retaining the structre of their elements*, so functors are "structure-preserving images" of collections of such relational sets within each other --- where we remember that "structures" are relationally encoded by maps between objects, so that "structure-preservation" is the homomorphic preservation of the composition operation on these maps.


### Natural transformations

Natural transformations are most transparently grasped by a picture, but let's try it in words.

Consider a pair of functors $F, G \colon \mathca{C} \longrightarrow \mathcal{D}$. If these were functions between sets, then their images would either coincide or not. But since the category $\mathcal{D}$ retains the structural relations between its elements, it now makes sense to ask whether and how the *whole image of $F$ is related to the image of $G$*!

If we think of these images as networks (graphs) of objects with maps between them, then we are asking whether we can *move* one network into the other, so that objects come to sit on objects and maps in maps.

This *movement* must be for each object $C$ of $\mathcal{C}$ a map $F(C) \xrightarrow{ \eta_C } G(C)$ between its two images in $\mathcal{D}$. 

But for this to be consistent with all the relational structure we have in these categories, it should be that the compositions that arise now, between the maps in the images (the images of maps under the functors) and these "movement" maps are all compatible with each other. This is the *naturality condition* on the $\eta_C$. 

A *natural transformation* $F \Rightarrow G$ is a collection of such $F(C) \xrightarrow{ \eta_C } G(C)$ for each object $C$ of $\mathcal{C}$ such that these naturality conditions hold.

For example: Consider a pair of functors $\rho, \rho' \colon \mathbf{B}G \longrightarrow Vect$. We saw that these are linear representations. Now a natural transformation between them is a single linear map $V \xrightarrow{\phi} V'$ that *intertwines* the two group actions. In fact, such a natural transformation is precisely an *intertwiner* between these linear representations (a homomorphism of representations).

Incidentally, thereby we have also found a new category: The category of linear representations.

Generally, for $\mathcal{C}$, $\mathcal{D}$ a pair of categories. there is the *functor category* $Func(\mathcal{C}, \mathcal{D})$ between them, whose objects are the functors, and whose maps are the natural transformation.


### Adjunctions


- Hom-functor...




An *adjunction* between a pair of mutually reverse functors 

$
  L \colon 
  \mathcal{C}
  \rightleftarrows 
  \mathcal{D}
  \colon
  R
$

is invertible natural transformation

$$
  Hom\big(L (-), d\big)
  \simeq  
  Hom\big((-), R(-)\big)
$$

So a natural bijection between 

* maps into images of $R$

and

* maps out of image of $L$






(...)


(...)




















 









(...)