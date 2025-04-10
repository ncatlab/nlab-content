
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

The **fundamental groupoid** $\Pi_1(X)$ of a topological space $X$ is the [[groupoid]] whose set of objects is $X$ and whose morphisms from $x$ to $y$ are the equivalence classes of homotopy of homotopy relative to $\partial I$ $[\gamma]$ of continuous maps $\gamma : [0,1] \to X$ whose endpoints map to $x$ and $y$ (which the homotopies are required to fix). Composition is by concatenation (and reparametrization) of representative maps. Under the [[homotopy]]-[[equivalence relation]] this becomes an associative and unital composition with respect to which every morphism has an inverse; hence $\Pi_1(X)$ is a groupoid.

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


When $X$ is not semi-locally simply connected, the set of arrows of the fundamental groupoid inherits the [[quotient space|quotient topology]] from the path space such that the fibres of $(s,t):Mor(\Pi_1(X)) \to X\times X$ are not discrete, which is an obstruction to the above-mentioned source fibre\'s being a covering space. However the composition is no longer continuous. When $X$ is not locally path-connected, $\Pi_0(X)$ also inherits a non-discrete topology (the quotient topology of $X$ by the relation of path connections).

In circumstances like these more sophisticated methods are appropriate, such as [[shape theory]].  This is also related to the [[fundamental group of a topos]], which is in general a [[progroup]] or a [[localic group]] rather than an ordinary group.


### $\Pi_1(X)$ with a chosen set of basepoints

An improvement on the fundamental group and the total fundamental groupoid  relevant to the [[van Kampen theorem]] for computing the fundamental group or groupoid is to use $\Pi_1(X,A)$, defined for a set $A$ to be the full subgroupoid of $\Pi_1(X)$ on the set $A\cap X$, thus giving a set  of base points which can be  chosen according to the geometry at hand. Thus if $X$ is the union of two open sets $U,V$ with intersection $W$ then we can take $A$ large enough to meet each path-component of $U,V,W$; note that by the above definition we can write $\Pi_1(U,A)$, etc.  If $X$ has an action of a group $G$ then $G$ acts on $\Pi_1(X,A)$ if $A$ is a union of orbits of the action. Thus $\Pi_1(X,A)$ can represent some symmetry of a given situation. 

 The notion of $\Pi_1(X,A)$ was introduced in 1967 by [[Ronnie Brown]]  to give a version of the Seifert-van Kampen Theorem which allowed the determination  of the fundamental group of a connected space which is the union of connected subspaces with nonconnected intersection, such as the  circle, a space  which is, after all, THE basic example in topology.

