# Idea #

The category of [[smooth manifolds]] is not [[cartesian closed]], even when [[infinite dimensional manifolds]] are allowed.  However, that does not mean that _no_ mapping spaces between certain smooth manifolds can be given the structure of a smooth manifold.  This is true when the source is compact.  Thus, in particular, this applies to [[loop spaces]].

An alternative way to approach this question is to embed the category of smooth manifolds in some [[generalized smooth space|larger category]] which is cartesian closed.  Then the mapping spaces are objects in the larger category and one can ask for conditions when they are objects in the subcategory of smooth manifolds.  An advantage of this approach is that the source does not have to be a smooth manifold itself but can be a more general object.  For example, this applies to [[path spaces]] since the interval is a [[smooth manifold with boundary]].

In this alternative approach there is a choice to be made: that of the ambient category.  The inclusion of the category of smooth manifolds into each of the ambient categories listed at [[generalized smooth space]] factors through the category of [[Frölicher spaces]] and thus the choice of ambient category only changes what sources we allow for our mapping spaces.  For those categories that take a "maps in" approach, the smooth maps from an object into a Fr&#246;licher space factors through the Fr&#246;licher space associated to the source and so there is no loss of generality by simply taking it to be a  Fr&#246;licher space in the first place.  Thus we take the category of  Fr&#246;licher spaces for our ambient category and simply note that these results extend to [[diffeological spaces]] and [[Chen spaces]].

The main result is the following.

