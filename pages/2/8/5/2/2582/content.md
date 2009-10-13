
#Contents#

* automatic table of contents goes here
{:toc}

# Description #

The _Whitehead tower_ of a [[pointed space]] $(X,x)$ is a sequence of fibrations 

$$
\ldots \to X\langle n\rangle \to \ldots \to X\langle 1 \rangle \to X\langle 0 \rangle \to X
$$

where each $X\langle n\rangle \to X\langle n-1 \rangle$ induces isomorphisms on [[homotopy group]]s $\pi_i$ for $i\gt n$ and such that $X\langle n\rangle$ is $n$-connected (has trivial [[homotopy group]]s $\pi_i$ for $i \leq n$).

For $n=0$ we require that $X\langle 0 \rangle \hookrightattow X$ is the inclusion of the path-component of $x$. Really this is defined up to [[homotopy (as an operation)|homotopy]], but we have a canonical model. If $X$ is locally connected and semilocally path-connected, then $X\langle 1\rangle$ can be chosen as the [[universal covering space]]. 

In traditional models this construction is highly non-[[functor]]ial, except for nice spaces in low dimensions as remarked above. 


# Construction by co-killing of homotopy groups #

The whitehead tower may be constructed by iteratively [[co-killing homotopy groups]]:

start with the map

$$
  X \to \pi_0(X)
$$

that maps each point to its path-connected component. Then the [[homotopy fiber]]

$$
  \array{
    X\langle 0\rangle &\to& {*}
    \\
    \downarrow && \downarrow^{[x]}
    \\
    X &\to& G_0
  }
$$

is just an ordinary [[pullback]] and in fact $X\langle 0 \rangle$ is just the path-connected component of  the base point $x \in X$, as desired. 

Remark: It is not entirely unreasonable to notice at this step that instead of the set $\pi_0(X)$ we could use here just $\{0,1\}$ and send each point in the path connected component  of $x$ to 1 and all others to 0. Then ${*} \stackrel{1}{\hookrightarrow} \{0,1\}$ is the [[subobject classifier]] in [[Set]] and co-killing the 0-th homotopy "group" is the same as taking the [[subobject]] classified by the characteristic connected-component map $X \to \mathbb{Z}_2$.

Next let $\pi_1(X,x)$ be the first [[homotopy group]] of $X$ at $x$ and $\mathcal{B} \pi_1(X,x)$ its [[delooping]]. There is then naturally a map $X \to \mathcal{B} \pi_1(X)$ and the [[homotopy fiber]]

$$
  \array{
    \hat X &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathcal{B} \pi_1(X,x)
  }
$$

is the [[universal cover]] (universal 1-connected cover) of $X$.

And so on. 

Notice that after the second step for $X\langle n \rangle$ with $n \geq 1$ the [[Hurewicz theorem]] ensures that the first non-vanishing [[homotopy group]] $\pi_{n+1}(X\langle n \rangle)$ is [[isomorphism|isomorphic]] to the [[homology group]] $H_{n+1}(X \langle n\rangle, \mathbb{Z})$. This in turn, if it has no nontrivial [[torsion subgroup]], is isomorphic to the [[cohomology group]] $H^{n-1}(X\langle n\rangle, \mathbb{Z})$.


# Non-traditional approaches #

**The following is some semblance of current research, except the stuff about the string 2-group. All errors and stupid ideas are mine - David Roberts**

For locally nice spaces (say locally contractible), it is desirable to have a functorial construction of the Whitehead tower. A shadow of a low-dimensional case of this can be seen in the construction of the [[string 2-group]] given by Baez-Crans-Schreiber-Stevenson. Since finite-dimensional Lie groups have non-trivial third homotopy group, it is not possible to form the 3-connected cover in the [[category]] $fin.dim.LieGrp$, like it is possible to take the 0-, and 1-connected covers. While most people give up the smoothness and make do with the [[topological group]] $String_G$, The BCSS construction leaps out of that [[category]] into that of strict ([[Frechet space|Frechet]]) Lie [[2-group]]s. The construction is also functorial.

As an aside, I know of two classes of spaces with explicitly  constructed (i.e. not via co-killing homotopy groups) 2-connected covers: the 2-sphere and its quotients by $\mathbf{Z}/n$ (lens spaces), and the [[loop group]] $\Omega G$ of a compact, simple, simply-connected Lie group $G$ (the latter is the level-1 central extension by $U(1)$, the first needs no introduction).

However, without one could demand a conceptually similar approach to the $n$-connected cover of a general (locally nice) space or smooth manifold. For $n=2$, and taking only [[topological space]]s for consideration, this is contained in [[David Roberts|my]] thesis work.
The rough result is that one gets a 2-connected topological groupoid $X^{(2)}$ equipped with a map to $X$ that factors through the universal covering space $X^{(1)}$. This is functorial, and generalises to higher connected covers (at least heuristically - I don't have $n$-categorical superpowers).

But the general idea is that one would get an $(n-1)$-groupoid $X^{(n)}$ over $X$ which is $n$-connected and such that the map to $X$ factors through the $(n-2)$-groupoid $X^{(n-1)}$. The map to $X$ should induce [[isomorphism]]s on homotopy groups $\pi_i$ for $i\gt n$, as in the usual Whitehead tower.

#Literature#

For instance

example 4.20 in

* [[Alan Hatcher]], _Algebraic Topology_ ([pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))

