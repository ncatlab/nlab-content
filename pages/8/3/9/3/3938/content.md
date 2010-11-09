
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Transgression is a tool in [[algebraic topology]] to transfer [[cohomology]] classes from one [[space]] to another without needing a [[morphism]] between them.  Rather, one has a third space with morphisms to each of the two spaces.  Of course, not just _any_ third space will do.

The topological set up is as follows.  We have two [[topological space]]s, $X$ and $Y$, and a [[generalised cohomology theory]] $E^*(-)$.  We want to be able to transfer ( _transgress_ ) $E^*$-classes from $X$ to $Y$.  We find a third space, $Z$, which has morphisms to both $X$ and $Y$.  We usually write this in the following way:

$$
\begin{matrix}
Z & \to& X \\
\downarrow \\
Y
\end{matrix}
$$

(Note to self: replace with SVG, write $f \colon Z \to X$ and $g \colon Z \to Y$.)

An important example is that where we have some parameter space $\Sigma$ (for instance the circle $\Sigma = S^1$) and set $Z = \Sigma \times [\Sigma,X]$,  the [[product]] of $\Sigma$ with the [[internal hom|mapping space]] $[\Sigma,X]$ of maps from $\Sigma$ to $X$ (for instance the [[loop space]] of $X$). Then the morphism on the right is taken to be evaluation and the morphism on the left is projection onto the mapping space $[\Sigma,X]$:

$$
  \array{
    \Sigma \times [\Sigma, X] &\stackrel{ev}{\to}& X
    \\
    \downarrow^{\mathrlap{p_2}}
    \\
    [\Sigma,X]
  }
  \,.
$$

This setup induces **transgression to mapping spaces** in the following.

Now we apply the generalised cohomology theory to this diagram.  As it is a cohomology theory, the arrows reverse.  We have part of our route from $E^*(X)$ to $E^*(Y)$, namely from $E^*(X)$ to $E^*(Z)$.  However, the way from $E^*(Y)$ to $E^*(Z)$ is blocked: it is a one-way street and we want to go the _wrong_ way.

However, under certain special circumstances, cohomology theories admit push-forward maps.  That is, if $g \colon Z \to Y$ is particularly nice, there is a map $g_! \colon E^*(Z) \to E^*(Y)$.  The notation $g_!$ (pronounced "g shriek") has the explanation that it is a surprise that there is a map in this direction[^shriek].
Note that the push-forward map, $g_! \colon E^*(Z) \to E^*(Y)$, often results in a change of degree. This is described at [[fiber integration]] and [[Pontrjagin-Thom collaps map]].

[^shriek]: To the best of [[Andrew Stacey|my]] knowledge, this remark is attributable to [[Ralph Cohen]].

Thus the key to transgression is to understand the conditions where the map $g \colon Z \to Y$ admits a push-forward map.  The simplest case is where $Z$ is a product space, $Y \times W$, and $W$ is [[orientable]] for the generalised cohomology theory $E^*(-)$.  This means that $W$ has a fundamental class in $E^*(W)$ and evaluation on this class gives a morphism $E^*(Y \times W) \to E^*(Y)$.

## Definition

### By pullback and fiber integration

(...)

### Transgression of forms through fiber bundles


A related construction called _transgression_ is the following

For $P \to X$ a [[fiber bundle]] with typical fiber $F$ and $[\omega] \in H_{dR}^n(F)$ a class in [[de Rham cohomology]] of the fiber, we say this is _transgessive_ if 

* there exists a form $cs \in \Omega^{n}(P)$ on the total space of the bundle;

* such that restricted along $F \hookrightarrow P$ to the fiber it is $\sim \omega$;

* and such that $d \omega$ is the pull-back of a form $\kappa \in \Omega^{n+1}(X)$ on the based along the bundle projection .

