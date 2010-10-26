
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

(...)

## Details

For the _van Kampen theorem_ for the [[fundamental groupoid]] of [[topological space]] it is convenient to define $\pi_1(X,X_0)$ of a space $X$ and a set $X_0$ to be the full subgroupoid of $\pi_1 X$ on the set $X \cap X_0$. Suppose $X_* =(X,X_0)$ is a pair consisting of a space $X$ and a set $X_0$ of base points. We say $X_*$ is _connected_ if $X_0$ meets each path component of $X$. 


Let  $X$ be the union of the interiors of sets $U^i$, $i \in I$.  If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$, and  let $U^e_*$ be the pair $(U^e,X_0 \cap U^e)$, $e \in I \cup I^2$.  We then have a [[coequalizer|coequaliser]] diagram of pairs of  spaces where $a,b,c$ are determined by inclusions: 

$$\bigsqcup_{d \in I^2} U^d_* \rightrightarrows ^a_b \bigsqcup _{i \in I} U^i_* \to ^c X_*.$$

+--{.un_theorem}
###### van Kampen theorem

If the pairs of  spaces $U^f_*$ are  connected for all 1-,2-, or 3-fold  intersections $U^f_*$ of the pairs $U^i_*$, then

1. (Conn) The pair  $X_*$ is connected; and

1. (Iso) The [[fundamental groupoid]] functor $\pi_1$ takes the 
   above coequaliser diagram of pairs of  spaces to a coequaliser 
   diagram of groupoids.

=--


**Remarks**

1. Emphasising the connectivity result becomes more  important for [[higher homotopy van Kampen theorem]]s. 

1. This uses the idea of Lebesgue covering dimension to reduce to the 3-fold intersection condition.  

1. Naturally the proof can and should go by verifying the universal property for a coequaliser. The  basic techniques of the proof include: subdivide a path;  deform a subdivision so that it is product of paths joining points of $X_0$; subdivide a homotopy rel end points, and deform this subdivision so that _all_ subpaths join points of $X_0$; any composition of [[commutative square]]s in a groupoid is commutative.

1. One should take a hard line with those who try to reduce this to a  theorem about groups. For example $X$ may be a connected space which is the union of two connected open sets whose intersection has 15 path components. Or the connected $X$ may be the union of 23 open sets whose three fold intersections have 123 path components. In each case the fundamental group one might want to calculate  is in the middle of this complicated combinatorial situation, but at least the theorem has turned a topological problem into a group theory and combinatorial problem, and the remarkable fact is that the fundamental groups are _completely_ determined by the theorem. This is an **anomaly** for traditional algebraic topology, where invariants relating adjacent dimensions may be determined by exact sequences which do not give complete information.

1. It was the last anomaly which suggested that [[higher homotopy van Kampen theorem]]s might give new kinds of homotopical information, i.e. colimit theorems for higher homotopy invariants. And this has proved to be so. 

1. The theorem can be extended to more general kinds of colimits, using homotopy colimits: $\pi_1$ preserves homotopy colimits.  Under some conditions, we can replace the homotopy colimit by a strict colimit.  (For more details see Emmanuel Dror Farjoun, "Fundamental group of homotopy colimits", Adv. in Math. 182 (2004), 1-27; a draft is available here: &lt;http://www.cs.biu.ac.il/~katzmik/colloquium/col3.ps>.)

+--{| .query}
[[Ronnie Brown|Ronnie]] This paper does not seem to mention the fundamental groupoid on a set of base points.  Is there a version of the result on homotopy colimits for many base points? 

The original idea for many base points was to calculate the fundamental group of the circle via a van Kampen type theorem for non connected spaces: this required the many base point version. 

It seems useful to use $\pi_1(X,X_0)$ where  $X_0$ is chosen according to the geometry at hand, usually somewhere between a single point and the whole space. Grothendieck agreed! 

Arguments for (and against!) groupoids are more fully set out on &lt;http://www.bangor.ac.uk/r.brown/gpdsweb.html>. 

[[Mathieu Dupont|Mathieu]] I don't think one need to use a set of base points in the case of homotopy colimits, since in this case we work up to equivalences of groupoids.  If you apply $\pi_1$ to the circle presented as the homotopy pushout of the map $2\to 1$ along itself (where $2$ is the discrete space on two elements), you get a groupoid equivalent to the (bicategorical) pushout in the 2-category of groupoids of $2\to 1$ along itself (this time, seen as discrete groupoids), which is (up to equivalence) the group $\Z$ seen as a one-object groupoid. 

[[Ronnie Brown|Ronnie]] This all seems more complicated than the statement:  the group $\Z$ is up to _isomorphism_ obtained from the unit interval groupoid $I$ by identifying 0 and 1, in the category of groupoids.  Analogous  lower dimensional identifications become more significant in the applications of [[higher homotopy van Kampen theorem]]s, which allow for some computations for example of homotopy 2-types, not so far obtained by homotopy colimit methods. These require higher homotopy groupoids for their proof. 

The many base point case is used in proving subgroup theorems in group theory.  Higgins also gave in 1976 a very nice normal form for the fundamental groupoid of a graph of groups; since a graph has vertices, is is not surprising that this groupoid has the same vertices as the graph. This elegant idea has been ignored by the experts in that area. 

I agree that homotopy colimits are interesting. For example, I like to consider the _trefoil groupoid_ $T$ which is the homotopy pushout in the category of groupoids 
of the two maps $\Z \to \Z$ given by multiplication by 2 and by 3. There are advantages in keeping this with two objects, as reducing to the trefoil group loses some structure, such as the distinction between two generators. 

Similarly, it is convenient to consider $\pi_1(\Delta^n, \Delta^n_0)$, the fundamental groupoid of the $n$-simplex on its set of vertices. This keeps the geometry of the simplex. So the nerve of a groupoid $G$ is the [[simplicial set]] which in dimension $n$ is $Gpd(\pi_1(\Delta^n, \Delta^n_0),G)$. 

For all I know, there may be advantages in replacing loop space theory by a many-pointed theory, involving the structures which arise from considering all paths, and even all cubes, between the base points! 

Quickly reducing a groupoid to one object is to me a bit like _always_ choosing a basis for a vector space. 

=--


## Generalizations

* [[van Kampen theorem for toposes]]

* [[higher homotopy van Kampen theorem]]

## References

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_

