
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Definition

A _cubical $T$-complex_ is a [[cubical set]] $K$ which is also a special kind of [[Kan complex]], in that it has a family $T_n \subseteq K_n$ (for $n \geq 1$) of _[[thin element]]s_ with the properties, (due first to Keith Dakin, for the [[simplicial T-complex|simplicial case]], in his  doctoral thesis):

* T1) Degenerate elements are thin. 

* T2) Every box in $K$ has a unique thin filler. 

* T2) If all but one face of a thin element are thin, then so also is the remaining face. 

Cubical T-complexes are equivalent to [[crossed complex]]es, and also to [[cubical omega-groupoid]]s with connections.

A modification of axiom T2) to be more like an axiom for a [[quasi-category]] is suggested in the paper by Steiner below. 

## Related concepts

* [[T-complex]]

  * [[simplicial T-complex]]

  * **cubical $T$-complex**

* [[algebraic Kan complex]]

## References##

[[T-complex]]es first appeared in:

* M.K. Dakin, _Kan complexes and multiple groupoid structures_ , PhD Thesis, University of Wales, Bangor, (1976).

A main application of the idea of thin elements in the cubical case was to define the notion of commutative cube. In the case of cubical $\omega$-groupoids with connection, the boundary of a cube is commutative if and only if the boundary has a thin filler. One consequence is that any composition of thin elements is thin. This is a key element of the proof of the Higher Homotopy van Kampen theorem in the _colimits_ paper, which thus nicely generalises the proof of the 1-dimensional van Kampen theorem for the fundamental groupoid on a set of base points.  


Cubical T-complexes are thus a key concept in the long series of articles by  Brown and Higgins on [[strict omega-groupoid|strict omega-groupoids]]. For instance

* [[Ronnie Brown]], P.J. Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

*  [[Ronnie Brown]], P.J. Higgins, _On the algebra of cubes_,  J. Pure Appl.  Algebra 21 (1981) 233-260.

* R. Brown, P.J. Higgins, _Colimit theorems for relative homotopy groups_, J. Pure Appl. Algebra 22 (1981) 11-41.

and generally

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).

For more on 'thinness' in a cubical context, see:

* P.J. Higgins, _Thin elements and commutative shells in
cubical  $\omega$-categories_, Theory Appl. Categ.,
14 (2005) 60--74.

* R. Steiner, _Thin fillers in the cubical nerves of
omega-categories_, Theory Appl. Categ. 16 (2006), 144--173.