+-- {: .num_theorem #mfdmap}
###### Theorem ($\beta$ version)
Let $N$ be a functionally compact Fr&#246;licher space.  Let $M$ be a smooth manifold which admits a [[local addition]].  Then the Fr&#246;licher space $C^\infty(N,M)$ is a smooth manifold.
=--

This can be strengthened to a relative version whereby $M$ is equipped with a family of submanifolds and $N$ with a family of subsets and the maps are constrained to take the subsets to the corresponding submanifolds.

+-- {: .query}
[[Andrew Stacey]]: The above theorem is actually a conjecture!  I'm working out the proof as I go along.  Of course, as the proof evolves, the theorem will change to reflect what I actually need in order to prove it.  I know it works if $N$ is a compact manifold and I'm pretty sure that there's no problem if we allow manifolds-with-corners.  And at no point do we actually use the manifold structure of $N$, so I don't see why we can't replace it with an arbitrary Frolicher space, but there may be some hidden subtlety that will only become apparent in the proof.

So this theorem is released as a $\beta$-version!  It's known to work under controlled conditions, but may break if applied more generally.
=--

# Charts #

Let $M$ be a smooth manifold (possibly infinite dimensional) modelled on the [[convenient vector space]] $V$.  Let $N$ be a functionally compact [[Frölicher space]].  Let $\{P_i : P_i \subseteq M\}$ be a family of submanifolds of $M$.  Let $\{Q_i : Q_i \subseteq N\}$ be a family of subsets of $N$ with the same indexing set.  We consider the space $C^\infty(N,M;Q_i,P_i)$ of smooth maps $N \to M$ which map each $Q_i$ into the corresponding $P_i$.  As a smooth manifold, $M$ naturally has the structure of a Fr&#246;licher space so this mapping space is well-defined.

We assume that the _pair_ $(M,\{P_i\})$ admits a [[local addition]].  By that, we mean that $M$ admits a local addition, say $\eta$, with the property that it restricts to a local addition on each $P_i$.  We shall also assume, for simplicity, that the domain of $\eta$ is $T M$.

Let $g \colon N \to M$ be a smooth map with $g(Q_i) \subseteq P_i$.  Let $E_g$ be the space of sections of $g^* T M$ with the property that the sections over each $Q_i$ are constrained to lie in the corresponding $g^* T P_i$.  In more detail, we define $g^* T M$ in the usual manner:

$$
g^* T M \coloneqq \{(x,v) \in N \times T M : g(x) = \pi(v)\}
$$

and then take the space of smooth maps $f \colon N \to g^* T M$ with the property that the composition $N \to g^* T M \to N$ is the identity.  Within that space, we further restrict to those $f$ such that the image of the map $Q_i \to g^* T M \to T M$ lies in $T P_i$.

Although $N$ could be quite complicated, because $T M \to M$ is a vector bundle, $E_g$ is a vector space.  Furthermore, by trivialising $g^* T M$ using a finite number of trivialisations (possible as $N$ is functionally compact), we can embed $E_p$ as a closed subspace of $C^\infty(N,V^n)$ for some $n$.  This embedding shows that $E_p$ is a [[convenient vector space]], in the sense of [Kriegl and Michor](#km).

+-- {: .query}
[[Andrew Stacey]] This, I think, is the crucial part: that $E_p$ is a convenient vector space.  I need to expand on this and check that all is as I think it is.
=--

We define a map for $\Phi \colon E_g \to C^\infty(N,M;\{Q_i\},\{P_i\})$ as follows.  Let $f \in E_p$.  Then $f$ is a section of $g^* T M$ and so is a map $N \to g^* T M$.  By the definition of $g^* T M$, we can think of $f$ as a map $N \to N \times T M$ which projects to the identity on the first factor.  By applying the projection to the second factor, we obtain a map $\hat{f} \colon N \to T M$.  Composing with $\eta$ produces a map $\eta \circ \hat{f} \colon N \to M$.  As $f \in E_g$, the restriction of $\hat{f}$ to $Q_i$ lands in $T P_i$, whence $\eta \circ \hat{f}$ takes $Q_i$ into $P_i$.  The map $f \mapsto \eta \circ \hat{f}$ is what we call $\Phi$.

Let us identify its image.  Let $V \subseteq M \times M$ be the image of the local addition.  Define $U_g \subseteq C^\infty(N,M;\{Q_i\},\{P_i\})$ to be the set of those functions $h$ such that $(g,h) \colon N \to M \times M$ takes values in $V$.  We claim that the image of $\Phi$ is $U_g$ and that $\Phi$ is a bijection $E_g \to U_g$.

Let us start with the image.  Let $h \in U_g$.  Then $(g,h) \colon N \to M \times M$ takes values in $V$, so we can compose with $(\pi \times \eta)^{-1}$ to get a map $\check{h} \colon N \to T M$.  Together with the identity on $N$, we get a map $N \to N \times T M$.  By construction, $\pi \check{h} = g$ and so this map ends up in $g^* T M$ (which has the subspace structure).  Again by construction, the projection of this map to $N$ is the identity and so it is a section of $g^* T M$.  That it takes $Q$ to $T P$ follows from the fact that $\eta$ restricts to a local addition on $P$, whence as $h(Q) \subseteq P$, $\check{h}(Q) \subseteq T P$.  Hence $\Phi$ is onto.  Moreover, this construction yields the inverse of $\Phi$ and so it is a bijection.

Thus we have charts for $C^\infty(N,M;Q,P)$.

# Transition Functions #

The next step is the transition functions.  To prove this in full generality, we assume not just two different functions at which to base our charts, but also two different local additions to define them.  This will show that our resulting manifold structure is independent of this choice.  We could go further than we do, and allow our local additions to be in the most general form given at [[local addition]], but this would crowd the notation with little benefit.

Thus we start with $g_1, g_2 \in C^\infty(N,M;Q,P)$ and two local additions $\eta_1, \eta_2 \colon T M \to M$.  Let us write $V_1$ and $V_2$ for the images of $(\pi \times \eta_1)$ and $(\pi \times \eta_2)$.  Let $E_1 = E_{g_1}$ and $E_2 = E_{g_2}$.

We define $W_{1 2} \in g_1^* T M$ as follows.  We describe a point in $g_1^* T M$ by specifying its point in $N \times T M$.

$$
W_{1 2} \coloneqq \{(x,v) \in g_1^* T M : (g_1(x),\eta_1(v)) \in V_2\}
$$

and $W_{2 1} \subseteq g_2^* T M$ similarly.

