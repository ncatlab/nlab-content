
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



# The Isbell Envelope of a Category
* table of contents
{: toc}

## Idea

Given a category $\mathcal{T}$ of "test objects", one can consider "things" which $\mathcal{T}$ can detect.  If one already has a class of objects in mind, one can consider $\mathcal{T}$-structures on those objects by looking at morphisms to and from objects of $\mathcal{T}$.  Then one considers questions only in so far as they can be distinguished after mapping into $\mathcal{T}$.  A simple example is that of smooth [[manifold]]s where many questions are solved by transporting the problem to Euclidean spaces via charts.  Another example is the use of weak topologies on locally convex topological spaces.  Without a class of objects in mind, the natural definition of an object probeable by $\mathcal{T}$-objects involves presheaves and copresheaves and is as follows.

+-- {: .num_defn #IsbellEnvelope}
###### Definition
Let $\mathcal{T}$ be an [[small category|essentially small]] category.  The _Isbell envelope_ of $\mathcal{T}$, written $E(\mathcal{T})$, is the category whose objects are triples $(P,F,c)$ where

1. $P$ is a contravariant functor $\mathcal{T} \to Set$ (a presheaf),
2. $F$ is a covariant functor $\mathcal{T} \to Set$ (a co-presheaf),
3. $c : P \times F \to \mathcal{T}(-,-)$ is a natural transformation of bifunctors $\mathcal{T}^{op} \times \mathcal{T} \to Set$.

and where a morphism $X \to Y$ is a pair of natural transformations $(\alpha,\beta)$ with $\alpha : P_X \to P_Y$ $\beta : F_Y \to F_X$ which satisfy the relation $c_X(-,\beta -) = c_Y(\alpha -,-)$.
=--

The requirement that $\mathcal{T}$ be essentially small implies that the collections of natural transformations form sets, and thus that this is a [[locally small category]].

Certain elementary properties are easy to prove.

+-- {: .num_prop #ElemProp}
###### Proposition
There is an obvious embedding of $\mathcal{T}$ as a full subcategory of $E(\mathcal{T})$ via

\[
T \mapsto (\mathcal{T}(-,T), \mathcal{T}(T,-), \circ)
\]

Identifying $\mathcal{T}$ with its image, we have natural isomorphisms

\[
\mathcal{T}^g(T,X) \cong P_X(T), \qquad \mathcal{T}^g(X,T) \cong F_X(T)
\]

_Other elementary properties to follow_
=--

## Profunctors

The Isbell envelope of a category can be viewed as a category of [[distributor|profunctors]].
In short, the Isbell envelope of $\mathcal{T}$ consists of the _lax factorisations of $Hom$ through $1$_.

Let us spell this out.
Recall that a profunctor $\mathcal{A} \to \mathcal{B}$ is a functor $\mathcal{A} \times \mathcal{B}^{op} \to Set$.
Both covariant and contravariant functors to $Set$ are special examples of profunctors: a covariant functor $\mathfrak{F} : \mathcal{A} \to Set$ is a profunctor $\mathcal{A} \to 1$, where $1$ is the terminal category, and a contravariant functor $\mathfrak{G} : \mathcal{B} \to Set$ is a profunctor $1 \to \mathcal{B}$.
The composition of these as profunctors produces the obvious  profunctor $\mathfrak{F} \times \mathfrak{G} : \mathcal{A} \times \mathcal{B}^{op} \to Set$.
Thus extracting the functor part of the definition of an object in the Isbell envelope of $\mathcal{T}$ produces a profunctor $\mathcal{T} \to \mathcal{T}$ which factors through $1$.

There is an obvious profunctor $\mathcal{T} \to \mathcal{T}$ given by the $Hom$-bifunctor.
This is the identity for profunctor composition.
The natural transformation from the definition of an object in the Isbell envelope of $\mathcal{T}$ defines a morphism of profunctors from the corresponding profunctor to $Hom$.
Thus an object in the Isbell envelope of $\mathcal{T}$ corresponds to an object in the subcategory of the slice category of profunctors over $Hom$ of those objects which factor through $1$.

In other words, a lax factorisation of $Hom$ through $1$.

## Concrete Envelopes

A variant of the above involves having a background category, say $\mathcal{U}$.  The test objects should be viewable also as objects of $\mathcal{U}$, usually via a faithful functor.  Any object of $\mathcal{U}$ defines a profunctor $\mathcal{T} \to \mathcal{T}$ (which factors through $1$) via

\[
\begin{aligned}
\mathcal{T} \times \mathcal{T}^{op} &\to \mathcal{U} \times \mathcal{U}^{op} &&\to Set \\
(T_1, T_2) &\mapsto (|T_1|, |T_2|) &&\mapsto \mathcal{U}(U,|T_1|) \times \mathcal{U}(|T_2|,U)
\end{aligned}
\]

Then one can consider those objects of the Isbell envelope of $\mathcal{T}$ that are sub-profunctors of one of this type.
In addition one should restrict the morphisms to those that are induced by morphism of objects of $\mathcal{U}$.
Translating this back to the language of functors yields the following definition.

+-- {: .num_defn #ConcIsbellEnvelope}
###### Definition
Let $\mathcal{T}$ and $\mathcal{U}$ be categories with a faithful functor $\mathcal{T} \to \mathcal{U}$ which we shall write as $T \mapsto |T|$.  The _$\mathcal{U}$-concrete  Isbell envelope_ of $\mathcal{T}$, which we shall write $E_{\mathcal{U}}(\mathcal{T})$, is the category whose objects are triples $(U,P,F)$ where

1. $U$ is an object of $\mathcal{U}$,
2. $P : \mathcal{T} \to Set$ is a subfunctor of the (contravariant) functor $T \mapsto \mathcal{U}(|T|,U)$,
3. $F : \mathcal{T} \to Set$ is a subfunctor of the (covariant) functor $T \mapsto \mathcal{U}(U,|T|)$,

such that the image of the natural transformation
\[
P \times F \to \mathcal{U}(|-|,|-|),
\]
which comes from composition in $\mathcal{U}$, lies in the image of the natural transformation $\mathcal{T}(-,-) \to \mathcal{U}(|-|,|-|).$

A morphism in $E_{\mathcal{U}}(\mathcal{T})$ is a $\mathcal{U}$-morphism on the underlying $\mathcal{U}$-objects that defines natural transformations $P_X \to P_Y$ and $F_Y \to F_X$.
=--

Having a background category ensures that the size issues with natural transformations do not occur and so we can drop the requirement that $\mathcal{T}$ be essentially small.

## Enrichment

These notions can be considered in the enriched setting by replacing $Set$ wherever it occurs (explicitly or implicitly) by the enriching category.

## Isbell Duality

Within the Isbell envelope of $\mathcal{T}$ one can consider various subcategories where the objects satisfy extra conditions.  An obvious condition is that the presheaf is actually a sheaf.  Another useful condition is that of Isbell Duality.

+-- {: .num_defn #IsbelDuality}
###### Definition
An object $X$ of $E(\mathcal{T})$ is said to be _$P$-saturated_ if the obvious natural transformations

\[
P_X(T) \to NatTrans(F_X,F_T)
\]

are isomorphisms.  It is said to be _$F$-saturated_ if the obvious natural transformations

\[
F_X(T) \to NatTrans(P_X,P_T)
\]

are isomorphisms.  It is said to satisfy _Isbell duality_ if it is both $P$- and $F$-saturated.
=--

Within $E(\mathcal{T})$ one can consider the full subcategories of $P$-saturated objects, of $F$-saturated objects, and those satisfying Isbell duality.  Clearly, the last is the intersection of the first two.  There are idempotent functors onto the first two categories given by replacing one of $P_X$ or $F_X$ by the natural transformations of the other.  An interesting question is to ask whether or not the obvious iteration stabilises after a finite number of steps (which would result in an object satisfying Isbell duality).


If the test category has, or "morally has", a representable functor to $Set$ then there is a strong relationship between saturation and concreteness.

+-- {: .num_defn #ConstSep}
###### Definition
A _constant separator_ in a category is an object, say $S$, with the property that if $f \ne g : A \to B$ then there is a [[constant morphism]] $c : S \to A$ such that $f c \ne g c$.
=--

As the constant morphisms form a two-sided ideal, any object $C_0$ in a category $\mathcal{C}$ defines a covariant functor $|-|_{C_0} : \mathcal{C} \to Set$ which on objects sends $C$ to the set of constant morphisms from $C_0$ to $C$.
A morphism $C_0 \to C_0'$ defines a natural transformation (in the opposite direction) between the corresponding functors.
From the properties of constant morphisms one can easily deduce that two different morphisms between the same objects induce the same natural transformations between the functors.
Thus if there are morphisms between two objects in both directions the two functors are naturally isomorphic.

The property of being a constant separator is clearly equivalent to the condition that this constant functor be faithful.
Moreover, it is easy to show that in a non-trivial category, any two constant separators have morphisms between them in both directions and so induce naturally isomorphic functors.
Indeed, not just naturally isomorphic but naturally naturally isomorphic in that there is a canonical choice of natural isomorphism.

Now we transfer this to the Isbell envelope of $\mathcal{T}$.

+-- {: .num_defn #GenSpaceConst}
###### Definition
Let $X=(P,F,c)$ be an object of $E(\mathcal{T})$.
An element $\alpha \in P(T)$, for $T$ an object of $\mathcal{T}$, is said to be _constant_ if $\phi \circ \alpha \in \mathcal{T}(T,T')$ is constant for all $T'$ objects of $\mathcal{T}$ and $\phi \in F(T')$.

Let us write $|X|_T$ for the set of constant elements in $P(T)$.
=--

+-- {: .num_lemma #GenSpConsFun}
###### Lemma
Let $T_0$ be an object in $\mathcal{T}$.
The assignment $X \to |X|_{T_0}$ is functorial and extends the assignment $T \to |T|_{T_0}$.
A $\mathcal{T}$--morphism $T_0 \to T_1$ defines a natural transformation of functors.
=--

+-- {.proof}
###### Proof
Let $X_i = (P_i,F_i,c_i)$, $i = 1,2$, be two objects in $E(\mathcal{T})$.
Let $(\alpha,\beta)$ be a morphism from the first to the second.
Then $\alpha$ is a natural transformation $P_1 \to P_2$ so in particular defines a morphism of sets $P_1(T_0) \to P_2(T_0)$.
Let $\gamma \in P_1(U_0)$ be a constant element.
Let $T$ be an object in $\mathcal{T}$ and $\phi \in F_2(T)$.
We need to show that $\phi \circ (\alpha \circ \gamma)$ is a constant morphism.
By the definition of a morphism in $E(\mathcal{T})$, $\phi \circ (\alpha \circ \gamma) = (\phi \circ \beta) \circ \gamma$ and this latter is a constant morphism since $\gamma \in P_1(T_0)$ is a constant element.

For the extension, we observe that for $\gamma \in P_T(T_0)$ then if $\gamma$ is a constant morphism, $c_T(\phi,\gamma) = \phi \circ \gamma$ is constant for all $\phi$; whilst if $c_T(\phi,\gamma)$ is constant for all $\phi$ then in particular $\gamma = c_T(1_T,\gamma)$ is constant.
That the morphisms correspond is obvious.

A $\mathcal{T}$--morphism $\psi : T_0 \to T_1$ defines a map $P(T_1) \to P(T_0)$ as $P$ is a contravariant functor.
Let $\gamma \in P(T_1)$ be a constant element.
Then for $T'$ an object in $\mathcal{T}$ and $\phi \in F(U')$, $\phi \circ (\gamma \circ \psi) = (\phi \circ \gamma) \circ \psi$ and $\phi \circ \gamma$ is a constant morphism in $\mathcal{T}(T_1,T')$ so $\phi \circ (\gamma \circ \psi)$ is a constant morphism in $\mathcal{T}(T_0,T')$.
Hence $\gamma \circ \psi$ is a constant element in $P(T_0)$.
=--

The result that the natural transformations depend only on the existence of a morphism does not carry over to this extended setting.

+-- {: .query}
[[Andrew Stacey|Andrew]]: Useful to have an example here, of course.
=--

Let us fix a $\mathcal{T}$--object $T_0$.
We have two bifunctors $\mathcal{T} \times E(\mathcal{T}) \to Set$ given by
$$
(T,X) \mapsto P_X(T)
$$
and
$$
(T,X) \mapsto Set(|T|_{T_0},|X|_{T_0})
$$
Let us, to simplify notation, identify $T$ with its image in $E(\mathcal{T})$.
Then $P_X(T)$ is naturally isomorphic to $E(\mathcal{T})(T,X)$ so the fact that $X \mapsto |X|_{T_0}$ is a functor defines a natural transformation from the first to the second via
$$
P_X(T) \cong E(\mathcal{T})(T,X) \to Set(|T|_{T_0}, |X|_{T_0})
$$
In a similar fashion, we obtain a natural transformation
$$
F_X(T) \cong E(\mathcal{T})(X,T) \to Set(|X|_{T_0},|T|_{T_0}).
$$
We therefore obtain a functorial choice of underlying concrete object (with the underlying category being $Set$).
We can refine the notion of concreteness slightly.

+-- {: .num_defn #ConcGenSp}
###### Definition
Let $\mathcal{T}$ be an essentially small category with a concrete separator, say $T_0$.
Let $X = (P_X,F_X,c_X)$ be an object of $E(\mathcal{T})$.
We say that $X$ is _$P$--concrete_ if the map of sets
$$
P_X(T) \to Set(|T|_{T_0},|X|_{T_0})
$$
is injective for all $\mathcal{T}$--objects, $T$.

Similarly, we say that $X$ is _$F$--concrete_ if the map of sets
$$
F_X(T) \to Set(|X|_{T_0}, |T|_{T_0})
$$
is injective for all $\mathcal{T}$--objects, $T$.
=--

Clearly, if it is both $P$-concrete and $F$-concrete then it is concrete.  Changing the concrete separator does not alter concreteness.

+-- {: .num_theorem #ConcreteIsbell}
###### Theorem
Let $\mathcal{T}$ be an essentially small category admitting a constant separator.
Then for an object $X$ of $E(\mathcal{T})$, the following hold:

1. If $X$ is $P$-saturated then it is $P$-concrete,
2. If $X$ is $F$-saturated then it is $F$-concrete,
3. If $X$ satisfies Isbell duality then it is concrete.
=--

+-- {: .proof}
###### Proof
Clearly the first and second statements imply the third.

Let us consider the first.

Let $X$ be an object of $E(\mathcal{T})$ such that $P_X(T) = NatTrans(F_X,F_T)$ for all $\mathcal{T}$--objects $T$.
Let $S$ be a concrete separator in $\mathcal{T}$.  We shall write $|-|$ for $|-|_S$.
Let $T$ be an object of $\mathcal{T}$.
Let $\alpha \ne \beta \in P_X(T)$.
As $P_X(T) = NatTrans(F_X,F_T)$, their inequality means that they differ as natural transformations.
Thus there is some $T'$ for which $\alpha$ and $\beta$ induce different morphisms $F_X(T') \to F_T(T')$.
Thus there is some $\phi \in F_X(T')$ such that $\alpha_{T'}(\phi) \ne \beta_{T'}(\phi) \in \mathcal{T}(T,T')$.

As $S$ is a constant separator, there is thus a constant morphism $\delta : S \to T$ such that $\alpha_{T'}(\phi) \circ \delta \ne \beta_{T'}(\phi) \circ \delta$.
Using composition notation, we rewrite this as $\phi \circ \alpha \circ \delta \ne \phi \circ \beta \circ \delta$.
As $\delta$ is a constant morphism, $\alpha \circ \delta$ and $\beta \circ \delta$ are constant elements of $P_X(S)$.
Since $\phi \circ \alpha \circ \delta \ne \phi \circ \beta \circ \delta$, they must be different constant elements.
Thus the maps $\alpha,\beta : |T| \to |X|$ are different and so $X$ is $P$--concrete.

The second statement is very similar.

Let $X$ be an object of $E(\mathcal{T})$ such that $F_X(U) = NatTrans(P_X,P_T)$ for all $\mathcal{T}$--objects $T$.
Let $S$ be a concrete separator in $\mathcal{T}$.
Let $T$ be an object of $\mathcal{T}$.
Let $\phi \ne \psi \in F_X(T)$.
As $F_X(T) = NatTrans(P_X,P_T)$, their inequality means that they differ as natural transformations.
Thus there is some $T'$ for which $\phi$ and $\psi$ induce different morphisms $P_X(T') \to P_T(T')$.
Thus there is some $\alpha \in P_X(T')$ such that $\phi_{T'}(\alpha) \ne \psi_{T'}(\alpha) \in \mathcal{T}(T',T)$.

As $S$ is a constant separator, there is thus a constant morphism $\delta : S \to T'$ such that $\phi_{T'}(\alpha) \circ \delta \ne \psi_{T'}(\alpha) \circ \delta$.
Using the composition notation, we rewrite this as $\phi \circ \alpha \circ \delta \ne \psi \circ \alpha \circ \delta$.
As $\delta$ is a constant morphism, $\alpha \circ \delta \in P_X(S)$ is a constant element.
We therefore have an element of $|X|$ which distinguishes between the induced maps from $\phi$ and $\psi$.
Hence $X$ is $F$--concrete.
=--


[[!redirects Isbell envelope]]
[[!redirects Isbell envelopes]]
[[!redirects generalized object]]
[[!redirects generalized objects]]
