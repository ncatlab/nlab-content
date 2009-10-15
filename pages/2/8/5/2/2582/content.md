
#Contents#

* automatic table of contents goes here
{:toc}

# Description #

The _Whitehead tower_ of a [[pointed space]] $(X,x)$ is a sequence of fibrations 

$$
\ldots \to X\langle n\rangle \to \ldots \to X\langle 1 \rangle \to X\langle 0 \rangle \to X
$$

where each $X\langle n\rangle \to X\langle n-1 \rangle$ induces isomorphisms on [[homotopy group]]s $\pi_i$ for $i\gt n$ and such that $X\langle n\rangle$ is $n$-connected (has trivial [[homotopy group]]s $\pi_i$ for $i \leq n$).

For $n=0$ we require that $X\langle 0 \rangle \hookrightarrow X$ is the inclusion of the path-component of $x$. Really this is defined up to [[homotopy (as an operation)|homotopy]], but we have a canonical model. If $X$ is locally connected and semilocally path-connected, then $X\langle 1\rangle$ can be chosen as the [[universal covering space]]. 

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

### Whitehead's construction ###

In

*  _Fiber Spaces and the Eilenberg Homology Groups_, PNAS **38**, No. 5 (1952)

G. W. Whitehead answers the question, posed by Hurewicz, of the existence of what we would now call $n$-connected \'covers\' of a given space $X$, taking this to mean a fibration $X^{(n)} \to X$ with $X^{(n)}$ $n$-connected and otherwise inducing isomorphisms on homotopy groups. The construction proceeds as follows (using modern terminology). Given a pointed space $(X,x)$,

* Choose a representative for the [[Postnikov section]] $X_n$ such that $X \hookrightarrow X_n$ is a closed subspace (I would be tempted to make it a closed cofibration, but I don't know any reason for this to be necessary -DMR).

* Form the $\infty$-connected cover of $X_n$, i.e. the [[path fibration]] $PX = P_xX$. This is a [[Hurewicz fibration]].

* Pull this back to $X$, to get $p:X^{(n)} \to X$, which is still a fibration. The induced maps on long exact sequences in homotopy can be compared, and show that $p$ has the desired properties. 

This gives us a single $n$-connected cover, but by considering the [[Postnikov tower]]
$$
X \to (\ldots \to X_n \to X_{n-1} \to \ldots \to X_1 \to X_0)
$$
of $X$, where each map $X \to X_n$ is the inclusion of a closed subspace, it is simple to see there are induced maps $X^{(n)} \to X^{(n-1)}$ over $X$ for all $n$.

One way of obtaining a Postnikov section as above is to choose representatives $\phi_g:S^{n+1} \to X$ of generators $g$ of $\pi_n(X,x)$ and attaching cells: $X(1) := B^{n+2} \cup_{\{\phi_g\}} X$. We then choose representatives for the generators of $\pi_{n+2}(X(1),x)$ and attach cells and so on. The colimit $\lim_{\to n} X(n)$ is then a Postnikov section with the properties we require.

Understandably, this process is unbelievably non-canonical, and so we are generally reduced to existence theorems using this method -- unless there is a functorial way to construct Postnikov sections. Strictly speaking we can only say _an_ $n$-connected cover (except in special cases, like when $n=1$ and $X$ is a [[well-connected space]]).

## In other $(\infty,1)$-topoi ##

Given an $(\infty,1)$-topos $C$ we can talk about [[n-truncated object of an (infinity,1)-topos|n-truncated objects]] in $C$. The above construction then has an analogue in $C$ (may need something like properness so as to get the pullback of a fibration to be a fibration -- I'm making this section up as I go along -DMR). The path fibration is replaced by the trivial cofibration-fibration factorisation of the inclusion of the basepoint $* \to X$ (probably want this to be functorial for my liking -DMR).

For example, in $sSet$, we have a functoral $n$-truncation operation, via the [[coskeleton]] endofunctor $Cosk_{n+1}: sSet \to sSet$ (I think I have the indexing right - it may be $Cosk_n$. -DMR). We also have the [[decalage]] functor, which gives us the factorisation $* \to Dec^1 X \to X$. The pullback of $Dec^1Cosk_{n+1} X \to \Cosk_{n+1} X$ (again, indexing) along the unit $X \to Cosk_{n+1}X$ gives the $n$-connected cover of $X$, and now we are justified in saying [[the]]. This idea of the canonical Postnikov tower is explored in low dimensions by Duskin in

*  Simplicial matrices and the nerves of weak $n$-categories I: Nerves of bicategories, TAC **9** no. 2, (2002).

In Duskin's treatment the inclusion $X \to Cosk_3X$ for $X$ a Kan complex is just the map sending an $\infty$-groupoid into the bigroupoid representing its 2-type.

# Non-traditional approach in $Top$ #

**The following is some semblance of current research, except the stuff about the string 2-group. All errors and stupid ideas are mine - David Roberts**

For locally nice spaces (say locally contractible), it is desirable to have a functorial construction of the Whitehead tower. A shadow of a low-dimensional case of this can be seen in the construction of the [[string 2-group]] given by Baez-Crans-Schreiber-Stevenson. Since finite-dimensional Lie groups have non-trivial third homotopy group, it is not possible to form the 3-connected cover in the [[category]] $fin.dim.LieGrp$, like it is possible to take the 0-, and 1-connected covers. While most people give up the smoothness and make do with the [[topological group]] $String_G$, The BCSS construction leaps out of that [[category]] into that of strict ([[Frechet space|Frechet]]) Lie [[2-group]]s. The construction is also functorial.

+--{: .query}
[[David Roberts]]: As an aside, I know of two classes of spaces with explicitly  constructed (i.e. not via co-killing homotopy groups) 2-connected covers: the 2-sphere and its quotients by $\mathbf{Z}/n$ (lens spaces), and the [[loop group]] $\Omega G$ of a compact, simple, simply-connected Lie group $G$ (the latter is the level-1 central extension by $U(1)$, the first needs no introduction). Does anybody know of any other $n$-connected covers (other than, say, the Hopf fibrations) that are canonically given?
=--

However, without one could demand a conceptually similar approach to the $n$-connected cover of a general (locally nice) space or smooth manifold. For $n=2$, and taking only [[topological space]]s for consideration, this is contained in [[David Roberts|my]] thesis work.
The rough result is that one gets a 2-connected topological groupoid $X^{(2)}$ equipped with a map to $X$ that factors through the universal covering space $X^{(1)}$. This is functorial, and generalises to higher connected covers (at least heuristically - I don't have $n$-categorical superpowers).

But the general idea is that one would get an $(n-1)$-groupoid $X^{(n)}$ over $X$ which is $n$-connected and such that the map to $X$ factors through the $(n-2)$-groupoid $X^{(n-1)}$. The map to $X$ should induce [[isomorphism]]s on homotopy groups $\pi_i$ for $i\gt n$, as in the usual Whitehead tower.

#Literature#

For instance:

example 4.20 in

* [[Alan Hatcher]], _Algebraic Topology_ ([pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))

