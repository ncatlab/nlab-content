{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


# Fr&#246;licher Spaces and Isbell Envelopes

[[Frölicher spaces]] are examples of [[generalized smooth space|generalised smooth spaces]].  The category of Fr&#246;licher spaces is also closely related to the concept of the [[Isbell envelope]] of a category.

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


[[!redirects Frölicher spaces and Isbell envelopes]]
[[!redirects Frolicher spaces and Isbell envelopes]]
[[!redirects Froelicher spaces and Isbell envelopes]]