See for instance section 9 of ([Borel](#Borel)).

## Examples

### Transgression in de Rham Cohomology ###

With a [[cohomology theory]] that has a good geometric model, such as [[de Rham cohomology]], there is often a similar geometric model for the push-forward map.  In the case of de Rham cohomology, it goes by the name of _[[fiber integration|integration along the fibres]]_.

Using the notation above, with the simple case of $Z = Y \times W$, we have the formula

$$
\alpha \in H^k_{dR}(X) \mapsto \int_W f^* \alpha \in H^{k - \dim W}_{dR}(Y)
$$

### Transgression of de Rham cohomology to loop spaces

A particular application of this is in respect to the cohomology of [[loop spaces]], and in particular to [[iterated integrals]].  The aim here is to transfer information from a space $X$ to its [[free loop space object|free loop space]], $L X$.  The intermediate space in this situation is $S^1 \times L X$ with evaluation as the map to $X$ and projection to $L X$.  Note that although $L X$ is rather large, the [[fibre]] is $S^1$ and it is that which needs to be controlled.

If we worked in the realm of pure [[algebraic topology]] (i.e. didn't care about geometry) this transfer would be almost trivial.  Indeed, if we worked with _based_ loops, it would be a tautology since then the push-forward $H^*(S^1 \wedge \Omega X) \to H^{*-1}(\Omega X)$ is simply the suspension isomorphism.  (We use the [[smash product]] as we are working with _based_ spaces here.)

However, we wish to have a geometric interpretation of this, and so work in the realm of [[differential topology]]: i.e. with smooth [[manifold]]s (albeit possibly infinite dimensional).  We therefore have the diagram:

$$
\array{
S^1 \times L M & \to & M \\
\downarrow \\
L M
}
$$

The general lore of transgression says that this induces a map in cohomology $H^k_{dR}(M) \to H^{k-1}_{dR}(L M)$ via

$$
\alpha \mapsto \int_{S^1} ev^*\alpha.
$$

As with any cohomological construction, there is always the question as to whether or not it is purely cohomological or whether or not it can be lifted to whatever-it-was that defined the cohomology theory.  In this case, that is [[differential form]]s.  In this case we are in the happy circumstance that the lift exists.  Expressed purely in terms of differential forms, the formula doesn't change.  However, we can think of differential forms as "that which acts on [[tangent vector]]s" and ask for a formulation that involves tangent vectors.  This can make the integration step clearer.

To reformulate transgression thus we need to understand tangent vectors on $L M$.  The simplest way to view a tangent vector on $L M$ is to identify $T L M$ with $L T M$.  That is, we view a tangent vector $x \in T_\gamma L M$ as a loop in $T M$ with the property that $x(t) \in T_{\gamma(t)} M$.  In one view ($T L M$), $x$ tells $\gamma$ which direction to move in; in the other view ($L T M$), each $x(t)$ tells each $\gamma(t)$ which direction to move in.

That done, we have an obvious evaluation map $S^1 \times T L M \to T M$, $x \mapsto x(t)$ and so, given a differential form on $M$, we can evaluate it on tangent vectors coming from $L M$.

However, that's not all we need.  There's a very special [[vector field]] on $L M$ which we want to throw into the mix.  This is the vector field which assigns to $\gamma \in L M$ the tangent vector $\gamma' \in L T M$.  This is the rotation vector field: if we rotate the circle on $S^1 \times L M$ then to keep the evaluation map consistent, we have to rotate the loops in $L M$ as well.

So starting with a $k$-form, say $\alpha$, on $M$, we fix a loop $\gamma \in L M$, $t \in S^1$, and take $k-1$ tangent vectors at $\gamma$, say $x_1, \dots, x_{k-1}$.  We evaluate these at $t$ to get $x_1(t), \dots, x_{k-1}(t) \in T_{\gamma(t)} M$ and also throw in $\gamma'(t)$.  That gives $k$ vectors at $T_{\gamma(t)} M$ on which we can evaluate $\alpha$:

$$
\alpha(x_1(t),x_2(t),\dots,x_{k-1}(t),\gamma'(t))
$$

This is a number.  Hence, by varying $t \in S^1$, it defines a function $S^1 \to \mathbb{R}$.  Integrating this function around $S^1$ yields a number:


$$
\int_{S^1} \alpha(x_1(t),x_2(t),\dots,x_{k-1}(t),\gamma'(t)) dt
$$


Thus we have a map $\bigotimes^{k-1} T(L M) \to \mathbb{R}$.  It can be shown that it is alternating and $(k-1)$-linear, and that it varies smoothly over $L M$, hence defines an element of $\Omega^{k-1}(L M)$.

There is much more to tell in this particular story.  It is possible to replacing $S^1$ by a [[simplex]] (but keeping $L M$ the same) and so build up more complicated objects in $\Omega^*(L M)$.  This is the starting point of Chen's theory of [[iterated integrals]] and further developments of the theory can be found in the work of Jones, Getzler, and Petrack.

## Transgression to mapping spaces in terms of internal homs {#InternalHom}

> just a rough remark, for the moment

At least for some cases of transgressoin to [[mapping space]]s, the concept has an [[nPOV]] description in terms of [[internal hom]]s.

This makes crucial use of the [[nPOV]] notion of [[cohomology]], as described there.

Let $\mathbf{H} = $ [[Top]] $\simeq$ [[∞Grpd]]. For $X \in \mathbf{H}$ and for $\Sigma$ a $k$-dimensional closed oriented [[manifold]], and for $K$ an [[abelian group]] that is injective as a $\mathbb{Z}$-module, we may identify transgression to the mapping space $[\Sigma,X]$ as the composite

$$
  trans_\Sigma : \mathbf{H}(X,\mathbf{B}^n K)
  \stackrel{[\Sigma,-]}{\to}
  \mathbf{H}([\Sigma,X], [\Sigma, \mathbf{B}^n K])
  \stackrel{(\tau_{n-k})_*}{\to}
  \mathbf{H}([\Sigma,X], \tau_{n-k} [\Sigma, \mathbf{B}^n K])
  \simeq
  \mathbf{H}([\Sigma,X], \mathbf{B}^{n-k} K)
  \,.
$$

Here the first step is application of the [[internal hom]], then the second is postcomposition with [[truncated|truncation]], and then the last step uses the [[universal coefficient theorem]]. Note that the transgression map $trans_\Sigma$ depends on the choice of an equivalence $\tau_{n-k} [\Sigma, \mathbf{B}^n K]\simeq \mathbf{B}^{n-k} K$. Up to homotopy, this choice is precisely the datum of the [[orientation]] on $\Sigma$.

> more details go here....

This plays a role in the [[quantization]] process that yields [[FQFT]]s. For an application see [[Dijkgraaf-Witten theory]].

> more details, and more polishing later...

## Related entries

* [[transgression of bundle gerbes]]

## References

The classical notion of transgression of forms through fiber bundles is described in section 9 of

* [[Armand Borel]], _Topology of Lie groups and characteristic classes_  Bull. Amer. Math. Soc. Volume 61, Number 5 (1955), 397-432. ([EUCLID](http://projecteuclid.org/euclid.bams/1183520007))
{#Borel}

