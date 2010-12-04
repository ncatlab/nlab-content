+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

##Classical Triangulations##
###Aim###
The aim of this entry is to describe some of the classical versions of important concepts which are needed elsewhere. This may serve as an entry point for someone versed in a more classical version of algebraic topology, or being adept at the nPOV, and its ramifications, needs to bridge the gap to more classical ideas to understand some more classically written source. (It may also be useful if some classically written source is not at hand when you need it!) The exposition will be fairly 'classical' with asides to explain the significance for later developments and for connections to the nPOV.

##Triangulations &#224; l'ancienne##
Let $X$ be a [[polyhedron]] (in the sense of polyhedral space), i.e. a space homeomorphic to the [[geometric realisation]] of a [[simplicial complex]]. 

+--{: .un_defn}
######Definition
A **classical triangulation** of $X$ is a pair $(K,f)$, where $K$ is a simplicial complex and $f : |K|\to X$ is a homeomorphism. 
=--
 (In this context we will often drop the term 'classical' referring to 'triangulation' if there is little risk of confusion.)

##Classical subdivision##

The older form of [[subdivision]] involved the geometric realisation in the following way:
+--{: .un_defn}
######Definition
If $K$ is a simplicial complex, a **(classical) subdivision** of $K$ is a simplicial complex, $K^\prime$, such that

a) the vertices of $K^\prime$ are (identified with)  points of $|K|$;

b) if $s^\prime$ is a simplex of $K^\prime$  there is a simplex, $s$ of $K$ such that $s^\prime \subset |s|$; and


c) the mapping from $|K^\prime|$ to $|K|$, that extends the mapping of vertices of $K^\prime$ to the corresponding points of $|K|$, is a homeomorphism.
=--

The interpretation, in [[simplicial complex]], of the points of $|K|$ as convex combinations of the  vertices, allows an interpretation to be ascribed to $K^\prime$.  The general question of the meaning of 'refinements' that  will be examined later may need a deeper  examination of this subdivision process as it is a simple case of such a refinement.  

###Properties of Classical Subdivisions###

* Any subdivision of a subdivision of $K$ is a subdivision of $K$.

* If $K'$ and  $K''$ are subdivisions of $K$ then there is a subdivision $K'''$  of $K$ that is a subdivision of both $K'$ and $K''$.

##Barycentric subdivision (classical geometric forms)
The barycentric subdivision is one of the best known and most useful natural subdivisions available in general.  (Other are also used, for instance, the middle edge or [[ordinal subdivision]].)  The barycentric subdivision has the good property that it exists without recourse to the realisation process, although usually introduced via that process. It is in that form that it is  discussed in [[subdivision]].  Here we give the 'classical' form and go from that towards the other functorial form.


+--{: .un_defn}
######Definition
If $\sigma = \{ v_0, \ldots, v_q\} \in K_q$, the set of $q$-simplices of a simplicial complex, $K$, then its **barycentre**, $b(\sigma)$, is the point 

$$b(\sigma) = \sum_{0\leq i \leq q}\frac{1}{q + 1} v_i \in |K|.$$

The **barycentric subdivision**, $sd K$, of $K$ is the simplicial complex whose vertices are the barycentres of the simplices of $K$ and whose simplices are finite non-empty collections of barycentres of simplices, which are totally ordered by  the face relation of $K$, i.e., by inclusion when considered as subsets of $V(K)$.
=--
As $b(\sigma)$ is completely determined by $\sigma$, this can be rephrased as:



+--{: .un_defn}
######Definition: (Alternative form)
The **barycentric subdivision**, $sd K$, of $K$ is the simplicial complex specified by

* the vertices of $sd K$ are the simplices of $K$;
* the subset $\{\sigma_0, \ldots \sigma_q\}$ is a simplex of $sd K$ if there is a total order on its elements (which will be assumed to be the given order, as written) such that

$$\sigma_0\subset  \ldots \subset\sigma_q.$$
=--

##Triangulations and Covers##
We now need a bit more terminology:

+--{: .un_defn}
######Definition: 
 Given any vertex $v$ of $K$, its **star** is defined by 

$$st( v) = \{ \alpha \in |K| \mid \alpha(v)\neq 0\}.$$

=--

The set, $st(v)$, is open in $|K|$. We have 

$$st(v) = \bigcup \{\langle s \rangle\mid v is a vertex of s\},$$

the union of the interiors of those simplices that have $s$ as a vertex.  These vertex stars give an [[open cover]], $\mathcal{U}$, of $|K|$ and the following classical result tells us that the nerve $N(\mathcal{U})$ of this covering is $K$ itself (up to isomorphism):

+--{: .un_prop}
######Proposition (cf. Spanier, p. 114)
Let $\mathcal{U} = \{st(v)\mid v \in V(K)\}$.  The vertex map $\phi$ from $K$ to $N(\mathcal{U})$ defined by 

$$\phi (v) = \langle st(v)\rangle$$

is a simplicial isomorphism

$$\phi : K \cong N(\mathcal{U}).$$
=--





category:motivation