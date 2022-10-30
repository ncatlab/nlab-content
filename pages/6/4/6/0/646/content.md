
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea 

The notion of **homotopy $n$-type** is a coarsened variant of the notion of [[homotopy type]], which is recovered for $n = \infty$.

For instance a [[homotopy 1-type]] has trivial [[homotopy groups]] above degree 2, and a [[homotopy 2-type]] has trivial homotopy groups above degree 3.

Among the most important invariants of a [[topological space]] $X$ or, more generally, of an object $X$ in an [[∞-stack]] [[(∞,1)-topos]] are its [[homotopy group]]s $\pi_k(X)$. We say that an object $X$ for which all $\pi_k(X)$ with $k \gt n$ are trivial is a **homotopy $n$-type**. More precisely, these are the [[n-truncated object of an (infinity,1)-topos|n-truncated objects]] and one says that two object $X$, $Y$ are _of the same homotopy $n$-type_ if there is a zig-zag of morphisms connecting them that induces [[isomorphism]]s on [[homotopy group]]s $\pi_k(X) \stackrel{\simeq}{\to} \pi_k(Y)$ for $0 \leq k \leq n$.

So homotopy $n$-types are the [[equivalence classes]] of an [[equivalence relation]] imposed on objects in [[Top]] (or objects in another [[(∞,1)-topos]]). Thus, we often say that two spaces 'have the same homotopy $n$-type' if their [[homotopy group]]s agree up to $\pi_n$, and 'a homotopy $n$-type' can equally well be represented by any space having that $n$-type.  This is analogous to the definition of 'a [[real number]]' as an equivalence class of Cauchy sequences.
However, as usual in [[homotopy theory]], merely having isomorphic homotopy groups is not enough; rather there needs to be a map _inducing_ such an isomorphism.  Thus, the relevant equivalence relation relates two spaces when there is a zigzag of maps between them, all inducing isomorphisms on homotopy groups $\pi_k$ for $k\le n$.  One can then show that any space is equivalent, in this sense, to one having trivial homotopy groups above level $n$, so that the other definition is also correct.

The use of [[topological space]]s is not, of course, essential; we could just as well use any other structure that models the same [[homotopy theory]], such as [[simplicial set]]s, [[simplicial groupoid]]s, or (for [[connected space]]s) [[simplicial group]]s.  Moreover, the fact that homotopy $n$-types can be modeled by spaces that are 'homotopically trivial' above level $n$ raises the possibility of finding reasonably complete _algebraic_ models for such $n$-types.




## Definition 

A continuous map $X \to Y$ is a **homotopy $n$-equivalence** if it induces isomorphisms on $\pi_i$ for $0 \leq i \leq n$ at each basepoint.  Two spaces share the same **homotopy $n$-type** if they are linked by a zig-zag chain of homotopy $n$-equivalences.

More formally, inverting the $n$-equivalences in [[Top]] gives a [[homotopy category]] $\Ho_n(\Top)$, and two spaces have the same **homotopy $n$-type** if they become isomorphic in $\Ho_n(\Top)$.

For any space $X$, you can kill its homotopy groups in higher dimensions by attaching cells, thus constructing a new space $Y$ so that the inclusion of $X$ into $Y$ is a homotopy $n$-equivalence; up to (weak) [[homotopy equivalence]], the result is the same for any space with the same homotopy $n$-type as $X$.  Accordingly, a **homotopy $n$-type** may alternatively be defined as a space with trivial $\pi_i$ for $i \gt n$, or as the unique (weak) [[homotopy type]] of such a space, or as its fundamental $\infty$-[[fundamental infinity-groupoid|groupoid]] (which should be an $n$-[[n-groupoid|groupoid]], by one direction of the [[homotopy hypothesis]]).

One can also construct [[model category|model structures]] on $\Top$ whose homotopy categories are the categories $\Ho_n(\Top)$.  This is one of the original examples of [[Bousfield localization]].  From this perspective, the above replacement of a space by one having trivial $\pi_k$ for $k\gt n$ is an example of _fibrant replacement_.


## Algebraic models 

We will use simplicial groups and simplicial groupoids rather than spaces below as they are already partially algebraicised.  So in the definition above, 'space' means a simplicial group(oid) and 'continuous map' means a homomorphism of simplicial group(oid)s.

Considerable effort has gone into finding 'good' algebraic models for (connected) homotopy $n$-types. In low dimensions the results are 'old' or 'classical'.  We will consider connected cases (simplicial groups) only.  The extension to the non-connected case (simplicial groupoids) is 'routine'.

* The 1-type of a connected space is completely determined by its [[fundamental group]], so groups form an algebraic model for [[homotopy 1-type]]s. For the non pointed case, we can say [[groupoid]]s form an algebraic model. 

* [[crossed module|Crossed modules]] form an algebraic model for (connected) [[homotopy 2-type]]s by a result of Mac Lane and Whitehead,
     
*  S. Mac Lane and J. H. C. Whitehead, _On the 3-type of a complex_, Proc. Nat. Acad. Sci. U.S.A., 36, (1950), 41 &#8211; 48.

The use of crossed modules of groupoids and their [[classifying space]] for the non pointed case is explained under [[homotopy 2-type]]. 


*  Finding the algebraic model for the $n$-types is just a start.  Ideally one searches for algebraic models of all the higher homotopy structure as well.

* The method initiated by J.H.C. Whitehead was to approximate homotopy theory by models which analysed particular types of behaviour. One of his most widely followed models is that of [[stable homotopy theory]]. The opposite method was to find algebraic models of restricted classes of spaces, such as 2-types, or with cells in a small range of dimensions.  H.-J. Baues has followed up many of the latter ideas. 

It is sensible to regard [[crossed complex|crossed complexes]] as giving a _linear_ model of homotopy types. These crossed complexes are equivalent to [[strict omega-groupoid|strict globular]] $\infty$-groupoids. Although these are restricted model of homotopy types, they are convenient in many aspects, because of the many analogies with the familiar [[chain complex]]es. 

Crossed complexes capture operations of the fundamental groupoid, but not quadratic information such as Whitehead products (for dimensions $\gt 1$). However one can define $n$-fold crossed complexes inductively as crossed complexes internal to $(n-1)$-fold crossed complexes. So one can give the 

*(Conjecture) double crossed complexes capture the quadratic information on homotopy types, triple crossed complexes capture the cubic information, etc., etc. 

This has the possibility of leading to computations, by applying [[van Kampen theorem]]s to specific levels.

## Examples and special cases

[[!include homotopy n-types - table]]


## Related concepts

* [[n-groupoid]], [[n-truncated object in an (∞,1)-category]]

* [[model structure for homotopy n-types]]

[[!redirects n-type]]
[[!redirects homotopy n-types]]
[[!redirects n-types]]

[[!redirects 1-type]]
[[!redirects 1-types]]
[[!redirects homotopy 1-type]]
[[!redirects homotopy 1-types]]



[[!redirects 3-type]]
[[!redirects 3-types]]
[[!redirects homotopy 3-type]]
[[!redirects homotopy 3-types]]

