# Basics

+-- {: .num_defn #FroelicherSpace}
###### Definition
A _Fr&#246;licher Space_ is a triple $(X,C_X,F_X)$ where

1. $X$ is a set;
2. $C_X$ is a set of _curves_ in $X$; that is, $C_X \subseteq Set(\mathbb{R},X)$;
3. $F_X$ is a set of _functionals_ on $X$; that is, $F_X \subseteq Set(X, \mathbb{R})$;

subject to the following saturation conditions

1. if $c : \mathbb{R} \to X$ is a set map with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_X$ then $c \in C_X$, and
2. if $f : X \to \mathbb{R}$ is a set map with the property that $f c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $c \in C_X$ then $f \in F_X$.

A _morphism_ of Fr&#246;licher spaces, say $(X,C_X,F_X) \to (Y,C_Y,F_Y)$ is a set map $g : X \to Y$ satisfying the following (equivalent) conditions:

1. $g c \in C_Y$ for all $c \in C_X$,
2. $f g \in F_X$ for all $f \in F_Y$,
3. $f g c \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $f \in F_Y$ and $c \in C_X$.
=--

Fr&#246;licher spaces and their morphisms form a category with an obvious faithful functor to the category of sets.
The properties of this category are as follows.

+-- {: .num_theorem #FroelicherCategory}
###### Theorem
The [[category]] of Fr&#246;licher spaces is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[cartesian closed category|cartesian closed]].  It is [[topological category|topological]] over $Set$.  It is an [[construct|amnestic, transportable construct]].
=--

+-- {: .query}
[[Andrew Stacey|Andrew]]: I don't think that this category is _locally_ cartesian closed but the only evidence that I have for that is a side remark by Lawvere on the category mailing list.
=--

# Isbell Duality

Fr&#246;licher spaces are examples of [[generalized smooth space|generalised smooth spaces]].  They are also examples of [[space and quantity|generalised spaces]] in the following sense.

+-- {: .num_defn #GenSpace}
###### Definition
Let $\mathcal{U}$ be a [[category]].  A _generalised $\mathcal{U}$--space_ is a triple $(C,F,c)$ where $C$ is a [[functor|contravariant functor]] $\mathcal{U} \to Set$, $F$ is a [[functor|covariant functor]] $\mathcal{U} \to Set$, and $c$ is a [[natural transformation]] $C \times F \to \mathcal{U}(-,-)$.  We refer to $c$ as _composition_.

A _morphism of generalised $\mathcal{U}$--spaces_ $(C_1,F_1,c_1) \to (C_2,F_2,c_2)$ is a pair of natural transformations $\alpha : C_1 \to C_2$ and $\beta : F_2 \to F_1$ satisfying the identity $c_1(-,\beta(-)) = c_2(\alpha(-),-)$.

For $\gamma \in C(U)$ and $\eta \in \mathcal{U}(U',U)$ we shall write $C(\eta)(\gamma)$ as $\gamma \circ \eta$.
Similarly for $\phi \in F(U)$ and $\psi \in \mathcal{U}(U,U')$ we shall write $F(\psi)(\phi)$ as $\psi \circ \phi$.
We shall also write $c(\gamma,\phi)$ as $\phi \circ \gamma$.
If we need to distinguish $\circ$ from its proper usage we shall label it appropriately.

Given a morphism $(\alpha, \beta)$, $\gamma \in C_1(U)$, and $\phi \in F_2(U')$ we shall write $\alpha_U(\gamma)$ as $\alpha \circ \gamma$ (or $\alpha \circ_1 \gamma$ if the context requires it) and $\beta_{U'}(\phi)$ as $\phi \circ \beta$.
=--

+-- {: .query}
[[Andrew Stacey|Andrew]]: I presume that we need some hypothesis on $\mathcal{U}$ to ensure that the natural transformations form a set.  Is there a concise way to put this?

We should also settle on a convention for what to call $C$ and $F$.  My notation and nomenclature is obviously influenced by Fr&#246;licher spaces but that's not a good basis for making a decision.

[[Mike Shulman|Mike]]: Well, certainly if $U$ is essentially small (equivalent to a small category), then the natural transformations between any two functors $U\to Set$ or $U^{op}\to Set$ form a set, so that your category of generalized spaces will be locally small.  Conversely, it's true (though not obvious) that if the category $Psh(U)$ of Set-valued presheaves on $U$ is locally small, then $U$ is essentially small (although the natural transformations between some _particular_ pair of presheaves could be a set without $U$ being small).  So almost certainly the condition you want is that $U$ is (essentially) small.

I might suggest that maybe the generalities on this page, not specific to Frolicher spaces, would fit better on a page such as "generalized space"?  Although that is such a generic-sounding word that maybe a better name should be found.  "Frolicher object over $U$"?  "Bi-presheaf"?

[[Andrew Stacey|Andrew]]: Yes, I was coming round to the idea of having a separate "generalised space" page, but wanted to know what to call it first - hence my first question on [[request for help]].

_Toby_: Keep in mind that we\'ve already got [[generalized smooth space]].
=--

Here, $\mathcal{U}(-,-)$ is the $Hom$--functor on $\mathcal{U}$ (strictly, $\mathcal{U}^{op} \times \mathcal{U}$).


For a generalised $\mathcal{U}$--space $X = (C,F,c)$, $C(U)$ is to be viewed as the morphisms from an object $U$ to $X$ whilst $F(U)$ as the morphisms to $U$ from $X$.
This motivates the alternative notation.
For $\alpha \in C(U)$ and $\phi \in F(U')$, $c_{U,U'}(\alpha, \phi)$ is in $\mathcal{U}(U,U')$.
Then for $\beta \in \mathcal{U}(U'',U)$, $C(\beta)$ is a set map $C(U) \to C(U'')$ so we have $C(\beta)(\alpha) \in C(U'')$.
Then
$$
c_{U'',U'}(C(\beta)(\alpha), \phi) = c_{U,U'}(\alpha,\phi) \circ \beta
$$
With the alternative notation, this becomes
$$
\phi \circ (\alpha \circ \beta) = (\phi \circ \alpha) \circ \beta
$$
Thus the identity that morphisms have to satisfy is that
$$
(\phi \circ_2 \beta) \circ_1 \gamma = \phi \circ_2 (\alpha \circ_1 \gamma).
$$

There is an obvious embedding of $\mathcal{U}$ in the [[category]] of generalised $\mathcal{U}$--spaces.

+-- {: .num_lemma #UEmbed}
###### Lemma
The assignment
\[
U \mapsto (\mathcal{U}(-,U),\mathcal{U}(U,-),\circ), \qquad f \mapsto (f \circ -,- \circ f)
\]
defines an embedding of $\mathcal{U}$ in the category of generalised $\mathcal{U}$--objects.
=--

Inside the category of generalised $\mathcal{U}$--spaces one can consider various subcategories defined by taking those generalised $\mathcal{U}$--spaces satisfying some condition.  One example of such is if $\mathcal{U}$ is a [[site]], then one can consider those generalised $\mathcal{U}$--spaces for which the contravariant functor $C$ satisfies the [[sheaf]] condition (there are ways to essentially ignore the covariant functor $F$).

+-- {: .query}
[[Andrew Stacey|Andrew]]: I would love to know if there are antecedents for what I describe in the above paragraph.  It seems to generalise the concept of a sheaf in an obvious way but being fairly new to category theory I have no idea what to search for on MathSciNet!  Maybe someone's called them _Armadillos_ (the reference being Rudyard Kipling's story wherein armadillos are a blend of hedgehog and tortoise).
=--

The condition relevant for Fr&#246;licher spaces is that of [[Isbell duality]].

+-- {: .num_defn #IsbellDuality}
###### Definition
A generalised $\mathcal{U}$--space $(C,F,c)$ is said to satisfy _Isbell duality_ if the following conditions hold for all objects $U$ of $\mathcal{U}$.

1. $C(U) = NatTrans(F,F_U)$
2. $F(U) = NatTrans(C,C_U)$

where $(C_U,F_U,\circ)$ is the generalised $\mathcal{U}$--space corresponding to $U$.
=--

+-- {: .num_theorem #FroelicherDual}
###### Theorem
The Fr&#246;licher spaces are precisely the generalised $\mathcal{R}$--objects satisfying Isbell Duality for $\mathcal{R}$ the category with a single object and morphism set $C^\infty(\mathbb{R}, \mathbb{R})$.

More generally, if $\mathcal{U}$ is a full subcategory of _known smooth spaces_ then the Fr&#246;licher spaces are precisely the generalised $\mathcal{U}$--objects satisfying Isbell Duality.
=--

+-- {: .query}
[[Andrew Stacey|Andrew]]: I know I need to clarify "known smooth spaces".  Basically, it contains everything where there is an indisputable smooth structure.
=--

The essential part of this proof is to show that generalised $\mathcal{U}$--spaces are [[concrete]] in the sense that they have underlying sets.
First, we need to make sure that ordinary $\mathcal{U}$--spaces have underlying sets.

+-- {: .num_defn #ConstSep}
###### Definition
A _constant separator_ in a category is an object, say $S$, with the property that if $f \ne g : A \to B$ then there is a [[constant morphism]] $c : S \to A$ such that $f c \ne g c$.
=--

As the constant morphisms form a two-sided ideal, any object $U_0$ in $\mathcal{U}$ defines a covariant functor $Const(U_0,-) : \mathcal{U} \to Set$ which on objects sends $U$ to the set of constant morphisms from $U_0$ to $U$.
A morphism $U_0 \to U_0'$ defines a natural transformation (in the opposite direction) between the corresponding functors.
From the properties of constant morphisms one can easily deduce that two different morphisms between the same objects induce the same natural transformations between the functors.
Thus if there are morphisms between two objects in both directions the two functors are naturally isomorphic.

The property of being a constant separator is clearly equivalent to the condition that this constant functor be faithful.
Moreover, it is easy to show that in a non-trivial category, any two constant separators have morphisms between them in both directions and so induce naturally isomorphic functors.
Indeed, not just naturally isomorphic but naturally naturally isomorphic in that there is a canonical choice of natural isomorphism.

Now we transfer this to generalised $\mathcal{U}$--spaces.

+-- {: .num_defn #GenSpaceConst}
###### Definition
Let $(C,F,c)$ be a generalised $\mathcal{U}$--space.
An element $\alpha \in C(U)$, for $U$ an object of $\mathcal{U}$, is said to be _constant_ if $\phi \circ \alpha \in \mathcal{U}(U,U')$ is constant for all $U'$ objects of $\mathcal{U}$ and $\phi \in F(U')$.

Let us write $Const(C(U))$ for the set of constant elements in $C(U)$.
=--

+-- {: .num_lemma #GenSpConsFun}
###### Lemma
Let $U_0$ be an object in $\mathcal{U}$.
The assignment $(C,F,c) \to Const(C(U_0))$ is functorial and extends the assignment $U \to Const(U_0,U)$.
A $\mathcal{U}$--morphism $U_0 \to U_1$ defines a natural transformation of functors.
=--

+-- {.proof}
###### Proof
Let $(C_i,F_i,c_i)$, $i = 1,2$, be two generalised $\mathcal{U}$--spaces.
Let $(\alpha,\beta)$ be a morphism from the first to the second.
Then $\alpha$ is a natural transformation $C_1 \to C_2$ so in particular defines a morphism of sets $C_1(U_0) \to C_2(U_0)$.
Let $\gamma \in C_1(U_0)$ be a constant element.
Let $U$ be an object in $\mathcal{U}$ and $\phi \in F_2(U)$.
We need to show that $\phi \circ (\alpha \circ \gamma)$ is a constant morphism.
By the definition of a morphism of generalised $\mathcal{U}$--spaces, $\phi \circ (\alpha \circ \gamma) = (\phi \circ \beta) \circ \gamma$ and this latter is a constant morphism since $\gamma \in C_1(U_0)$ is a constant element.

For the extension, we observe that for $\gamma \in C_U(U_0)$ then if $\gamma$ is a constant morphism, $c_U(\phi,\gamma) = \phi \circ \gamma$ is constant for all $\phi$; whilst if $c_U(\phi,\gamma)$ is constant for all $\phi$ then in particular $\gamma = c_U(1_U,\gamma)$ is constant.
That the morphisms correspond is obvious.

A $\mathcal{U}$--morphism $\psi : U_0 \to U_1$ defines a map $C(U_1) \to C(U_0)$ as $C$ is a contravariant functor.
Let $\gamma \in C(U_1)$ be a constant element.
Then for $U'$ an object in $\mathcal{U}$ and $\phi \in F(U')$, $\phi \circ (\gamma \circ \psi) = (\phi \circ \gamma) \circ \psi$ and $\phi \circ \gamma$ is a constant morphism in $\mathcal{U}(U_1,U')$ so $\phi \circ (\gamma \circ \psi)$ is a constant morphism in $\mathcal{U}(U_0,U')$.
Hence $\gamma \circ \psi$ is a constant element in $C(U_0)$.
=--

The result that the natural transformations depend only on the existence of a morphism does not carry over to the generalised space setting.

+-- {: .query}
[[Andrew Stacey|Andrew]]: Useful to have an example here, of course.
=--

Let us fix a $\mathcal{U}$--object $U_0$.
We have two bifunctors $\mathcal{U} \times \mathcal{U}^g \to Set$ given by
$$
(U,X) \mapsto C_X(U)
$$
and
$$
(U,X) \mapsto Set(Const(C_U(U_0)),Const(C_X(U_0)))
$$
Let us, to simplify notation, identify $U$ with its image in $\mathcal{U}^g$.
Then $C_X(U)$ is naturally isomorphic to $\mathcal{U}^g(U,X)$ so the fact that $X \mapsto Const(C_X(U_0))$ is a functor defines a natural transformation from the first to the second via
$$
C_X(U) \cong \mathcal{U}^g(U,X) \to Set(Const(C_U(U_0)), Const(C_X(U_0)))
$$
In a similar fashion, we obtain a natural transformation
$$
F_X(U) \cong \mathcal{U}^g(X,U) \to Set(Const(C_X(U_0)), Const(C_U(U_0))).
$$

+-- {: .num_defn #ConcGenSp}
###### Definition
Let $X = (C_X,F_X,c_X)$ be a generalised $\mathcal{U}$--space.
We say that $X$ is _$C$--concrete_ if the map of sets
$$
C_X(U) \to Set(Const(C_U(U_0)), Const(C_X(U_0)))
$$
is injective for all $\mathcal{U}$--objects, $U$.

Similarly, we say that $X$ is _$F$--concrete_ if the map of sets
$$
F_X(U) \to Set(Const(C_X(U_0)), Const(C_U(U_0)))
$$
is injective for all $\mathcal{U}$--objects, $U$.

We say that $X$ is _concrete_ if it is both $C$--concrete and $F$--concrete.
=--

+-- {: .num_theorem #ConcreteIsbell}
###### Theorem
Let $\mathcal{U}$ be a category admitting a constant separator.
Then for a generalised $\mathcal{U}$--space $X$ the following hold:

1. If $C_X(U) = NatTrans(F_X,F_U)$ for all $\mathcal{U}$--objects $U$ then $X$ is $C$--concrete.
2. If $F_X(U) = NatTrans(C_X,C_U)$ for all $\mathcal{U}$--objects $U$ then $X$ is $F$--concrete.
3. If $X$ satisfies Isbell duality then it is concrete.
=--

+-- {: .proof}
###### Proof
Clearly the first and second statements imply the third.

Let us consider the first.

Let $X$ be a generalised $\mathcal{U}$--space such that $C_X(U) = NatTrans(F_X,F_U)$ for all $\mathcal{U}$--objects $U$.
Let $S$ be a concrete separator in $\mathcal{U}$.
Let $U$ be an object of $\mathcal{U}$.
Let $\alpha \ne \beta \in C_X(U)$.
As $C_X(U) = NatTrans(F_X,F_U)$, their inequality means that they differ as natural transformations.
Thus there is some $U'$ for which $\alpha$ and $\beta$ induce different morphisms $F_X(U') \to F_U(U')$.
Thus there is some $\phi \in F_X(U')$ such that $\alpha_{U'}(\phi) \ne \beta_{U'}(\phi) \in \mathcal{U}(U,U')$.

As $S$ is a constant separator, there is thus a constant morphism $\delta : S \to U$ such that $\alpha_{U'}(\phi) \circ \delta \ne \beta_{U'}(\phi) \circ \delta$.
Using composition notation, we rewrite this as $\phi \circ \alpha \circ \delta \ne \phi \circ \beta \circ \delta$.
As $\delta$ is a constant morphism, $\alpha \circ \delta$ and $\beta \circ \delta$ are constant elements of $C_X(S)$.
Since $\phi \circ \alpha \circ \delta \ne \phi \circ \beta \circ \delta$, they must be different constant elements.
Thus the maps $\alpha,\beta : Const(S,U) \to Const(C_X(S))$ are different and so $X$ is $C$--concrete.

The second statement is very similar.

Let $X$ be a generalised $\mathcal{U}$--space such that $F_X(U) = NatTrans(C_X,C_U)$ for all $\mathcal{U}$--objects $U$.
Let $S$ be a concrete separator in $\mathcal{U}$.
Let $U$ be an object of $\mathcal{U}$.
Let $\phi \ne \psi \in F_X(U)$.
As $F_X(U) = NatTrans(C_X,C_U)$, their inequality means that they differ as natural transformations.
Thus there is some $U'$ for which $\phi$ and $\psi$ induce different morphisms $C_X(U') \to C_U(U')$.
Thus there is some $\alpha \in C_X(U')$ such that $\phi_{U'}(\alpha) \ne \psi_{U'}(\alpha) \in \mathcal{U}(U',U)$.

As $S$ is a constant separator, there is thus a constant morphism $\delta : S \to U'$ such that $\phi_{U'}(\alpha) \circ \delta \ne \psi_{U'}(\alpha) \circ \delta$.
Using the composition notation, we rewrite this as $\phi \circ \alpha \circ \delta \ne \psi \circ \alpha \circ \delta$.
As $\delta$ is a constant morphism, $\alpha \circ \delta \in C_X(S)$ is a constant element.
We therefore have an element of $Const(C_X(S))$ which distinguishes between the induced maps from $\phi$ and $\psi$.
Hence $X$ is $F$--concrete.
=--

There are a few more pertinent results.
The presence of the constant separator is extremely useful.
Given a generalised $\mathcal{U}$--space, say $X$, one can consider alternately replacing each family $C_X$ and $F_X$ by the natural transformations of the other.
The hope is, of course, that this process with terminate at some point resulting in a generalised $\mathcal{U}$--space satisfying Isbell duality.
The presence of a constant separator implies that this happens after at most two replacements.

+-- {: .num_lemma #IsbellCompletion}
###### Lemma
Let $X$ be a generalised $\mathcal{U}$--space.
Let $\hat{C}_X(U) = NatTrans(F_X,F_U)$ and $\hat{F}_X(U) = NatTrans(\hat{C}_X,C_U)$.
Then $(\hat{C}_X, \hat{F}_X, c_X)$ is a generalised $\mathcal{U}$--space satisfying Isbell duality and this assignment is functorial in $X$.

The same is true starting with $\check{F}_X = NatTrans(C_X,C_U)$.
=--

+-- {: .proof}
###### Proof
...
=--

The second important result concerns changing the category $\mathcal{U}$.
Let $\matcal{V}$ be a full subcategory of $\mathcal{U}$.
Given a generalised $\mathcal{U}$--space we obtain a generalised $\mathcal{V}$--space by restriction.

+-- {: .num_defn #SubDecider}
###### Definition
Let $\mathcal{U}$ be a category with a faithful functor to $Set$.
A full subcategory $\mathcal{V}$ is said to be _sufficient_ for $\mathcal{U}$ if it can detect $\mathcal{U}$--morphisms in $Set$.

That is to say, for two objects $U_1$ and $U_2$ of $\mathcal{U}$, a map of sets $\beta : |U_1| \to |U_2|$ underlies a $\mathcal{U}$--morphism if and only if for all $\mathcal{V}$--objects $V_1$ and $V_2$ and $\mathcal{U}$--morphisms $\alpha : V_1 \to U_1$ and $\gamma : U_2 \to V_2$, $|\gamma| \beta |\alpha|$ underlies a $\mathcal{V}$--morphism from $V_1$ to $V_2$.
=--

+-- {: .query}
I suspect that there's a proper name for this ...

_Mike_: I don't know a whole lot about the terminology in common use here, but if there is no established term, my inclination would be to call it something like _concretely dense_ or _relatively dense_.  This is because it is equivalent to saying that the functor $U\to CPsh(V)$ is full and faithful, where $CPsh(V)$ is the category of _concrete presheaves_ on $V$, i.e. presheaves on $V$ equipped with a monomorphism to $Set(|-|,S)$ for some set $S$.  And of course _dense_ means that $U\to Psh(V)$ is full and faithful, where $Psh(V)$ is the category of ordinary presheaves on $V$.
=--



+-- {: .num_prop #IsbellCatChange}
###### Proposition
Let $\mathcal{U}$ be a category with a constant separator.
Let $\mathcal{V}$ be a full subcategory that is sufficient.
Then the category of generalised $\mathcal{U}$--objects that satisfy Isbell duality is isomorphic to that of generalised $\mathcal{V}$--objects satisfying Isbell duality.
=--

+-- {: .proof}
###### Proof
...
=--

+-- {: .query}
Obviously, I'm not done here but that's all I have time for right now.
=--


#Discussion

[[Urs Schreiber|Urs]]: Hi [[Andrew Stacey|Andrew]]. One question: I forget if we and in particular you ever finished proving or disproving the conjecture that Fr&#246;licher spaces are precisely the Isbell self-dual presheaves? Can you remind me of what the status of this idea is? If you had a full proof of this, it would definitely deserve to be stated here (unless top secret, of course.)

[[Andrew Stacey|Andrew]]: Hi [[Urs Schreiber|Urs]].  In my mind the proof was complete.  Whether or not I communicated that to you (plural) is moot.  One of my goals for this page is to gather and straighten out things like that.

[[Urs Schreiber|Urs]]: Ah, that's really good to hear. I'd think this will be the best selling point for the relevance of Fr&#246;licher spaces from a general abstract point of view. I'll see if I find the time to add an entry [[Isbell duality]] accompanying [[duality]] and [[dualizing object]] and [[space and quantity]], so that you can refer to it here.
