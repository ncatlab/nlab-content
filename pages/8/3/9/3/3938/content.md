_Under Construction - The following material needs the blessing of an expert._

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Transgression is a tool in algebraic topology to transfer cohomology classes from one space to another without needing a morphism between them.  Rather, one has a third space with morphisms to each of the two spaces.  Of course, not just _any_ third space will do.

The set up is as follows.  We have two topological spaces, $X$ and $Y$, and a [[generalised cohomology theory]] $E^*(-)$.  We want to be able to transfer ( _transgress_ ) $E^*$-classes from $X$ to $Y$.  We find a third space, $Z$, which has morphisms to both $X$ and $Y$.  We usually write this in the following way:

$$
\begin{matrix}
Z & \to& X \\
\downarrow \\
Y
\end{matrix}
$$

(Note to self: replace with SVG, write $f \colon Z \to X$ and $g \colon Z \to Y$.)

An important example is that where we have some parameter space $\Sigma$ (for instance the circle $\Sigma = S^1$) and set $Z = \Sigma \times [\Sigma,X]$,  the [[product]] of $\Sigma$ with the [[internal hom|mapping space]] $[\Sigma,X]$ of maps from $X$ to $Y$ (for instance the [[loop space]] of $X$). Then the morphism on the right is taken to be evaluation and the morphism on the left is projection onto the mapping space $[\Sigma,X]$:

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


## Examples

### Transgression in de Rham Cohomology ###

With a cohomology theory that has a good geometric model, such as [[de Rham cohomology]], there is often a similar geometric model for the push-forward map.  In the case of de Rham cohomology, it goes by the name of _[[fiber integration|integration along the fibres]]_.

Using the notation above, with the simple case of $Z = Y \times W$, we have the formula

$$
\alpha \in H^k_{dR}(X) \mapsto \int_W f^* \alpha \in H^{k - \dim W}_{dR}(Y)
$$

A particular application of this is in respect to the cohomology of [[loop spaces]], and in particular to [[iterated integrals]].  The aim here is to transfer information from a space $X$ to its free loop space, $L X$.  The intermediate space in this situation is $S^1 \times L X$ with evaluation as the map to $X$ and projection to $L X$.  Note that although $L X$ is rather large, the fibre is $S^1$ and it is that which needs to be controlled.

If we worked in the realm of pure algebraic topology (i.e. didn't care about geometry) this transfer would be almost trivial.  Indeed, if we worked with _based_ loops, it would be a tautology since then the push-forward $H^*(S^1 \wedge \Omega X) \to H^{*-1}(\Omega X)$ is simply the suspension isomorphism.  (We use the smash product as we are working with _based_ spaces here.)

However, we wish to have a geometric interpretation of this, and so work in the realm of differential topology: i.e. with smooth manifolds (albeit possibly infinite dimensional).

_... to be continued ..._

Given a smooth morphism $f:M\to N\in Diff$, an $n$-dimensional connected open subset $U \subseteq M$ and a differential $n$-form $\omega\in\Omega^n(N)$, we have the pullback $f^*\omega\in\Omega^n(M)$ and the pushforward $f_*U$ that satisfy

$$\int_U f^*\omega = \int_{f_*U} \omega.$$

_Transgression_ can be thought of as a generalization of this situation. For instance, given a smooth manifold $M$, let $L M$ denote the [[loop space]] of $M$, that is, $Hom(S^1,M)$.
+-- {: .query}
_Harry_: It's not obvious whether or not you mean the space of smooth loops or continuous loops, nor how you equip this space, which presumably has the compact-open topology, with a smooth manifold structure at all.  This is important for the next part.  Also, the the connected open subset U was originally called a "subdomain", but I looked it up and could not find any references.  Since domain means connected open set, I assume that my replacement of the term "subdomain" with the much more common "connected open subset" did not change the meaning.  

Note: I changed the thing about the loop space for clarity, but it's still not clear to me which loop space and which smooth structure we give it.

I'm also afraid that calling the loop space functor L could be confusing, given that the loop space is traditionally denoted by $\Omega$, but this is unfortunate given the also-very-standard symbol for the module of differentials.

[[David Roberts]]: LM is standard notation for the free loop space, as is mentioned in the text. The Frechet manifold structure on LM does, a little surprisingly, not give rise to the compact-open topology, as I learned recently. For details of the manifold LM see almost anything of what [[Andrew Stacey]] has written. Oh, and it is always smooth loops, not continuous loops.
=--
A $0$-form $f:L M\to \mathbb{R}$ induces a $1$-form $L^*f\in \Omega^1(M)$ and a loop $\gamma: S^1\to M$ in $M$ determines a point $L_*\gamma$ in $L M$. Then we give the condition that for any $0$-form $f: L M\to \mathbb{R}$ and any loop $\gamma: S^1\to M$,

$$\int_\gamma L^*f = \int_{L_*\gamma} f.$$

The right-hand side is simply evaluation of the $0$-form at the point determined by $\gamma$, from which it follows that the integral of a 1-form $L^*f$ over a loop $\gamma: S^1 \to M$ can be computed simply by evaluation.
