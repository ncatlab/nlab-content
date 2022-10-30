
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* toc
{: toc}

## Idea

The **fundamental groupoid** of a space $X$ is a [[groupoid]] whose objects are the points of $X$ and whose morphisms are [[paths]] in $X$, identified up to endpoint-preserving [[homotopy]].

In parts of the literature the fundamental groupoid, and more generally the [[fundamental ∞-groupoid]], is called the **Poincar&#233; groupoid**.


## Definition

The **fundamental groupoid** $\Pi_1(X)$ of a topological space $X$ is the [[groupoid]] whose set of objects is $X$ and whose morphisms from $x$ to $y$ are the homotopy-classes $[\gamma]$ of continuous maps $\gamma : [0,1] \to X$ whose endpoints map to $x$ and $y$ (which the homotopies are required to fix). Composition is by concatenation (and reparametrization) of representative maps. Under the [[homotopy]]-[[equivalence relation]] this becomes an associative and unital composition with respect to which every morphism has an inverse; hence $\Pi_1(X)$ is a groupoid.


## Remarks

### Relationship to fundamental group

For any $x$ in $X$ the first homotopy group $\pi_1(X,x)$ of $X$ based at $X$ arises as the [[automorphism group]] of $x$ in $\Pi_1(X)$:
$$
  \pi_1(X,x) = Aut_{\Pi_1(X)}(x)
  \,.
$$
So the fundamental groupoid is an improvement on the idea of the fundamental group, which gets rid of the choice of basepoint. The set of connected components of $\Pi_1(X)$ is precisely the set $\Pi_0(X)$ of path-components of $X$.  (This is not to be confused with the set of connected components of $X$, sometimes denoted by the same symbol.  Of course they are the same when $X$ is locally path-connected.)


### Topologizing the fundamental groupoid

The fundamental groupoid $\Pi_1(X)$ can be made into a [[topological groupoid]] (i.e. a [[internal groupoid|groupoid internal]] to [[Top]]) when $X$ is [[path-connected space|path-connected]], [[locally path-connected space|locally path-connected]] and [[semi-locally simply connected space|semi-locally simply connected]].
This construction is closely linked with the construction of a [[universal covering space]] for a path-connected pointed space. The object space of this groupoid is just the space $X$.

+-- {: .query}
[[Mike Shulman]]: Could you say something about what topology you have in mind here?  Is the space of objects just $X$ with its original topology?

[[David Roberts]]: The short answer is that it is propositions 4.17 and 4.18 in my [[davidroberts:HomePage|thesis]], but I will put it here soon.

Regarding topology on the fundamental groupoid for a general space; it inherits a topology from the path space $X^I$, but there is also a topology (unless I've missed some subtlety) as given in 4.17 mentioned above, but the extant literature on the topological fundamental group uses the first one.
=--

When $X$ is not semi-locally simply connected, the arrows of the fundamental groupoid inherits the [[quotient space|quotient topology]] from the path space such that the fibres of $(s,t):Mor(\Pi_1(X)) \to X\times X$ are not discrete, which is an obstruction to the above-mentioned source fibre\'s being a covering space. However the composition is no longer continuous. When $X$ is not locally path-connected, $\Pi_0(X)$ also inherits a non-discrete topology (the quotient topology of $X$ by the relation of path connections).

In circumstances like these more sophisticated methods are appropriate, such as [[shape theory]].  This is also related to the [[fundamental group of a topos]], which is in general a [[progroup]] or a [[localic group]] rather than an ordinary group.


### $\Pi_1(X)$ with a chosen set of basepoints

An improvement on this relevant to the [[van Kampen theorem]] for computing the fundamental group or groupoid is to take $\Pi_1(X,A)$, defined to be the full subgroupoid of $\Pi_1(X)$ on a set $A$ of base points, chosen according to the geometry at hand. Thus if $X$ is the union of two open sets $U,V$ with intersection $W$ then we can take $A$ large enough to meet each path-component of $U,V,W$. If $X$ has an action of a group $G$ then $G$ acts on $\Pi_1(X,A)$ if $A$ is a union of orbits of the action.

[[Ronnie Brown]] is a big booster of $\Pi_1(X,A)$, which is fundamental to his development of [[homotopy theory]] in _Elements of Modern Topology_ (1968).

Notice that $\Pi_1(X,X)$ recovers the full fundamental groupoid, while $\Pi_1(X,\{a\})$ is the [[delooping]] of the [[fundamental group]] $\pi_1(X,a)$.


### In higher category theory

See [[fundamental ∞-groupoid]].


## Related concepts

* **fundamental groupoid**, [[fundamental ∞-groupoid]]

* [[fundamental category]], [[fundamental (∞,1)-category]]

* [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]

## References

* R. Brown and G. Danesh-Naruie,  The fundamental groupoid as a
topological groupoid, _Proc. Edinburgh Math. Soc._ 19 (1975)
237-244.

* R. Brown, _Topology and groupoids_, Booksurge (2006). (See particularly 10.5.8, using lifted topologies to topologise $(\pi_1 X)/N$ where $N$ is a normal, totally disconnected subgroupoid of $\pi_1 X$, and $X$ admits a universal cover). 

Discussion from the point of view of [[Galois theory]] is in

* Luis Javier Hern&#225;ndez-Paricio, _Fundamental pro-groupoids and covering projections_([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm156/fm15611.pdf))


[[!redirects fundamental groupoid]]
[[!redirects fundamental groupoids]]

[[!redirects Poincaré groupoid]]
[[!redirects Poincaré groupoids]]
[[!redirects Poincaré-groupoid]]
[[!redirects Poincaré-groupoids]]
[[!redirects Poincare groupoid]]
[[!redirects Poincare groupoids]]
[[!redirects Poincare-groupoid]]
[[!redirects Poincare-groupoids]]