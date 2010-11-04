
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Content#
* automatic table of contents goes here
{:toc}

## Idea

Simplicial sets generalize the idea of [[simplicial complex]]es: a _simplicial set_ is like a combinatorial space built up out of gluing abstract [[simplex|simplices]] to each other. Equivalently, it is an object equipped with a rule for how to consistently map the objects of the [[simplex category]] into it.

More concretely, a simplicial set $S$ is a collection of [[sets]] $S_n$ for $n \in \mathbb{N}$, so that elements in $S_n$ are to be thought of as $n$-[[simplex|simplices]], equipped with a rule that says:

* which $(n-1)$-simplices in $S_{n-1}$ are faces of which elements of $S_n$;
* which $(n+1)$-simplices are [[thin element|thin]] in that they are really just $n$-simplices regarded as degenerate $(n+1)$-simplices.

One of the main uses of simplicial sets is as combinatorial _models_ for [[topological spaces]]. They can also be taken as models for [[∞-groupoids]]. This is encoded in the [[model structure on simplicial sets]].

## Definition

A **simplicial set**  is a [[presheaf]] on the [[simplex category]] $\Delta$, that is, a functor $X : \Delta^{op} \to Sets$.

This is, of course, a [[simplicial object]] in the category [[Set]] of sets.

With the standard morphisms of [[presheaf|presheaves]] as morphisms, simplicial sets form the category [[sSet]] (also called $SSet$ or $sSet$). See there for more details.

## Remarks

### Simplicial sets as spaces built of simplices

* The definition is to be understood from the point of view of [[space and quantity]]: a **simplicial set** is a space characterized by the fact that and how it may be _probed_ by mapping standard simplices into it: the set $S_n$ assigned by a simplicial set to the standard $n$-simplex $[n]$ is the **set of $n$-simplices** in this space, hence the way of mapping a standard $n$-simplex into this spaces.

* For $S$ a simplicial set, the **face map** 
  $$
    d_i := S(\delta^i): S_n \rightarrow S_{n-1}
  $$ 
  is dual to the unique injection $\delta^i : [n-1] \rightarrow [n]$ in the category $\Delta$ whose image omits the element $i \in [n]$. 

* Similarly, the **degeneracy map** 
  $$
    s_i := S(\sigma^i) : S_n \rightarrow S_{n+1}
  $$ 
  is dual to the unique surjection $\sigma^i : [n+1] \rightarrow [n]$ in $\Delta$ such that $i \in [n]$ has two elements in its preimage. 

* The maps $\delta^i$ and $\sigma^i$ satisfy certain obvious relations -- the [[simplicial identities]] -- dual to those  spelled out at [[simplex category]].


### Visualisation
(based on [[cubical set]])

The **face maps**  go from sets $S_{n+1}$ of $(n+1)$-dimensional simplices to the corresponding set $S_{n}$ of $n$-dimensional simplices and can be thought of as sending each simplex in the simplicial set to one of its faces, for instance for $n=1$ the set $S_2$ of 2-simplices would be sent in three different ways by three different face maps to the set of $1$-simplices, for instance one of the face maps would send

$$
  \left(
  \array{
       &          & b
     \\
       & \nearrow & \Downarrow^F & \searrow
     \\
     a &          & \rightarrow  &          & c
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
       &          & b
     \\
       & \nearrow
     \\
     a
  }
  \right)
$$

another one would send

$$
  \left(
  \array{
       &          & b
     \\
       & \nearrow & \Downarrow^F & \searrow
     \\
     a &          & \rightarrow  &          & c
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
     a &          & \rightarrow  &          & c
  }
  \right)
  \,.
$$

On the other hand, the **degeneracy maps** go the other way round and send sets $S_n$ of $n$-simplices to sets $S_{n+1}$ of $(n+1)$-simplices by regarding an $n$-simplex as a degenerate or "thin" $(n+1)$-simplex in the various different ways that this is possible. For instance again for $n=1$ a degeneracy map may act by sending

$$
  \left(
  \array{
     a
     &\stackrel{f}{\to}&
     b
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
       &            & b
     \\
       & \nearrow_f & \Downarrow^{Id} & \searrow^{Id}
     \\
     a &            & \stackrel{f}\to &               & b
  }
  \right)
  \,.
$$

Notice the $Id$-labels, which indicate that the edges and faces labeled by them are "[[thin element|thin]]" in much the same way as an [[identity morphism]] is thin (notice however that a simplicial set by itself is not equipped with a notion of composition of simplices. If it were, we'd call it a [[simplicial category]]).

## Examples

* Let $[n]$ denote the object of $\Delta$ corresponding to the totally ordered set $\{ 0, 1, 2,\ldots, n\}$. Then the represented presheaf $\Delta(-, [n])$, which we typically write as $\Delta[n]$ is an example of a simplicial set. By the Yoneda lemma, the $n$-simplices of a simplicial set $X$ are in natural bijective correspondence to maps $\Delta[n] \rightarrow X$ of simplicial sets.

* If $C$ is a small category, the **nerve** of $C$ is a simplicial set which we denote $NC$. If we intepret the poset $[n]$ defined above as a category, we define the $n$-simplices of $NC$ to be the set of functors $[n] \rightarrow C$. Equivalently, the $0$-simplices of $NC$ are the objects of $C$, the $1$-simplices are the morphisms, and the $n$-simplices are strings of $n$ composable arrows in $C$. Face maps are given by composition (or omission, in the case of $d_0$ and $d_n$) and degeneracy maps are given by inserting identity arrows.

* Recall from [[simplex category]] or [[geometric realization]] the standard functor $\Delta \to Top$ which sends $[n] \in \Delta$ to the standard topological $n$-simplex $\Delta^n$.  This functor induces for every [[topological space]] $X$ the simplicial set
$$
  S X : [n] \mapsto Hom_{Top}(\Delta^n, X)
$$
called the **simplicial singular complex** of $X$. This simplicial set is always a [[Kan complex]] and may be regarded as the [[fundamental ∞-groupoid]] of $X$.


* A [[symmetric set]] is a simplicial set equipped with additional *transposition maps* $t^n_i: X_n \to X_n$ for $i=0,\ldots,n-1$.  These transition maps generate an [[action]] of the [[symmetric group]] on $X_n$ and satisfy certain commutation relations with the face and degeneracy maps.

## Related concepts

* [[simplicial group]]

* [[bisimplicial set]]

* [[dendroidal set]]


## References

A pedagogical introduction to simplicial sets is

* Greg Friedman, _An elementary illustrated introduction to simplicial sets_ ([arXiv](http://arxiv.org/abs/0809.4221))

A useful (if old) survey article is: 

*  E. Curtis, _Simplicial Homotopy Theory_, Advances in Math., 6, (1971), 107 &#8211; 209.


More advanced treatments include 

* P. G. Goerss and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))


[[!redirects simplicial sets]]

[[!redirects cosimplicial set]]
[[!redirects cosimplicial sets]]