
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

What is called _Cantor space_, after [[Georg Cantor]], is the [[topological space]] obtained from the [[closed interval]] $[0,1]$ by 

1. removing the middle third, retaining only $[0,\tfrac{1}{3}]$ and $[\tfrac{2}{3}, 1]$;

1. removing from  these two pieces _their_ middle thirds, to retain the pieces $[0,\tfrac{1}{9}]$, $[\tfrac{2}{9},\tfrac{1}{3}]$, $[\tfrac{2}{3}, \tfrac{7}{9}]$, $[\tfrac{8}{9},1]$;

1. and so ever on.

$$
  \array{
    \mathrlap{[0} && &,& &&  \mathllap{1]}
    \\
    \mathrlap{[0} &,& \mathllap{\tfrac{1}{3}]} 
     &\phantom{(\tfrac{1}{2}, \tfrac{2}{3})} 
     &  \mathrlap{[\tfrac{2}{3}} &,& \mathllap{1]}
    \\
    \mathrlap{[0,\tfrac{1}{9}]}
    &
    \phantom{AAAAAAAA}
    &
    \mathllap{[\tfrac{2}{9}, \tfrac{1}{3} ]}
    &
    \phantom{  (\tfrac{1}{3}, \tfrac{2}{3}) }
    &
    \mathrlap{[\tfrac{2}{3}, \tfrac{7}{9}]}
    &
    \phantom{AAAAAAAA}
    &
    \mathllap{[\tfrac{8}{9}, 1]}
    \\
    &&& \vdots
  }
$$

Cantor space is a fundamental object of [[descriptive set theory]]; some indications of its use may be found at [[Polish space]]. Among its applications is a simple construction of a "[[Peano curve|space-filling curve]]" (q.v.).


