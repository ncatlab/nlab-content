+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$ a [[natural number]], the $n$-[[dimension]]al **ball** or **$n$-disk** is the [[topological space]]

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

## Properties {#Properties}

### Closed balls 

A simple result on the _homeomorphism_ type of _closed_ balls is the following:  

+-- {: .un_thm}
######Theorem 
A [[compact]] [[convex]] [[subset]] $D$ in $\mathbb{R}^n$ with [[nonempty]] [[interior]] is [[homeomorphic]] to $D^n$. 
=-- 

+-- {: .proof}
######Proof
Without loss of generality we may suppose the origin is an interior point of $D$. We claim that the map $\phi: v \mapsto v/\|v\|$ maps the boundary $\partial D$ homeomorphically onto $S^{n-1}$. By convexity, $D$ is homeomorphic to the cone on $\partial D$, and therefore to the cone on $S^{n-1}$ which is $D^n$. 

Shouldn't the claim be obvious? 

* The restricted map $\phi: \partial D \to S^{n-1}$ is continuous. 

* It's surjective: $D$ contains a ball $B = B_{\varepsilon}(0)$ in its interior, and for each $x \in B$, the positive ray through $x$ intersects $D$ in a bounded half-open line segment. For the extreme point $v$ on this line segment, $\phi(v) = \phi(x)$. Thus every unit vector $u \in S^{n-1}$ is of the form $\phi(v)$ for some extreme point $v \in D$, and such extreme points lie in $\partial D$. 

* It's injective: for this we need to show that if $v, w \in \partial D$ are distinct points, then neither is a positive multiple of the other. Supposing otherwise, we have $w = t v$ for $t \gt 1$, say. Let $B$ be a ball inside $D$ containing $0$; then the convex hull of $\{w\} \cup B$ is contained in $D$ and contains $v$ as an interior point, contradiction.  

So the unit vector map, being a continuous bijection $\partial D \to S^{n-1}$ between compact [[Hausdorff space]]s, is a homeomorphism. 
=--

+-- {: .un_cor}
######Corollary
Any compact convex set $D$ of $\mathbb{R}^n$ is homeomorphic to a disk. 
=-- 

+-- {: .proof} 
######Proof
$D$ has nonempty interior relative to its affine span which is some $k$-plane, and then $D$ is homeomorphic to $D^k$ by the theorem. 
=--

### Open Balls

Open balls are a little less rigid than closed balls, so that we can manipulate them up to diffeomorphism: 

+-- {: .un_lemma}
###### Observation

The open $n$-ball is [[homeomorphic]] and even [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use for instance the map 

$$
  f : \mathbb{R}^n \to \mathbb{B}^n
$$

given by

$$
  (x^1, \cdots, x^n) 
  \mapsto
  \left(
    \frac{x^1}{\sqrt{1 + r^2}},
    \cdots
    \frac{x^n}{\sqrt{1 + r^2}}
  \right)
  \,,
$$

where $r^2 = \sum_{i = 1}^n (x^i)^2$.

=--

So the open $n$-ball is naturally a ([[smooth manifold|smooth]]) [[manifold]]. And every (smooth) $n$-dimensional manifold is locally isomorphic to $\mathbb{B}^n$.

From very general existence results about [[smooth structure]]s on [[Cartesian space]]s we have that

+-- {: .un_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is [[homeomorphic]] to $\mathbb{B}^d$ is also [[diffeomorphic]] to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 


+-- {: .un_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$. 

=--

+-- {: .un_theorem}
###### Theorem

Let $C \subset \mathbb{R}^n$ be a [[star-shaped]] [[open subset]] of a [[Cartesian space]]. Then $C$ is [[diffeomorphic]] to $\mathbb{R}^n$.

=--

This appears as [theorem 237](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf#page=154) of ([Ferus](#Ferus)).  Even an explicit construction of a diffeomorphism as asserted by the theorem is given there.



+-- {: .un_example}
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

(Thanks to [[Todd Trimble]].)

## References

* V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))
{#Ozols}

* [[Dirk Ferus]], _Analysis III_ ([pdf](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf)) 
{#Ferus}


[[!redirects  balls]]

[[!redirects open ball]]
[[!redirects open balls]]

[[!redirects open n-ball]]
[[!redirects open n-balls]]

[[!redirects closed ball]]
[[!redirects closed balls]]

[[!redirects closed n-ball]]
[[!redirects closed n-balls]]

[[!redirects disk]]
[[!redirects disks]]

[[!redirects n-disk]]
[[!redirects n-disks]]