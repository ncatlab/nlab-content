
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### Geometric


For $n \in \mathbb{N}$ a [[natural number]], the $n$-[[dimension|dimensional]] **ball** or **$n$-disk** in $\mathbb{R}^n$ is the [[topological space]]

$$
  D^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \leq 1\}
  \subset \mathbb{R}^n
$$ 

equipped with the [[induced topology]] as a subspace of the [[Cartesian space]] $\mathbb{R}^n$.

Its [[interior]] is the **open $n$-ball**

$$
  \mathbb{B}^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \lt 1 \}
  \subset \mathbb{R}^n
  \,.
$$ 

Its [[boundary]] is the $(n-1)$-[[sphere]].

More generally, for $(X,d)$ a [[metric space]] then an open ball in $X$ is a subset of the form

$$
  B(x,r) \coloneqq \{x \in X \;|\; d(x,y) \lt r \}
$$

for $x \in X$ and $r \in (0,\infty) \subset \mathbb{R}$.
(The collection of all open balls in $X$ form the [[basis of a topology|basis]] of the [[metric topology]] on $X$.)


### Combinatorial

There are also combinatorial notions of _disks_. For instance that due to ([Joyal](#Joyal)), as entering the definition of the [[Theta-category]]. See for instance ([Makkai-Zawadowski](#MakkaiZawadowski)).


## Properties 
 {#Properties}

### Closed balls 

A simple result on the _homeomorphism_ type of _closed_ balls is the following:  

+-- {: .num_theorem}
###### Theorem 
A [[compact space|compact]] [[convex subset|convex]] [[subset]] $D$ in $\mathbb{R}^n$ with [[nonempty set|nonempty]] [[interior]] is [[homeomorphic]] to $D^n$. 
=-- 

+-- {: .proof}
###### Proof
Without loss of generality we may suppose the origin is an interior point of $D$. We claim that the map $\phi: v \mapsto v/{\|v\|}$ maps the boundary $\partial D$ homeomorphically onto $S^{n-1}$. By convexity, $D$ is homeomorphic to the cone on $\partial D$, and therefore to the cone on $S^{n-1}$ which is $D^n$. 

The claim reduces to the following three steps. 

1. The restricted map $\phi: \partial D \to S^{n-1}$ is continuous. 

1. It's surjective: $D$ contains a ball $B = B_{\varepsilon}(0)$ in its interior, and for each $x \in B$, the positive ray through $x$ intersects $D$ in a bounded half-open line segment. For the extreme point $v$ on this line segment, $\phi(v) = \phi(x)$. Thus every unit vector $u \in S^{n-1}$ is of the form $\phi(v)$ for some extreme point $v \in D$, and such extreme points lie in $\partial D$. 

1. It's injective: for this we need to show that if $v, w \in \partial D$ are distinct points, then neither is a positive multiple of the other. Supposing otherwise, we have $w = t v$ for $t \gt 1$, say. Let $B$ be a ball inside $D$ containing $0$; then the convex hull of $\{w\} \cup B$ is contained in $D$ and contains $v$ as an interior point, contradiction.  

So the unit vector map, being a continuous bijection $\partial D \to S^{n-1}$ between [[compact Hausdorff space]]s, is a homeomorphism. 
=--


+-- {: .num_cor}
###### Corollary
Any compact convex set $D$ of $\mathbb{R}^n$ is homeomorphic to a disk. 
=-- 

+-- {: .proof} 
###### Proof
$D$ has nonempty interior relative to its affine span which is some $k$-plane, and then $D$ is homeomorphic to $D^k$ by the theorem. 
=--


### Open Balls

Open balls are a little less rigid than closed balls, in that one can more easily manipulate them within the _smooth_ category: 

+-- {: .num_lemma}
###### Observation

The open $n$-ball is [[homeomorphic]] and even [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

=--

+-- {: .proof}
###### Proof

For instance, the smooth map

$$
  x\mapsto \frac{x}{\sqrt{1+|x|^2}} : \mathbb{R}^n \to \mathbb{B}^n
$$

has smooth inverse

$$
  y\mapsto \frac{y}{\sqrt{1-|y|^2}} : \mathbb{B}^n \to \mathbb{R}^n.
$$

=--

This probe from ${\mathbb{R}}^n$ witnesses the property that the open $n$-ball is a ([[smooth manifold|smooth]]) [[manifold]]. Hence, each (smooth) $n$-dimensional manifold is locally isomorphic to both ${\mathbb{R}}^n$ and $\mathbb{B}^n$.

From general existence results about [[smooth structure]]s on [[Cartesian space]]s we have that

+-- {: .num_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is [[homeomorphic]] to $\mathbb{B}^d$ is also [[diffeomorphic]] to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 


+-- {: .num_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$. See [De Michelis-Freedman](#DeMFreed). 

=--

+-- {: .num_theorem #StarShapedOpenDiffeomorphicToOpenBall}
###### Theorem
**(star-shaped domains are diffeomorphic to open balls)**

Let $C \subset \mathbb{R}^n$ be a [[star-shaped]] [[open subset]] of a [[Cartesian space]]. Then $C$ is [[diffeomorphic]] to $\mathbb{R}^n$.

=--

+-- {: .num_remark #LiteratureOnStarShapedOpenDiffeoToOpenBall}
###### Remark

Theorem \ref{StarShapedOpenDiffeomorphicToOpenBall} is a [[folk theorem]], but explicit **proofs** in the literature are hard to find. See the discussion at [References](#References). An explicit proof has been written out by Stefan Born, and this appears as the proof of [theorem 237](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf#page=154) in ([Ferus 07](#Ferus07)). A simpler proof is given in [Gonnord-Tosel 98](#GonnordTosel98) reproduced [here](http://mathoverflow.net/a/212595/381).

=--

Here is another proof:

+-- {: .proof}
###### Proof
Suppose $T$ is a star-shaped open subset of ${\mathbb {R}}^n$ centered at the origin. Theorem 2.29 in [Lee](#Lee) proves that there is a function $f$ on ${\mathbb{R}}^n$ such that $f\gt 0$ on $T$ and $f$ vanishes on the complement of $T$. By applying [[bump functions]] we can assume that $f\le 1$ everywhere and $f=1$ in an open $\epsilon$-neighborhood of the origin; by rescaling the ambient space we can assume $\epsilon=2$.

The smooth vector field $V\colon x\mapsto f(x)\cdot x/{\|x\|}$ is defined on the complement of the origin in $T$. Multiply $V$ by a smooth bump function $0\le b\le 1$ such that $b=1$ for ${\|x\|} \gt 1/2$ and $b=0$ in a neighborhood of 0.
The new vector field $V$ extends smoothly to the origin and defines a smooth global flow $F\colon \mathbb{R} \times T\to T$. (The parameter of the flow is all of $\mathbb{R}$ and not just some interval $(-\infty,A)$ because the norm of $V$ is bounded by 1.) Observe that for $1/2\lt {\|x\|} \lt 2$ the vector field $V$ equals $x\mapsto x/{\|x\|}$. Also, all flow lines of $V$ are radial rays.

Now define the flow map $p\colon{\mathbb{R}}^n_{\gt 1/2}\to T_{\gt 1/2}$ as $x\mapsto F({\|x\|}-1, \frac{x}{{\|x\|}})$ for ${\|x\|} \gt 1/2$. (The subscript $\gt 1/2$ removes the closed ball of radius $1/2$.) The flow map is the composition of two diffeomorphisms, 

$${\mathbb{R}}^n_{\gt 1/2}\to(-1/2,\infty)\times S^{n-1} \to T_{\gt 1/2},$$ 

hence itself is a diffeomorphism. (Note particularly that the latter map is surjective. In detail: a flow line is a smooth map of the form $L: (A,B) \to T$, where $A$ and $B$ can be finite or infinite. If $B$ is finite and the limit of $L(t)$ as $t \to B$ exists, then the vector field $V$ vanishes at $B$. In our case $V$ can only vanish at the boundary of $T$, which is precisely what we want for surjectivity.)

Finally, define the desired diffeomorphism $d\colon{\mathbb{R}}^n\to T$ as the gluing of the identity map for ${\|x\|} \lt 2$ and as $p$ for ${\|x\|}\gt 1/2$.
The map $g$ is smooth because for $1/2\lt {\|x\|} \lt 2$ both definitions give the same value.
=--

And here is another proof, due to Gonnord and Tosel, translated into English by Erwann Aubry and available on MathOverflow:

\begin{theorem}
Every open star-shaped set $\Omega$ in $\mathbb{R}^n$ is $C^\infty$-diffeomorphic to $\mathbb{R}^n$.
\end{theorem}

\begin{proof}
For convenience assume that $\Omega$ is star-shaped at $0$.

Let $F=\mathbf{R}^n\setminus\Omega$ and $\phi:\mathbf{R}^n\rightarrow\mathbb{R}_+$ (here $\mathbf{R}_+=[0,\infty)$) be a $C^\infty$-function such that $F=\phi^{-1}(\{0\})$.
(Such $\phi$ exists by the [[Whitney extension theorem]].)

Now we define $f:\Omega\rightarrow\mathbb{R}^n$ via the formula:
$$f(x)=\overbrace{\left[1+\left(\int_0^1\frac{dv}{\phi(vx)}\right)^2\|x\|^2\right]}^{\lambda(x)}\cdot x=\left[1+\left(\int_0^{\|x\|}\frac{dt}{\phi(t\frac{x}{\|x\|})}\right)^2\right]\cdot x.$$
Clearly $f$ is smooth on $\Omega$.

We set $A(x)=\sup\{t\gt0\mid t\frac{x}{\|x\|}\in\Omega\}$.
$f$ sends injectively the segment (or ray) $[0,A(x))\frac{x}{\|x\|}$ to the ray $\mathbf{R}_+\frac{x}{\|x\|}$.
Moreover, $f(0\frac{x}{\|X\|})=0$ and
$$\lim_{r\rightarrow A(x)}\left\|f(r\frac{x}{\|x\|})\right\|=\lim_{r\to A(x)}\left[1+\left(\int_0^{r}\frac{dt}{\phi\left(t\cdot\frac{rx}{\|x\|}\cdot\left\|\frac{\|x\|}{rx}\right\|\right)}\right)^2\right]\cdot r= \left[1+\left(\int_0^{A(x)}\frac{dt}{\phi(t\frac{x}{\|x\|})}\right)^2\right]\cdot A(x)=+\infty.$$
Indeed, if $A(x)=+\infty$, then it holds for obvious reason.
If $A(x)\lt+\infty$, then by definitions of $\phi$ and $A(x)$ we get that $\phi(A(x)\frac{x}{\|x\|})=0$.
Hence by the [[mean value theorem]] and the fact that $\phi$ is $C^1$ due to
$$\phi\left(r\frac{x}{\|x\|}\right)\le M(A(x)-r)$$
for some constant $M$ and every $r$.
As a result,
$$\int_0^{A(x)}\frac{dt}{\phi\left(t\frac{x}{\|x\|}\right)}$$
diverges.
Hence we infer that $f([0,A(x))\frac{x}{\|x\|})=\mathbf{R}_+\frac{x}{\|x\|}$ and so $f(\Omega)=\mathbf{R}^n$.

To end the proof we need to show that $f$ has a $C^\infty$-inverse.
But as a corollary from the [[inverse function theorem]] we get that it is sufficient to show that $df$ vanishes nowhere. 

Suppose that $d_x f(h)=0$ for some $x\in\Omega$ and $h\neq 0$.
From definition of $f$ we get that
$$d_x f(h)=\lambda(x)h+d_x \lambda(h)x.$$
Hence $h=\mu x$ for some $\mu\neq 0$ and from that $x\neq 0$.
As a result $\lambda(x)+d_x \lambda(x)=0$.
But we have that $\lambda(x)\ge1$ and function $g(t):=\lambda(tx)$ is increasing, so $g'(1)=d_x \lambda(x)\gt0$, which gives a contradiction.
\end{proof}


+-- {: .num_example}
###### Example


Let $I(\Delta^n) \subset \mathbb{R}^n$ be the [[interior]] of the standard $n$-[[simplex]]. Then there is a diffeomorphism to $\mathbb{B}^n$ defined as follows:

Parameterize the $n$-simplex as

$$
  I(\Delta^n) 
  =
  \left\{
    (x^1, \cdots, x^n) \in \mathbb{R}
    |
     (\forall i : x^i \gt 0)\; and \; ( \sum_{i=1}^n x^i \lt 1)
  \right\}
  \,.
$$

Then define the map $f : I(\Delta^n) \to \mathbb{R}^n$ by

$$
  (x^1, \ldots, x^n) 
  \mapsto 
  (\log(\frac{x^1}{1 - x^1 - \ldots -x^n}), 
  \ldots, 
  \log(\frac{x^n}{1 - x^1 - \ldots - x^n}))
  \,.
$$ 

=--

(Thanks to [[Todd Trimble]].) One way to think about it is that $I(\Delta^n)$ is the positive orthant of an open $n$-ball in $l^1$ norm, so that in the opposite direction we have a chain of invertible maps 

$$\array{
\mathbb{R}^n & \stackrel{\exp^n}{\to} & \mathbb{R}_+^n & \to & I(\Delta^n) \\ 
 & & \vec{x} & \mapsto & \vec{x}/(1 + {\|\vec{x}\|}_1) 
}$$ 

which we simply invert to get the map $f$ above. 


### Good covers by balls

One central application of balls is as building blocks for [[covering]]s. See [[good open cover]] for some statements.


## Related concepts

* [[unit ball]]

## References 
 {#References}

### Geometric

* {#Ozols}  V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))


That an open subset $U \subseteq \mathbb{R}^4$ homeomorphic to $\mathbb{R}^4$ equipped with the smooth structure inherited as an open submanifold of $\mathbb{R}^4$ might nevertheless be non-diffeomorphic to $\mathbb{R}^4$, see 

* De Michelis, Stefano; Freedman, Michael H. (1992) "Uncountably many exotic $\mathbb{R}^4$'s in standard 4-space", J. Diff. Geom. 35, pp. 219-254.
{#DeMFreed} 

### Star-shaped regions diffeomorphic to open ball
 {#ReferencesStarShapedReasonDiffeomorphicToOpenBall}

The proof that open star-shaped regions are diffeomorphic to a ball appears as [theorem 237](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf#page=154) in

* {#Ferus07} [[Dirk Ferus]], _Analysis III_ (2007) ([pdf](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf)) 

It is a lengthy proof, due to Stefan Born. 

A simpler version of the proof apparently appears on page 60 of

* {#GonnordTosel98} Stéphane Gonnord, Nicolas Tosel, _Calcul Différentiel_, ellipses (1998) 

and is reproduced in

* [MathOverflow answer 212595](http://mathoverflow.net/a/212595).

Apparently this proof is little known. For instance in a remark below lemma 10.5.5 of

* Lawrence Conlon, _Differentiable manifolds_, Birkh&#228;user (last edition 2008)

it says:

> It seems that open star shaped sets $U \subset M$ are always diffeomorphic to $\mathbb{R}^n$, but this is extremely difficult to prove. 

And in 

* {#Lee}  Jeffrey Lee, _Manifolds and differential geometry_  (2009)
 
one finds the statement:

> Actually, the assertion that an open geodesically convex set in a Riemannian manifold is diffeomorphic to $\mathbb{R}^n$ is common in literature, but it is a more subtle issue than it may seem, and references to a complete proof are hard to find (but see [Grom]).

Here "Grom" refers to

* [[Mikhail Gromov]], _Convex sets and K&#228;hler manifolds_, Advances in differential geometry and topology. F. Tricerri ed., World Sci., Singapore,
(1990), 1-38. ([pdf](http://www.ihes.fr/~gromov/PDF/%5B68%5D.pdf))

where the relevant statement is 1.4.C1 on page 8. Note however that the diffeomorphism considered there is only of $C^1$ class, not $C^\infty$, so this is not a proof either.

For a discussion of diffeomorphisms between geodesically convex regions and open balls see at _[[good open cover]]_.

See also the Math Overflow discussion [here](http://mathoverflow.net/questions/41853/explicit-diffeomorphim-between-open-simplex-and-open-ball). 

### Combinatorial


* {#Joyal} [[Andre Joyal]], _Disks, duality and Theta-categories_ ([[JoyalThetaCategories.pdf:file]])
 

* {#MakkaiZawadowski} [[Mihaly Makkai]], Marek Zawadowski, _Duality for Simple $\omega$-Categories and Disks_ ([TAC](http://www.emis.de/journals/TAC/volumes/8/n7/8-07abs.html))
 

[[!redirects ball]]
[[!redirects balls]]
[[!redirects  balls]]
[[!redirects n-ball]]
[[!redirects n-balls]]

[[!redirects open ball]]
[[!redirects open balls]]
[[!redirects open balll]]
[[!redirects open n-ball]]
[[!redirects open n-balls]]

[[!redirects closed ball]]
[[!redirects closed balls]]
[[!redirects closed n-ball]]
[[!redirects closed n-balls]]

[[!redirects disk]]
[[!redirects disks]]
[[!redirects disc]]
[[!redirects discs]]

[[!redirects open disk]]
[[!redirects open disks]]
[[!redirects open disc]]
[[!redirects open discs]]

[[!redirects closed disk]]
[[!redirects closed disks]]
[[!redirects closed disc]]
[[!redirects closed discs]]


[[!redirects n-disk]]
[[!redirects n-disks]]
[[!redirects n-disc]]
[[!redirects n-discs]]

[[!redirects open n-disk]]
[[!redirects open n-disks]]
[[!redirects open n-disc]]
[[!redirects open n-discs]]
