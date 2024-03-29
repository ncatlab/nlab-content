
#Contents#
* automatic table of contents goes here
{:toc}

 
## Idea 

At its simplest, a [[smooth manifold]] is a place where one can do calculus without worries.  Let us consider the formula for a derivative:

$$
f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}
$$

From the fractional part of this, it appears that to be able to discuss calculus, we need to be working in a space which allows addition and scalar multiplication.  However, the fact that we are considering a limit means that we only need to be able to do such things in a neighbourhood of a given point.  That is, we need the concept of a _local_ addition.

Thus at its most general, a local addition at a point is simply the structure of a (piece of a) vector space near that point.  This is, of course, the notion of a [[chart]].  At this point, one starts to think about notions of compatibility between different local additions.  By concentrating on what it means for two charts to be compatible at a point, one soon arrives at the notion of an [[atlas]].

Another direction that one could take is to ask for a system of local additions, one for each point, and ask that these fit together in some nice manner as one moves over the manifold.  This leads to the notion of a **local addition**.

## Definition 

The broadest definition is the following.

+-- {: .num_defn #locadd}
###### Definition
A **local addition** on $M$ consists of a vector bundle $\pi \colon E \to M$, an open neighbourhood of the zero section, $U \subseteq E$, and a smooth map $\eta \colon U \to M$ such that

1. The composition of $\eta$ with the zero section of $E$ is the identity on $M$, and
2. there exists an open neighbourhood, say $V$, of the diagonal in $M \times M$ such that the map $\pi \times \eta \colon U \to M \times M$ is a diffeomorphism onto $V$.
=--

### Remarks 

1. By considering the derivative of $\eta$, one can see that the bundle $E$ must be isomorphic to $T M$.  However, it is not necessary to specify an isomorphism in advance since $\eta$ naturally defines one.  Nonetheless, it is common simply to take $E = T M$.

2. Another way to simplify the definition is to take $U = E$.  In [KM &#167;42.4](#km), this is called a _globally defined_ local addition (though such a conjunction of "global" and "local" may grate).  Given a local addition with arbitrary $U$, it is possible to define a "globally defined" one simply by using a smooth fibrewise embedding (preserving the zero section) of $E$ onto an open subset of $U$.

3. A useful source of local additions is from Riemannian geometry: the exponential map coming from a Riemannian structure defines a local addition.

4. Another source of local additions is to apply the tubular neighbourhood theorem to the embedding of the diagonal $M \to M \times M$.

## Charts from Local Additions

### Charts for $M$ 

Local additions are used in constructing the manifold structure on certain mapping spaces.  In brief, if $M$ is a manifold (possibly infinite dimensional) admitting a local addition, and if $N$ is a compact manifold (possibly with boundary) then $C^\infty(N,M)$ can be given the structure of a smooth manifold and the construction of the charts uses the local addition on $M$.  For details, see [KM &#167;42](#km).  Applying this to the case $N = pt$, we obtain charts for $M$ itself.  These charts are useful since then we have charts on both $M$ and the various mapping spaces which are all defined using the same method and so the relationships between them are that much clearer.

+-- {: .num_prop #Mcharts}
###### Proposition
Let $M$ be a smooth manifold, $\eta \colon E \supseteq U \to M$ a local addition on $M$.  Let $V \subseteq M \times M$ be the image of $\pi \times \eta$.  Let $p \in M$.  Let $U_p \coloneqq E_p \cap U$ be the fibre of $U$ over $p$.  Let $V_p \subseteq M$ be such that $\{p\} \times V_p = V \cap \left(\{p\} \times M\right)$.  Then the restriction of $\eta$ to $U_p$ defines a diffeomorphism $\eta_p \colon U_p \to 
V_p$.
=--

+-- {: .proof}
###### Proof
Let us start by showing that $\eta_p$ is well-defined.  Clearly, we can restrict $\eta$ to $U_p$ to get _something_, the only question is its image.  To find that, we look at the image of $U_p$ under $\pi \times \eta$.  Since $U_p \subseteq E_p = \pi^{-1}(p)$, the image of $U_p$ is contained in $V \cap \left(\{p\} \times M\right)$, which is what we have called $V_p$.  Conversely, if $q \in V_p$ then $(p,q) \in V$ and so $(\pi \times \eta)^{-1}(p,q) \in U$.  Since $\pi(\pi \times \eta)^{-1}(p,q) = p$, we have $(\pi \times \eta)^{-1}(p,q) \in U \cap E_p$ and thus there is some $r \in U_p$ such that $\eta(r) = q$.  Hence the image of $\eta_p$ is $V_p$ as claimed.

The rest follows from the simple fact that we can also define $\eta_p$ as the restriction of the diffeomorphism $(\pi \times \eta) \colon U \to V$ to the subset $U_p$ on the source and $\{p\} \times V_p$ on the target.
=--

### Charts for Mapping Spaces 

Local additions are used to great effect in constructing charts for mapping spaces.

Let $M$ be a smooth manifold (possibly infinite dimensional).  Let $N$ be a functionally compact [[Frölicher space]].  Let $P \subseteq M$ be a submanifold.  Let $Q \subseteq N$ be a subset.  We consider the space $C^\infty(N,M;Q,P)$ of smooth maps $N \to M$ which map $Q$ into $P$.  As a smooth manifold, $M$ naturally has the structure of a Fr&#246;licher space so this mapping space is well-defined.

We assume that the _pair_ $(M,P)$ admits local addition.  By that, we mean that $M$ admits a local addition, say $\eta$, with the property that it restricts to a local addition on $P$.  We shall also assume, for simplicity, that the domain of $\eta$ is $T M$.

Let $g \colon N \to M$ be a smooth map with $g(Q) \subseteq P$.  Let $E_g$ be the space of sections of $g^* T M$ with the property that the sections over $Q$ are constrained to lie in $g^* T P$.  In more detail, we define $g^* T M$ in the usual manner:

$$
g^* T M \coloneqq \{(x,v) \in N \times T M : g(x) = \pi(v)\}
$$

and then take the space of smooth maps $f \colon N \to g^* T M$ with the property that the composition $N \to g^* T M \to N$ is the identity.  Within that space, we further restrict to those $f$ such that the image of the map $Q \to g^* T M \to T M$ lies in $T P$.

Although $N$ could be quite complicated, because $T M \to M$ is a vector bundle, $E_g$ is a vector space.  Furthermore, by trivialising $g^* T M$ using a finite number of trivialisations (possible as $N$ is functionally compact), we can embed $E_p$ as a closed subspace of $C^\infty(N,\mathbb{R}^n)$ for some $n$.  This embedding shows that $E_p$ is a convenient vector space, in the sense of [Kriegl and Michor](#km).

We define a map for $\Phi \colon E_g \to C^\infty(N,M;Q,P)$ as follows.  Let $f \in E_p$.  Then $f$ is a section of $g^* T M$ and so is a map $N \to g^* T M$.  By the definition of $g^* T M$, we can think of $f$ as a map $N \to N \times T M$ which projects to the identity on the first factor.  By applying the projection to the second factor, we obtain a map $\hat{f} \colon N \to T M$.  Composing with $\eta$ produces a map $\eta \circ \hat{f} \colon N \to M$.  As $f \in E_g$, the restriction of $\hat{f}$ to $Q$ lands in $T P$, whence $\eta \circ \hat{f}$ takes $Q$ into $P$.  The map $f \mapsto \eta \circ \hat{f}$ is what we call $\Phi$.

Let us identify its image.  Let $V \subseteq M \times M$ be the image of the local addition.  Define $U_g \subseteq C^\infty(N,M;Q,P)$ to be the set of those functions $h$ such that $(g,h) \colon N \to M \times M$ takes values in $V$.  We claim that the image of $\Phi$ is $U_g$ and that $\Phi$ is a bijection $E_g \to U_g$.

Let us start with the image.  Let $h \in U_g$.  Then $(g,h) \colon N \to M \times M$ takes values in $V$, so we can compose with $(\pi \times \eta)^{-1}$ to get a map $\check{h} \colon N \to T M$.  Together with the identity on $N$, we get a map $N \to N \times T M$.  By construction, $\pi \check{h} = g$ and so this map ends up in $g^* T M$ (which has the subspace structure).  Again by construction, the projection of this map to $N$ is the identity and so it is a section of $g^* T M$.  That it takes $Q$ to $T P$ follows from the fact that $\eta$ restricts to a local addition on $P$, whence as $h(Q) \subseteq P$, $\check{h}(Q) \subseteq T P$.  Hence $\Phi$ is onto.  Moreover, this construction yields the inverse of $\Phi$ and so it is a bijection.

Thus we have charts for $C^\infty(N,M;Q,P)$.  The next step is the transition functions.  To prove this in full generality, we assume not just two different functions at which to base our charts, but also two different local additions to define them.  This will show that our resulting manifold structure is independent of this choice.

_... to be continued ..._



## Diffeomorphisms from Local Additions 

Another useful construction from a local addition relates to diffeomorphisms.  In differential topology, manifolds have a certain amount of "flexibility": a common picture is of a rubber sheet that can be deformed.  The amount of flexibility is less than that allowed in algebraic topology, but certainly more than that in differential geometry.  Being able to deform a manifold a little is a very useful trick in establishing the relationships between the various mapping spaces (for example, it is used in showing that the loop space fibration $\Omega M \to L M \to M$ is a [[fibre bundle]] and not just a fibration) and so it is useful to have a consistent way to perform these deformations that is compatible with a given local addition.

The aim of this construction is to produce, for each $v \in U$, a 1-parameter family of diffeomorphisms, $\phi_{(t,v)}$, such that $\phi_{(t,v)}(\pi(v)) = \eta(t v)$.  That is, the basepoint $p = \pi(v)$ is deformed along the path $\eta(t v)$ to $\eta(v)$, and the rest of the manifold is dragged along behind it.  (In actual fact, only a very small amount of the manifold is dragged along - although our manifolds are flexible, they have a high amount of tension.)

So let $\eta \colon U \to M$ be a local addition.  Let $\nu \colon U \to \mathbb{R}$ be a smooth function with the following fibrewise property: for each $r \in \mathbb{R}$, the set $\{q \in U_p : \nu(q) \le r\}$ is a compact, [[radial]] subset.  The square of the norm coming from a smooth orthogonal structure would suffice.  Let $\rho \colon \mathbb{R} \to [0,1]$ be a smooth function such that $\rho(t) = 1$ for $t \le 0$ and $\rho(t) = 0$ for $t \ge 1$.

Now for $v \in U$, we define a vector field $\hat{X}_v$ on $U_p$, where $p = \pi(v)$, by

$$
\hat{X}_v(w) \coloneqq \rho(\nu(w) - \nu(v))v
$$

Notice that if $\nu(w) \ge \nu(v) + 1$ then $\hat{X}_v(w) = 0$ whilst if $\nu(w) \le \nu(v)$ (so in particular if $w = t v$ for some $t \in [0,1]$) then $\hat{X}_v(w) = v$.  By the first of these, we see that $\hat{X}_v$ is compactly supported on $U_p$.  We can transfer it via $\eta_p$ to $V_p$ and, as it is compactly supported, extend it to all of $M$ by defining it to be $0$ outside $V_p$.  Let us write $X_v$ for this vector field.

By construction, the map $v \to X_v$ is smooth.  As $X_v$ is compactly supported, we can apply the exponentiation map $\mathcal{X}_c(M) \to Diff(M)$ and so obtain, for each $v \in U$, a 1-parameter family of diffeomorphisms of $M$, say $\phi_{(t,v)}$.  From the construction of $X_v$, it is clear that all the "action" of this family of diffeomorphisms takes place in $V_p$.  Moreover, by construction, the point $p$ moves along the line $t \mapsto \eta(t v)$ for $t \in [0,1]$.

## References 

* Kriegl and Michor, _A Convenient Setting of Global Analysis_
{#km}
* [[Andrew Stacey]], _The Differential Topology of Loop Spaces_ [main page](http://www.math.ntnu.no/~stacey/Seminars/diffloop.html) (Note: this was designed as an "easy reader" version of [KM](#km))
* [[Andrew Stacey]], _Constructing Smooth Manifolds of Loop Spaces_ [main page](http://www.math.ntnu.no/~stacey/Research/Papers/smooth.html)
