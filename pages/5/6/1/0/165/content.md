#Idea#

The **fundamental groupoid** of a space $X$ is a [[groupoid]] whose objects are the points of $X$ and whose morphisms are paths in $X$, identified up to endpoint-preserving [[homotopy]].

#Definition#



The **fundamental groupoid** $\pi_1(X)$ of a topological space  $X$ is the [[groupoid]] whose set of objects is $X$ and whose morphism from $x$ to $y$ are the homotopy-classes $[\gamma]$ of continuous maps $\gamma : [0,1] \to X$ whose endpoints map to $x$ and $y$ (which the homotopies are required to fix). Composition is by concatenation of representative maps. Under the [[homotopy]]-[[equivalence relation]] this becomes an associative and unital composition with respect to which every morphism has an inverse.




#Remarks#

For any $x$ in $X$ the first homotopy group $\pi_1(X,x)$ of $X$ based at $X$ arises as the [[automorphism group]] of $x$ in $\Pi_1(X)$:
$$
  \pi_1(X,x) = Aut_{\Pi_1(X)}(x)
  \,.
$$
So the fundamental groupoid is an improvement on the idea of the fundamental group, which gets rid of the choice of basepoint. The set of connected components of $\pi_1(X)$ is precisely the set $\pi_0(X)$ of path-components of $X$ (not to be confused with the set of connected components of $X$, sometimes denoted by the same symbol).

The fundamental groupoid $\pi_1(X)$ can be made into a [[topological groupoid]] (i.e. a [[internal groupoid|groupoid internal]] to [[Top]]) when $X$ is [[path-connected space|path-connected]], [[locally path-connected space|locally path-connected]] and [[semi-locally simply connected space|semi-locally simply connected]].
This construction is closely linked with the construction of a [[universal covering space]] for a path-connected pointed space.

When $X$ is not semi-locally simply connected, the  fundamental group inherits a non-discrete topology from $\pi_1(X)$, which is an obstruction to the above-mentioned source fibre\'s being a covering space.  When $X$ is not locally path-connected, $\pi_0(X)$ inherits a non-discrete topology from $\pi_1(X)$. In circumstances like these more sophisticated methods would be appropriate, such as [[shape theory]].

An improvement on this relevant to the [[van Kampen theorem]] for computing the fundamental group or groupoid is to take $\pi_1(X,A)$, namely the full subgroupoid of $\pi_1(X)$ on a set $A$ of base points, chosen according to the geometry at hand. Thus if $X$ is the union of two open sets $U,V$ with intersection $W$ then we can take $A$ large enough to meet each path-component of $U,V,W$. If $X$ has an action of a group $G$ then $G$ acts on $\pi_1(X,A)$ if $A$ is a union of orbits of the action.  

In parts of the literature the fundamental groupoid and in particular the [[fundamental infinity-groupoid]] of a space is called the **Poincar&#233;-groupoid**.

The fundamental groupoid and its higher generalization play a fundamental role in the definition of [[Trimble n-category]].

Following Trimble's definition, it is possible to generalize the notion of fundamental $n$-groupoids from [[Top]] to other [[closed monoidal homotopical category|closed monoidal homotopical categories]] using the concept of categories with [[interval object]].

There are  constructions of strict fundamental $\omega$-groupoids  of various types (globular, simplicial, cubical) for a filtered space, and more complicated fundamental [[cat-n-group]] of an $n$-cube of pointed spaces. For the former see the references in 

*  R. Brown, A new higher homotopy groupoid: the fundamental  globular $\omega$-groupoid of a filtered space, Homotopy, Homology and Applications, 10 (2008), No. 1, pp.327-343.

For the latter, see 

*  R. Brown and J.-L. Loday, Van Kampen theorems for diagrams of spaces,  Topology 26 (1987) 311-334.

In both cases, the structures are strict and the functors satisfy a van Kampen type theorem, i.e. preserve certain colimits, so that one can do some calculation, in many cases of a nonabelian type. 