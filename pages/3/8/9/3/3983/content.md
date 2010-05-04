{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

# Topological Notions of Fr&#246;licher Spaces # {#topology}

Although the definition of a [[Frölicher space]] does not use a topology, it is topological in flavour and there are many topological concepts that can be defined for Fr&#246;licher spaces.  In other pages, we have used the notion of a Hausdorff Fr&#246;licher space and have used a vague notion of a topology on the functions on a Fr&#246;licher space.  In this page, we shall investigate the connections between the theory of Fr&#246;licher spaces and topological spaces a little more consistently.

There are two different ways of thinking of topological notions on Fr&#246;licher spaces.
One says that there is a functor (actually two functors) from the category of F&#246;licher space to the category of topological spaces so we can say that a Fr&#246;licher space has topological property $P$ if the corresponding topological space has it.
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
When looking for the right functional definition, we have an obvious place in topology to start looking: the ring of continuous real-valued functions on a topological space.
For the curvaceous definition, an obvious place to look is at paths in a topological space.
Although there are some topological ideas have good "path" variants, this is not true of many.
What is more common is to have a "sequential" variant of a general concept.
In sufficiently nice topological spaces, sequences can be turned into paths, and convergent sequences into extendible paths.
One way to use this would be to take a sequential definition, convert it to one about paths, and then replace "path" by "smooth path".
Unfortunately, the reformulation of topological properties from the sequential language to that of paths is rarely neat - consider how to express "$(x_{n_k})$ is a subsequence of $(x_n)$" in path-speak.
So instead of using continuous paths as our bridge from sequential topology to curvaceous smootheology, we shall introduce the notion of "smoothly convergent sequences" and use them instead.

+-- {: mynumdef #SmoothSeq}
###### Definition ######
Let $(X,C_X,F_X)$ be a Fr&#246;licher space.  Let $(x_n)$ be a sequence in $X$ and $x \in X$ a point.  The sequence $(x_n)$ is said to be **smoothly convergent** to $x$ if there is a smooth curve $c \colon \mathbb{R} \to X$, a sequence $(t_n) \to 0$ in $\mathbb{R}$, and $N \in \mathbb{N}$ such that $c(t_n) = x_n$ for $n \ge N$ and $c(0) = x$.
=--

In the continuous case, we could simply take the sequence $(t_n)$ to be some standard sequence, say $(\frac1n)$.  This is because homeomorphisms are easy to come by and so if $(t_n)$ and $(s_n)$ are strictly decreasing sequences converging to $0$ then there is a homeomorphism $(0,1) \to (0,1)$ mapping $t_n$ to $s_n$.  This does not hold in the smooth case.


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

The corresponding curvaceous notion rests for its inspiration on the notion of [[sequential compactness]].  Here is one case where there is not a pathwise version of compactness and so we use the notion of "smoothly convergent sequences" instead.


+-- {: .num_defn #DefCurvComp}
###### Definition
Let $(X, C_X,F_X)$ be a Fr&#246;licher space.  We say that $X$ is **curvaceously compact** if every sequence has a smoothly convergent subsequence.
=--

The following property is why curvaceously compact Fr&#246;licher spaces are suitable sources for [[manifolds of mapping spaces]].

+-- {: .num_prop #CurvCompProd}
###### Proposition ######
A Fr&#246;licher space $(X, C_X, F_X)$ is curvaceously compact if and only if the curvaceous topology on $\mathbb{R} \times X$ has the property that if $U$ is an open neighbourhood of $\{0\} \times X$ then there is some $\epsilon \gt 0$ such that $(-\epsilon,\epsilon) \times X \subseteq U$.
=--

+-- {: .proof}
###### Proof
Let $(X, C_X, F_X)$ be a curvaceously compact Fr&#246;licher space.  Let $U$ be a set containing $\{0\} \times X$ with the property that there is no $\epsilon \gt 0$ such that $(-\epsilon,\epsilon) \times X \subseteq U$.  We shall show that $U$ is not open in the curvaceous topology.

By assumption, for each $n$ there is some $x_n \in X$ such that $(\frac1n,x_n) \notin U$.  As $X$ is curvaceouly compact, there is a subsequence $(x_{n_k})$ of $(x_n)$, a smooth curve $\check{c} \colon \mathbb{R} \to X$ such that $\check{c}(\frac1k) = x_{n_k}$.  Let $c \colon \mathbb{R} \to \mathbb{R} \times X$ be the curve $c(t) = (t, \check{c}(t))$.  By definition of products, this is a smooth curve in $\mathbb{R} \times X$.  Let us consider $c^{-1}(U)$.  As $\{0\} \times X \subseteq U$, $c(0) = (0,\check{c}(0)) \in U$ and so $0 \in c^{-1}(U)$.  But for $k \in \mathbb{N}$, $c(\frac1k) = (\frac1k,x_{n_k}) \notin U$ so $\frac1k \notin c^{-1}(U)$.  Hence $c^{-1}(U)$ is not open and so $U$ is not open in the curvaceous topology.

Conversely, let $(X,C_X,F_X)$ be a a Fr&#246;licher space with the property that an open neighbourhood of $\{0\} \times X$ in $\mathbb{R} \times X$ contains a subset of the form $(-\epsilon, \epsilon) \times X$.  Let $(x_n)$ be a sequence in $X$.  Let $U$ be the set formed by taking $(-2,2) \times X$ and removing the set $(\frac1n, x_n)$.  By assumption, this is not an open neighbourhood of $\{0\} \times X$ and so there must be a smooth curve $c \colon \mathbb{R} \to \mathbb{R} \times X$ with the property that $c^{-1}(U)$ is not open in $\mathbb{R}$.  We can write $c$ as $s \times \check{c}$ where $s \in C^\infty(\mathbb{R},\mathbb{R})$ and $\check{c} \colon \mathbb{R} \to X$.  As $c^{-1}(U)$ is not open, it must be non-empty and have a point that is a limit from outside.  By translation if necessary, we assume that this point is $0$.  So there is a sequence $(t_k) \to 0$ such that $t_k \to 0$ and $c(t_k) \notin U$.

As $t_k \to 0$ and $s$ is continuous at $0$, we can assume (by passing to a subsequence if necessary) that $s(t_k) \in (-2,2)$ for all $k$.  Thus as $c(t_k) \notin U$, it must be the case that $c(t_k) = (\frac1{n_k}, x_{n_k})$ for some $n_k \in \mathbb{N}$.  Again by passing to a subsequence if necessary, we can assume that the sequence $(n_k)$ is stricly increasing and thus that $(x_{n_k})$ is a subsequence of $(x_n)$.
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

