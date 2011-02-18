
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

Let $X : \Delta^{op} \to Top$ be a [[simplicial topological space]].

Such $X$ is called

* **good** if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all closed cofibrations;

* **proper** if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a closed cofibration, where $s X_n = \bigcup_i s_i(X_{n-1})$.


## Properties

### General

+-- {: .un_defn #GoodSimplicialSpace}
###### Definition 

A [[simplicial topological space]] $X_\bullet$ is **good** in the sense of [[Graeme Segal|Segal]] if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are closed cofibrations.

=--

+-- {: .un_defn #ProperSimplicialSpace}
###### Definition

A simplicial topological space $X_\bullet$ is **proper** in the sense of [May](#May) if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[Hurewicz cofibration|closed cofibration]], where $s X_n := \bigcup_i s_i(X_{n-1})$.

=--

For more on these conditions see [[nice simplicial topological space]].

+-- {: .un_prop}
###### Proposition

A good simplicial topological space is proper.

=--

A proof appears as [Lewis, corollary 2.4 (b)](#Lewis). A generalization of this result is in [RobertsStevenson](#StevensonRoberts).

+-- {: .un_prop #ProperIsReedyCofibrant}
###### Proposition

The proper simplicial topological spaces are precisely those that are cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Str}]_{Reedy}$ on simplicial topological spaces, where [[Top]] is equipped with the [[Strøm model structure]] $Top_{Strm}$.

=--

+-- {: .un_prop}
###### Proposition

For $X_\bullet$ any simplicial topological space, then ${|Sing X_\bullet|}$ is proper and the natural morphism

$$
  {|Sing X_\bullet|} \to X_\bullet
$$

is a cofibrant [[resolution]] of $X_\bullet$ in $[\Delta^{op},Top_{Strm}]_{Reedy}$.


=--

This follows by results in ([Lewis](#Lewis)).


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