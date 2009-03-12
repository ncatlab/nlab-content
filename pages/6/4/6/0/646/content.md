# Idea #

A homotopy $n$-type is a space where we consider its properties only up to the $n$th [[homotopy group]] $\pi_n$.
+-- {: .query}
[[Tim Porter|Tim]]:  When teaching homotopy theory I found blank looks from students if I used this idea as motivation as they felt it was too vague. I also do not like the idea of an $n$-type being a space as it does not allow one to say that two spaces 'have the same $n$-type.' 
=--
# Motivation #

For [[nice topological space|'nice' spaces]], 
+-- {: .query}
[[Tim Porter|Tim]]: As I read the entry on nice topological spaces, it really refers to 'nice categories' rather than 'nice spaces'! I have always thought of spaces such as CW-complexes and polyhedra as being 'locally nice', but the corresponding categories are certainly not 'nice' in the sense of  [[nice topological space]]. Perhaps we need to adjust that other entry in some way.
=--
e.g., CW-complexes, a weak [[homotopy equivalence]] is the same as a homotopy equivalence.  Here a weak homotopy equivalence is a map which induces an isomorphism on all [[homotopy group]]s:
$$f:X\to Y \Leftrightarrow \pi_k(f) : \pi_k(X)\to \pi_k(Y)$$
for all $k \geq 0$ and all choices of base point.  (For [[simplicial group]]s or [[groupoid]]s, we have a similar notion.)

What if we only have that $\pi_k(f)$ is an isomorphism up to some dimension, $n$, what can we say about the 'homotopy types'? Any space is equivalent in this truncated form to a space with trivial homotopy groups above level $n$, so can we find reasonably complete _algebraic_ models for such $n$-types.

# Definition #

A continuous map $X \to Y$ is a **homotopy $n$-equivalence** if it induces isomorphisms on $\pi_i$ for $0 \leq i \leq n$ at each basepoint.  Two spaces share the same **homotopy $n$-type** if they are linked by a zig-zag chain of homotopy $n$-equivalences.

More formally, inverting the $n$-equivalences in a category $\Sp$ of nice spaces gives a category $\Ho_n(\Sp)$ and two spaces have the same **homotopy $n$-type** if they are isomorphic in $\Ho_n(\Sp)$.

For any nice space $X$, you can kill its homotopy groups in higher dimensions by attaching cells, thus constructing a new space $Y$ so that the inclusion of $X$ into $Y$ is a homotopy $n$-equivalence; up to (weak) [[homotopy equivalence]], the result is the same for any space with the same homotopy $n$-type as $X$.  Accordingly, a **homotopy $n$-type** may alternatively be defined as a space with trivial $\pi_i$ for $i \gt n$, or as the unique (weak) [[homotopy type]] of such a space, or as its fundamental $\infty$-[[fundamental infinity-groupoid|groupoid]] (which should be an $n$-[[n-groupoid|groupoid]], by one direction of the [[homotopy hypothesis]]).

# Algebraic models #

We will use simplicial groups and simplicial groupoids rather than spaces below as they are already partially algebraicised.

Considerable effort has gone into finding 'good' algebraic models for (connected) homotopy $n$-types. In low dimensions the results are 'old' or 'classical'.  (We will consider connected cases only.  The extension to the non-connected case is 'routine'.)

* The 1-type of a connected space is completely determined by its [[fundamental group]], so groups form an algebraic model for [[homotopy 1-type]]s. For the non pointed case, we can say [[groupoid]]s form an algebraic model. 

* [[crossed module|Crossed modules]] form an algebraic model for [[homotopy 2-type]]s by a result of Mac Lane and Whitehead
     
     *  S. Mac Lane and J. H. C. Whitehead, _On the 3-type of a complex_, Proc. Nat. Acad. Sci. U.S.A., 36, (1950), 41 &#8211; 48.

The use of crossed modules of groupoids and their [[classifying space]] for the non pointed case is explained under [[homotopy 2-type]]. 


*  Finding the algebraic model for the $n$-types is just a start.  Ideally one searches for algebraic models of all the higher homotopy structure as well.

* The method initiated by J.H.C. Whitehead was to approximate homotopy theory by models which analysed particular types of behaviour. One of his most widely followed models is that of [[stable homotopy theory]]. The opposite method was to find algebraic models of restricted classes of spaces, such as 2-types, or with cells in a small range of dimensions.  H.-J. Baues has followed up many of the latter ideas. 

It is sensible to regard [[crossed complex|crossed complexes]] as giving a _linear_ model of homotopy types. These crossed complexes are equivalent to [[strict omega-groupoid|strict globular]] $\infty$-groupoids. Although these are restricted model of homotopy types, they are convenient in many aspects, because of the many analogies with the familiar [[chain complex]]es. 

Crossed complexes capture operations of the fundamental groupoid, but not quadratic information such as Whitehead products (for dimensions $\gt 1$). However one can define $n$-fold crossed complexes inductively as crossed complexes internal to $(n-1)$-fold crossed complexes. So one can give the 

*(Conjecture) double crossed complexes capture the quadratic information on homotopy types, triple crossed complexes capture the cubic information, etc., etc. 

This has the possibility of leading to computations, by applying [[van Kampen theorem]]s to specific levels.