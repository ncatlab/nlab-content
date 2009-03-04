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
(\{0,1\},\{\mathbb{R}^{\{0,1\}}\},\mathbb{R})
\]
where this is taken to mean that all curves are smooth and only the constant functionals are smooth.
The problem here is that there are far more curves than the functionals warrant.
Put another way, the functionals cannot distinguish between the points of the set.
This suggests a simple notion that is certainly required for a Fr&#246;licher space to satisfy Isbell duality.

+-- {: .num_defn #FroHausdorff}
###### Definition
A Fr&#246;licher space is said to be _Hausdorff_ if the smooth functions separate points.
=--

+-- {: .num_lemma #IsbellHausdorff}
###### Lemma
The Fr&#246;licher space corresponding to a generalised $\mathcal{R}$-object satisfying Isbell duality is Hausdorff.
=--

+-- {: .proof}
This is a simple consequence of the fact that as the curves are the natural transformations on the functions, two curves that are indistinguishable by functions must be viewed as the same curve.
=--

The converse of this result is true.

+-- {: .query}
I believe!
=--

Half of this result is simple.

+-- {: .num_prop #FroFSat}
###### Proposition
The generalised $\mathcal{R}$-object corresponding to a Fr&#246;licher space is $F$-saturated.
=--

+-- {: .proof}
Let $(X,C,F)$ be a Hausdorff Fr&#246;licher space.
Recall from [[generalized object# IsbelDuality|generalised object]] that $F$-saturated means that $F$ is precisely the set of $C^\infty(\mathbb{R}, \mathbb{R})$-homs $C \to C^\infty(\mathbb{R},\mathbb{R})$.

We know that every element of $F$ gives a map $C \to C^\infty(\mathbb{R}, \mathbb{R})$ which commutes with the right actions.
As $C$ contains the constant functions at the points of $X$, this assignment is injective.

Let $\phi : C \to C^\infty(\mathbb{R},\mathbb{R})$ commute with the right actions.
Define $|\phi| : X \to \mathbb{R}$ by $|\phi|(x) = \phi(\delta_x)$ where $\delta_x \in C$ is the constant function at $x$.
Then for $\alpha \in C$, $|\phi| \circ \alpha (t) = |\phi|(\alpha(t)) = |\phi|(\alpha \circ \delta_t) = \phi(\alpha \circ \delta_t) = \phi(\alpha) \circ \delta_t = \phi(\alpha)(t)$.
Hence $|\phi| \circ \alpha \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $\alpha \in C$ and so $|\phi|$ is in $F$.

Hence $(X,C,F)$ is $F$-saturated.
=--

Notice that this did not require the Fr&#246;licher space to be Hausdorff.

The other half is more complicated.

+-- {: .num_prop #FroHausCSat}
###### Proposition
A Hausdorff Fr&#246;licher space is $C$-saturated.
=--

+-- {: .proof}
The key to this proof is to show that when taking the set of natural transformations $F \to C^\infty(\mathbb{R}, \mathbb{R})$, no new points are added.

Let $(X,C,F)$ be a Hausdorff Fr&#246;licher space.
Let $\overline{X}$ be the set of maps $F \to C^\infty(\mathbb{R}, \mathbb{R})$ that commute with the left actions and which are constant.
By "constant" we mean that $x(\phi) : \mathbb{R} \to \mathbb{R}$ is a constant function for every $\phi \in F$.

We first note that there is a canonical map $X \to \overline{X}$ given by $\overline{x}(\phi) = \phi(x)$.
As $(X,C,F)$ is Hausdorff, this map is injective.
We want to show that this is bijective.

+-- {: .query}
To be continued ...
=--

=--