## Definition
 {#Definition}

Traditionally the Cantor space was conceived of 

* [as a subspace of the real line](#AsSubspaceOfTheRealLine)

but of course it may also be described

* [as an abstract space](#AsAbstractTopologicalSpace)

in itself.


### As an abstract space
 {#AsAbstractTopologicalSpace}

In brief, Cantor space may be abstractly described as the [[topological space|topological]] [[product]] of countable many copies of the [[discrete space]] $\{0, 1\}$. In more concrete detail: 

Recall that a __[[binary digit]]__ is either $0$ or $1$; the [[set]] (or [[discrete space]]) of binary digits is the [[Boolean domain]] $\mathbb{B}$.

A __point__ in Cantor space is an [[infinite sequence]] of binary digits.  Accordingly, Cantor space may be denoted $\mathbb{B}^{\mathbb{N}}$, since its set of points is a [[function set]].

An __open__ in Cantor space is a collection $G$ of [[list|finite sequences]] of binary digits (that is a [[subset]] of the [[free monoid]] $\mathbb{B}^*$) such that:

*  If $u \in G$ and $v$ is an extension of $u$ (that is $u$ with possibly additional digits added to the end), then $v \in G$;

*  If $u:0 \in G$ and $u:1 \in G$ (where $u:i$ is the immediate extension of $u$ by the digit $i$), then $u \in G$.

A point $\alpha$ __belongs__ to an open $G$ if, for some $u$ in $G$, $\alpha$ is an extension of $u$.

An alternative characterization of Cantor space is as the [[terminal coalgebra for an endofunctor|terminal coalgebra]] for the endofunctor on [[Top]], $X \mapsto X + X$.


### What kind of space?

Traditionally, Cantor space is understood as a [[topological space]].  We start with the points, as defined above, then specify which sets of points are [[open subset|open]].  Although there are other ways to state which sets are open, we may define a set to be open if it is the set of points that belong to some open $G$ as defined above.

A newer approach is to understand Cantor space as a [[locale]].  Then we start with the opens and define an [[order]] relation on them to define a [[frame]].  In this case, the order relation is the obvious one, that $G \leq H$ if $G \subseteq H$ as subsets of $\mathbb{B}^*$.  Then the [[point of a locale|points]] come for free, and correspond precisely to the points as defined above.

In [[classical mathematics]], these two approaches are equivalent; a point is determined by its opens, and an open is determined by its points.  The theorem that a point is determined by its opens (so that Cantor space, as a topological space, is [[sober space|sober]]) is valid [[internalisation|internal]] to any [[pretopos]] with an [[exponential object|exponentiable]] [[natural numbers object]]; as such, it applies even in [[predicative mathematics|predicative]] and [[constructive mathematics|constructive]] mathematics.  However, the theorem that an open is determined by its points (so that Cantor space, as a locale, is [[spatial locale|topological]]) is equivalent to the [[fan theorem]]; it is true in some pretoposes and accepted by some schools of constructivism but false in other pretoposes and rejected, or even refuted, by other constructivists.

When the fan theorem is not valid, the localic approach is probably better; it allows more of the useful properties of Cantor space to hold.


### As a subspace of the real line
 {#AsSubspaceOfTheRealLine}

Cantor space is usually conceived of as a [[topological subspace]] of the [[real line]]:

Write $Disc(\{0,1\})$ for the the [[discrete topological space]] with two points. Write $\underset{n \in \mathbb{N}}{\prod} Disc(\{0,1\})$ for the [[product topological space]] of a [[countable set]] of copies of this discrete space with itself (i.e. the corresponding [[Cartesian product]] of sets $\underset{n \in \mathbb{N}}{\prod} \{0,1\}$ equipped with the [[Tychonoff topology]] induced from the [[discrete topology]] of $\{0,1\}$).

Then consider the [[function]]

$$
  \array{
    \underset{n \in \mathbb{N}}{\prod}
      &\overset{\kappa}{\longrightarrow}&
    [0,1]
    \\
    (a_i)_{i \in \mathbb{N}}
    &\overset{\phantom{AAAA}}{\mapsto}&
    \underoverset{i = 1}{\infty}{\sum} \frac{2 a_i}{3^i}
  }
$$

which sends an element in the product space, hence a [[sequence]] of binary digits, to the value of the [[power series]] as shown on the right.

One checks that this is a [[continuous function]] (from the [[product topology]] to the [[Euclidean space|Euclidean]] [[metric topology]] on the [[closed interval]]). Moreover with its [[image]] $\kappa\left( \underset{n \in \mathbb{N}}{\prod} \{0,1\}\right) \subset [0,1]$ equipped with its [[subspace topology]], then this is a [[homeomorphism]] onto its image:

$$
  \underset{n \in \mathbb{N}}{\prod} Disc(\{0,1\})
    \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
  \kappa\left(
    \underset{n \in \mathbb{N}}{\prod} Disc(\{0,1\})
  \right)
    \overset{\phantom{AAAA}}{\hookrightarrow}
  [0,1]
  \,.
$$

This image is the _Cantor space_ as a subspace of the closed interval.

From the localic perspective, a [[continuous map]] is given by a [[homomorphism]] of frames in the opposite direction.  Given an open $\sim$ in $\mathbb{R}$ (as a [[binary relation]] on [[rational numbers]], as described at [[locale of real numbers]]), this is mapped to the open $G$ in Cantor space such that $u \in G$ if and only if
$$ \sum_{i=1}^{len(u)} \frac { 2 u_i } { 3^i } \sim \sum_{i=1}^{len(u)} \frac { 2 u_i } { 3^i } + \frac 1 { 3^{-len(u)} } .$$
One then checks that this is an embedding.

+-- {: .query}
I should check this some day; for the moment, I am taking it on faith.  ---Toby
=--

In either case, the idea is:

*  A point of Cantor space corresponds to a number written in base $3$ with infinitely many digits, using only the digits $0$ and $2$ (which are the options for $2 a_i$ when $a_i \in \{0,1\}$); while

*  An open corresponds to a union of intervals, each of which is given by approximating a number in base $3$ to a finite number of digits, using only the digits $0$ and $2$.

One sometimes speaks of the __Cantor set__ to stress that one is considering Cantor space as a subspace of the real line. 

As we can also consider Cantor space as a product space $(\mathbb{Z}/2)^n$ of countably many copies of $\mathbb{Z}/(2)$, which carries a group structure, we can view Cantor space $C$ as a [[topological group]]. In particular, it is a [[homogeneous space]] (its group of self-homeomorphisms acts transitively on the space). 


## Properties

Cantor space, especially in its guise as a subspace of the real line, is quite famous; see [Wikipedia](http://en.wikipedia.org/wiki/Cantor_set).  Here are some headline properties:

*  Cantor space is a [[compact Hausdorff space]].  (For the topological space, this statement is again equivalent to the [[fan theorem]]; for the locale, it holds regardless.)

*  Cantor space is [[connected space|totally disconnected]]. 

* Thus Cantor space is a [[Stone space]]. 

*  Cantor space is [[metric space|metrizable]], and every compact metrizable space is a [[quotient space]] of Cantor space (see Theorem \ref{HA} below).

*  As a subspace of $\mathbb{R}$, the Cantor set is [[perfect space|perfect]] and [[uncountable set|uncountable]] but of [[Lebesgue measure|Lebesgue]] [[null set|measure zero]].

*  The Cantor set is a precisely self-similar [[fractal]] with [[Hausdorff dimension]] $\log_3 2 \approx 0.631$. 

+-- {: .num_theorem #Theorem} 
###### Theorem 

A [[topological space]] is [[homeomorphism|homeomorphic]] to Cantor space if and only if it is [[inhabited set|nonempty]], [[compact topological space|compact]], [[totally disconnected topological space|totally disconnected]], [[metric  space|metrizable]], and [[perfect topological space|perfect]]. 

=-- 

This result is sometimes called **[[Brouwer]]'s theorem**. It can be seen from the perspective of [[Stone duality]], where the dual result is that any two [[countable set|countable]] [[atom|atomless]] [[Boolean algebras]] are [[isomorphism|isomorphic]]; this dual result can be proven by a [[back-and-forth argument]]. 

+-- {: .num_cor #CorA} 
###### Corollary 

The  [[one-point compactification]] $\widebar{X}$ of a space $X$ that is [[second-countable space|second-countable]] [[local compactum|locally compact]] [[Hausdorff topological space|Hausdorff]], [[totally disconnected space|totally disconnected]] and perfect, is homeomorphic to Cantor space (provided $X$ is not itself compact). 

=-- 

+-- {: .proof} 
###### Proof 
$\widebar{X}$ is also second-countable, compact Hausdorff and therefore compact regular, and so by the [[Urysohn metrization theorem]] it is compact metrizable. The point $p$ at infinity is not isolated since we assume $X$ is not compact, so $\widebar{X}$ is perfect. If $V$ is any open neighborhood of $p$, so $V = \neg K$ for some compact $K \subset X$, then we claim there exists a clopen that contains $K$; in that case $V$ contains a clopen whence $\{p\}$ is the quasi-component of $p$ (hence also the connected component since we're in a compact Hausdorff space). But the argument [here](/nlab/show/compact+Hausdorff+rings+are+profinite#compopen) shows that for each $x \in K$ there is a clopen neighborhood of $x$ contained in $\neg \{p\}$; finitely many of these clopens cover $K$, and the claim follows by considering their union. 
=-- 

It follows from this result that all such spaces $X$ are homeomorphic: they all have Cantor space as their one-point compactifications, and so they are all homeomorphic to the space obtained obtained by removing a single point from Cantor space. This applies for example to spaces obtained by removing a finite number $n \geq 1$ of points from Cantor space. 

Cantor space is also a "universal" compact metric space in the following sense. 

+-- {: .num_theorem #HA} 
###### Theorem 
**(Hausdorff-Alexandroff)** 
Every compact metric space is a continuous image of Cantor space. 
=-- 

This implies that every compact metric space is a [[quotient space]] of Cantor space, since a surjective map between [[compact Hausdorff spaces]] is a closed surjection, and closed surjections are quotient maps. 

+-- {: .proof} 
###### Proof 
First, every compact metric space $X$ is [[separable space|separable]]: has a [[countable set|countable]] [[dense set]] $\{x_0, x_1, \ldots\}$. Assume, as we may, that the metric $d: X \times X \to [0, \infty)$ is valued in $[0, 1]$. Then the map $y: X \to [0, 1]^\mathbb{N}$ to the [[Hilbert cube]], defined by 

$$y(x) = (d(x, x_n))_{n \in \mathbb{N}}$$ 

(a type of restricted "[[Yoneda embedding]]", regarding [[metric spaces]] as [[enriched categories]]), is continuous and maps $X$ onto a [[closed subspace]] of $I^\mathbb{N}$. As mentioned at [Peano curve](https://ncatlab.org/nlab/show/Peano+curve#construction), there is a continuous surjection $C \to I^\mathbb{N}$. Taking the [[pullback]] in [[Top]] 

$$\array{
K & \hookrightarrow & C \\ 
\mathllap{surj} \downarrow & & \downarrow \mathrlap{surj} \\ 
X & \stackrel{y}{\hookrightarrow} & I^\mathbb{N}
}$$ 

we see that to produce a continuous surjection $C \to X$, it suffices to exhibit a continuous surjection $C \to K$. 

In fact, every closed subspace $K \hookrightarrow C$ admits a retraction. There is a clever trick for seeing this: represent Cantor space $C$ instead as the subspace of $[0, 1]$ whose points, when written in base $6$, have just $0$\'s and $5$\'s in their representation. This subspace has the geometric property that if $x, y \in C$, then $\frac{x+y}{2} \notin C$. As a result, for $x, y, z \in C$ we have $d(x, y) = d(x, z)$ only if $y = z$ and so: given a closed subspace $K$ of $C$, there is for each $x \in C$ a *unique* element $k_x \in K$ such that $d(x, k_x) = d(x, K)$. The assignment $x \mapsto k_x$ is continuous (in fact a [[locally constant function]] on $C \setminus K$, and continuous on $K$ as is easily seen) and provides the desired retraction. 
=-- 

## Related concepts

* [[Peano curve]]

* [[Sierpinski space]]

* [[long line]], [[Warsaw circle]],

* [[line with two origins]]

* [[Baire space of sequences]]

## References

Named after [[Georg Cantor]].


* [[Friedhelm Waldhausen]], p. 3-4 in _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))


* Proof Wiki, _[Cantor Space as Countably Infinite Product](https://proofwiki.org/wiki/Cantor_Space_as_Countably_Infinite_Product)_

[[!redirects Cantor space]]
[[!redirects Cantor set]]
