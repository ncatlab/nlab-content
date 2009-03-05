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

# Generalised Spaces

Fr&#246;licher spaces are examples of [[generalized smooth space|generalised smooth spaces]].  They are also examples of [[generalized object|generalised objects]] (indeed, concrete ones).


+-- {: .num_defn #RCat}
###### Definition
Let $\mathcal{R}$ denote the category with one object and morphism set $C^\infty(\mathbb{R},\mathbb{R})$.
=--

There is a close relationship between Fr&#246;licher spaces and the category of generalised $\mathcal{R}$-objects satisfying Isbell Duality.

+-- {: .num_prop #IsbellIsFroelicher}
###### Proposition
A generalised $\mathcal{R}$-object that satisfies Isbell duality is a Fr&#246;licher space.
=--

+-- {: .proof}
Let $X = (C,F)$ be a generalised $\mathcal{R}$-object satisfying Isbell duality.
From the page on [[generalized object#ConcreteIsbell|generalised objects]], $X$ is concrete.
Let $|X|$ denote the set of constant elements of $C$.
By concreteness, $C$ injects into $Set(\mathbb{R},|X|)$ and $F$ injects into $Set(|X|,\mathbb{R})$.
For clarity, we shall distinguish between an element of $C$ and its image in $Set(\mathbb{R},|X|)$ writing $\alpha$ for the former and $|\alpha|$ for the latter.
We shall do similarly for elements of $F$.

Suppose that $\beta : \mathbb{R} \to |X|$ is such that $|\phi| \circ \beta \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $\phi \in F$.
Then the map $\phi \mapsto |\phi|\circ \beta$ is a natural transformation $F \to C^\infty(\mathbb{R},\mathbb{R})$ (it obvious commutes with the left $C^\infty(\mathbb{R},\mathbb{R})$-actions).
Hence it is an element of $C$.
That is, there is an element $\alpha$ of $C$ such that $\alpha(\phi) = |\phi| \circ \beta$ for all $\phi \in F$.

Let us compare $|\alpha|$ with $\beta$.
Let us put $\delta_t : \mathbb{R} \to \mathbb{R}$ as the constant function at $t$ then for all $\phi \in F$,
\[
\phi \circ (|\alpha|(t)) = \phi \circ \alpha \circ \delta_t = \alpha(\phi) \circ \delta_t = |\phi| \circ \beta \circ \delta_t = |\phi|(\beta(t)) = \phi \circ (\beta(t))
\]
But if $|\alpha|$ and $\beta$ differ, then they differ at some $t \in \mathbb{R}$.
Now for $x \ne y \in |X|$, as $X$ satisfies Isbell duality, there must be some $\phi \in F$ such that $\phi \circ x \ne \phi \circ y$.
Hence $|\alpha| = \beta$ and so $\beta$ is in the image of $C$ in $Set(\mathbb{R}, |X|)$.

For the other part, let $\theta : |X| \to \mathbb{R}$ be such that $\theta \circ |\alpha| \in C^\infty(\mathbb{R},\mathbb{R})$ for all $\alpha \in C$.
Then, exactly as above, we define a natural transformation $C \to C^\infty(\mathbb{R},\mathbb{R})$ by $\alpha \mapsto \theta \circ |\alpha|$.
This corresponds to some $\psi \in F$ and it remains to compare $|\psi|$ with $\theta$.
This is simpler since $x \in |X|$ is an element of $C$ and so $|\psi|(x) = \psi(x) = \theta \circ |x| = \theta(x)$.
=--

However, not all Fr&#246;licher spaces can be obtained in this manner.
The simplest example is the following:
\[
(\{0,1\},\mathbb{R}^{\{0,1\}},\mathbb{R})
\]
where this is taken to mean that all curves are smooth and only the constant functionals are smooth.
The problem here is that there are far more curves than the functionals warrant.
Put another way, the functionals cannot distinguish between the points of the set.

All Fr&#246;licher spaces satisfy half of the requirements for Isbell duality: the functions are always the natural transformations of the curves.

+-- {: .num_prop #FroFSat}
###### Proposition
The generalised $\mathcal{R}$-object corresponding to a Fr&#246;licher space is $F$-saturated.
=--

+-- {: .proof}
Let $(X,C,F)$ be a Fr&#246;licher space.
Recall from [[generalized object# IsbelDuality|generalised object]] that $F$-saturated means that $F$ is precisely the set of $C^\infty(\mathbb{R}, \mathbb{R})$-homs $C \to C^\infty(\mathbb{R},\mathbb{R})$.

We know that every element of $F$ gives a map $C \to C^\infty(\mathbb{R}, \mathbb{R})$ which commutes with the right actions.
As $C$ contains the constant functions at the points of $X$, this assignment is injective.

Let $\phi : C \to C^\infty(\mathbb{R},\mathbb{R})$ commute with the right actions.
Define $|\phi| : X \to \mathbb{R}$ by $|\phi|(x) = \phi(\delta_x)$ where $\delta_x \in C$ is the constant function at $x$.
Then for $\alpha \in C$, $|\phi| \circ \alpha (t) = |\phi|(\alpha(t)) = |\phi|(\alpha \circ \delta_t) = \phi(\alpha \circ \delta_t) = \phi(\alpha) \circ \delta_t = \phi(\alpha)(t)$.
Hence $|\phi| \circ \alpha \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $\alpha \in C$ and so $|\phi|$ is in $F$.

Hence $(X,C,F)$ is $F$-saturated.
=--

The other half is more complicated.
Using concreteness one can see that the essence depends on comparing the set $X$ with the set of _constant_ natural transformations $F \to C^\infty(\mathbb{R}, \mathbb{R})$.
That is, those natural transformations $\gamma$ with the property that $\gamma(\phi)$ is a constant function in $C^\infty(\mathbb{R}, \mathbb{R})$ for all $\phi \in F$.

+-- {: .num_lemma #Spec}
###### Lemma
The set $F$ is a $C^\infty(\mathbb{R}, \mathbb{R})$-algebra and the constant natural transformations on $F$ correspond with the algebra homomorphisms $F \to \mathbb{R}$.
=--

That is, we are looking at $Spec(F)$.

Now every point of $X$ defines a constant natural transformation via evaluation but this map need be neither injective nor surjective.
However, we can determine conditions on when it is injective or surjective.
Injectivity is related to a fairly simple condition (as indicated by the example earlier).

+-- {: .num_defn #FroHausdorff}
###### Definition
A Fr&#246;licher space is said to be _Hausdorff_ if the smooth functions separate points.
=--

+-- {: .num_prop #FroHausCSat}
###### Proposition
A Fr&#246;licher space $(X,C,F)$ is Hausdorff if and only if the map $X \to Spec(F)$ is injective.
=--

+-- {: .proof}
The key point here is that an element of $Spec(F)$ is completely determined by its effect on functions in $F$.
Thus $x, y \in X$ are such that they define the same element of $Spec(F)$ if and only if $\phi(x) = \phi(y)$ for all $\phi \in F$.
This means that the smooth functions do not separate $x$ and $y$.
Hence $(X,C,F)$ is Hausdorff if and only if $X \to Spec(F)$ is injective.
=--

It is simple to construct non-Hausdorff Fr&#246;licher spaces.
Indeed, the example earlier was one.

For surjectivity we need a kind of completeness result.

+-- {: .num_lemma #SpecSurj}
###### Lemma
For a Fr&#246;licher space $(X,C,F)$ the following conditions are equivalent.
1. $X \to Spec(F)$ is surjective.
2. Whenever $\tau : F \to \mathbb{R}$ is such that $\phi^{-1}(\tau(\phi)) \cap \psi^{-1}(\tau(\psi)) \ne \emptyset$ for any $\phi, \psi \in F$ then $\tau$ is evaluation at some $x \in X$.
=--

Before proving this, let us note that the second condition implies that for each pair $\phi, \psi \in F$ there is some $x$ such that $\phi(x) = \tau(\phi)$ and $\psi(x) = \tau(\psi)$.
We could call such a $\tau$ a _pairwise_ evaluation.
The condition says that all pairwise evaluations are genuine evaluations.

+-- {: .proof}
* 1 implies 2.

  Let $\tau : F \to \mathbb{R}$ satisfy the condition of (2).
We need to show that $\tau$ is an algebra homomorphism.

  We start by showing that $\tau$ is a natural transformation.
That is, that for $\phi \in F$ and $\theta \in C^\infty(\mathbb{R}, \mathbb{R})$ then $\tau(\theta \circ \phi) = \theta(\tau(\phi))$.
The assumption on $\tau$ implies that there is some $x \in X$ such that $\phi(x) = \tau(\phi)$ and $(\theta \circ \phi)(x) = \tau(\theta \circ \phi)$.
Thus
\[
\tau(\theta \circ \phi) = (\theta \circ \phi)(x) = \theta(\phi(x)) = \theta(\tau(\phi)).
\]

=--

+-- {: .query}
To be continued ...
=--

