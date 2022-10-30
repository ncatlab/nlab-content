
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _nice simplicial topological space_ is a [[simplicial topological space]] that satisfies certain extra properties that make it well behaved in [[homotopy theory]], notably so that its [[geometric realization of simplicial spaces]] is its [[homotopy colimit]].

## Definition

+-- {: .un_defn }
###### Definition 

Let $X : \Delta^{op} \to Top$ be a [[simplicial topological space]].

Such $X$ is called

* **good** if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all [[closed cofibration]]s;

* **proper** if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[closed cofibration]], where $s X_n = \bigcup_i s_i(X_{n-1})$.

In other words this says: $X_\bullet$ is proper if it is a cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Strom}]_{Reedy}$ on [[simplicial object]]s with respect to the [[Strøm model structure]] on [[Top]].

=--

The notion of good simplicial topological space goes back to ([Segal](#Segal)), that of proper simplicial topological space to ([May](#May)). 


## Properties

### General

+-- {: .un_prop}
###### Proposition

A good simplicial topological space is proper.

=--

A proof appears as [Lewis, corollary 2.4 (b)](#Lewis). A generalization of this result is in [RobertsStevenson](#StevensonRoberts).


+-- {: .un_prop}
###### Proposition

For $X_\bullet$ any simplicial topological space, then ${|Sing X_\bullet|}$ is good, hence proper, and the natural morphism

$$
  {|Sing X_\bullet|} \to X_\bullet
$$

is degreewise a [[weak homotopy equivalence]].

=--

This follows by results in ([Lewis](#Lewis)).

+-- {: .proof}
###### Proof

Since for $X \in Top$ the map $|Sing X| \to X$ is a cofibrant [[resolution]] in the standard [[model structure on topological spaces]], we have that

$$
  |Sing X_\bullet| \to X_\bullet
$$

is a degreewise [[weak homotopy equivalence]]. In particular each space $|Sing X_n|$ is a [[CW-complex]], hence in particular a [[locally equi-connected space]]. By ([Lewis, p. 153](#Lewis)) inclusions of [[retract]]s of locally equi-connected spaces are [[closed cofibration]]s, and since degeneracy maps are retracts, this means that the degeneracy maps in $|Sing X_\bullet|$ are closed cofibrations.

=--


### Models for the homotopy colimit

+-- {: .un_prop}

###### Proposition

Let $X_\bullet$ be a [[simplicial topological space]]. Then there is a [[natural transformation|natural]] [[weak homotopy equivalence]] 

$$
 \Vert X_\bullet\Vert \simeq hocolim_{n \in \Delta} X_n
$$

from its fat [[geometric realization of simplicial topological spaces]] to the [[homotopy colimit]] over the simplicial diagram $X : \Delta^{op} \to Top$.

If moreover $X_\bullet$ is [proper](#ProperSimplicialSpace), then the [[natural transformation|natural morphism]]  $ {\Vert X\Vert} \to {|X|}$ is a [[weak homotopy equivalence]], and hence also the ordinary geometric realization is a model for the homotopy colimit.

=-- 

+-- {: .proof}
###### Proof

That the [[geometric realization of simplicial topological spaces]] of a proper simplicial space is is homotopy colimit follows from the [above fact](#ProperIsReedyCofibrant) that proper spaces are Reedy cofibrant, and using the general statement discussed at [[homotopy colimit]] about description of homotopy colimits by [[coend]]s.

=--

+-- {: .un_remark}
###### Remark

In the case $X_\bullet$ that is a [good](#GoodSimplicialSpace) [[simplicial topological space]], a direct (i.e., not using the fact that goodness implies properness) proof that $ \Vert X\Vert  \to |X|$ is a weak homotopy equivalence has been sketched by [[Graeme Segal]] and then refined by Tammo tom Dieck.

=--

## Related concepts

* [[simplicial topological space]], **nice simplicial topological space**

* [[simplicial topological group]]

* [[geometric realization of simplicial spaces]].


## References

The definition of _proper_ simplicial space goes back to 

* [[Peter May]], _The Geometry of Iterated Loop Spaces_ ,
  Lecture Notes in Mathematics, 1972, Volume 271(1972), 100-112, 
  ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))

May originally said _strictly proper_ for what now is just called _proper_ .

The definition of _good_ simplicial space goes back to 

* [[Graeme Segal]], _Configuration-Spaces and Iterated Loop-Spaces_ , 
  Inventiones math. 21,213-221 (1973)

The implication $good \Rightarrow proper$ seems to be handled like a folk theorem. Its origin is maybe in 

* L. Gaunce Lewis Jr., _When is the natural map 
  $X \to \Omega \Sigma X$ a cofibration?_ ,
  Trans. Amer. Math. Soc. 273 (1982), 147--155.
  {#Lewis}

Comments on the relation between properness and cofibrancy in the [[Reedy model structure]] on $[\Delta^{op}, Set]$ are made in 

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537)).

[[!redirects good simplicial space]]
[[!redirects proper simplicial space]]

[[!redirects good simplicial topological space]]
[[!redirects proper simplicial topological space]]