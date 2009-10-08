
<div class="rightHandSide toc">
[[!include homotopy - contents]]
***
[[!include synthetic differential geometry - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

An _infinitesimal interval object_ is like an [[interval object]] that is an [[infinitesimal space]].

Where maps out of an [[interval object]] model paths that may arrange themselves into [[path ∞-groupoid]]s, maps out of infinitesimal interval object model infinitesimal paths that may arrange themselves into [[infinitesimal path ∞-groupoid in a smooth topos|infinitesimal path ∞-groupoid]].

# Definition #

In any [[lined topos]] $(\mathcal{T},(R,+,\cdot))$ the line object $R$ is naturally regarded as a [[interval object|cartesian interval object]]. 

$$
  \array{
    && R
    \\
    & 
    {}^{0_{*}}\nearrow && \nwarrow^{1_{*}}
    \\
    {*}
    &&&&
    {*}
  }
  \,.
$$

If the [[lined topos]] $(\mathcal{T}, R)$ is also a [[smooth topos]] in that it satisfies the [[Kock-Lawvere axiom]] it makes sense to consider the [[subobject]] $D$ of $R$ defined as the [[equalizer]]

$$
  D = \lim\left( R \stackrel{\stackrel{(-)^2}{\to}}{\stackrel{0}{\to}} R \right)
$$

or equivalently expressed in [[topos]] [[logic]] as

$$
  D = \{x \in R | x^2 = 0 \}
  \,.
$$

and think of $D$ as the **infinitesimal interval object** of the [[smooth topos]] $(\mathcal{T},R)$ inside its finite [[interval object]] $R$. By the axioms satisfied by a [[smooth topos]] it is in particular an [[infinitesimal object]].

Various constructions induced by a finite [[interval object]] have their infinitesimal analog for infinitesimal interval objects.

In particular, where the [[interval object]] $R$ induces the [[path ∞-groupoid in a lined topos]] $\Pi(-) : \mathcal{T} \to [\Delta^{op}, \mathcal{T}]$, the infinitesimal interval object induces the [[infinitesimal path ∞-groupoid in a smooth topos]] $\Pi^{inf}(-) : \mnathcal{T} \to [\Delta^{op}, \mathcal{T}]$ and a canonical inclusion

$$
  \Pi^{inf}(-) \hookrightarrow \Pi(-)
  \,.
$$

While the [[k-morphism]]s in the finite path $\infty$-groupoid $\Pi(X)$ are $k$-dimensional families of path-connected points in $X$ -- as seen by $R$ -- the [[k-morphism]] in $\Pi^{inf}(X)$ are $(k+1)$-tuples of [[infinitesimal neighbour]] points in $X$ -- as seen by $D$.

#Infintesimal path $\infty$-groupoid induced from infinitesimal interval#

Recall the discussion at [[interval object]] of how the interval ${*}\sqcup {*} \stackrel{\to}{\to} R$ in $\mathcal{T}$ alone gave rise to the [[cosimplicial object]]

$$
  \Delta_R : \Delta \to \mathcal{T}
$$

of (collared) $k$-simplices modeled on $R$, and how that induces for each object $X \in \mathcal{T}$ the [[simplicial object]]

$$
  \Pi(X) := X^{\Delta_R^\bullet}
  \,.
$$ 

Here as an object in $\mathcal{T}$ the $k$-simplex is actually a $k$-cube $\Delta_R^k := R^k$, but equipped with face and degeneracy maps that identify the boundary of a $k$-simplex inside the $k$-cube thus realizing the interior of that boundary as the $k$-simplex proper and the exterior as its _collar_ .

We want to mimic that construction with the finite interval $R$ replaced by the infinitesimal interval object $D$, to get a simplicial object $\Pi^{inf}(X)$ for every object $X$.

While the infinitesimal situation is formally very similar to the finite situation, one technical diference is that the infinitesimal interval does not fit into a nontrivial [[cospan]] as the finite interval does. This is because $D$ typically has a _unique_ morphism ${*} \to D$ from the terminal object, as a consequence of the fact that all the infinitesimal elements it contains are genuinely [[generalized element]]s.

The natural way to encode an infinitesimal path between two elements in an object $X$ in the [[smooth topos]] $\mathcal{T}$ is therefore not as an element of $X^D$ but of $X^D \times D$, which we may think of as the space of pairs consisting of infinitesimal paths in $X$ and infinitesimal parameter lengths of these paths.

This naturally yields the [[span]]

$$
  \array{
    && X^D \times D
    \\
    & {}^{d_1 := p_{T X} p_1}\swarrow && \searrow^{d := ev}
    \\
    X &&&& X
  }
  \,,
$$

where 

* the left leg is the projection $X^D \times D \to X^D$ followed by the [[tangent bundle]] projection $p_{T X} = X^{(* \to D)} : X^D \to X$ 

* the right leg is the evaluation map, i.e. the [[inner hom]]-[[adjunct]] of $Id : X^D \to X^D$.

With this setup a pair of ([[generalized element|generalized]]) elements $x,y \in X$ may be thought of as connected by an infinitesimal path if there is an element $(v,\epsilon) \in X^D \times D$ such that 

$$
  \delta_1(v,\epsilon) = v(0) = x
$$ 

and 

$$
  \delta_0(v,\epsilon) = v(\epsilon) = y
  \,.
$$

But not all elements $(v,\epsilon)$ define _different_ pairs of [[infinitesimal neighbour]] elements this way: specifically in the case that $X$ is a [[microlinear space]], the [[tangent bundle]] object $X^D$ is fiberwise $R$-linear, and thus for any $t \in R$ the elements $(v,t \epsilon)$ and $(t v, \epsilon)$ defne the same pair of [[infinitesimal neighbour]]s, $x = v(0)$ and $y = (t v)(\epsilon) = v(t \epsilon)$.

We may identify such elements $(t v, \epsilon)$ and $(v, t \epsilon)$ by passing to the [[tensor product]] $X^D \otimes_R D$, i.e. the coequalizer of

$$
  X^D \times R \times D \stackrel{\stackrel{\cdot \times Id}{\to}}{\stackrel{Id \times \cdot}{\to}}
  X^D \times D
$$

where $\cdot$ here denotes the [[monoid]]-[[action]] of $(R,\cdot)$ on $D$ (by the embedding $D \hookrightarrow R$) and on $X^D$ (by the fact that $X$ is assumed to be [[microlinear space|microlinear]]).

In this same fashion we can then define infinitesimal analogs of the finite higher path object $X^{\Delta_R^k} = X^{R^{\times k}}$.

Let $D(n)$ be the [[infinitesimal space|k-dimensional infinitesimal interval]]

$$
  D(n) = \{(x_i) \in R^k | \forall i,j : x_i x_j = 0\}
$$

then set

$$
  X^{\Delta^\bullet_{inf}}
  :=
  \left(
    \cdots
    X^{D(2)}\otimes_{R^2} D(2)
    \stackrel{\to}{\stackrel{\to}{\to}}
    X^D \otimes_R D
    \stackrel{\to}{\to}
    X
  \right)
$$

...