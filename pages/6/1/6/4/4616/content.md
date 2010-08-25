
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
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

+-- {: .un_prop}
###### Proposition

A good simplicial space is also proper: $good \Rightarrow proper$.

=--

This is apparently due to ([Lewis1982](#Lewis)).

+-- {: .un_prop}
###### Proposition

For $X_\bullet$ proper its [[geometric realization of a simplicial space]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to its [[homotopy colimit]] in the [[model structure on topological spaces]] over $\Delta$

$$
  |X_\bullet| \simeq hocolim_{n} X_n
  \,.
$$

=--

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