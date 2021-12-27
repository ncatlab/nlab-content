
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

The use of the fundamental groupoid of a manifold for describing the monodromy principle on the extension of local morphisms is discussed in the paper by Brown/Mucuk listed below. 


## Remarks

### Relationship to fundamental group

For any $x$ in $X$ the first homotopy group $\pi_1(X,x)$ of $X$ based at $x$ arises as the [[automorphism group]] of $x$ in $\Pi_1(X)$:
$$
  \pi_1(X,x) = Aut_{\Pi_1(X)}(x)
  \,.
$$
So the fundamental groupoid gets rid of the choice of basepoint for the fundamental group, and this is valuable for some applications. The set of connected components of $\Pi_1(X)$ is precisely the set $\Pi_0(X)$ of path-components of $X$.  (This is not to be confused with the set of connected components of $X$, sometimes denoted by the same symbol.  Of course they are the same when $X$ is locally path-connected.)


### Topologizing the fundamental groupoid

The fundamental groupoid $\Pi_1(X)$ can be made into a [[topological groupoid]] (i.e. a [[internal groupoid|groupoid internal]] to [[Top]]) when $X$ is [[path-connected space|path-connected]], [[locally path-connected space|locally path-connected]] and [[semi-locally simply connected space|semi-locally simply connected]]. This is a special case of ([Brown 06, 10.5.8](#Browno6)). 
This construction is closely linked with the construction of a [[universal covering space]] for a path-connected pointed space. The object space of this groupoid is just the space $X$.

+-- {: .query}
[[Mike Shulman]]: Could you say something about what topology you have in mind here?  Is the space of objects just $X$ with its original topology?

[[David Roberts]]: The short answer is that it is propositions 4.17 and 4.18 in my [[davidroberts:HomePage|thesis]], but I will put it here soon. 



Regarding topology on the fundamental groupoid for a general space; it inherits a topology from the path space $X^I$, but there is also a topology (unless I've missed some subtlety) as given in 4.17 mentioned above, but the extant literature on the topological fundamental group uses the first one.

[[Ronnie Brown]]: See the account in "Topology and Groupoids" referred to below. But there is also an account using path spaces in Proposition 6.2 of Mackenzie's 1987  book  "Lie groupoids and Lie algebroids in differential geometry".  
=--

When $X$ is not semi-locally simply connected, the set of arrows of the fundamental groupoid inherits the [[quotient space|quotient topology]] from the path space such that the fibres of $(s,t):Mor(\Pi_1(X)) \to X\times X$ are not discrete, which is an obstruction to the above-mentioned source fibre\'s being a covering space. However the composition is no longer continuous. When $X$ is not locally path-connected, $\Pi_0(X)$ also inherits a non-discrete topology (the quotient topology of $X$ by the relation of path connections).

In circumstances like these more sophisticated methods are appropriate, such as [[shape theory]].  This is also related to the [[fundamental group of a topos]], which is in general a [[progroup]] or a [[localic group]] rather than an ordinary group.


### $\Pi_1(X)$ with a chosen set of basepoints

An improvement on the fundamental group and the total fundamental groupoid  relevant to the [[van Kampen theorem]] for computing the fundamental group or groupoid is to use $\Pi_1(X,A)$, defined for a set $A$ to be the full subgroupoid of $\Pi_1(X)$ on the set $A\cap X$, thus giving a set  of base points which can be  chosen according to the geometry at hand. Thus if $X$ is the union of two open sets $U,V$ with intersection $W$ then we can take $A$ large enough to meet each path-component of $U,V,W$; note that by the above definition we can write $\Pi_1(U,A)$, etc.  If $X$ has an action of a group $G$ then $G$ acts on $\Pi_1(X,A)$ if $A$ is a union of orbits of the action. Thus $\Pi_1(X,A)$ can represent some symmetry of a given situation. 

 The notion of $\Pi_1(X,A)$ was introduced in 1967 by [[Ronnie Brown]]  to give a version of the Seifert-van Kampen Theorem which allowed the determination  of the fundamental group of a connected space which is the union of connected subspaces with nonconnected intersection, such as the  circle, a space  which is, after all, THE basic example in topology.

Grothendieck writes in his 1984 [[Esquisse d'un Programme]] (English translation):

" ..,people still obstinately persist,  when calculating with fundamental groups, in fixing a single base point, instead of cleverly choosing a whole packet of points which is invariant under  the symmetries of the situation, which thus get lost on the way.  In certain situations (such as descent theorems for fundamental groups \`a la van  Kampen) it is much more elegant,  even indispensable for understanding  something, to work with fundamental groupoids with respect to a suitable    packet of base points,..". 

Notice that $\Pi_1(X,X)$ recovers the full fundamental groupoid, while $\Pi_1(X,\{x\})$ is simply  the [[fundamental group]] $\pi_1(X,x)$. 

 Basically, $\Pi_1(X,A)$  allows for the _computation of homotopy 1-types_; the theory was developed in  _Elements of Modern Topology_ (1968), now available as _Topology and Groupoids_ (2006). These accounts show  the use of the algebra of  groupoids in 1-dimensional   [[homotopy theory]], for example for [[covering space]]s,  and, in the later edition,  for [[orbit space]]s. Another text in English which covers this notion is  by Philip Higgins, see below.   



### In higher category theory

See [[fundamental ∞-groupoid]].


### Simplicial version

See [[simplicial fundamental groupoid]].


## Related concepts

* **fundamental groupoid**, [[fundamental ∞-groupoid]]

* [[simplicial fundamental groupoid]]

* [[fundamental category]], [[fundamental (∞,1)-category]]

* [[equivariant fundamental groupoid]]

* [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]

## References

* R. Brown, Groupoids and Van Kampen's theorem, _Proc. London
Math. Soc_. (3)   17 (1967) 385-401.

* R. Brown and G. Danesh-Naruie,  The fundamental groupoid as a
topological groupoid, _Proc. Edinburgh Math. Soc._ 19 (1975)
237-244.

* R. Brown and O. Mucuk,  The monodromy groupoid of a Lie
groupoid, _Cah. Top. G\'eom. Diff. Cat_. 36 (1995) 345-369.

* {#Brown06} [[Ronnie Brown]], _Topology and Groupoids_, Booksurge (2006). (See particularly 10.5.8, using lifted topologies to topologise $(\pi_1 X)/N$ where $N$ is a normal, totally disconnected subgroupoid of $\pi_1 X$, and $X$ admits a universal cover). ([more info] (http://pages.bangor.ac.uk/~mas010/topgpds.html))

Relations with group theory are discussed in: 

* P.J. Higgins, _Notes on Categories and Groupoids_, Mathematical  Studies, Volume 32. Van Nostrand Reinhold Co. London (1971); _Reprints in Theory and Applications of   Categories_, No. 7 (2005) pp 1--195.

Discussion from the point of view of [[Galois theory]] is in

* [[Luis Javier Hernández-Paricio]], _Fundamental pro-groupoids and covering projections_, Fund. Math. (1998), ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm156/fm15611.pdf))

* The use of many base points is  discussed at  this ([mathoverflow page] (http://mathoverflow.net/questions/40945/compelling-evidence-that-two-basepoints-are-better-than-one)).

Discussion of the fundamental groupoid (for good [[topological spaces]] and for [[noetherian schemes]]) as the [[costack]] (via the [[Seifert-van Kampen theorem]]) characterized as being 2-[[terminal object|terminal]] is in 

* {#Pirashvili14a} [[Ilia Pirashvili]], _The fundamental groupoid as a terminal costack_ ([arXiv:1406.4419](https://arxiv.org/abs/1406.4419))

* {#Pirashvili14b} [[Ilia Pirashvili]], _The &#201;tale Fundamental Groupoid as a Terminal Costack_ ([arXiv:1412.5473](https://arxiv.org/abs/1412.5473))

 A recent paper in the area of dynamical systems which uses  fundamental groupoids on many base points   is:

* Paul, E. and Ramis, J.-P.
Dynamics on Wild Character Varieties, _SIGMA_ 11 (2015), 068, 21 pages. arXiv:1508.03122. 

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