
#Contents#

* automatic table of contents goes here
{:toc}

## Definition

The **Whitehead tower** of a [[topological space]] $X$ is a sequence of topological spaces 

$$* \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X$$

where [[generalized the|the]] space $X^{(n)}$ is [[generalized the|the]] [[homotopy fiber]] of [[generalized the|the]] map $X \to X_{(n+1)}$ into the item $X_{(n+1)}$ in the [[Postnikov tower]] of $X$.

Here each [[homotopy pullback]]

$$
  \array{
    X^{(n)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& X_{(n+1)}
  }
$$

in the [[(∞,1)-category]] [[Top]] may be computed (as described at [[homotopy pullback]]) as an ordinary [[pullback]] in the 1-[[category]] [[Top]] of a fibrantly replaced diagram, for instance with the point $*$ replaced by the path fibration $P X_{(n+1)} \simeq *$, which is a [[Hurewicz fibration]] $P X_{(n+1)} \to X_{(n+1)}$. In this case also the ordinary [[pullback]] $X^{(n)}\to X$
  
$$
  \array{
    X^{(n)} &\to& P X_{(n+1)}
    \\
    \downarrow && \downarrow
    \\
    X &\to& X_{(n+1)}
  }
$$

is a fibration, and this is often taken as part of the definition of the Whitehead tower.

From this perspective the _Whitehead tower_ of a [[pointed space]] $(X,x)$ is a sequence of fibrations 

$$
\ldots \to X\langle n\rangle \to \ldots \to X\langle 1 \rangle \to X\langle 0 \rangle \to X
$$

where each $X\langle n\rangle \to X\langle n-1 \rangle$ induces isomorphisms on [[homotopy group]]s $\pi_i$ for $i\gt n$ and such that $X\langle n\rangle$ is $n$-[[connected]] (has trivial [[homotopy group]]s $\pi_i$ for $i \leq n$).

For $n=0$ we require that $X\langle 0 \rangle \hookrightarrow X$ is the inclusion of the path-component of $x$. Really this is defined up to [[homotopy (as an operation)|homotopy]], but we have a canonical model. If $X$ is locally connected and semilocally path-connected, then $X\langle 1\rangle$ can be chosen as the [[universal covering space]]. 

In traditional models this construction is highly non-[[functor]]ial, except for nice spaces in low dimensions as remarked above. 


## Constructions 

### Whitehead's construction 

In

*  _Fiber Spaces and the Eilenberg Homology Groups_, PNAS **38**, No. 5 (1952)

G. W. Whitehead answers the question, posed by Hurewicz, of the existence of what we would now call $n$-connected \'covers\' of a given space $X$, taking this to mean a fibration $X\langle n\rangle \to X$ with $X\langle n\rangle$ $n$-connected and otherwise inducing isomorphisms on homotopy groups. The construction proceeds as follows (using modern terminology). Given a pointed space $(X,x)$,

* Choose a representative for the [[Postnikov section]] $X_n$ such that $X \hookrightarrow X_n$ is a closed subspace (I would be tempted to make it a closed cofibration, but I don't know any reason for this to be necessary -DMR).

* Form the $\infty$-connected cover of $X_n$, i.e. the [[path fibration]] $P X_n$. This is a [[Hurewicz fibration]].

* Pull this back to $X$, to get $p:X\langle n\rangle \to X$, which is still a fibration. The induced maps on long exact sequences in homotopy can be compared, and show that $p$ has the desired properties. 

This gives us a single $n$-connected cover, but by considering the [[Postnikov tower]]
$$
X \to (\ldots \to X_n \to X_{n-1} \to \ldots \to X_1 \to X_0)
$$
of $X$, where each map $X \to X_n$ is the inclusion of a closed subspace, it is simple to see there are induced maps $X\langle n\rangle \to X\langle n-1\rangle$ over $X$ for all $n$.

One way of obtaining a Postnikov section as above is to choose representatives $\phi_g:S^{n+1} \to X$ of generators $g$ of $\pi_n(X,x)$ and attaching cells: $X(1) := B^{n+2} \cup_{\{\phi_g\}} X$. We then choose representatives for the generators of $\pi_{n+2}(X(1),x)$ and attach cells and so on. The colimit $\lim_{\to n} X(n)$ is then a Postnikov section with the properties we require.

Understandably, this process is unbelievably non-canonical, and so we are generally reduced to existence theorems using this method -- unless there is a functorial way to construct Postnikov sections. Strictly speaking we can only say _an_ $n$-connected cover (except in special cases, like when $n=1$ and $X$ is a [[well-connected space]]).

### Functorial constructions 

The $n$th stage of the Whitehead tower of $X$ is the [[homotopy fiber]] of the map from $X$ to the $n$th (or so) stage of its [[Postnikov tower]], so one can use a functorial construction of the Postnikov tower plus a functorial construction of the homotopy fiber (such as the usual one using the [[path object|path space]] of the target).

The $n$th stage of the Whitehead tower of $X$ is also the cofibrant replacement for $X$ in the right [[Bousfield localization]] of [[Top]] with respect to the object $S^n$ (or so). Since [[Top]] is right proper and cellular this localization exists by the result of chapter 5 of Hirschhorn's book on [[localization]]s of [[model category|model categories]]. 

## Examples 

### Whitehead tower of the orthogonal group 

The Whitehead tower of the [[orthogonal group]] $O(n)$ starts out as

$$
   \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to O(n)
$$

where the terms are

...
$\to$
[[fivebrane group]]
$\to$
[[string group]]
$\to$
[[spin group]]
$\to$
[[special orthogonal group]]
$\to$
[[orthogonal group]]

## Whitehead tower in general $(\infty,1)$-toposes

While a notion of [[Postnikov tower in an (∞,1)-category]] depends on the _categorical_ [[homotopy groups in an (∞,1)-topos|homotopy groups in an (∞,1)-category]], the notion of Whitehead tower makes good sense with respect to the _geometric_ homotopy groups. 

A good notion of geometric [[homotopy groups in an (∞,1)-topos]] exist in a [[locally contractible (∞,1)-topos]]. The notion of Whitehead tower in this context is discussed at 

* [[Whitehead tower in an (∞,1)-topos]].

## References 

The classical notion of Whitehead tower is reviewed for instance as  example 4.20 in

* [[Alan Hatcher]], _Algebraic Topology_ ([pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))