Grothendieck writes in his 1984 [[Esquisse d'un Programme]] (English translation):

" ..,people still obstinately persist,  when calculating with fundamental groups, in fixing a single base point, instead of cleverly choosing a whole packet of points which is invariant under  the symmetries of the situation, which thus get lost on the way.  In certain situations (such as descent theorems for fundamental groups \`a la van  Kampen) it is much more elegant,  even indispensable for understanding  something, to work with fundamental groupoids with respect to a suitable    packet of base points,..". 

Notice that $\Pi_1(X,X)$ recovers the full fundamental groupoid, while $\Pi_1(X,\{x\})$ is simply  the [[fundamental group]] $\pi_1(X,x)$. 

 Basically, $\Pi_1(X,A)$  allows for the _computation of homotopy 1-types_; the theory was developed in  _Elements of Modern Topology_ (1968), now available as _Topology and Groupoids_ (2006). These accounts show  the use of the algebra of  groupoids in 1-dimensional  [[homotopy theory]], for example for [[covering space]]s,  and, in the later edition,  for [[orbit spaces]]. spring



### In higher category theory

See [[fundamental ∞-groupoid]].


### Simplicial version

See [[simplicial fundamental groupoid]].


## Related concepts

* [[fundamental group]], 

* [[fundamental 2-groupoid]], [[fundamental ∞-groupoid]]

* [[fundamental theorem of covering spaces]]

* [homotopy of smooth paths relative to their endpoints](smooth+homotopy#HomotopyOfSmoothPathsRelativeToTheirEndpoints)

* [[simplicial fundamental groupoid]]

* [[fundamental category]], [[fundamental (∞,1)-category]]

* [[equivariant fundamental groupoid]]

* [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]


## References

A detailed treatment:

* [[Nicolas Bourbaki]], _Topologie Algébrique_, Chapitres 1 à 4, Springer (1998, 2016)  [doi:10.1007/978-3-662-49361-8](https://doi.org/10.1007/978-3-662-49361-8), ISBN 978-3-662-49361-8.

Monographs:

* [[George W. Whitehead]], (1.7) in: *Elements of Homotopy Theory*, Springer (1978) &lbrack;[doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0)&rbrack;


* [[Philip J. Higgins]], §6 of: *Categories and Groupoids*, Mathematical  Studies **32**, van Nostrand New  York (1971), Reprints in Theory and Applications of Categories **7** (2005) 1-195 &lbrack;[tac:tr7] (http://www.tac.mta.ca/tac/reprints/articles/7/tr7abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/7/tr7-2a4.pdf)&rbrack;

* {#Brown06} [[Ronnie Brown]]: Chapter 6 of: *Topology and Groupoids*, Booksurge (2006) &lbrack;[pdf](https://groupoids.org.uk/pdffiles/topgrpds-e.pdf), [webpage](https://groupoids.org.uk/topgpds.html)&rbrack; 

Review and Exposition:

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) &lbrack;[arXiv:1106.5650](https://arxiv.org/abs/1106.5650), [pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf), [[Moller-FundamentalGroup.pdf:file]]&rbrack;

* Alberto Santini, *Topological groupoids* (2011) &lbrack;[pdf](http://web.math.ku.dk/~moller/students/alberto.pdf), [[Santini-Groupoids.pdf:file]]&rbrack;
  > (about [[groupoids]] in [[topology]], notably [[fundamental groupoids]] -- not about [[topological groupoids]])

* [[Urs Schreiber]]: *[[Introduction to Topology -- 2]]*

See also:

* R. Brown, Groupoids and Van Kampen's theorem, _Proc. London
Math. Soc_. (3)   17 (1967) 385-401.

* R. Brown and G. Danesh-Naruie,  The fundamental groupoid as a
topological groupoid, _Proc. Edinburgh Math. Soc._ 19 (1975)
237-244.

* R. Brown and O. Mucuk,  The monodromy groupoid of a Lie
groupoid, _Cah. Top. G\'eom. Diff. Cat_. 36 (1995) 345-369.



Discussion from the point of view of [[Galois theory]] is in

* [[Luis Javier Hernández-Paricio]], _Fundamental pro-groupoids and covering projections_, Fund. Math. (1998), ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm156/fm15611.pdf))

* The use of many base points is  discussed at  this ([mathoverflow page] (http://mathoverflow.net/questions/40945/compelling-evidence-that-two-basepoints-are-better-than-one)).

Discussion of the fundamental groupoid (for good [[topological spaces]] and for [[noetherian schemes]]) as the [[costack]] (via the [[Seifert-van Kampen theorem]]) characterized as being 2-[[terminal object|terminal]] is in 

* {#Pirashvili14a} [[Ilia Pirashvili]], _The fundamental groupoid as a terminal costack_ ([arXiv:1406.4419](https://arxiv.org/abs/1406.4419))

* {#Pirashvili14b} [[Ilia Pirashvili]], _The &#201;tale Fundamental Groupoid as a Terminal Costack_ ([arXiv:1412.5473](https://arxiv.org/abs/1412.5473))

Discussion in the context of [[dynamical systems]]:

* Emmanuel Paul, Jean-Pierre Ramis, *Dynamics on Wild Character Varieties*, _SIGMA_ **11** (2015) 068 &lbrack;[arXiv:1508.03122](https://arxiv.org/abs/1508.03122), [doi:10.3842/SIGMA.2015.068](https://doi.org/10.3842/SIGMA.2015.068)&rbrack;

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