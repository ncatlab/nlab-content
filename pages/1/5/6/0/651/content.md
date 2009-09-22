{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

* Here followeth the table of contents.
{:toc}

#Idea#

A Fr&#246;licher space is one flavour of a [[generalized smooth space]]. 

Fr&#246;licher smooth spaces are determined by a rule for 

* how to map the real line smoothly into it, 

* and how to map out of the space smoothly to the real line.

In the general context of [[space and quantity]], Fr&#246;licher spaces take an intermediate symmetric position: they are both [[presheaf|presheaves]] as well as copresheaves on their test domain (which here is the full [[subcategory]] of manifolds on the real line) and both of these structures determine each other.

The general abstract idea behind this is described at [[Isbell envelope]].

+-- {: goal}
###### Goal
The intention for this page is to develop the basic tools of differential topology for Fr&#246;licher spaces.
This means taking the basic pieces of "ordinary" differential topology and considering what they might look like for Fr&#246;licher spaces; including what looks the same and what looks different.

This project will both record existing structure and develop new ideas.
It is intentionally in the main area of the $n$-Lab to encourage contributions.
=--

# Basics # {#basics}

+-- {: mynumdef #FroelicherSpace}
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

To its eternal shame, the category of Fr&#246;licher spaces is __not__ [[locally cartesian closed category|locally cartesian closed]].

## Examples

1. Any smooth [[manifold]] defines a Fr&#246;licher space with curves $C^\infty(\mathbb{R}, M)$ and functions $C^\infty(M, \mathbb{R})$.

2. Taking quotients in the category of Fr&#246;licher spaces is straightforward: the smooth functions are those that pull-back to smooth functions on the original space.

   As an example, consider the plane $\mathbb{R}^2$ quotiented out by the $x$-axis.
Let us write this as $X$.
This example is closely related to taking cones and suspensions in algebraic topology.
The smooth functions on $X$ are simple to describe: the set is equivalent to those smooth functions $\mathbb{R}^2 \to \mathbb{R}$ which are constant on the $x$-axis.

   Now let us consider the smooth curves.
Let $\alpha : \mathbb{R} \to X$ be a smooth curve.
We can partition $\mathbb{R}$ into two pieces: those points that are mapped to the squashed point in $X$ and those points that aren't.
Let us write $A$ for the set of points that are __not__ mapped to the squashed point.
Using bump functions it is easy to show that $A$ is open in $\mathbb{R}$.
As the quotient map $\mathbb{R}^2 \to X$ is bijective off the $x$-axis, the restriction of $\alpha$ to $A$ has a unique lift to $\mathbb{R}^2$.
Let us write $\alpha_x$ and $\alpha_y$ for the coordinate functions of this lift.
Again using bump functions, it is easy to show that $\alpha_x$ and $\alpha_y$ are smooth on $A$.
Furthermore, as the projection $(x,y) \mapsto y$ descends to a smooth function on $X$, $\alpha_y$ is actually the restriction to $A$ of a smooth function $\mathbb{R} \to \mathbb{R}$ which we shall also denote by $\alpha_y$.
Note that $A = \alpha_y^{-1}(0)$.

   The interesting part comes when looking at what happens to $\alpha_x$ at the boundary of $A$.
As $A$ is open, it is a disjoint union of open intervals.
The boundaries of each of these intervals forms part of the boundary of $A$ and it is simplest to start with these points.
For further simplicity, let us assume that $(0,1)$ is one of the components of $A$ and we are considering the boundary point $0$.
Thus we wish to consider $\lim_{t \to 0^+} \alpha_x(t)$.

   We wish to show that this limit exists.
There are basically two cases to rule out here:

   1. $t \mapsto (\frac1t,t)$,
   2. $t \mapsto (\sin \frac1t, t)$.

   Both can be ruled out using the function $\phi : \mathbb{R}^2 \to \mathbb{R}$ defined by $\phi(x,y) = x y$.
This is constant, indeed zero, on the $x$-axis and so descends to a smooth function on $X$.
In the first case, $\phi \circ \alpha(t) = 1$ for $t \in (0,1)$ but $\phi \circ \alpha(0) = 0$.
In the second case, $\phi \circ \alpha$ is continuous at $0$ but not differentiable there.
Thus as $\phi \circ \alpha$ must be smooth, neither case is possible.

   Thus $\alpha_x$ extends to a continuous function on $[0,1)$.
It is straightforward to extend this to show that $\alpha_x$ extends to a smooth function on $[0,1)$, where by "smooth" we mean that the all one-sided derivatives exist at $0$.

   Thus the original curve $\alpha$ consists of a sequence of paths in either the upper or lower half planes with endpoints anchored on the $x$-axis.
These paths are parametrised by smooth paths $[a,b] \to \mathbb{R}^2$ with domains that are disjoint except, perhaps, for endpoints.
If the endpoints of two of these paths coincide then one of two things must happen:

   1. The paths are infinitely flat at the common endpoint, in which case nothing can be said about the corresponding points on the $x$-axis.
   2. The paths are not infinitely flat at the common endpoint, in which case the image of this point in $\mathbb{R}^2$ is the same under each path and the joined path is again smooth.

   The final thing to determine is what happens if we have a sequence of endpoints that converge in the domain.

   +-- {: .query}

   [[Andrew Stacey]]:
Note finished with this example, of course.
Some pictures would be nice, I guess.
As it's an example I'm not sure how much detail to give.
Comments would be helpful on that score!

   =--

3. Let us give an example that shows that the category of Fr&#246;licher spaces is not [[locally cartesian closed category|locally cartesian closed]].
Consider a [[coequaliser]] diagram $\mathbb{R} \setminus \{0\} \to \mathbb{R} \amalg \mathbb{R}$ where the two maps are the inclusions into the two cofactors.

   The coequaliser of this diagram is $\mathbb{R} \cup \{*\}$ where the $*$ is a doubled-point at $0$.  (So this is the well-known example of a non-Hausdorff [[manifold]].)
Thus any smooth function $\psi : \mathbb{R} \cup \{*\} \to \mathbb{R}$ has to satisfy $\psi(0) = \psi(*)$, which means that any smooth curve $\alpha : \mathbb{R} \to \mathbb{R} \cup \{*\}$ can choose whether to pass through $0$ or $*$ completely arbitrarily.

   We consider this as a coequaliser of spaces over $\mathbb{R}$ by taking the obvious map to $\mathbb{R}$ in each case.
The colimit is the same whether we work in the full category of Fr&#246;licher spaces or just those over $\mathbb{R}$.

   Now let $Y$ be any Fr&#246;licher space and consider it as a space over $\mathbb{R}$ via the [[constant function|constant]] zero map, $\omicron : Y \to \mathbb{R}$.
We take the [[fibred product]] over $\mathbb{R}$ of the coequaliser diagram.
Since $\mathbb{R} \setminus \{0\}$ has no points mapping to $0$, $(\mathbb{R} \setminus \{0\}) \times_{\mathbb{R}} Y = \emptyset$.
For the third space, we see that $(\mathbb{R} \amalg \mathbb{R}) \times_{\mathbb{R}} Y = Y \amalg Y$.
Thus the coequaliser diagram is now $\emptyset \to Y \amalg Y$.
The coequaliser is thus $Y \amalg Y$.
Note that smooth curves into $Y \amalg Y$ are of the form $(i, \beta)$ where $i$ is a constant in $\{0,*\}$ that distinguishes the cofactors and $\beta : \mathbb{R} \to Y$ is a smooth curve in $Y$.

   Let us consider the product over $\mathbb{R}$ of $\mathbb{R} \cup \{*\}$ with $Y$.
As a set, this is just $Y \amalg Y$ again.
However, as a Fr&#246;licher space it has different functions to those on $Y \amalg Y$.
The product over $\mathbb{R}$ is a subspace of $(\mathbb{R} \cup \{*\}) \times Y$ and thus a curve into it is smooth if and only if it is smooth into $(\mathbb{R} \cup \{*\}) \times Y$, whence it is smooth if and only if the projections to $\mathbb{R} \cup \{*\}$ and to $Y$ are smooth.
As we are considering curves in $(\mathbb{R} \cup \{*\}) \times_\mathbb{R} Y$, the projection to $\mathbb{R} \cup \{*\}$ must have image in $\{0,*\}$.
Thus _any_ curve is allowed by this and so the smooth curves into $(\mathbb{R} \cup \{*\}) \times_\mathbb{R} Y$ are of the form $(\alpha, \beta)$ where $\alpha$ is *any* function from $\mathbb{R}$ into $\{0,*\}$ and $\beta : \mathbb{R} \to Y$ is a smooth curve in $Y$.

   +-- {: .query}
   I notice that in some classically false versions of [[constructive mathematics]], the only functions from $\mathbb{R}$ to $\{0,*\}$ are the constant ones.  It would be nice if there were a nonclassical dream universe in which the category of Fr&#246;licher spaces were locally cartesian closed!  Unfortunately, the counterexample can be saved by using a continuously parametrised coproduct $\coprod_{\mathbb{R}} \mathbb{R}$ instead of $\coprod_{\{0,*\}} \mathbb{R} = \mathbb{R} \amalg \mathbb{R}$.  ---Toby

   [[Andrew Stacey]] I think I'd be disappointed if locally cartesian became a property of what set theory was being used!  I suspect that the real reason this example works is the fact that $Y \to \mathbb{R}$ has such bad path-lifting properties and the coequaliser diagram that I chose is just a simple one that demonstrates it.

   I've been pondering how one might fix this.  I ought to write up Kriegl and Michor's extension of a manifold as, although they haven't done much with it, it contains some ideas that may be of interest.  What makes me think of it here is that that definition of a manifold (which isn't, by the way, the one in their weighty tome) has two parts: a space and its tangent space, and relationships between them.  This suggests that a smooth space, of whatever variety, should be more than just one space but some sort of diagram of spaces.

   This is also suggested by trying to generalise the Frolicher "idea" to non-set-based theories.  It's not immediately obvious how to make the saturation condition work, but the basic idea is to have objects as $(C,F,c)$ with $c : C \times F \to Hom$ and morphisms as $f : C_X \times F_Y \to Hom$.  The saturation condition, whatever it is, is what is needed to make this into a category.  So here it's obvious that objects are just special morphisms.  Feeding this back into the definition you get a glimmer of an idea that maybe a morphism (let me go back to genuine Frolicher spaces here for clarity) $f : X \to Y$ needs some sort of saturation condition as well as a compatibility condition.
   =--

   This is not the same as $Y \coprod Y$ and thus the functor $- \times_{\mathbb{R}} Y$ does not preserve colimits.
It cannot, therefore, be a left adjoint and so the category of Fr&#246;licher spaces is not locally cartesian closed.

   This example works because of the structure of $\mathbb{R} \cup \{*\}$.
If one were to work in an "input only" category, then the structure on $\mathbb{R} \cup \{*\}$ would be determined by those curves which lift to $\mathbb{R} \coprod \mathbb{R}$.
Such maps could not arbitrarily swap between $0$ and $*$ because up in $\mathbb{R} \coprod \mathbb{R}$ these two points are far apart.
Thus the subspace structure on $\{0,*\}$ in an "input only" category is _discrete_.
However, in the category of Fr&#246;licher spaces the outputs control the behaviour of quotients.
Functions out of $\mathbb{R} \cup \{*\}$ cannot detect the difference between $0$ and $*$.
Thus curves into $\mathbb{R} \cup \{*\}$ are allowed to swap between them with aplomb.
The subspace structure on $\{0,*\}$ is thus the _indiscrete_ structure.

   Working in the category of _Hausdorff_ Fr&#246;licher spaces (see [below](#hausdorff)) does not improve matters.
Then we need to replace each coequaliser but its Hausdorffification.
Now the distinction is clear since taking the product and then the coequaliser yields $Y \coprod Y$ as before but taking the coequaliser and then the product yields just $Y$.

   It is also worth pointing out that with the modification of the previous paragraph, this example only involves manifolds (assuming that $Y$ is chosen to be a manifold).  It therefore shows that a category extending that of smooth manifolds can __either__ be locally cartesian closed __or__ preserve limits and colimits from manifolds _but not both_.

***

# Isbell Envelope # {#isbell}

Fr&#246;licher spaces are examples of [[generalized smooth space|generalised smooth spaces]].  The category of Fr&#246;licher spaces is also closely related to the concept of the [[Isbell envelope]] of a category.

+-- {: mynumdef #RCat}
###### Definition
Let $\mathcal{R}$ denote the category with one object and morphism set $C^\infty(\mathbb{R},\mathbb{R})$.
=--

There is a close relationship between Fr&#246;licher spaces and the subcategory of $E(\mathcal{R})$, the Isbell envelope of $\mathcal{R}$, of those objects satisfying Isbell duality.

+-- {: .num_prop #IsbellIsFroelicher}
###### Proposition
An object of $E(\mathcal{R})$ that satisfies Isbell duality is a Fr&#246;licher space.
=--

+-- {: myproof}
###### Proof
Let $X = (C,F)$ be a generalised $\mathcal{R}$-object satisfying Isbell duality.
From the page about the [[Isbell envelope]], $X$ is concrete.
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
The object of $E(\mathcal{R})$ corresponding to a Fr&#246;licher space is $F$-saturated.
=--

+-- {: myproof}
###### Proof
Let $(X,C,F)$ be a Fr&#246;licher space.
Recall from the page about the [[Isbell envelope]] that $F$-saturated means that $F$ is precisely the set of $C^\infty(\mathbb{R}, \mathbb{R})$-homs $C \to C^\infty(\mathbb{R},\mathbb{R})$.

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

+-- {: .num_lemma #NatTransFSet}
###### Lemma
A constant natural transformation $F \to C^\infty(\mathbb{R}, \mathbb{R})$ is a function $\alpha : F \to \mathbb{R}$ with the property that $\alpha(\phi \circ \psi) = \phi(\alpha(\psi))$.
=--

Let us write $|F|$ for this set.

Now every point of $X$ defines a constant natural transformation via evaluation but the map $X \to |F|$ need be neither injective nor surjective.
However, we can determine conditions on when it is injective or surjective.
Injectivity is related to a fairly simple condition (as indicated by the example earlier).

+-- {: mynumdef #FroHausdorff}
###### Definition
A Fr&#246;licher space is said to be _[[Hausdorff space|Hausdorff]]_ if the smooth functions separate points.
=--

+-- {: .num_prop #FroHausCSat}
###### Proposition
A Fr&#246;licher space $(X,C,F)$ is Hausdorff if and only if the map $X \to |F|$ is injective.
=--

+-- {: myproof}
###### Proof
The key point here is that an element of $|F|$ is completely determined by its effect on functions in $F$.
Thus $x, y \in X$ are such that they define the same element of $|F|$ if and only if $\phi(x) = \phi(y)$ for all $\phi \in F$.
This means that the smooth functions do not separate $x$ and $y$.
Hence $(X,C,F)$ is Hausdorff if and only if $X \to |F|$ is injective.
=--

It is simple to construct non-Hausdorff Fr&#246;licher spaces.
Indeed, the example earlier was one.

Surjectivity is more complicated.
As currently stated, not even very simple Fr&#246;licher spaces satisfy the surjectivity condition.

+-- {: .num_lemma #PlaneNonSurj}
###### Lemma
The Fr&#246;licher space defined by the usual structure on $\mathbb{R}^2$ does not satisfy the surjectivity condition.
=--

+-- {: myproof}
###### Proof
We need to construct a map $\alpha : F \to C^\infty(\mathbb{R}, \mathbb{R})$ such that $\alpha(\psi \circ \phi) = \psi(\alpha(\phi))$ but which does not correspond to a point in $\mathbb{R}^2$.

A non-zero point $p \in \mathbb{R}^2$ defines an element $\pi_p$ of $F$ by composing orthogonal projection $\mathbb{R}^2 \to \langle p \rangle$ with the map $\langle p \rangle \to \mathbb{R}$ defined by $p \mapsto 1$.
If $p, q \in \mathbb{R}^2$ are not collinear then the only situation in which $\psi \circ \pi_p = \phi \circ \pi_q$ is if $\psi$ and $\phi$ are constant functions.
To see this, let $p'$ be orthogonal to $p$ and $q'$ orthogonal to $q$ be such that the orthogonal projection of $p'$ to the line spanned by $q$ is $q$, and similarly $q'$ maps to $p$.
Then $p'$ and $q'$ span $\mathbb{R}^2$ and
\[
\begin{aligned}
\psi \circ \pi_p(\lambda p' + \mu q') &= \psi \circ \pi_p(\mu q') &&= \psi(\mu) \\
\phi \circ \pi_q(\lambda p' + \mu q') &= \phi \circ \pi_q(\lambda p') &&= \phi(\lambda)
\end{aligned}
\]
As this holds for all $\lambda, \mu$ we see that $\psi$ and $\phi$ are constant functions.

Moreover, the functions $\pi_p$ are "initial" in $F$ in the sense that if $\pi_p = \psi \circ \phi$ for some $\phi \in F$ then $\phi$ is of the form $\theta \circ \pi_p$.
We thus conclude that in defining a map $\alpha : F \to \mathbb{R}$ such that $\alpha(\psi \circ \phi) = \psi(\alpha(\phi))$ we have free choice on the values $\alpha(\pi_p)$.
However, the maps $F \to C^\infty(\mathbb{R}, \mathbb{R})$ which come from evaluation do not have this free choice: their value on $\pi_p$ is completely determined by the values on $\pi_x$ and $\pi_y$.
=--

However, all is not lost.
The set of functions in a Fr&#246;licher space has much more structure than simply composition by functions from $C^\infty(\mathbb{R}, \mathbb{R})$.

+-- {: .num_lemma #FroFunAlg}
###### Lemma
The set $F$ of functions in a Fr&#246;licher space is a commutative $\mathbb{R}$-algebra.
=--

+-- {: myproof}
###### Proof
Let $(X,C,F)$ be a Fr&#246;licher space.
Let $\phi, \psi, \theta \in F$.
Then $\phi \circ \alpha$, $\psi \circ \alpha$, and $\theta \circ \alpha$ lie in $C^\infty(\mathbb{R}, \mathbb{R})$.
Thus as $C^\infty(\mathbb{R}, \mathbb{R})$ is a ring,
\[
\phi \circ \alpha + (\theta \circ \alpha) \cdot (\psi \circ \alpha) = (\phi + \theta \cdot \psi) \circ \alpha
\]
is in $C^\infty(\mathbb{R}, \mathbb{R})$.
As this holds for all $\alpha \in C$, $\phi + \theta \cdot \psi \in F$.
It is commutative because $C^\infty(\mathbb{R}, \mathbb{R})$ is commutative.
Finally we note that there is an obvious ring homomorphism $\mathbb{R} \to F$ sending $\lambda$ to the function $x \mapsto \lambda$.
=--

This suggests that we should consider a Fr&#246;licher space not as a pair of functors $\mathcal{R}, \mathcal{R}^{op} \to Set$ but as a pair of functors $\mathcal{R} \to Set$ and $\mathcal{R}^{op} \to Alg$.

There is yet more structure on $F$.
Not only can we compose element of $F$ with elements of $C^\infty(\mathbb{R}, \mathbb{R})$ but if $\phi \in F$ is a particular element then we can compose $\phi$ with an element of $C^\infty(\im \phi, \mathbb{R})$.
This suggests that we ought to enlarge the category $\mathcal{R}$ so that its objects are the power set $\mathcal{P}(\mathbb{R})$.

(An alternative to this extension is to insist that the natural transformations be continuous with respect to a topology on $F$ compatible with the compact-open topology on $C^\infty(\mathbb{R}, \mathbb{R})$.)

With these two augmentations, a constant natural transformation from $F(A) \to C^\infty(-,A)$, with $A \subseteq \mathbb{R}$, defines an algebra homomorphism $F(\mathbb{R}) \to \mathbb{R}$ with the property that $\alpha(\psi) \in \im \psi$ for all $\psi \in F(\mathbb{R})$.

+-- {: .num_lemma #LemPairEval}
###### Lemma
Such a natural transformation, $\alpha$, has the property that for any pair $\phi, \psi \in F(\mathbb{R})$ there is a point $x \in X$ such that $\alpha(\psi) = \psi(x)$ and $\alpha(\phi) = \phi(x)$.
=--

+-- {: myproof}
###### Proof
Consider the function
\[
\theta = (\psi - \alpha(\psi))^2 + (\phi - \alpha(\phi))^2.
\]
As $\alpha$ is an algebra homomorphism, $\alpha(\theta) = 0$.
Since $\alpha(\theta) \in \im \theta$, there is thus some $x \in X$ such that $\theta(x) = 0$.
For this $x$ we therefore have that $\psi(x) = \alpha(\psi)$ and $\phi(x) = \alpha(\phi)$.
=--

This clearly extends to any finite family.
Indeed, from the proof of this result we deduce that the family
\[
\mathcal{A} := \big\{\{x : \phi(x) = \alpha(\phi)\} : \phi \in F(\mathbb{R})\big\}
\]
is directed and thus defines a filter on $X$.
If our natural transformation $\alpha$ is _not_ represented by a point on $X$ then this filter will have empty intersection.

Now consider the subfamily of $F(\mathbb{R})$ consisting of those functions $\phi$ with the property that $\im \phi \subseteq [0,1]$ and $\alpha(\phi) = 1$.
It is clear that if we restrict to this family then we still get all of $\mathcal{A}$.
We can order this family; there are two equivalent (but not isomorphic) orderings:

1. $\phi \leq \psi$ if $\phi(x) \leq \psi(x)$ for all $x \in X$, or
2. $\phi \leq \psi$ if $\phi^{-1}((0,1]) \subseteq \psi^{-1}((0,1])$.

This family is directed (downwards) since $\phi \psi \leq \phi$ (and $\psi$).
In any _reasonable_ topology on $F$ then this net converges to the zero function: on any compact subset of $X$ then we have $(\phi) \to 0$ uniformly.
Therefore if we simply add the condition that our natural transformation $\alpha$ be continuous (something we might have been ready to do anyway) we see that it must be represented by an element of $X$ since otherwise we have $\alpha(0) = \lim \alpha(\phi) = 1 \notin \im 0$.

Thus $X$ is the set of _continuous_ algebra homomorphisms $F \to \mathbb{R}$ and we finally see the relationship between Hausdorff Fr&#246;licher spaces as objects in the Isbell envelope of $\mathbf{R}$ satisfying Isbell duality.

***

# Topological Notions of Fr&#246;licher Spaces # {#topology}

In the above we used a couple of topological notions.
We used a vague notion of topology on the functions on a Fr&#246;licher space and we introduced the notion of a Hausdorff Fr&#246;licher space.
These illustrate two different ways of thinking of topological notions on Fr&#246;licher spaces.
The one says that there is a functor (actually two functors) from the category of F&#246;licher space to the category of topological spaces so we can say that a Fr&#246;licher space has topological property $P$ if the corresponding topological space has it.
The other approach says that we can directly define a property for Fr&#246;licher spaces that is _analogous_ to a topological property.
We then might hope for a theorem saying that a Fr&#246;licher space with property $P$ defines a topological space with the corresponding property $P$.
However, this would definitely be a theorem.
This second approach is the one that I want to study in this section.

Let us start by defining the two functors to topological spaces.

+-- {: mynumdef #FroTop}
###### Definition
The _curvaceous_ topology on a Fr&#246;licher space is the strongest topology for which the smooth curves are continuous.

The _functional_ topology on a Fr&#246;licher space is the weakest topology for which the smooth functions are continuous.
=--

It is clear that these assignments are functorial, and that the curvaceous topology is always at least as strong as the functional topology.

In general, we shall often define two notions of each topological property: a curvaceous one and a functional one.
Sometimes these will be the same.

Let us start with some very simple definitions.

+-- {: mynumdef #DiscIndisc}
###### Definition
A Fr&#246;licher space is said to be _indiscrete_ if all curves are smooth.

A Fr&#246;licher space is said to be _discrete_ if all functions are smooth.
=--

Let us observe that there is no need for functional or curvaceous versions of these definitions.

+-- {: .num_lemma #LemDiscIndisc}
###### Lemma
A Fr&#246;licher space is indiscrete if and only if the only smooth functions are the constant ones.

A Fr&#246;licher space is discrete if and only if the only smooth curves are the constant ones.
=--

+-- {: myproof}
###### Proof
If all curves are smooth then for any points $x, y \in X$ the curve
\[
\alpha(t) = \begin{cases}
x & t \leq 0 \\
y & t \ge 0
\end{cases}
\]
is smooth.
Composition with $\phi \in F$ yields the function
\[
t \mapsto \begin{cases}
\phi(x) & t \leq 0 \\
\phi(y) & t \ge 0
\end{cases}
\]
For this to be a smooth function in $C^\infty(\mathbb{R}, \mathbb{R})$ we must have $\phi(x) = \phi(y)$, hence $\phi$ is constant.

For the converse, if the only smooth functions are constant then any curve $\alpha : \mathbb{R} \to X$ satisfies the condition that $\phi \circ \alpha \in C^\infty(\mathbb{R}, \mathbb{R})$ for all $\phi \in F$ so is in $C$.
Hence all curves are smooth.

The discrete case is similar.
=--

Earlier we introduced the notion of a _Hausdorff_ Fr&#246;licher space.
Technically, we ought to have called that _functionally Hausdorff_ as it used the smooth functions in its definition.

+-- {: mynumdef #DefFroHausdorff}
###### Definition
A Fr&#246;licher space is said to be _functionally Hausdorff_ if the smooth functions separate points.

A Fr&#246;licher space is said to be _curvaceously Hausdorff_ if the only smooth curves with finite image are constant.
=--

However, the distinction is not important as the following lemma shows.

+-- {: .num_lemma #LemFroHausdorff}
###### Lemma
The notions of functional Hausdorff and curvaceously Hausdorff coincide and are equivalent to the underlying topological spaces being Hausdorff.
=--

+-- {: myproof}
###### Proof
Suppose that $(X,C,F)$ is not functionally Hausdorff.
Then there are $x \ne y \in X$ such that $\phi(x) = \phi(y)$ for all $\phi \in X$.
Let $\alpha : \mathbb{R} \to X$ be the function taking the value $x$ for $t \leq 0$ and $y$ for $t \ge 0$.
Then $\phi \circ \alpha$ is constant for all $\phi \in F$ so $\alpha \in C$.
However, $\alpha$ has finite image but is not constant.
Thus $(X,C,F)$ is not curvaceously Hausdorff.

Conversely, suppose that $(X,C,F)$ is not curvaceously Hausdorff.
Then there is some $\alpha \in C$ with finite image which is not constant.
Let $\phi \in F$.
Then $\phi \circ \alpha$ has finite image in $\mathbb{R}$ and hence is constant.
Thus for $x, y \in \im \alpha$, $\phi(x) = \phi(y)$ for all $\phi \in F$.
As $\alpha$ is not constant, there are thus $x \ne y \in X$ such that $\phi(x) = \phi(y)$ for all $\phi \in F$ and so $(X,C,F)$ is not functionally Hausdorff.

If a Fr&#246;licher space is Hausdorff then smooth functions separate points.
Thus for $x \ne y \in X$, there is a smooth function $\phi \in F$ with $\phi(x) = -1$ and $\phi(y) = 1$.
Then the sets $\phi^{-1}(-\infty,0)$ and $\phi^{-1}(0,\infty)$ are sufficient to show that $X$ with the functional topology is Hausdorff.
As the curvaceous topology is stronger than the functional one, it is thus also Hausdorff.

Suppose that $X$ with the curvaceous topology is Hausdorff.
Then any finite subset is discrete and so there are no non-constant continuous maps $\mathbb{R} \to X$ with finite image.
In particular, there are no non-constant smooth maps and so the original Fr&#246;licher space was Hausdorff.
=--

In light of this, we shall refer to just _Hausdorff_ Fr&#246;licher spaces.

Just as with topological spaces, there is a "Hausdorffification" functor.
Unlike topological spaces, this functor is split.

+-- {: .num_lemma #LemHausFunct}
###### Lemma
Let $(X,C,F)$ be a Fr&#246;licher space.
Let $Y$ be the quotient of $X$ by the relation $x \sim y$ if $\phi(x) = \phi(y)$ for all $\phi \in F$.
Then $Y$ inherits a Fr&#246;licher space structure from $X$ with respect to which it is Hausdorff.
The natural map $X \to Y$ is a quotient mapping in the category of Fr&#246;licher spaces.
It is split, but not canonically so.
However, any two splittings are related by a diffeomorphism on $X$.

The assignment $X \mapsto Y$ is left adjoint to the inclusion of the category of Hausdorff Fr&#246;licher spaces in the category of all Fr&#246;licher spaces.
=--

+-- {: myproof}
###### Proof
The Fr&#246;licher structure on $Y$ is defined by setting $F_Y$ to be the set of functions $\phi : Y \to \mathbb{R}$ such that the composition $X \to Y \xrightarrow{\phi} \mathbb{R}$ is in $F_X$.
The smooth curves are then defined by the saturation condition.
It is automatic from this definition that any smooth curve in $X$ projects down to a smooth curve in $Y$ which explains why this family of functions on $Y$ is also saturated and hence we have a Fr&#246;licher space structure on $Y$.

To show that $Y$ is Hausdorff, we merely observe that by slight abuse of notation, $F_X = F_Y$ so if $x,y \in X$ are such that $\phi(\overline{x}) = \phi(\overline{y})$ for all $\phi \in F_Y$ then $\phi(x) = \phi(y)$ for all $\phi \in F_X$, whence $overline{x} = \overline{y}$ in $Y$.

That this is a quotient is straightforward.
Any smooth map $g : X \to Z$ which factors through $Y$ _as a set_ must also do so as a Fr&#246;licher space.
In particular, if $g : X \to Z$ is a smooth map with $Z$ Hausdorff then this must factor through $Y$ as a set, whence as a Fr&#246;licher space.
This also establishes the necessary adjunction.

Finally, let us look at the splitting.
For each point in $Y$ choose a representative of the equivalence class.
This choice defines a map on the underlying sets $Y \to X$.
This is also smooth since the sets of functions $F_X$ and $F_Y$ are identified by the quotient mapping $X \to Y$.

Given two such splittings, say $i, j : Y \to X$, define a bijection $X \to X$ which interchanges $i(y)$ and $j(y)$.
As $i$ and $j$ are splits of the quotient mapping $X \to Y$ this is well-defined.
It is also clearly a diffeomorphism since $F_X$ cannot detect the difference between $i$ and $j$.
=--

This shows, incidentally, that every smooth curve in the Hausdorffification of $X$ lifts to a smooth curve in $X$.
This sort of behaviour does not _usually_ happen with quotients in the category of Fr&#246;licher spaces.

The fibres of the Hausdorffification are straightforward to identify.

+-- {: .num_lemma #FibHaus}
###### Lemma
The fibres of the Hausdorffification of a Fr&#246;licher space correspond precisely to the maximal subsets which inherit an indiscrete structure from the ambient space.
=--

+-- {: myproof}
###### Proof
Let $X$ be a Fr&#246;licher space, $Y$ its Hausdorffification.
For $y \in Y$, let $X_y$ be the corresponding fibre.
Then $X_y$ inherits a Fr&#246;licher space structure from its inclusion in $X$.
The smooth curves in $X_y$ are those that are smooth when considered as curves in $X$.
Let $\alpha : \mathbb{R} \to X_y$ be an arbitrary curve.
Then for $\phi \in F_X$, as $\im \alpha \subseteq X_y$, $\phi \circ \alpha$ is constant.
Hence $\alpha$ is smooth as a curve in $X$, and thus in $X_y$.
Thus $X_y$ is indiscrete.

Conversely, let $Z \subseteq X$ be a subset that inherits an indiscrete structure from $X$.
Let $x,y \in Z$.
Then there is a smooth curve $\alpha$ in $Z$ with $\im \alpha = \{x,y\}$.
This is then smooth in $X$ so for all $\phi \in F_X$, $\phi(x) = \phi(y)$.
Hence $Z$ is contained in a (unique) fibre of the quotient map $X \to Y$.
=--

Thus when we pass to the Hausdorffification we lose almost no information at all and one could certainly say that we lose no _interesting_ information.

Having dealt with Hausdorff Fr&#246;licher spaces, the obvious next thing to do is to consider the other separation properties.
Our next definition may be a little surprising at first.

+-- {: mynumdef #FroReg}
###### Definition
A Fr&#246;licher space is said to be _regular_ if the curvaceous and functional topologies agree.
=--

The point of this definition is that for the underlying topological space of a Fr&#246;licher space what one really wants to know is not whether or not it is regular but whether or not it is _smoothly_ regular.
This is automatic for the functional topology so the only reasonable question is whether or not it happens for the curvaceous topology.
However, a topology is smoothly regular if and only if the smooth functions generate the topology which means that the curvaceous topology is smoothly regular if and only if it agrees with the functional topology.
Hence the definition.

On another tack, it is straightforward to see what one version of [[compact space|compactness]] should be.

+-- {: mynumdef #FunComp}
###### Definition
A Fr&#246;licher space is _functionally compact_ if every smooth function has bounded image.
=--

The images are automatically compact as a smooth function with non-compact image can be converted to a smooth function with unbounded image by suitable composition.

+-- {: .num_lemma #LemFunComp}
###### Lemma
A Fr&#246;licher space is functionally compact if and only if the functional topology is compact.
=--

+-- {: myproof}
###### Proof
One way is obvious: if the functional topology is compact then as the smooth functions are continuous, they have compact image, hence bounded.

For the converse, assume that the functional topology is not compact.
Then we can find a countable family of points $(x_n)$ with no accumulation points.
As the functional topology is (smoothly) regular, we can find smooth functions $(\phi_n)$ such that $\phi_n(x_m) = \delta_{n m}$.
We claim that it is possible to modify these to have disjoint support.
This is done recursively using postcomposition by suitably chosen functions.
Once this is done, we can define a new smooth function by $\sum n \widehat{\phi_n}$.
This is smooth, as the components have disjoint support, and is unbounded.
Hence the Fr&#246;licher space is not functionally compact.
=--

Although it would be pleasant to have an intrinsic definition of curvaceously compact, the following lemma shows that we already have a way to determine whether or not the curvaceous topology is compact.

+-- {: .num_lemma #CurvComp}
###### Lemma
The curvaceous topology of a Fr&#246;licher space is compact if and only if the Fr&#246;licher space is functionally compact and regular.
=--

+-- {: myproof}
###### Proof
Since the topologies on a Fr&#246;licher space are the pull-backs of the topologies on the Hausdorffification, it is sufficient to prove this for a Hausdorff Fr&#246;licher space.

As the curvaceous topology is stronger than the functional, if the curvaceous topology is compact then so is the functional.
Moreover, as both are Hausdorff spaces, the identity map is a continuous bijection from a compact space to a Hausdorff space and hence a homeomorphism.
Thus the Fr&#246;licher space is regular.

Conversely, if the Fr&#246;licher space is regular its topologies agree and thus if it is functionally compact then its curvaceous topology is compact.
=--

Another obvious topological property is connectedness.
Here it is obvious what the two definitions should be.

+-- {: mynumdef #FroConnect}
###### Definition
A Fr&#246;licher space is _functionally connected_ if the only idempotents in its algebra of functions are the trivial ones.

More generally, the _functional connected components_ of a Fr&#246;licher space $(X,C,F)$ are the equivalence classes of the relation $x \sim y$ if whenever $\phi \in F$ is idempotent then $\phi(x) = \phi(y)$.

A Fr&#246;licher space is _curvaceously connected_ if every pair of points lie on a curve.

More generally, the _curvaceous connected components_ of a Fr&#246;licher space $(X,C,F)$ are the equivalence classes of the relation $x \sim y$ if there is a smooth curve $\alpha \in C$ with $\alpha(0) = x$ and $\alpha(1) = y$.
=--

That the second relation is an equivalence relation follows from the fact that piecewise smooth curves can be reparametrised to smooth curves.

+-- {: .num_lemma #LemConnect}
###### Lemma
The notions of functionally connected and curvaceously connected coincide.
=--

+-- {: myproof}
###### Proof
Let $(X,C,F)$ be a Fr&#246;licher space.
It is clear that if $x, y \in X$ are such that there is a smooth curve connecting them then $\phi(x) = \phi(y)$ for any idempotent $\phi \in F$.
Thus we need to show the reverse implication.
To do this, let $X' \subseteq X$ be a curvaceously connected component of $X$.
Let $\phi \colon X \to \mathbb{R}$ be the characteristic function of $X'$.
Then for any $\alpha \in C$, either $\im \alpha \subseteq X'$ or $\im \alpha \cap X' = \emptyset$.
Thus $\phi \circ \alpha$ is a constant function.
Hence $\phi \in F$.
Thus if $x$ and $y$ are in different curvaceously connected components there is an idempotent element of $F$ separating them.
Hence the two notions are the same.
=--

+-- {: .num_corollary #CorConnect}
###### Corollary
The functional and curvaceous topologies have the same connected components, and these are the same as the path-connected components.
=--

***

# Hausdorff Fr&#246;licher Spaces # {#hausdorff}

There is not a great deal of difference between a Hausdorff Fr&#246;licher space and a generic one.
Much less than the case with topological spaces.
To pass from all Fr&#246;licher spaces to Hausdorff Fr&#246;licher spaces involves only collapsing everything that is _indiscrete_.
This clears out a considerable amount of junk from the category but does remove two properties: it no longer has a weak subobject classifier and it is no longer topological over $\Set$.

On the other hand, the relationship between the category of Hausdorff Fr&#246;licher spaces and that of all Fr&#246;licher spaces is very good.
Not only is it a [[reflective subcategory]] with all that that implies, but the morphisms from the [[unit|unit natural transformation]] are [[retract|split epimorphisms]] (though not naturally split).

The category of Hausdorff Fr&#246;licher spaces is thus complete and co-complete.
It is also cartesian closed since the product and exponential objects of Hausdorff Fr&#246;licher spaces are again Hausdorff.

+-- {: .query}
Do I need to prove this, or is it automatic?
(I can prove it if necessary)

[[Mike Shulman|Mike]]: Completeness and cocompleteness are of course automatic.  It is not automatic that a reflective subcategory inherits cartesian closure; the closest thing I can think of is A4.3.1 in the [[Elephant]] which says that a reflective subcategory is an [[exponential ideal]] iff its reflector preserves finite products.

[[Andrew Stacey|Andrew]]: Is it true, then, that all I need to do is to prove that the exponential of one Hausdorff object by another Hausdorff object is again Hausdorff?

[[Mike Shulman|Mike]]: Yes, that would certainly suffice to show that the category of Hausdorff objects is cartesian closed.

[[Andrew Stacey|Andrew]]: Ah, and now I see from [[exponential ideal]] that I could just show that the Hausdorffification of a product is the product of the Hausdorffifications.  Both seem quite simple, not sure which is the simplest.
=--

In considering [[Isbell duality]] in the context of Fr&#246;licher spaces we saw one good reason to restrict to Hausdorff Fr&#246;licher spaces.
Another reason comes from the inclusion of the category of manifolds in that of Fr&#246;licher spaces.
This factors through Hausdorff Fr&#246;licher spaces and this inclusion has some very pleasant properties.

+-- {: .num_theorem #Manifolds}
###### Theorem
The inclusion functor from the category of Manifolds to that of Hausdorff Fr&#246;licher spaces preserves limits and colimits.
=--

+-- {: myproof}
Let us write $\mathcal{M}$ for the category of manifolds, $\mathcal{H}$ for the category of Hausdorff Fr&#246;licher spaces, and $\mathcal{F}$ for the category of all Fr&#246;licher spaces.
We shall not give the inclusion functors special symbols but trust to context to distinguish.
Let $\mathfrak{F} : I \to \mathcal{M}$ be a functor where $I$ is a small category.

Let us assume first that $\mathfrak{F}$ has a limit in $\mathcal{M}$, say $M_0$ with maps $\alpha_i : M_0 \to \mathfrak{F}(i)$.
Let us write $X_0$ for the limit of $\mathfrak{F}$ viewed as a functor into $\mathcal{H}$, with maps $\beta_i : X_0 \to \mathfrak{F}(i)$.
As $\mathcal{H}$ is a [[reflective subcategory]] of $\mathcal{F}$, $X_0$ is the same as the limit of $\mathfrak{F}$ in $\mathcal{F}$.

Since $M_0$, as a Fr&#246;licher space, is a source of $\mathfrak{F}$, there is a unique map, say $\gamma : M_0 \to X_0$, such that $\beta_i \gamma = \alpha_i$.

As a Fr&#246;licher space, $X_0$ is completely determined by its underlying set and its smooth curves.
Its underlying set is (naturally isomorphic to) $\mathcal{F}(*,X_0)$.
Let $x \in |X_0|$.
Composing with the $\beta_i$ defines maps $\beta_i x : * \to \mathfrak{F}$.
Since $*$ is a manifold and $M_0$ is the limit of $\mathfrak{F}$ in $\mathcal{M}$, there is a unique map $\widehat{x} : * \to M_0$ such that $\alpha_i \widehat{x} = \beta_i x$ for all $i \in I$.
Using the uniqueness of the factorisations, we see that $\gamma \widehat{x} = x$ and thus $\gamma$ induces a bijection $|M_0| \to |X_0|$.
Hence the underlying sets of $M_0$ and $X_0$ are the same.

The smooth curves of $X_0$ are the morphisms $\mathbb{R} \to X_0$.
Since $\mathbb{R}$ is a manifold, the same argument shows that $\gamma$ induces a bijection from the set of smooth curves in $M_0$ to that in $X_0$.
Hence $\gamma$ is an isomorphism of Fr&#246;licher spaces and so the inclusion functor $\mathcal{M} \to \mathcal{H}$ preserves limits.

Now let us assume that $\mathfrak{F}$ has a colimit in $\mathcal{M}$, say $M_1$ with maps $\lambda_i : \mathfrak{F}(i) \to M_1$.
Let us write $X_1$ for the colimit of $\mathfrak{F}$ viewed as a functor into $\mathcal{F}$, with maps $\mu_i \colon \mathfral{F}(i) \to X_1$.
Note that this is in $\mathcal{F}$ not $\mathcal{H}$.
To obtain the colimit in $\mathcal{H}$ we apply the reflector functor (Hausdorffification) to $X_1$.

Since $M_1$,  as a Hausdorff Fr&#246;licher space, is a sink of $\mathfrak{F}$ there is a unique morphism, say $\nu : X_1 \to M_1$, such that $\nu \mu_i = \lambda_i$.
This morphism factors uniquely through the Hausdorffification of $X_1$.

For the same argument as with the limits, the smooth functions on $X_1$ factor through those of $M_1$.
However, the underlying set functor is not represented by morphisms _into_ a smooth manifold so we have to be a little more careful to see that the $\nu$ induces an isomorphism from the Hausdorffification of $X_1$ to $M_1$.

Firstly, let us show that $\nu$ is surjective on underlying sets.
To see this, suppose for a contradiction that it is not.
Let $x \in |M_1|$ be a point not in the image of $\nu$.
Let $N = M_1 \smallsetminus \{x\}$.
Then $N$ is an open submanifold of $M_1$ and $\nu$ factors through the inclusion $N \to M_1$.
As $X_1$ is the colimit of $\mathfrak{F}$, the morphism $X_1 \to N$ establishes $N$ as a sink for $\mathfrak{F}$.
As $N$ is a manifold, there is thus a unique morphism $M_1 \to N$ factoring the morphisms from $\mathfrak{F}$ to $N$.
That is to say, the morphism $X_1 \to N$ uniquely factors through $\nu : X_1 \to M_1$.
This gives a factorisation of $\nu$ as
$$
X_1 \longrightarrow^{\nu} M_1 \to N \to M_1
$$
where the last morphism is the inclusion of $N$ in $M_1$.
However, the properties of $\nu$ imply that the morphism $M_1 \to M_1$ in the above diagram is the identity, contradicting the non-surjectivity of $N \to M_1$ and thus the non-surjectivity of $X_1 \to M_1$.

Hence $X_1 \to M_1$ is surjective.
We also have that the smooth functions on $X_1$ factor through $M_1$.
This is not enough to prove that $X_1$ and $M_1$ are isomorphic, but is enough to prove that the Hausdorffification of $X_1$ is isomorphic to $M_1$ (note that $M_1$, being a manifold, is already Hausdorff as a Fr&#246;licher space).
To see this, observe that with what we already have, all that remains is to show that $\nu$ induces an injective map from the underlying set of the Hausdorffification of $X_1$ to the underlying set of $M_1$.
Thus let $x, y$ be distinct points in the Hausdorffification of $X_1$.
There is thus a smooth function on $X_1$ which distinguishes them.
As this smooth function factors through $M_1$, we must have $\nu(x) \ne \nu(y)$ and hence $\nu$ is injective on the required underlying sets.

Thus the inclusion functor $\mathcal{M} \to \mathcal{H}$ preserves colimits.
=--

The inclusion of the category of Manifolds in that of all Fr&#246;licher spaces preserves limits (by the same proof as above) but not colimits.
However, it is thus only the issue of being Hausdorff that prevents it preserving colimits.
The simplest example is the classic non-Hausdorff manifold: consider the [[coequalizer|coequaliser]] of $\mathbb{R} \smallsetminus \{0\}$ included in each piece of $\mathbb{R} \coprod \mathbb{R}$.
The colimit in the category of [[manifold|Manifolds]] is simply $\mathbb{R}$.
The colimit of this in the category of Fr&#246;licher spaces is the real line with a double point at $\{0\}$, but upon Hausdorffification this becomes the real line.

+--{: .query}
[[Mike Shulman|Mike]]: What if we re-define "manifold" to remove the Hausdorff axiom?  Does the inclusion into Fr&#246;licher spaces then preserve colimits?

[[Andrew Stacey|Andrew]]: I think so, but the inclusion from manifolds to Fr&#246;licher spaces is then not full.  Let $X$ be the real line with a double point at the origin.  Take a curve $\mathbb{R} \to X$ which oscillates between the two points.  This is a morphism into the Fr&#246;licher space, but not into the manifold.

I think that to make it work, you have to redefine "Euclidean space" to include anything that becomes a Euclidean space upon Hausdorffification.
=--


***

# Tangential Topics of Fr&#246;licher Spaces # {#tangent}

+-- {: .query}
This section is essentially lifted from [Comparative Smootheology](http://arxiv.org/abs/0802.2225) as I intend to remove it from that article and this seems a good place to put it.
=--

Nearly every construction in differential topology starts with tangent or cotangent bundles.
As a conclusion of this note, we shall look at how one could define these in the more general setting.
An advantage of the dual nature of the definition of a smooth structure due to Fr&#246;licher is that just about every definition of a tangent or cotangent vector is possible.
Essentially, as we have access to both curves and functionals we can consider push-forwards and pull-backs.

The ideas in this section can be traced at least as far back as Fr&#246;licher's work in [MR842916](http://www.ams.org/mathscinet-getitem?mr=842916).
That there are different orders of tangent and cotangent vectors appears in Kriegl and Michor's book [MR1471480](http://www.ams.org/mathscinet-getitem?mr=1471480), though it doubtless has antecedents.
However in [MR1471480](http://www.ams.org/mathscinet-getitem?mr=1471480), only operational tangent vectors have higher orders.
This is because the context is that of manifolds and so non-trivial higher order kinematic tangent vectors do not appear.

Let us start with _kinematic tangent vectors_.
We start with a notion of what it means for a curve to be flat.


+-- {: mynumdef #Flatness}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 A curve $c \in \mathcal{C}$ is said to be _$k$-flat_ at $t \in \mathbb{R}$ if for each $f \in \mathcal{F}$, $(f c)^{(j)}(t) = 0$ for $1 \le j \le k$.
 It is _flat_ at $t \in \mathbb{R}$ if it is $k$-flat for all $k \in \mathbb{N}$.

 We write $\mathcal{C}_{x,k}$ for the subset of $\mathcal{C}$ consisting of those curves that map $0$ to $x$ and are $(k-1)$-flat at $0$.
=--

For convenience, in the next definition we will say that any curve is $0$-flat.

+-- {: mynumdef #FroTanSet}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 Let $x \in X$ and let $k \in \mathbb{N}$.
 The _$k$th kinematic tangent set_ at $x$, $T_{x,k} X$, is the quotient of $\mathcal{C}_{x,k-1}$ by the equivalence relation $c_1 \simeq c_2$ if
  $(f c_1)^{(k)}(t) = (f c_2)^{(k)}(t)$
 for all $f \in \mathcal{F}$.
=--

We write this as $T_{x,k} X$ rather than $T_x^k X$ to avoid conflict of notation with iterated tangent spaces.
Since any curve can be composed with a suitable smooth map $\mathbb{R} \to \mathbb{R}$ to produce a curve of higher flatness, there are natural inclusions
 $T_{x,k} X \to T_{x,k+1} X$.
For Euclidean spaces with their usual structure, all of these tangent sets coincide.

+-- {: mynumdef #FroKinTan}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 The _full kinematic tangent set_ of $X$ at $x$ is
  $T_{x,\infty} X = \bigcup_k T_{x,k} X$.
=--

It is obvious that each of these kinematic tangent sets is functorial in Fr&#246;licher spaces.

One would anticipate that in a given application the only two candidates for a kinematic tangent set will be either the full kinematic tangent set or the first kinematic tangent set.
Note that for a manifold with boundary, the first kinematic tangent set at a point in the boundary is the tangent space of the boundary whereas the full kinematic tangent set is the tangent space of the ambient manifold (including the outward pointing normal).

We have been careful in writing "tangent _set_" rather than "tangent _space_" so as not to imply any particular structure.
Reparametrisation of paths easily defines the structure of an $\mathbb{R}$-set on each tangent set but in general one will not be able to add tangent vectors.
Nonetheless, some addition may be possible and addition has nice properties when it is defined.

+-- {: mynumdef #TanSum}
###### Definition
Let $X$ be a Fr&#246;licher space, $x \in X$.
For $u,v, w \in T_{x,k} X$ we say that $w$ is a _sum_ of $u$ and $v$ if there are representatives $\alpha$, $\beta$, $\gamma$ such that $(f \alpha)^{(k)} = (f \beta)^{(k)} + (f \gamma)^{(k)}$ for all $f \in F_X$.

More generally, $u_1, \dots, u_k \in T_{x,k} X$ have a sum if there is some $w \in T_{x,k} X$ with $(f \beta)^{(k)} = \sum (f \alpha_i)^{(k)}$. 
=--

+-- {: .num_lemma #LemTanSum}
###### Lemma
Sums are unique if they exist.
=--

+-- {: myproof}
###### Proof
If $\beta$ and $\gamma$ both represent sums of $u_1, \dotsc, u_k$ then
\[
(f \beta)^{(k)} = \sum (f \alpha_i)^{(k)} = (f \gamma)^{(k)}
\]
so $\beta$ and $\gamma$ represent the same vector in $T_{x,k} X$.
=--

The construction of kinematic tangent vectors suggests a similar construction for cotangent vectors.
As with tangent vectors, we need an auxiliary definition.

+-- {: mynumdef #FlatFun}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 A functional $f \in \mathcal{F}$ is said to be _$k$-flat_ at $x \in X$ if for each $c \in \mathcal{C}$ with $c(0) = x$, $(f c)^{(j)}(0) = 0$ for $1 \le j \le k$.
 It is _flat_ at $x \in X$ if it is $k$-flat for all $k \in \mathbb{N}$.

 We write $\mathcal{F}_{x,k}$ for the subset of $\mathcal{F}$ of functionals that are $k$-flat at $x$.
=--

Again, for convenience we will say that all functionals are $0$-flat.

+-- {: mynumdef #KinCoTan}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 The _$k$th kinematic cotangent space_ at $x$, $T^*_{x,k} X$, is the quotient of $\mathcal{F}_{x,k-1}$ by the relation $f_1 \simeq f_2$ if
  $(f_1 c)^{(k)}(0) = (f_2 c)^{(k)}(0)$
 for all $c \in \mathcal{C}$ with $c(0) = x$.
=--

The same discussion for kinematic tangent vectors applies to kinematic cotangent vectors except for the fact that cotangent vectors automatically form vector spaces.

+-- {: mynumdef #KinFullCoTan}
###### Definition
 The _full kinematic cotangent space_ of $X$ at $x$ is
  $T^*_{x,\infty} X = \bigcup T^*_{x,k} X$.
=--

There are obvious pairings between kinematic tangent and cotangent vectors based on evaluation.
One defines a map
 $(f,c) \mapsto (f c)^{(k)}(0)$
and this descends to providing one knows that $(f c)^{(j)}(0)$ vanishes for $j \lt k$.
The simplest case of this is where one of the tangent or cotangent vectors has order $k$.
Thus the highest level pairing,
 $(f, c) \mapsto (f c)'(0)$,
defines a pairing for all tangent and cotangent vectors but one which vanishes unless both are of first order.



We can also define _operational tangent vectors_.
Recall that $\mathcal{F}$ is an algebra of functions.

+-- {: mynumdef #OpTanSet}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 An _operational tangent vector_ at $x$ is a derivation at $x$ of $\mathcal{F}$.
 That is, a linear map
  $\partial : \mathcal{F} \to \mathbb{R}$
 such that
  $\partial(f g) = f(x) \partial g + g(x) \partial f$.

 We write $D_x X$ for the vector space of operational tangent vectors at $x$ and $D_{x,k} X$ for the space of operational tangent vectors at $x$ that vanish on $\mathcal{F}_{x,k}$.
=--

The order of an operational tangent vector is defined to be the least $k$ for which it lies in $D_{x,k} X$, otherwise it is said to have infinite order.
Again, in a given application it may be preferable to restrict to operational tangent vectors of finite order, or of order $1$.

+-- {: .num_lemma #KinToOp}
###### Lemma
 There are natural maps
  $T_{x, k} X \to D_{x,k} X$
 compatible with the connecting maps on each side.
=--

+-- {: myproof}
###### Proof
 For $c \in \mathcal{C}_{x,k-1}$ and $f \in \mathcal{F}$ we define an operational tangent vector by
  $f \mapsto (f c)^{(k-1)}(0)$.
 This has the required properties.
=--

This map, however, need not be injective and neither need it map to a spanning set.



One can define two more versions of "cotangent vectors" by taking linear duals of the two versions of tangent vectors (this has to be done with care for the kinematic tangent vectors); however, these definitions may be thought of as one-step removed from the smooth structure itself.

# References #

A detailed discussion of the category of Fr&#246;licher spaces and their relation to other notions of [[generalized smooth space]]s is given in

* Andrew Stacey, _Comparative Smootheology_ ([arXiv](http://arxiv.org/abs/0802.2225))

This also lists all the relevant further references. 

A discussion of [[Lie algebra]]s on Fr&#246;licher [[group]]s ([[group object]]s [[internalization|internal to]] the category of Fr&#246;licher spaces) is in

* Martin Laubinger, _A Lie algebra for Fr&#246;licher groups_ ([arXiv](http://arxiv.org/abs/0906.4486))


[[!redirects Frölicher space]]
[[!redirects Frölicher spaces]]
[[!redirects Frolicher space]]
[[!redirects Frolicher spaces]]
[[!redirects Froelicher spaces]]