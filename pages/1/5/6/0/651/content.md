# Basics

+-- {: .num_defn #FroelicherSpace}
###### Definition
A _Fr&#246;licher Space_ is a triple $(X,C_X,F_X)$ where

1. $X$ is a set;
2. $C_X$ is a set of _curves_ in $X$; that is, $C_X \subseteq Set(\mathbb{R},X)$;
3. $F_X$ is a set of _functionals_ on $X$; that is, $F_X \subseteq Set(X, \mathbb{R})$;

subject to the following saturation conditions

1. if $c : \mathbb{R} \to X$ is a morphism of sets with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_X$ then $c \in C_X$, and
2. if $f : X \to \mathbb{R}$ is a morphism of sets with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $c \in C_X$ then $f \in F_X$.

A _morphism_ of Fr&#246;licher spaces, say $(X,C_X,F_X) \to (Y,C_Y,F_Y)$ is a set map $g \colon X \to Y$ satisfying the following (equivalent) conditions:

1. $g c \in C_Y$ for all $c \in C_X$,
2. $f g \in F_X$ for all $f \in F_Y$,
3. $f g c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_Y$ and $c \in C_X$.
=--

Fr&#246;licher spaces and their morphisms form a category with an obvious faithful functor to set.  The properties of this category are as follows.

+-- {: .num_theorem #FroelicherCategory}
##### Theorem
The [[category]] of Fr&#246;licher spaces is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[cartesian closed category|cartesian closed]].  It is [[topological category|topological]] over $Set$.  It is an [[construct|amnestic, transportable construct]].
=--

+--{.query}
[[Andrew Stacey|Andrew]]: I don't think that this category is _locally_ cartesian closed but the only evidence that I have for that is a side remark by Lawvere on the category mailing list.
=--

# Isbell Duality

Fr&#246;licher spaces are examples of [[generalized smooth spaces|generalised smooth spaces]].  They are also examples of [[space and quantity|generalised spaces]] in the following sense.

+-- {: .num_defn #GenSpace}
##### Definition
Let $\mathcal{U}$ be a [[category]].  A _generalised $\mathcal{U}$--space_ is a triple $(C,F,c)$ where $C$ is a [[functor|contravariant functor]] $\mathcal{U} \to Set$, $F$ is a [[functor|covariant functor]] $\mathcal{U} \to Set$, and $c$ is a [[natural transformation]] $C \times F \to \mathcal{U}(-,-)$.  We refer to $c$ as _composition_.

A _morphism of generalised $\mathcal{U}$--spaces_ $(C_1,F_1,c_1) \to (C_2,F_2,c_2)$ is a pair of natural transformations $\alpha : C_1 \to C_2$ and $\beta : F_2 \to F_1$ satisfying the identity $c_1(-,\beta(-)) = c_2(\alpha(-),-)$.
=--

+--{.query}
[[Andrew Stacey|Andrew]]: I presume that we need some hypothesis on $\mathcal{U}$ to ensure that the natural transformations form a set.  Is there a concise way to put this?

We should also settle on a convention for what to call $C$ and $F$.  My notation and nomenclature is obviously influenced by Fr&#246;licher spaces but that's not a good basis for making a decision.
=--

Here, $\mathcal{U}(-,-)$ is the $Hom$--functor on $\mathcal{U}$ (strictly, $\mathcal{U}^{op} \times \mathcal{U}$.

For a generalised $\mathcal{U}$--space $X = (C,F,c)$, $C(U)$ is to be viewed as the morphisms from an object $U$ to $X$ whilst $F(U)$ as the morphisms to $U$ from $X$.  There is an obvious embedding of $\mathcal{U}$ in the [[category]] of generalised $\mathcal{U}$--spaces.

+-- {: .num_lemma #UEmbed}
##### Lemma
The assignment
\[
U \mapsto (\mathcal{U}(-,U),\mathcal{U}(U,-),\circ), \qquad f \mapsto (f_*,f^*)
\]
defines an embedding of $\mathcal{U}$ in the category of generalised $\mathcal{U}$--objects.
=--

Inside the category of generalised $\mathcal{U}$--spaces one can consider various subcategories defined by taking those generalised $\mathcal{U}$--spaces satisfying some condition.  One example of such is if $\mathcal{U}$ is a [[site]], then one can consider those generalised $\mathcal{U}$--spaces for which the contravariant functor $C$ satisfies the [[sheaf]] condition (there are ways to essentially ignore the covariant functor $F$).

+-- {.query}
[[Andrew Stacey|Andrew]]: I would love to know if there are antecedents for what I describe in the above paragraph.  It seems to generalise the concept of a sheaf in an obvious way but being fairly new to category theory I have no idea what to search for on MathSciNet!  Maybe someone's called them _Armadillos_ (the reference being Rudyard Kipling's story wherein armadillos are a blend of hedgehog and tortoise).
=--

The condition relevant for Fr&#246;licher spaces is that of [[Isbell duality]].

+-- {: .num_defn #IsbellDuality}
##### Definition
A generalised $\mathcal{U}$--space $(C,F,c)$ is said to satisfy _Isbell duality_ if the following conditions hold for all objects $U$ of $\mathcal{U}$.

1. $C(U) = NatTrans(F,F_U)$
2. $F(U) = NatTrans(C_U,C)$

where $(C_U,F_U,\circ)$ is the generalised $\mathcal{U}$--space corresponding to $U$.
=--

+-- {: .num_theorem #FroelicherDual}
##### Theorem
The Fr&#246;licher spaces are precisely the generalised $\mathcal{R}$--objects satisfying Isbell Duality for $\mathcal{R}$ the category with a single object and morphism set $C^\infty(\mathcal{R}, \mathcal{R})$.

More generally, if $\mathcal{U}$ is a full subcategory of _known smooth spaces_ then the Fr&#246;licher spaces are precisely the generalised $\mathcal{U}$--objects satisfying Isbell Duality.
=--

+-- {.query}
[[Andrew Stacey|Andrew]]: I know I need to clarify "known smooth spaces".  Basically, it contains everything where there is an indisputable smooth structure.

Obviously, I'm not done here but that's all I have time for right now.
=--


#Discussion

[[Urs Schreiber|Urs]]: Hi [[Andrew Stacey|Andrew]]. One question: I forget if we and in particular you ever finished proving or disproving the conjecture that Fr&#246;licher spaces are precisely the Isbell self-dual presheaves? Can you remind me of what the status of this idea is? If you had a full proof of this, it would definitely deserve to be stated here (unless top secret, of course.)

[[Andrew Stacey|Andrew]]: Hi [[Urs Schreiber|Urs]].  In my mind the proof was complete.  Whether or not I communicated that to you (plural) is moot.  One of my goals for this page is to gather and straighten out things like that.

[[Urs Schreiber|Urs]]: Ah, that's really good to hear. I'd think this will be the best selling point for the relevance of Fr&#246;licher spaces from a general abstract point of view. I'll see if I find the time to add an entry [[Isbell duality]] accompanying [[duality]] and [[dualizing object]] and [[space and quantity]], so that you can refer to it here.