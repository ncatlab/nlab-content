
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **Segal category** is one of the models for that of [[(∞,1)-category]]. It can be understood as modelling the notion of an [[SSet]]-[[enriched category|enrichment]] _up to coherent [[homotopy]]_ , i.e. a _weak_ enrichment.

As such it is very similar to the notion of [[complete Segal space]].


A Segal category is a weak form of [[S-category|S-categories]], in which composition is only defined up to a coherent system of [[equivalence]]s.

Segal categories were defined in 1974 (implicitly) by [[Graeme Segal]]. They were named Segal categories first by William Dwyer--[[Daniel Kan]]--[[Jeff Smith]] in 1989. In their famous book _Homotopy invariant algebraic structures on topological spaces_, John Boardman and Rainer Vogt used [[quasi-category|quasi-categories]]; a quasi-category is a simplicial set satisfying the weak Kan condition, so quasi-categories are also called [[weak Kan complex]]es. All of these are [[Quillen equivalence|Quillen equivalent]] models of $(\infty,1)$-[[(infinity,1)-category|categories]].



## Definition

A __Segal category__ is a [[simplicial space]] (i.e. a [[simplicial object]] in an appropriate category of [[space]]s, such as [[topological space]]s or [[Kan complex]]es) $X$ such that $X_0$ (the set of points) is a discrete [[simplicial set]] and the [[Segal map]]
$$ \phi_k: X_k \to X_1 \times_{X_0} \cdots \times_{X_0} X_1 $$
(induced by $X(\alpha_i): X_k \to X_1$) assigned to $X$ is a [[weak equivalence]] of simplicial sets for $k \geq 2$.


## References

An overview is on pages 164 to 169 of

* [[Andre Joyal]], _The theory of Quasi-Categories and its Applications_ notes from a lecture at [Simplicial Methods in Higher Categories](http://www.crm.cat/HigherCategories/)

A discussion with emphasis on the comparison of the various [[model category]] structures is in

* [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239))

* see also [[Segal space]]


[[!redirects Segal categories]]