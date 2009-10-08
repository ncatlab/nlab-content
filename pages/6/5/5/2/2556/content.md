
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

