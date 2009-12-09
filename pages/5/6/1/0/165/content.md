* toc
{: toc}

#Idea#

The **fundamental groupoid** of a space $X$ is a [[groupoid]] whose objects are the points of $X$ and whose morphisms are paths in $X$, identified up to endpoint-preserving [[homotopy]].

In parts of the literature the fundamental groupoid, and more generally the [[fundamental ∞-groupoid]], is called the **Poincar&#233;-groupoid**.

#Definition#

The **fundamental groupoid** $\Pi_1(X)$ of a topological space $X$ is the [[groupoid]] whose set of objects is $X$ and whose morphisms from $x$ to $y$ are the homotopy-classes $[\gamma]$ of continuous maps $\gamma : [0,1] \to X$ whose endpoints map to $x$ and $y$ (which the homotopies are required to fix). Composition is by concatenation (and reparametrization) of representative maps. Under the [[homotopy]]-[[equivalence relation]] this becomes an associative and unital composition with respect to which every morphism has an inverse; hence $\Pi_1(X)$ is a groupoid.

# Remarks

## Relationship to fundamental group

For any $x$ in $X$ the first homotopy group $\pi_1(X,x)$ of $X$ based at $X$ arises as the [[automorphism group]] of $x$ in $\Pi_1(X)$:
$$
  \pi_1(X,x) = Aut_{\Pi_1(X)}(x)
  \,.
$$
So the fundamental groupoid is an improvement on the idea of the fundamental group, which gets rid of the choice of basepoint. The set of connected components of $\Pi_1(X)$ is precisely the set $\pi_0(X)$ of path-components of $X$.  (This is not to be confused with the set of connected components of $X$, sometimes denoted by the same symbol.  Of course they are the same when $X$ is locally path-connected.)

## Topologizing the fundamental groupoid

The fundamental groupoid $\Pi_1(X)$ can be made into a [[topological groupoid]] (i.e. a [[internal groupoid|groupoid internal]] to [[Top]]) when $X$ is [[path-connected space|path-connected]], [[locally path-connected space|locally path-connected]] and [[semi-locally simply connected space|semi-locally simply connected]].
This construction is closely linked with the construction of a [[universal covering space]] for a path-connected pointed space.

+--{: .query}
[[Mike Shulman]]: Could you say something about what topology you have in mind here?  Is the space of objects just $X$ with its original topology?
=--

When $X$ is not semi-locally simply connected, the fundamental groupoid inherits a non-discrete topology from the fundamental group $\pi_1(X)$, which is an obstruction to the above-mentioned source fibre\'s being a covering space.  When $X$ is not locally path-connected, $\pi_0(X)$ also inherits a non-discrete topology (the [[quotient topology]] of $X$ by the relation of path connections).

In circumstances like these more sophisticated methods are appropriate, such as [[shape theory]].  This is also related to the [[fundamental group of a topos]], which is in general a [[progroup]] or a [[localic group]] rather than an ordinary group.

## $\Pi_1(X)$ with a chosen set of basepoints

An improvement on this relevant to the [[van Kampen theorem]] for computing the fundamental group or groupoid is to take $\Pi_1(X,A)$, defined to be the full subgroupoid of $\Pi_1(X)$ on a set $A$ of base points, chosen according to the geometry at hand. Thus if $X$ is the union of two open sets $U,V$ with intersection $W$ then we can take $A$ large enough to meet each path-component of $U,V,W$. If $X$ has an action of a group $G$ then $G$ acts on $\Pi_1(X,A)$ if $A$ is a union of orbits of the action.

## Higher categorical connections

The fundamental groupoid and its higher generalizations play a fundamental role in the definition of [[Trimble n-category]].  Conversely, following Trimble's definition, it is possible to generalize the notion of fundamental $n$-groupoids from [[Top]] to other [[closed monoidal homotopical category|closed monoidal homotopical categories]] using the concept of categories with [[interval object]].

There are also constructions of strict fundamental $\omega$-groupoids  of various types (globular, simplicial, cubical) for a filtered space, and more complicated fundamental [[cat-n-group]] of an $n$-cube of pointed spaces. For the former see the references in 

*  R. Brown, A new higher homotopy groupoid: the fundamental  globular $\omega$-groupoid of a filtered space, Homotopy, Homology and Applications, 10 (2008), No. 1, pp.327-343.

For the latter, see 

*  R. Brown and J.-L. Loday, Van Kampen theorems for diagrams of spaces,  Topology 26 (1987) 311-334.

In both cases, the structures are strict and the functors satisfy a van Kampen type theorem, i.e. preserve certain colimits, so that one can do some calculation, in many cases of a nonabelian type. 

[[!redirects Poincare groupoid]]
[[!redirects Poincaré groupoid]]
