[[!redirects manifolds of mapping spaces]]

#Contents#
* automatic table of contents
{:toc}


## Idea ##

The category of [[smooth manifolds]] is not [[cartesian closed]], even when [[infinite-dimensional manifold]]s are allowed.  However, that does not mean that _no_ mapping spaces between certain smooth manifolds can be given the structure of a smooth manifold.  This is true when the source is compact.  Thus, in particular, this applies to [[loop spaces]].

The method of proving this depends mostly on the structure of the target and only minimally on that of the source.  It is not hard to generalise it to manifolds with boundary (to get, for example, [[path spaces]]), or even manifolds with corners.  This raises the obvious question as to how general this result can be made.  The purpose of this page is to determine the answer.  Our conjecture is the following:

+-- {: .num_theorem #mfdconj}
###### Conjecture
Let $N$ be a [[Frölicher space]] whose [[curvaceous topology]] is [[sequentially compact]].  Let $M$ be a smooth manifold that admits a [[local addition]].  Then the Fr&#246;licher space of smooth maps from $N$ to $M$ is a smooth manifold.
=--




## Background and Remarks ##

The question discussed here can be viewed as the counterpoint to the oft-heard maxim (attributed to Grothendieck):

> It is better to work in a nice category with nasty objects than in a nasty category with nice objects.

Smooth manifolds are an example of "nice objects in a nasty category"; for example, one can rarely take subobjects or quotients.  The standard proceedure at this point is to embed the nasty category in some larger, nicer category and work there.  In the case of smooth manifolds, this has led to all of the categories that are listed at [[generalized smooth space]].

One can now go on to study this enlarged category, and investigate how much of what is known about the original category extends to the larger one.  In this line, the original category is viewed mainly as a source of ideas.  An alternative approach, and that taken here, is to view the original category as being a subcategory of "special objects" inside the larger one.

One can make an analogy with the real and complex numbers.  Many aspects of the study of real numbers become much easier and clearer when extended to the complex numbers.  At this point, one has a choice: one can simply study the complex numbers or one can use the complex numbers as a tool to study the real ones.

Thus, to adapt a saying of Hadamard, we could introduce our own maxim:

> The shortest distance between two truths about nice objects often lies in a nice category.

Having mentioned the plethora of extensions of the category of smooth manifolds, we should comment on our choice of [[Frölicher spaces]]. 
The inclusion of the category of smooth manifolds into each of the extensions factors through the category of Fr&#246;licher spaces.  Therefore, if we work in, say, the category of [[diffeological spaces]] then we can split the question "Is the diffeological space $X$ a smooth manifold?" into "Is $X$ a Fr&#246;licher space?" and "Is the resulting Fr&#246;licher space a manifold?".  Moreover, as we are interested in $C^\infty(N,M)$ with $M$ a smooth manifold (and thus a  Fr&#246;licher space), then if we are working with one of the "maps in" approaches, we can replace the $N$ in $C^\infty(N,M)$ by its "Fr&#246;licherification" without changing the set.  Thus the key piece of the puzzle is to study $C^\infty(N,M)$ for $N$ a Fr&#246;licher space and the rest will follow by applying "general nonsense".

Another remark worth saying is that the conjecture stated is not the most general statement that could be considered.  It is simple to extend this conjecture to a relative version whereby $M$ is equipped with a family of submanifolds and $N$ with a family of subsets and the maps are constrained to take the subsets to the corresponding submanifolds.

Finally, let us note that the main results about the linear model spaces are recorded on the page [[linear mapping spaces]].

## Charts 

Let $M$ be a smooth manifold (possibly infinite dimensional) modelled on the [[convenient vector space]] $V$.  Let $N$ be a [[sequentially compact]] [[Frölicher space]].  Let $\{P_i : P_i \subseteq M\}$ be a family of submanifolds of $M$.  Let $\{Q_i : Q_i \subseteq N\}$ be a [[family of subsets]] of $N$ with the same indexing set.  We consider the space $C^\infty(N,M;Q_i,P_i)$ of smooth maps $N \to M$ which map each $Q_i$ into the corresponding $P_i$.  As a smooth manifold, $M$ naturally has the structure of a Fr&#246;licher space so this mapping space is well-defined.

We assume that the _pair_ $(M,\{P_i\})$ admits a [[local addition]].  By that, we mean that $M$ admits a local addition, say $\eta$, with the property that it restricts to a local addition on each $P_i$.  We shall also assume, for simplicity, that the domain of $\eta$ is $T M$.

Let $g \colon N \to M$ be a smooth map with $g(Q_i) \subseteq P_i$.  Let $E_g$ be the space of sections of $g^* T M$ with the property that the sections over each $Q_i$ are constrained to lie in the corresponding $g^* T P_i$.  In more detail, we define $g^* T M$ in the usual manner:

$$
g^* T M \coloneqq \{(x,v) \in N \times T M : g(x) = \pi(v)\}
$$

and then take the space of smooth maps $f \colon N \to g^* T M$ with the property that the composition $N \to g^* T M \to N$ is the identity.  Within that space, we further restrict to those $f$ such that the image of the map $Q_i \to g^* T M \to T M$ lies in $T P_i$.

Although $N$ could be quite complicated, because $T M \to M$ is a vector bundle, $E_g$ is a vector space.  Furthermore, by trivialising $g^* T M$ using a finite number of trivialisations (possible as $N$ is sequentially compact), we can embed $E_p$ as a closed subspace of $C^\infty(N,V^n)$ for some $n$.  This embedding shows that $E_p$ is a [[convenient vector space]], in the sense of [Kriegl and Michor](#km).

+-- {: .query}
[[Andrew Stacey]] This, I think, is the crucial part: that $E_p$ is a convenient vector space.  I need to expand on this and check that all is as I think it is.
=--

We define a map for $\Phi \colon E_g \to C^\infty(N,M;\{Q_i\},\{P_i\})$ as follows.  Let $f \in E_p$.  Then $f$ is a section of $g^* T M$ and so is a map $N \to g^* T M$.  By the definition of $g^* T M$, we can think of $f$ as a map $N \to N \times T M$ which projects to the identity on the first factor.  By applying the projection to the second factor, we obtain a map $\hat{f} \colon N \to T M$.  Composing with $\eta$ produces a map $\eta \circ \hat{f} \colon N \to M$.  As $f \in E_g$, the restriction of $\hat{f}$ to $Q_i$ lands in $T P_i$, whence $\eta \circ \hat{f}$ takes $Q_i$ into $P_i$.  The map $f \mapsto \eta \circ \hat{f}$ is what we call $\Phi$.

Let us identify its image.  Let $V \subseteq M \times M$ be the image of the local addition.  Define $U_g \subseteq C^\infty(N,M;\{Q_i\},\{P_i\})$ to be the set of those functions $h$ such that $(g,h) \colon N \to M \times M$ takes values in $V$.  We claim that the image of $\Phi$ is $U_g$ and that $\Phi$ is a bijection $E_g \to U_g$.

Let us start with the image.  Let $h \in U_g$.  Then $(g,h) \colon N \to M \times M$ takes values in $V$, so we can compose with $(\pi \times \eta)^{-1}$ to get a map $\check{h} \colon N \to T M$.  Together with the identity on $N$, we get a map $N \to N \times T M$.  By construction, $\pi \check{h} = g$ and so this map ends up in $g^* T M$ (which has the subspace structure).  Again by construction, the projection of this map to $N$ is the identity and so it is a section of $g^* T M$.  That it takes $Q$ to $T P$ follows from the fact that $\eta$ restricts to a local addition on $P$, whence as $h(Q) \subseteq P$, $\check{h}(Q) \subseteq T P$.  Hence $\Phi$ is onto.  Moreover, this construction yields the inverse of $\Phi$ and so it is a bijection.

Thus we have charts for $C^\infty(N,M;Q,P)$.

## Transition functions 

The next step is the transition functions.  To prove this in full generality, we assume not just two different functions at which to base our charts, but also two different local additions to define them.  This will show that our resulting manifold structure is independent of this choice.  We could go further than we do, and allow our local additions to be in the most general form given at [[local addition]], but this would crowd the notation with little benefit.

Thus we start with $g_1, g_2 \in C^\infty(N,M;Q,P)$ and two local additions $\eta_1, \eta_2 \colon T M \to M$.  Let us write $V_1$ and $V_2$ for the images of $(\pi \times \eta_1)$ and $(\pi \times \eta_2)$.  Let $E_1 = E_{g_1}$ and $E_2 = E_{g_2}$.

We define $W_{1 2} \in g_1^* T M$ as follows.  We describe a point in $g_1^* T M$ by specifying its point in $N \times T M$.

$$
W_{1 2} \coloneqq \{(x,v) \in g_1^* T M : (g_2(x),\eta_1(v)) \in V_2\}
$$

and $W_{2 1} \subseteq g_2^* T M$ similarly.

+-- {: .num_lemma #diff}
###### Lemma
$W_{1 2} \cong W_{2 1}$
=--

+-- {: .proof}
###### Proof
The map $g_2 \times \eta_1 \colon N \times T M \to M \times M$ is smooth and so the preimage of $V_2$ under this map is open in $N \times T M$.  Thus $W_{1 2}$ is open in $g^* T M$ and the map $(x, v) \mapsto (g_2(x), \eta_1(v))$ is a smooth map $W_{1 2} \to V_2$.  Since $(\pi \times \eta_2) \colon T M \to V_2$ is a diffeomorphism, we can define a smooth map $\theta_1 \colon W_{1 2} \to T M$ by

$$
\theta_1(x,v) = (\pi \times \eta_2)^{-1}(g_2(x), \eta_1(v))
$$

Now

$$
\pi \theta_1(x,v) = \pi(\pi \times \eta_2)^{-1}(g_2(x),\eta_1(v)) = g_2(x)
$$

so $\theta_1(x,v) \in T_{g_2(x)} M$ and thus $(x,\theta_1(x,v)) \in g_2^* T M$ for all $(x,v) \in W_{1 2}$.  Then

$$
\eta_2 \theta_1(x,v) = \eta_2(\pi \times \eta_2)^{-1}(g_2(x),\eta_1(v)) = \eta_1(v)
$$

so $(g_1(x),\eta_2\theta_1(x,v)) = (g_1(x),\eta_1(v))$ which is in $V_1$.  Hence $(x,\theta_1(x,v)) \in W_{2 1}$.  Thus we have a map

$$
\phi_{2 1} \colon W_{1 2} \to W_{2 1}, \qquad \phi_{1 2}(x,v) = (x, \theta_1(x,v))
$$

Similarly, we have a map $\phi_{1 2}$ in the other direction.  Both of these maps are smooth since they are smooth into $N \times T M$.

Let us consider $\phi_{1 2}\phi_{2 1}(x,v)$.  Expanding this out yields:

$$
\begin{aligned}
\phi_{1 2}\phi_{2 1}(x,v) &= \phi_{1 2}(x, \theta_1(x,v)) \\
&=(x, \theta_2(x, \theta_1(x,v))) \\
&=(x, (\pi \times \eta_1)^{-1}(g_1(x), \eta_2\theta_1(x,v))) \\
&=(x, (\pi \times \eta_1)^{-1}(g_1(x), \eta_1(v))) \\
&=(x, (\pi \times \eta_1)^{-1}(\pi(v),\eta_1(v))) \\
&=(x,v)
\end{aligned}
$$

where we have used the fact that $(x,v) \in g_1^*T M$ so $\pi(v) = g_1(x)$.  Thus $\phi_{2 1}$ and $\phi_{1 2}$ are inverses, whence they are diffeomorphisms.
=--

+-- {: .num_lemma #trans}
###### Lemma
The transition function is $f \mapsto \phi_{2 1} \circ f$.
=--

+-- {: .proof}
###### Proof
Let us start with the domain and codomain of the transition function.  The domain is $\{f \in E_1 : \Phi_1(f) \in U_2\}$.  The set $U_2$ consists of those functions $h \colon N \to M$ such that $(g_2, h)$ takes values in $V_2$.  Thus $\Phi_1(f) \in U_2$ if and only if $(g_2, \Phi_1(f)) \in V_2$.  Since $\Phi_1(f) = \eta_1 \circ \hat{f}$, we see that for $x \in N$, $v \coloneqq \hat{f}(x) \in T M$ must be such that $(g_2(x), \eta_1(v)) \in V_2$.  This is precisely the condition that $(x,v)$ be in $W_{1 2}$.  Thus the domain of the transition function is the set of sections $f \in E_1$ such that $f(x) \in W_{1 2}$ for each $x \in N$.

The transition function, $\Psi_{2 1}$, is given by $\Psi_{2 1} = \Phi_2^{-1} \Phi_1$.  It is therefore completely characterised by the fact that $\Phi_2 \Psi_{2 1} = \Phi_1$.

Let us consider $\Phi_2$ applied to $\psi_{2 1} \circ f$ for $f \in E_1$ such that $f$ takes values in $W_{1 2}$.  Expanding out the definition, we have:

$$
\begin{aligned}
(\psi_{2 1} \circ f)(x) &= \psi_{2 1}(f(x)) \\
&= (x, \theta_1(x, \hat{f}(x))) \\
&= (x, (\pi \times \eta_2)^{-1}(g_2(x), \eta_1\hat{f}(x)))
\end{aligned}
$$

Now the result applying $\Phi_2$ to $h$ is $\eta_2 \circ h$ where $h(x) = (x, \hat{h}(x))$.  Thus the result of applying $\Phi_2$ to $\psi_{2 1} \circ f$ is the function

$$
x \mapsto \eta_2 (\pi \times \eta_2)^{-1}(g_2(x), \eta_1\hat{f}(x)) = \eta_1\hat{f}(x)
$$

which is exactly the same function as $\Phi_1(f)$.  Hence

$$
\Psi_{2 1}(f) = \psi_{2 1} \circ f
$$

and thus $\Psi_{2 1}$ is a diffeomorphism.
=--

+-- {: .num_corollary #cordiff}
###### Corollary
$C^\infty(N,M;\{Q_i\},\{P_i\})$ is a smooth manifold.
=--

[[!redirects mapping spaces that are manifolds]]